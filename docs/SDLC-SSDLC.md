# SDLC ve SSDLC çalışma süreci

SDLC (Software Development Life Cycle) tüm ürün geliştirme akışımızdır. SSDLC (Secure SDLC), güvenlik çalışmalarını aynı akışın her aşamasına entegre eder. Kısa iterasyonlarla ilerleriz; bu belge ayrı bir şelale proje planı değildir.

Siber güvenlik alanındaki arkadaşımız güvenlik koordinatörüdür. Kişi-alan eşleştirmesi henüz paylaşılmadığı için isim atanmadı. Tüm geliştiriciler kendi değişikliklerinin güvenliğinden sorumludur; güvenlik koordinatörü gereksinimleri, incelemeleri ve güvenlik doğrulamasını yönlendirir.

| Aşama | Ekip / SDLC çıktısı | Güvenlik koordinatörü / SSDLC katkısı | Geçiş ölçütü |
|---|---|---|---|
| Planlama ve keşif | Problem, hedef kullanıcı, kapsam, kapasite ve bütçe varsayımları | Veri hassasiyeti, kötüye kullanım olasılıkları ve ilk risk listesi | Varsayımlar ve araştırma sorumluları kayıtlı |
| Gereksinim analizi | Kullanıcı hikâyeleri ve kabul ölçütleri | Yetki, veri saklama ve güvenlik kabul ölçütleri | Kritik akışların işlevsel ve güvenlik beklentileri tanımlı |
| Tasarım | Mimari, veri modeli, API ve ağ akışları | Tehdit modeli, güven sınırları, kimlik/yetki ve veri koruma tasarımı | Önemli tehditler ve azaltıcı önlemler incelenmiş |
| Geliştirme | Küçük PR'lar, kod incelemesi ve birim testleri | Güvenli kod incelemesi, bağımlılık ve secret kontrollerinin kurulmasına rehberlik | PR onaylı, ilgili kontroller başarılı |
| Test | Entegrasyon, uçtan uca ve kullanıcı kabul testleri | Yetkisiz erişim, girdi doğrulama, kötüye kullanım ve gerektiğinde güvenlik testleri | Bulgular kayıtlı; sürümü engelleyen açık sorun yok |
| Yayın | Tekrarlanabilir dağıtım, yapılandırma ve geri dönüş planı | En az yetki, secret yönetimi, güvenli yapılandırma ve log kontrolü | Yayın kontrol listesi tamamlanmış |
| Bakım ve iyileştirme | Kullanıcı geri bildirimi, hata ve performans takibi | Zafiyet takibi, yamalama, olay müdahalesi ve kök neden analizi | İşlerin sahibi ve önceliği belli |

## Üç ay içinde uygulanışı

İlk iki haftada keşif ve kapsam; sonraki haftalarda geliştirme/test iterasyonları; son bölümde pilot, yayın ve iyileştirme. Güvenlik gereksinimleri ve tehdit modeli erken hazırlanır, önemli değişikliklerde güncellenir. Ayrıntı: [yol haritası](ROADMAP.md).

## İş kaydı ve tamamlanma

Her iş issue ile takip edilir. Gereksinim, ilgili PR, test sonucu ve risk kararı bağlantılı tutulur. Her PR güvenlik etkisini belirtir; etkisi yoksa kısa gerekçe yeterlidir. Kimlik doğrulama, yetki, kullanıcı verisi, dış araç çağrısı veya ağ sınırı değiştiren PR'lar güvenlik koordinatörünün incelemesine sunulur. GitHub şu anda genel olarak bir onay zorunlu tutar; güvenlik kişisine özel CODEOWNERS kuralı henüz tanımlı değildir.

Güvenlik bulgusu için etki, tekrar üretim bilgisi, çözüm sorumlusu ve hedef tarih belirlenir. Yüksek etkili açık bulgular giderilmeden yayın yapılmaz. Repo public olduğu için istismar ayrıntıları ve hassas veriler genel issue'ya konmaz; [güvenlik bildirim süreci](../SECURITY.md) kullanılır.

## Başlangıçta hazırlanacak güvenlik çıktıları

- Güvenlik gereksinimleri ve kabul ölçütleri.
- Veri akışı / güven sınırları ve kısa tehdit modeli.
- Risk listesi: etki, olasılık, önlem, sorumlu, durum.
- Güvenlik test planı ve bulgu kayıtları.
- Yayın kontrol listesi ve olay müdahale adımları.

Bunlar proje seçildikten sonra ürünün riskine göre detaylandırılır. Kullanılacak tarama araçları, CI ve altyapı henüz seçilmedi; bu belgede çalışır durumda oldukları iddia edilmez.

Yaklaşım referansı: [NIST Secure Software Development Framework](https://csrc.nist.gov/projects/ssdf). NIST, güvenli geliştirme pratiklerinin SDLC'ye entegre edilmesini önerir; bu çalışma bir uyumluluk veya sertifikasyon iddiası değildir.
