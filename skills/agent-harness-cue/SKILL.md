---
name: agent-harness-cue
description: Cue içindeki bir yapay zekâ ajanının araç/action alanını, girdi ve çıktı sözleşmelerini, hata kurtarmasını veya bağlam kullanımını tasarlamak ya da iyileştirmek gerektiğinde kullan. Claude Code veya başka bir platforma özgü harness yönergelerini Cue'ya uyarlarken de kullan.
---

# Cue için ajan harness tasarımı

Bir ajanın hangi eylemleri yapabildiğini, araçları nasıl çağırdığını, sonuçları nasıl yorumladığını ve hatalardan nasıl güvenle toparlandığını tasarla veya incele. Kullanıcının istediği göreve yetecek en küçük, anlaşılır ve ölçülebilir action/tool alanını hedefle. Cue'da gerçekten mevcut olmayan bir yeteneği varmış gibi varsayma.

## Sınırlar

- Bu beceri, ajan araçlarının/action'larının yerel tasarımına ve çağrı sözleşmelerine odaklanır; tüm sistem mimarisini tasarlamaz. Bileşenler, dağıtım, veri saklama ve mimari alternatifler için `architecture-designer-cue` becerisini kullan.
- Çok adımlı işlerin sorumlularını, bağımlılıklarını ve devirlerini planlamaz; görev koordinasyonu için `paperclip-cue-skill` becerisini kullan.
- Bu bir tehdit modeli veya güvenlik denetimi değildir. AI/tool/MCP kötüye kullanım senaryoları ve güvenlik kontrolleri için `ai-threat-review-cue` becerisini kullan. Burada yalnızca eylemin yan etkisini, yetki kapsamını ve onay ihtiyacını sözleşmenin gerekli parçası olarak belirt.
- Claude Code, belirli bir agent framework'ü veya dış bir CLI için kurulum ve entegrasyon varsayma. Cue'nun ve görev ortamının fiilen sunduğu araçları incele.

## İş akışı

1. **Görevi ve mevcut durumu belirle.** Ajanın amacı, beklenen kullanıcı sonucu, kullanım ortamı, mevcut araçlar, kısıtlar ve başarının gözlenebilir kanıtını çıkar. Sağlanan araç tanımlarını, proje yönergelerini ve örnek çağrıları incele. Mevcut davranış, kullanıcı gereksinimi ve öneriyi birbirinden ayır. Önemli bir eksik bilgi tasarımı değiştirecekse sor; değilse varsayımı açıkça işaretle.
2. **Gerekli eylemleri listele.** Kullanıcı işlerini gerekli yeteneklere eşleştir: okuma/arama, dönüştürme, düzenleme, dış hizmette değişiklik veya başka yan etkili işlem. Her eylemin gerekçesini ve erişim/yetki sınırını belirt. Gereksiz veya örtüşen araçları kaldır; tek bir genel amaçlı araca bütün farklı yetkileri yükleme.
3. **Doğru kapsam ve tanecik düzeyini seç.** Güvenlik, izin, ödeme, silme, dağıtım veya benzeri yüksek etkili eylemleri dar ve denetlenebilir tut. Yaygın, düşük riskli işlemlerde uygun ölçüde işlevsel araçlar kullan. Çok sayıda gidiş-dönüş asıl maliyetse, yalnızca sınırları açık ve yan etkileri güvenli bir toplu eylem düşün. Onay gereksinimini yürürlükteki Cue politikası ve kullanıcı talimatlarına göre belirle; onay mekanizması varmış gibi uydurma.
4. **Her araç için sözleşme tanımla.** `templates/tool-contract.md` dosyasını gerektiği kadar kullan. Araç adı ve tekil amacı; girdi şeması; zorunlu/isteğe bağlı alanlar, türler, değer kümeleri ve sınırlar; varsayılanlar; yetki ve yan etki; idempotency/tekrar davranışı; başarı sonucu ve hata biçimini belirt. Şemayı dar, açık ve doğrulanabilir tut. Alan adlarını ve yanıt biçimini kararlı kıl.
5. **Gözlemi ve kurtarmayı tasarla.** Yanıt; başarı, uyarı, hata veya belirsiz sonucu ayırt etmeli, kısa bir özet ve sonraki güvenli adımı vermelidir. Kısmi başarıyı açıklamalı; varsa çıktı/kimlik/yol gibi kanıtı göstermelidir. Her hata yolu için olası neden ipucu, güvenli yeniden deneme koşulu ve durma koşulu tanımla. Dış yan etkili çağrıda zaman aşımı ya da bağlantı kopmasını otomatik olarak başarısızlık sayma; önce mevcut durumu doğrulamadan işlemi yineleme.
6. **Bağlam bütçesini yönet.** Her zaman gereken ve değişmeyen talimatları kısa tut; duruma bağlı uzun rehberi gerektiğinde yüklenen beceri/referansa taşı. Araç yanıtında sadece sonraki karara yarayan bilgiyi döndür, büyük sonuçları sayfalama veya sınırlama ile getir. Aşama geçişlerinde kararları, kısıtları, açık işleri ve kanıtı kompakt biçimde özetle; önemli bilgiyi sırf kısaltmak için silme. Token/bağlam sınırlarını yalnızca ortam gerçekten ölçebiliyor veya yapılandırabiliyorsa kullan.
7. **Kontrol et ve raporla.** Temsili kullanıcı görevleriyle adlandırma, şema doğrulaması, başarı/uyarı/hata yolları, tekrar güvenliği, yetki sınırı ve bağlam yeterliliğini sınamayı öner veya uygula. Ölçüm varsa görev tamamlama, yeniden denemeler, araç hataları ve bağlam kullanımı gibi ölçütleri kaydet. Henüz denenmemiş davranışı doğrulanmış gibi sunma. Sonucu mevcut durum, önerilen sözleşmeler, örnek yanıtlar, gerekçe ve açık doğrulama noktalarıyla raporla.

## Tasarım kararları

- Keşif yolu belirsiz görevlerde ajanın planlama ve araç seçimine alan bırak; yapısal ve deterministik işlemlerde türlenmiş, şemalı çağrıları tercih et. Hibrit yaklaşım çoğu zaman planlamayı yapılandırılmış yürütmeyle birleştirir; bunu her görev için tek doğru olarak sunma.
- Ajan yanıtı için yararlı bir asgari sözleşme: `status` (`success`, `warning`, `error` veya gerekiyorsa `unknown`), kısa `summary`, yapılandırılmış `result` ve uygulanabilir `next_actions`; dosya/kimlik üretilmişse `artifacts`. Alanları araca ve Cue arayüzüne göre sadeleştir, hepsini zorunlu kılma.
- Hata yanıtı, kullanıcıya yeniden denenebilirlik konusunda açık olmalı. Güvenli olmayan, izni olmayan veya sonucu belirsiz bir eylemi “tekrar dene” diye sunma.
- Araç sayısı, yanıt biçimi veya hız hedefi için ölçülmemiş rakamlar uydurma. Karar ölçüm gerektiriyorsa kontrollü değerlendirme için `agent-eval-cue` becerisini kullan.

## Kaynak ve lisans

Bu Cue uyarlaması, ECC deposundaki `skills/agent-harness-construction/SKILL.md` dosyasından türetilmiştir ve kapsamlı biçimde Cue'ya uyarlanmıştır. Sabit upstream commit: `b38be6a7f6350964d59328b52f0624e1d1d552d1`. [Kaynak dosya](https://github.com/affaan-m/ECC/blob/b38be6a7f6350964d59328b52f0624e1d1d552d1/skills/agent-harness-construction/SKILL.md). ECC MIT lisansının tam metni bu klasördeki `LICENSE` dosyasındadır; telif bildirimi © 2026 Affaan Mustafa. Bu, ECC'nin resmi becerisi veya onayı değildir.
