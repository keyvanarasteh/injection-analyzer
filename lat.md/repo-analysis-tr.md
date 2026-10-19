# Depo analizi şablonu (TR)

Bu sayfa, belgelenmiş enjeksiyon tekniklerini depo koduyla eşleştirmek için kısa ve tekrar kullanılabilir bir kontrol listesidir.

**Dil:** [EN](repo-analysis-en.md) | [TR](repo-analysis-tr.md) · [[lat.md#Repository injection analysis workflow|Akış diyagramı]]

## 1. Depoyu seç ve edin

İncelenen kaynağı ve edinme bilgilerini kaydedin.

- Depo URL'si: `[URL]`
- Revizyon (commit/etiket): `[revizyon]`
- Edinme tarihi: `[tarih]`
- Kapsam ve hariç tutulanlar: `[dizinler, üretilmiş veya vendored kod]`
- Kaynak notları: `[klon/arşiv kaynağı ve kısıtlar]`

## 2. Dilleri ve frameworkleri belirle

Manifest, kilit dosyaları, derleme ayarları ve kaynak dosyalarını kanıt olarak kullanın; mümkün olduğunda sürümleri kaydedin.

| Teknoloji | Sürüm kanıtı ve kaynağı | Resmi site | Dokümantasyon URL'leri |
|---|---|---|---|
| `[ad]` | `[dosya ve sürüm]` | `[URL]` | `[sürümle eşleşen URL ve bölüm]` |

## 3. Belgelenmiş enjeksiyon tekniklerini bul

Resmi ve sürümle eşleşen dokümantasyonu kullanın. Terimleri, koşulları, ilgili API veya ayar örüntülerini ve azaltma önlemlerini kaydedin.

| Teknik | Dokümantasyon kanıtı | Koşullar / tanınabilir örüntüler | Sürüm kapsamı |
|---|---|---|---|
| `[teknik]` | `[URL, bölüm, kısa açıklama]` | `[koşullar ve API'ler]` | `[sürümler]` |

Dokümantasyonun söylediğiyle kendi yorumunuzu ayrı tutun.

## 4. Teknikleri kaynak kodla eşleştir

Belgelenmiş API'leri, sink'leri, ayar örüntülerini ve ilişkili veri akışlarını arayın. İlgili her kaynak konumunu kaydedin; metinsel eşleşme tek başına istismar edilebilirliği kanıtlamaz.

| Teknik | Kaynak yolu ve satır/sembol | Rol ve veri akışı | Kanıt durumu |
|---|---|---|---|
| `[teknik]` | `[yol:satır veya sembol]` | `[kaynak → dönüşüm → sink]` | `[doğrulandı / kısmi / bulunamadı]` |

## 5. Fonksiyonları ve çağıranları izle

Her eşleşmenin bulunduğu fonksiyonu, çağıranları ve giriş noktasını belirleyin. Güvenilmeyen girdinin ilgili işleme ulaşıp ulaşmadığını izleyin.

| Kaynak sembolü | İçeren fonksiyon | Çağrı zinciri / giriş noktası | Girdi ve erişilebilirlik kanıtı |
|---|---|---|---|
| `[yol#sembol]` | `[fonksiyon/sınıf]` | `[çağrı zinciri]` | `[kaynak ve gerekçe]` |

Erişilebilirlik veya çağrı yolu doğrulanmamışsa bu sınırı açıkça belirtin.

## 6. İnsan tarafından okunabilir bulguları yaz

Kod davranışını, girdiyi, veri/kontrol akışını ve dokümantasyonla eşleşmeyi sade bir dille açıklayın.

- Bulgu: `[kısa başlık ve etkilenen bileşen]`
- Koşullar ve etki: `[hangi durumda önemli]`
- Güven düzeyi: `[yüksek / orta / düşük, gerekçesiyle]`
- Kanıt: `[kaynak konumları ve dokümantasyon URL'leri]`
- Varsayımlar veya boşluklar: `[maddeler]`

Olguları, analizi ve varsayımları ayrı tutun. Olumsuz aramalarda kapsamı ve arama örüntülerini belirtin; eşleşme bulunmaması yokluğun kanıtı değildir.

## 7. Sonraki aşamaya devret

Bir sonraki analiz aşamasının ihtiyaç duyacağı bilgileri kaydedin.

- Doğrulanmış bulgular: `[özet ve referanslar]`
- Kısmi eşleştirmeler veya kanıt boşlukları: `[maddeler]`
- Aranıp bulunamayan teknikler: `[kapsam ve terimler]`
- Sorular ve sonraki adımlar: `[maddeler]`
