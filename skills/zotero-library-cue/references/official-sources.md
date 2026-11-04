# Resmî Kaynaklar ve Sürüm Kontrolü

Bu aday sürümden bağımsız bir iş akışı sunar. API parametresi, paket sürümü, CLI/MCP özelliği veya izin akışı için her görevde güncel kaynakları kontrol edin; eski örnekleri doğrulamadan çalıştırmayın.

## Öncelikli kaynaklar

1. [Zotero Web API v3 — Basics](https://www.zotero.org/support/dev/web_api/v3/basics): API sürümü, kütüphane kimlikleri, rate limit, sürümleme ve genel sözleşmeler.
2. [Zotero Web API v3 — Local API](https://www.zotero.org/support/dev/web_api/v3/local_api): yerel API erişimi, masaüstü izinleri ve yerel davranış farkları.
3. [Zotero API — Write Requests](https://www.zotero.org/support/dev/web_api/v3/write_requests): kayıt oluşturma/güncelleme ve yazma yanıtları.
4. [Pyzotero resmi belgeleri](https://pyzotero.readthedocs.io/): güncel API istemci, CLI ve varsa MCP kullanımı.
5. [Pyzotero PyPI sayfası](https://pypi.org/project/pyzotero/): yayımlanmış paket sürümü ve paket metadatası.
6. [Pyzotero kaynak deposu](https://github.com/urschrei/pyzotero): sürüm etiketi, kaynak kodu ve değişiklik geçmişi.
7. [Pyzotero lisansı](https://github.com/urschrei/pyzotero/blob/main/LICENSE.md): yazılım paketinin kendi lisansı; bu becerinin K-Dense lisansından ayrıdır.

PyPI sayfası, Pyzotero yazılımını Blue Oak Model Licence 1.0.0 kapsamında gösteriyor. Bu paketteki MIT bildirimi K-Dense beceri-teksti/uyarlaması içindir; Pyzotero yazılımının kodunu, lisansını veya yeniden dağıtım hakkını kapsamaz. Pyzotero'yu kurmadan, kodunu yeniden dağıtmadan veya ona dayalı başka bir paket hazırlamadan önce kendi lisansını ve güncel sürümünü yeniden kontrol edin.

## Bu adayın kaynak sürümündeki uyarı

Sağlanan arşivdeki K-Dense `pyzotero` metni 1.15.2 sürümünü ve 2026-09-30 inceleme tarihini belirtiyor. 2026-11-05 tarihli dış kaynak kontrolünde PyPI sayfası ve dokümantasyon sürüm gösterimleri birbiriyle tam uyuşmadı. Bu nedenle bu Cue uyarlaması sabit bir Pyzotero sürümü, kurulum komutu veya MCP/CLI sözleşmesi vermiyor. Gerçek çalıştırmadan önce PyPI, Pyzotero belgeleri ve Zotero API sayfalarındaki sürüm ve yetkilendirme bilgilerini karşılaştırın; bu kaynaklardan emin olunamazsa yalnızca okuma veya kullanıcı tarafından dışa aktarılmış dosyalarla devam edin.

## Cue erişimi hakkında

Pyzotero'nun CLI/MCP belgelerinde başka istemciler ve yerel Zotero kurulumu için örnekler olabilir. Bunlar Cue'nun kurulu entegrasyonu oldukları anlamına gelmez. Cue'da Zotero bağlantısı/izinli yürütme aracı gerçekten yoksa yerel API, masaüstü uygulaması, dosyalar veya kimlik bilgileri üzerinde işlem yapmayın; kullanıcıya bunu açıkça söyleyin.
