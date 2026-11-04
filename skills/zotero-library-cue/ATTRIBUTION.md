# Kaynak ve Uyarlama Bildirimi

Bu Cue becerisi, K-Dense Inc. tarafından hazırlanan `pyzotero` agent skill'inden yararlanılarak yeniden düzenlenmiştir:

- Kaynak depo ve sabitlenen commit: [`K-Dense-AI/scientific-agent-skills`, `a92663a0214b3b9fa1ba6b958284ffd919c00a0c`](https://github.com/K-Dense-AI/scientific-agent-skills/tree/a92663a0214b3b9fa1ba6b958284ffd919c00a0c)
- Kaynak dosya: [`skills/pyzotero/SKILL.md`](https://github.com/K-Dense-AI/scientific-agent-skills/blob/a92663a0214b3b9fa1ba6b958284ffd919c00a0c/skills/pyzotero/SKILL.md)
- Kaynak lisans: MIT; bu pakette `LICENSE` dosyasında korunmuştur.
- Sabitlenen upstream dosyasındaki metadata: skill sürümü 1.4, son inceleme 2026-09-30, Pyzotero hedef sürümü 1.15.2. K-Dense'in 2026-10-01 tarihli upstream commit geçmişinde bu dosya son kez güncellenmiş görünür; commit imzası doğrulanmış değildir.

Uyarlama; OpenClaw'a özgü metadata'yı ve başka istemciye yönelik kurulum örneklerini kaldırır; Cue'da gerçekten erişilebilir araç gerektiren bir kullanım kapısı, varsayılan salt-okunur işlem, açık yazma onayı, kimlik bilgisi gizliliği, veri minimizasyonu, zaman aşımı/tekrarlama güvenliği ve güncel sürüm belgelerine başvuru ekler. Upstream'ın uzun API/CLI/MCP referansları, 1.15.2 sürümüne bağlı ve güncel kamu belgeleriyle tutarsız olabildiğinden kopyalanmamıştır. Bu nedenle paket yalnızca yüksek seviyeli iş akışı ve kaynak bağlantılarını yeniden kullanır.

Uyarlama upstream yazarının veya K-Dense Inc.'in onayı/endorsmanı değildir. Yeniden dağıtımda MIT `LICENSE` dosyasını ve bu atıf bildirimini koruyun. Bu kaynak becerisi bilimsel çıktıya veya yazılım yayınlamaya maddi katkı sağlarsa, K-Dense becerisinin atıf talimatına uygun olarak en güncel bibliyografik kaydı kontrol edin:

Kassis, T., Agarwal, V., He, Y., Patel, D., & Brueckner, A. M. (2026). *Scientific Agent Skills: A Library of Procedural Knowledge for Research Agents*. arXiv:2609.00065. https://doi.org/10.48550/arXiv.2609.00065

Arşiv kaydı 2026-09-02 tarihinde güncellenen v2 sürümünü gösteriyordu; atıf DOI'si ve sürümsüz arXiv bağlantısı en güncel kayıt için kullanılmalıdır. Bu atıf, Pyzotero yazılımının kendi lisansının yerini almaz.
