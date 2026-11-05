# Araç / action sözleşmesi

> Her araç için kopyala. Bilinmeyen alanları varsayımla doldurmak yerine `bilinmiyor` olarak işaretle.

## Kimlik ve kapsam

- **Ad:** `[kararlı, açık araç adı]`
- **Amaç:** `[tek cümle; hangi kullanıcı görevini çözer?]`
- **Dahil olanlar:** `[kapsam]`
- **Dahil olmayanlar:** `[yakın araçlardan sınır]`
- **Yan etki / etki düzeyi:** `[salt-okunur | yerel değişiklik | dış hizmet değişikliği | yüksek etkili]`
- **Yetki / onay:** `[hangi erişim var, hangi durumda kullanıcı onayı gerekir?]`
- **İdempotency / tekrar davranışı:** `[güvenli tekrar koşulu; belirsiz sonuçta yapılacak kontrol]`
- **Sınırlar:** `[zaman aşımı, öğe sayısı, veri boyutu vb.; bilinmiyorsa belirt]`

## Girdi sözleşmesi

| Alan | Tür / değer aralığı | Zorunlu? | Varsayılan | Açıklama / doğrulama |
|---|---|---|---|---|
| `[alan]` | `[string / enum / number / object]` | `[evet/hayır]` | `[yok/değer]` | `[kısıt]` |

## Yanıt sözleşmesi

- **Başarı:** `[kararlı alanlar; sonucu ve kanıtı belirt]`
- **Kısmi başarı:** `[hangi durumlarda; tamamlanan ve tamamlanmayan işler]`
- **Hata:** `[status, kısa neden, güvenli sonraki adım]`
- **Belirsiz sonuç:** `[ör. zaman aşımından sonra durum kontrolü; körlemesine yeniden çağırma yok]`
- **Üretilen artifact:** `[dosya yolu / kayıt kimliği / yok]`

## Örnek yanıt

```json
{
  "status": "success | warning | error | unknown",
  "summary": "[tek cümle]",
  "result": {},
  "artifacts": [],
  "next_actions": []
}
```

## Kontrol örnekleri

1. **Geçerli girdi:** `[beklenen sonuç]`
2. **Geçersiz girdi:** `[reddedilme ve açıklama]`
3. **Yetkisiz/onarım gerektiren çağrı:** `[engelleme veya onay akışı]`
4. **Bağımlılık hatası/zaman aşımı:** `[güvenli kurtarma ve durma koşulu]`
5. **Tekrar çağrısı:** `[idempotency davranışı]`
