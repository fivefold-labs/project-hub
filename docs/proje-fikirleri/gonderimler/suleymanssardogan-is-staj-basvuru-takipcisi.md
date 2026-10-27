# Proje Fikri Önerisi

> Şablon v1.1 · Durum: öneri; ekip kararı ve onaylanmış müşteri projesi değildir.

- Proje adı: İş / Staj Başvuru Takipçisi
- Öneren / GitHub: @suleymanssardogan; agent desteğiyle hazırlanmıştır.
- Tarih: 2026-10-27
- Fikir sürümü: v01
- Şablon sürümü: 1.1
- İlgili issue: [Fikir havuzu #2](https://github.com/fivefold-labs/project-hub/issues/2)
- Birlikte okunacak: [İki app için FDE değerlendirmesi](../raporlar/2026-10-27-iki-app-fde-degerlendirmesi.md)

## 01. Problem ve kullanıcı

İş/staj arayan kişi farklı sitelerdeki başvurularını, kullandığı CV sürümünü, görüşmelerini ve sonraki adımlarını tek yerde takip etmek isteyebilir. Bugünkü yöntemler notlar, tablolar, takvimler ve mevcut takip ürünleridir; hedef kitlenin gerçekten ne kullandığı görüşmeyle belirlenecek.

Bireysel uygulama: kullanıcı ilan bağlantısını ve metnini ekler, başvuru aşamasını günceller ve sonraki adımı hatırlar. FDE uyarlaması: bir kariyer merkezi veya bootcamp'in mevcut başvuru/mentorluk takibine uyarlanmış küçük çalışma alanı. Öğrencinin kendi seçtiği başvuru kayıtlarını danışmanla paylaşması ve kurumun kendi tablo biçiminde rapor alması hedeflenir.

Müşteri olduğu varsayılmıyor. Üniversite öğrencilerine erişim, kariyer merkezi karar vericisine veya kurum verisine erişildiği anlamına gelmez.

## 02. Kanıt ve varsayımlar

Doğrulanmış bulgular: Teal ücretsiz sınırsız başvuru takibi sunuyor; Huntr ücretsiz planda 100 işe kadar takip sunuyor. JobTeaser ve Symplicity kurumlara yönelik kariyer platformlarına sahip. Bu nedenle genel bir takip panosu yeni bir kategori değil.

Varsayımlar: öğrenciler mevcut ücretsiz araçları yetersiz buluyor; bir küçük kurum danışmanlık sürecinde tablo güncelleme işi yaşıyor; bireysel paylaşım kontrolleri yeterli; kurumdan izinli örnek veri ve süreç sahibi bulunabiliyor. Müşteri görüşmesi, kurumsal anlaşma ve ödeme kanıtı henüz yok.

## 03. Değer önerisi ve alternatifler

Değer önerisi: adayın başvuru ve sonraki adımını tek yerde tutarken, izin verdiği kayıtları danışmanın mevcut iş akışına bağlamak.

| Alternatif | Doğrulanan kapsam / fiyat | Fark için sınanacak hipotez |
|---|---|---|
| Teal | Ücretsiz sınırsız iş takibi; Teal+ 29 USD/30 gün | Küçük kurumun kendi alanları ve danışman iş akışı |
| Huntr | Ücretsiz 100 iş; Pro 40 USD/ay | Kuruma özgü içe/dışa aktarım ve dar Türkçe staj akışı |
| JobTeaser / Symplicity | Üniversite kariyer hizmetleri ve öğrenci/işveren süreçleri | Tam platform değişimi yerine küçük pilotun belirli işini kolaylaştırma |
| Excel / Notion / takvim | Görüşmede incelenecek mevcut iş akışı | Güncelleme ve danışman hazırlama süresinde azalma |

Türkçe arayüz, mobil kullanım veya AI eklemek tek başına üstünlük kanıtı değil. Kurum mevcut platformuyla ihtiyacını çözüyorsa yeni ürün satma gerekçesi zayıftır.

## 04. MVP kapsamı ve ana akış

En fazla üç temel özellik:

1. Link/metin veya izinli CSV'den kayıt: şirket, rol, kaynak, kullanıcı tarafından doğrulanan son tarih ve başvuru aşaması.
2. Başvuru başına not, kullanılan CV sürümünün kullanıcı tarafından verilen etiketi, sonraki aksiyon ve hatırlatıcı.
3. Tek kurumsal pilot için kayıt bazında öğrenci kontrollü paylaşım, danışman görünümü ve kurumun bir CSV iş akışına uyarlama.

Akış: ilanı ekle → bilgiyi doğrula → başvuru aşamasını güncelle → sonraki adımı belirle → istenen kaydı danışmanla paylaş → danışman görüşmesinde kullan.

Kapsam dışı: otomatik başvuru, iş sitelerini topluca kazıma, e-posta hesabını okuma, ATS entegrasyonları, CV üretimi, canlı AI mülakatı, işe alınma puanı ve aday sıralama. İlk sürümde CV dosyası saklamak yerine etiket kullanılabilir. Mobil uygulama ana kullanım; danışman için küçük web görünümü. Tek framework/platform seçimi ekip kapasitesiyle doğrulanır.

## 05. Gereksinimler ve başarı ölçütleri

- Başvuru durumu sistemin tahmini değil, kullanıcının beyanı olmalı; değişiklik kaydı tutulmalı.
- Öğrenci kendi kayıtlarını dışa aktarabilmeli ve silebilmeli. Danışman yalnızca açıkça paylaşılan kayıtları görebilmeli; paylaşım geri alınabilmeli.
- Eksik son tarih uydurulmamalı. Bildirim kapalıysa kullanıcı görebilmeli; hatırlatma kesin teslim garantisi taşımamalı.
- CSV aktarımı kuru çalıştırma/önizleme ve doğrulama sunmalı; tekrar aktarım kontrolsüz çoğaltmamalı.

Önerilen pilot hedefleri: 15 gönüllü katılımcı; en az 10'unun iki haftada tekrar durum/aksiyon güncellemesi; 5 görevden 4'ünün yardımsız tamamlanması; danışmanın görüşme hazırlama süresinde %30 azalma. Bunlar ölçülmüş sonuç değil; pilot öncesi kurumla kabul edilecek eşiklerdir. İşe girme oranı üç aylık MVP'nin başarı iddiası değildir.

## 06. Teknik yaklaşım ve ekip katkısı

Önerilen yapı: mobil istemci ve küçük danışman web ekranı → tek uygulama sunucusu → ilişkisel veritabanı → tek CSV adapteri. Kurumsal pilot tek kurumla sınırlandırılır; kurumun aşamaları ve alanları yapılandırma olarak tutulur. Ortak çekirdek ile müşteri yapılandırması ayrılır.

İlan metninden şirket/rol/tarih taslağı çıkarımı opsiyoneldir. Başlangıçta manuel giriş ve kurallar kullanılabilir; model kullanılırsa kullanıcı doğrulaması zorunlu, çıkarılan alanların kaynak metni görünür olmalı. AI aday seçmez, işe alım kararı vermez ve hassas özelliklerden puan üretmez. İki app fikrini birleştirmek MVP kapsamı değildir.

| Alan | Önerilen katkı |
|---|---|
| Süleyman / AI ve sistem tasarımı | Alan modeli, opsiyonel metin çıkarımı ve değerlendirme |
| Web/istemci | Mobil aday akışı ve dar danışman paneli |
| Agent/backend | Başvuru durumları, CSV adapteri ve onaylı veri akışı |
| Siber güvenlik | Öğrenci/danışman yetkileri, paylaşım ve silme testleri |
| Ağ/altyapı | Pilot dağıtımı, izleme, yedekleme, geri yükleme ve devir |

Kişi-alan dağılımı ekipçe doğrulanacak; her üyeye gereksiz modül veya agent yazdırılmayacak.

## 07. SDLC ve üç aylık plan

- 1–2. hafta: bir kariyer/mentorluk ekibi ve beş adayla görüşme; mevcut tablo örneği, alan eşleme, veri izinleri ve başlangıç ölçümü.
- 3–4. hafta: kayıt ekleme, aşamalar ve sonraki aksiyon; müşteriyle haftalık demo.
- 5–6. hafta: mobil kullanılabilirlik, hatırlatıcı ve tek CSV içe/dışa aktarımı.
- 7–8. hafta: kayıt bazında paylaşım, danışman görünümü ve izin testleri; test ortamında kabul.
- 9–10. hafta: 15 gönüllüyle sınırlı pilot; davranış ve süre ölçümü, hataların izlenmesi.
- 11–12. hafta: düzeltmeler, kurulum/yedekleme devri, kullanıcı eğitimi ve anonim vaka raporu.

Pilot kurum bulunamazsa tüketici prototipi yapılabilir, ancak gerçek müşteriyle FDE deneyimi elde edildiği iddia edilmez. Süreç çıktıları mevcut SDLC/SSDLC rehberine göre tutulur.

## 08. SSDLC ve güvenlik riskleri

| Risk | Önlem / test |
|---|---|
| Başka öğrencinin özel başvurusuna erişim | Sunucu tarafında sahiplik kontrolü; doğrudan kayıt kimliğiyle erişim testleri |
| Danışmana gereğinden fazla veri açılması | Kayıt bazında açık paylaşım; geri alma; CSV dışa aktarımında aynı filtrelerin uygulanması |
| İlan metni veya linkten zararlı içerik | İçeriği veri olarak işleme; güvenli görüntüleme; sunucudan rastgele URL getirmeme; dış eylem öncesi onay |

Ekran görüntüsü, CV ve aday notları genel loglara yazılmaz. Gerçek kayıtlar public repoya eklenmez. Pilot başlamadan veri alanları, saklama süresi, silme, katılımcı bilgilendirmesi ve kurum sorumlusu netleşir. Kurum etiketi/giriş sistemi dahil yeni gereksinimler ayrıca kapsam değerlendirmesine alınır. Bu belge mevzuata uyumluluk iddiası değildir.

## 09. Test, yayın ve işletim

Aşama geçişleri, tarih/saat dilimi, eksik alanlar, tekrarlanan ilan ve CSV kodlaması sınanır. Paylaşımı geri alınan kaydın danışman görünümünden kalkması, dışa aktarımın gizli kayıtları içermemesi ve silmenin doğru çalışması test edilir. Bildirim izni reddi ve yeniden giriş davranışı gerçek cihazlarda kontrol edilir.

Kurumun izinli örnek dosyasıyla uçtan uca kabul: içe aktar → düzelt → durum değiştir → paylaş → danışman görsün → paylaşımı geri al. Pilot için hata izleme, yedekten geri yükleme denemesi ve önceki sürüme dönüş adımı gerekir. Kuruma işleyiş, alan eşlemesi ve operatör rehberi teslim edilir.

## 10. Pazar, maliyet ve uygulanabilirlik

Bireysel adaylar ilk kullanıcı olabilir; güçlü ücretsiz rakipler nedeniyle temel takip işinden ücret almak zor olabilir. FDE sürümünde olası ödeme yapan taraf küçük bootcamp, kariyer/mentorluk kuruluşu veya üniversite birimidir. Satın alma süresi ve izin süreçleri üç ayı aşabilir; ilk iki haftada süreç sahibi ve izinli pilot bulunması gerekir.

Bütçe önerisi: küçük pilot için aylık 0–30 USD altyapı üst hedefi; opsiyonel AI denemesi 0–10 USD/ay ile sınırlandırılır. Bunlar onaylanmış harcama veya güncel servis fiyat teklifi değil; tasarım bütçesidir. Barındırma, veri saklama, destek ve yedekleme gerçek tüketimle ölçülür. AI'sız akış çalışmalı. Müşteri ortamında kurulumun da işletim maliyeti ve sorumlusu vardır.

Gelir hipotezi: dar bir kurumsal pilot için kurulum/uyarlama bedeli ve isteğe bağlı dönemlik destek. Fiyat ve ödeme isteği doğrulanmadı; rakip abonelikleri bizim ürün için fiyat kanıtı değildir. Müşteriye özel her isteği kodlamak yerine tekrarlanabilir tek adapter ve yapılandırma hedeflenir.

## 11. İlk doğrulama deneyi

Bir haftada beş aktif iş/staj arayan kişi ve en az iki danışman/koordinatörle görüşün. Son takip yöntemlerini ve bir danışman görüşmesini gözlemleyin. Gerçek kişisel verileri toplamadan örnek CSV ve alan eşleme çıkarın. Sorumlular ilk ekip toplantısında atanacak.

Devam koşulu: bir kurum iki haftalık pilotu, bir süreç sahibi ve izinli örnek akışı kabul eder; en az üç aday bir haftada ikinci kez kullanır; danışmanın hazırlık süresinde azalma görülür. FDE devam koşulu kurum erişimidir, öğrenci sayısı tek başına yeterli değildir. Kurum arayışı ikinci hafta sonunda sonuçsuzsa FDE önceliği için başka aday seçilir.

## 12. Kaynaklar, açık sorular ve karar isteği

Kaynak erişim tarihi: 27 Ekim 2026. Fiyatlar resmî liste beyanıdır; vergi, bölge ve paket koşulları değişebilir. Özellikler bağımsız test edilmedi.

- [Teal fiyatları](https://www.tealhq.com/pricing): ücretsiz sınırsız takip, 29 USD/30 gün Teal+ seçeneği.
- [Huntr resmî yardım / planlar](https://help.huntr.co/en/articles/9806024-faq): ücretsiz 100 iş, aylık 40 USD Pro.
- [JobTeaser](https://www.jobteaser.com/en): kariyer merkezi modeli.
- [Symplicity öğrenci uygulaması](https://www.symplicity.com/en-us/symplicity-jobs-and-careers-symplicity): kurumsal kariyer süreçleri.
- [SLU'nun Symplicity kullanım açıklaması](https://www.slu.edu/law/career-services/symplicity.php): kurum içi kullanım örneği; bizim pilot talebimizi doğrulamaz.

Açık sorular: hangi kurum, hangi veri alanları, hangi izin modeli, tekrar kullanım ve ödeme isteği var mı? İstenen karar: bu fikri seçmek değil, kurum görüşmeleri ve dar pilot için değerlendirmeye almak.
