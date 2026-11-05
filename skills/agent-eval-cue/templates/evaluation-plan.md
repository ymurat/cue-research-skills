# Cue ajanı değerlendirme planı

## Karar sorusu

- **Soru:** `[hangi kararı destekleyecek?]`
- **Baseline:** `[tam yapılandırma adı/sürümü]`
- **Aday(lar):** `[karşılaştırılacak yapılandırmalar]`
- **Değişen ana unsur:** `[tek değişken; birden fazlaysa listele]`
- **Değişmeden kalacak koşullar:** `[görev, izin, veri, sınırlar vb.]`

## Sabit yapılandırmalar

| Alan | Baseline | Aday | Kaynak / not |
|---|---|---|---|
| Ajan / model / sürüm | | | |
| Başlangıç yönergesi | | | |
| Etkin beceriler | | | |
| Araçlar / şemalar / izinler | | | |
| Bağlam ayarı | | | |
| Başlangıç verisi / revizyon | | | |
| Zaman / maliyet sınırı | | | |
| Puanlayıcı / rubrik sürümü | | | |

## Sabit görev kümesi

| Görev ID | Kategori | Başlangıç durumu ve istek | İzinler / kısıtlar | Başarı ölçütü ve kanıt | Puanlayıcı | Ağırlık |
|---|---|---|---|---|---|---|
| `T-01` | | | | | | |

## Çalıştırma protokolü

- **Görev kümesi sürümü:** `[etiket/commit]`
- **Deneme sayısı:** `[aday başına; gerekçe]`
- **Başlangıç durumunu sıfırlama:** `[nasıl]`
- **Çalıştırma sırası:** `[sabit/dengeli/rastgele ve nasıl kaydedilecek]`
- **Dışlama kuralı:** `[önceden tanımlı geçersiz deneme koşulları]`
- **Güvenli test verisi / yan etki kontrolü:** `[sentetik veri, sandbox, izin]`

## Deneme kayıtları

| Run ID | Tarih/saat | Aday | Görev ID | Tekrar | Başarı/puan | Süre | Maliyet+birim | Yeniden deneme | Araç hatası / insan müdahalesi | Kanıt / not |
|---|---|---|---|---|---|---|---|---|---|---|
| | | | | | | | | | | |

`ölçülmedi`, `bilinmiyor` ve `uygulanamaz` değerlerini birbirinden ayır. Başarısız/yarım kalan çalıştırmaları da kaydet.

## Sonuç özeti

| Aday | Başarı payı (n/N) | Kalite (rubrik) | Süre (medyan/aralık) | Maliyet (ölçüm kaynağı) | Tutarlılık / hata örüntüsü |
|---|---|---|---|---|---|
| Baseline | | | | | |
| Aday | | | | | |

## Yorum ve karar

- **Önemli farklar:** `[mutlak fark ve payda]`
- **Başarısızlık örüntüleri:** `[görev kimlikleri ve kanıt]`
- **Karar / gerekçe:** `[sonuçların desteklediği sınırlı iddia]`
- **Sınırlamalar:** `[örneklem, ölçüm eksikleri, puanlayıcı, temsil gücü]`
- **Sonraki tekrar için saklananlar:** `[görev sürümü, yapılandırmalar, ham kayıtlar]`
