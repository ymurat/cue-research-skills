---
name: agent-eval-cue
description: Cue ajanı, model, araç seti, istem veya iş akışını tekrarlanabilir görevlerle karşılaştırmak; sürüm değişikliklerini ölçmek; başarı, süre, maliyet ve güvenilirlik sonuçlarını raporlamak gerektiğinde kullan. Dış değerlendirme CLI'si gerektirmeden değerlendirme planı oluşturmak veya yürütmek için de kullan.
---

# Cue için tekrarlanabilir ajan değerlendirmesi

Ajan yapılandırmalarını izlenebilir, adil ve görev temsili olan bir değerlendirmeyle karşılaştır. İzlenim yerine sabit görevler, sabitlenmiş yapılandırmalar, açık puanlama kuralları ve ham çalıştırma kayıtları kullan. Bu beceri bir yöntemdir; değerlendirme CLI'si, Python paketi veya belirli bir çalıştırma platformu sağlamaz ve bunlara bağımlı değildir.

## Ne zaman kullanılır

- Ajan/model/istem/beceri/araç yapılandırmaları arasında seçim yaparken.
- Bir yapılandırma değişikliğinin gerçek görev performansını etkileyip etkilemediğini ölçerken.
- Sürüm, araç veya politika güncellemesinden sonra gerileme kontrolü planlarken.
- Bir ekip ya da araştırma grubu için kanıta dayalı karşılaştırma ve karar kaydı hazırlarken.

## İş akışı

1. **Karar sorusunu sabitle.** Neyi karşılaştırdığını ve hangi kararı destekleyeceğini yaz. Aday yapılandırmaları ve aynı kalacak unsurları belirle. Bir turda mümkünse tek ana değişkeni değiştir; aynı anda birden çok değişiklik varsa sonucu bunlardan hangisinin doğurduğunu iddia etme. Mevcut temel/baseline'ı kaydet.
2. **Temsili ve sürümlenmiş görev kümesi oluştur.** `templates/evaluation-plan.md` dosyasını kullan. Görevleri gerçek kullanım dağılımından seç; kolay, tipik, zor ve hata/kenar durumlarını dahil et. Her görev için benzersiz kimlik, başlangıç girdisi ve durumu, kullanıcı isteği, izin verilen araçlar, kısıtlar, başarı ölçütü, puanlayıcı/kanıt ve önem ağırlığını tanımla. Aynı görev tanımlarını tüm adaylara uygula; değerlendirme sırasında görev veya eşik değiştirilirse sürüm ve gerekçeyi kaydet.
3. **Yapılandırmaları ve ortamı sabitle.** Ajan ve model adı/sürümü biliniyorsa, sistem/başlangıç yönergeleri, etkin beceriler, araç şemaları ve izinleri, bağlam ayarları, başlangıç verisi/depo revizyonu, yargıç sürümü ve çalıştırma koşullarını kaydet. Bilinmeyen sürüm veya maliyet bilgisini tahmin etme; `bilinmiyor` olarak işaretle. Aynı araç erişimi, veri, zaman sınırı ve benzer koşulları uygula.
4. **İzole ve kontrollü çalıştır.** Önceki denemelerden kalan durumun sonraki adayı etkilemesini önle; mümkünse her denemeye temiz başlangıç ver. Gizli kullanıcı verisi ve canlı yan etkiler yerine sentetik veya yetkili test verisi kullan. Sıra etkisi olasıysa adayların sırasını dengele veya kaydet. Mevcut onaylı Cue araçlarıyla, elle ya da var olan test altyapısıyla çalış; `agent-eval` adlı dış CLI'yi kurmayı/çağırmayı gerektirme.
5. **Deneme sayısını ve puanlamayı belirle.** Rastlantısallık beklenen görevlerde her yapılandırmayı aynı görevlerde en az üç kez çalıştırmayı varsayılan öneri olarak kullan; maliyet, etki veya istikrar gereksinimi farklıysa sayıyı gerekçelendir. Önceden belirlenmiş deterministik kontrolleri (test, şema, beklenen alan, politika uyumu) önceliklendir. İnsan veya model yargıcı gerekiyorsa ölçütlü rubrik kullan; modeli tek hakem yapma, mümkünse körle ve küçük bir insan kontrol örneklemiyle kalibre et.
6. **Çalıştırma başına ham kayıt tut.** Zaman damgası, görev/sürüm kimlikleri, yapılandırma, deneme numarası, başarı ve puanlama kanıtı, süre, gözlenmiş maliyet ve para birimi, yeniden deneme sayısı, araç hataları, insan müdahalesi ve eksik ölçümleri kaydet. Süreyi ve maliyeti gerçekten ölçmediysen bunları yaklaşık gerçekmiş gibi yazma; `yok` veya `ölçülmedi` de. Başarısız, yarıda kalmış veya protokol dışı denemeleri sessizce silme; dışlama kuralını önceden belirle ve sonucu ayrıca raporla.
7. **Sonuçları karşılaştır.** Görev ve deneme paydalarını göstererek tamamlanma/başarı oranını hesapla; varsa kısmi kaliteyi önceden tanımlı rubrikle ayrıca raporla. Süre ve maliyet için ortalama yanında dağılımı (ör. medyan ve aralık) göster. Güvenilirlik için tekrarlar arasındaki başarı tutarlılığını, yeniden denemeleri ve araç hatalarını raporla. Mutlak farkı ve göreli farkı karıştırma; küçük örneklemden istatistiksel anlamlılık veya genellenebilirlik iddia etme. Görevler arası ağırlıklı puan kullandıysan ağırlıkları açıkla.
8. **Karar ve sınırlamaları bildir.** Kısa sonuç, değerlendirme sorusu, baseline ve aday ayarları, görev kümesi, ölçütler, sonuç tablosu, önemli başarısızlık örüntüleri, maliyet/süre dengesi, eksik veriler ve kapsam dışını sun. Hangi kararın desteklendiğini ve hangi kararın bu örneklemden çıkarılamayacağını ayır. Görev kümesini, yapılandırma snapshot'larını ve ham kayıtları sonraki regresyon karşılaştırması için sakla.

## Ölçütleri yorumlama

| Ölçüt | Kaydetme ve yorumlama |
|---|---|
| Başarı/tamamlama | Başarılı görev sayısı / geçerli görev denemesi sayısı; ölçütün ve başarısızlık tanımının ne olduğunu açıkla. |
| Kalite | Önceden tanımlı rubrik puanı ve kanıt; başarı oranından ayrı tut. |
| Süre | Aynı başlangıç/bitiş kuralıyla ölçülen duvar saati; dağılımı ve varsa zaman aşımını göster. |
| Maliyet | Yalnızca gözlenebilir kullanım maliyeti ve para birimi; kaynak/hesaplama yöntemi biliniyorsa belirt. Bilinmeyeni tahmin etme. |
| Güvenilirlik | Tekrar başına sonuç dağılımı, tutarlılık, yeniden deneme/araç hatası ve insan müdahalesi. |

## Koruyucu ilkeler

- Sonuçlar ajan kalitesi kadar görev seçimi, puanlayıcı, araç izinleri, örneklem büyüklüğü ve çalışma koşullarına da bağlıdır. Bunları raporda görünür kıl.
- Puanlayıcı ölçütlerini sonuca bakarak değiştirme. Değiştirmen gerekirse görev kümesini yeni sürümle yeniden değerlendir veya değişikliği ayrı belirt.
- Model tabanlı puanlamanın gürültüsünü, yargıç talimatını ve kalibrasyonunu raporla; yargıç yanıtını nesnel gerçek sayma.
- Birkaç testteki başarıyı tüm kullanıcı işlerine genelleme. Üretim güvenliği, güvenlik denetimi ya da bilimsel geçerlilik iddia etmek için bu becerinin verdiğinden daha geniş kanıt gerekir.
- Bu görev operasyonel/hafif bir ürün değerlendirmesinden akademik deney tasarımına genişliyorsa `research-design` veya ilgili araştırma becerisini de kullan; burada bu becerilerin yerine geçme.

## Kaynak ve lisans

Bu Cue uyarlaması, ECC deposundaki `skills/agent-eval/SKILL.md` dosyasının yöntemini temel alır; Cue kullanımına göre yeniden yazılmıştır. Sabit upstream commit: `b38be6a7f6350964d59328b52f0624e1d1d552d1`. [Kaynak dosya](https://github.com/affaan-m/ECC/blob/b38be6a7f6350964d59328b52f0624e1d1d552d1/skills/agent-eval/SKILL.md). ECC MIT lisansının tam metni bu klasördeki `LICENSE` dosyasındadır; telif bildirimi © 2026 Affaan Mustafa. Upstream skill'in bağlantı verdiği `joaquinhuigomez/agent-eval` ayrı projedir; bu uyarlama o projenin kodunu veya CLI'sini içermiyor ve onu kurmayı gerektirmiyor. Bu, ECC'nin resmi becerisi veya onayı değildir.
