# Proje Fikri Önerisi

> Şablon v1.1 · Durum: öneri; ekip kararı ve onaylanmış müşteri projesi değildir.

- Proje adı: Ekran Görüntüsünden Aksiyon
- Öneren / GitHub: @suleymanssardogan; agent desteğiyle hazırlanmıştır.
- Tarih: 2026-10-27
- Fikir sürümü: v01
- Şablon sürümü: 1.1
- İlgili issue: [Fikir havuzu #2](https://github.com/fivefold-labs/project-hub/issues/2)
- Birlikte okunacak: [İki app için FDE değerlendirmesi](../raporlar/2026-10-27-iki-app-fde-degerlendirmesi.md)

## 01. Problem ve kullanıcı

İnsanlar ilan, ürün veya etkinlik ekran görüntüsü kaydediyor; daha sonra içeriği bulmak, tarihi hatırlamak ve bir işlem yapmak için tekrar elle düzenleme gerekiyor. Bu davranışın sıklığı ve aciliyeti henüz kullanıcı görüşmesiyle doğrulanmadı.

Bireysel kullanım: kullanıcı seçtiği görseli uygulamaya paylaşır; metin ve alan taslağını kontrol eder, aranabilir kayda dönüştürür ve hatırlatıcı ekler. İlk mobil deneme Android ve tek içerik türüyle sınırlandırılır; tür pilot görüşmesinde seçilir.

FDE pilotu için önerilen uyarlama: küçük bir yazılım ajansında destek koordinatörü, müşteriden gelen hata ekran görüntüsünü başlık, açıklama ve takip adımı içeren taslağa dönüştürür; inceleyip mevcut iş takip sistemine aktarır. Bu, kişisel uygulama fikrinin kuruma uyarlanmış ayrı pilot kapsamıdır. Ajansın gerçek akışına ihtiyaç kanıtlanmadan geliştirilmez.

## 02. Kanıt ve varsayımlar

Doğrulanmış masa başı bulguları: Pixel Screenshots arama ve hatırlatma sunuyor; mymind görüntü içindeki metinle arama ve otomatik etiketleme sunuyor. Bu özellikler yeni değil. Google ML Kit, Android üzerinde OCR için teknik bir aday; Türkçe desteklenen diller arasında. Kaynaklar bölümünde resmî bağlantılar var.

Henüz doğrulanmayanlar: Türkçe kullanıcıların bu sorun için ayrı uygulama açacağı, destek ekiplerinin ekran görüntülerini yapılandırmakta yeterince zaman kaybettiği, müşterinin entegrasyon erişimi sağlayacağı ve ödeme yapacağı. Kullanıcı görüşmesi, pilot, doğruluk testi veya ücretli satış yapılmadı.

## 03. Değer önerisi ve alternatifler

Değer önerisi: seçilen ekran görüntüsünü, kaynağı görülebilen ve kullanıcı tarafından doğrulanmış bir takip kaydına dönüştürmek.

| Alternatif | Doğrulanan özellik / mevcut yaklaşım | Araştırılacak fark |
|---|---|---|
| Pixel Screenshots | Görsellerde arama, önerilen aksiyonlar ve hatırlatıcı | Hedef kullanıcıların cihaz/dil ihtiyacı ve kurumsal akışı |
| mymind | Görsel metni tanıma, etiketleme ve arama; Student of Life planı 7,99 USD/ay | Kişisel arşiv yerine belirli aksiyona ve kurum alanlarına dönüşüm |
| Galeri + not uygulaması | Kullanıcının kendi mevcut yöntemi; görüşmede gözlemlenecek | Daha az düzeltme ve daha kısa kayıt süresi |

Yerel OCR ve Türkçe arayüz tek başına benzersizlik iddiası değildir. İlk ajans, mevcut aracının yerleşik özellikleri veya bir otomasyonla aynı işi daha kolay yapabiliyorsa projeyi yeniden değerlendirin.

## 04. MVP kapsamı ve ana akış

En fazla üç temel özellik:

1. Kullanıcının seçtiği görselden cihazda OCR, alan taslağı ve kaynakla yan yana doğrulama.
2. Düzenlenebilir aksiyon kaydı: başlık, açıklama, etiket, kullanıcı tarafından doğrulanan tarih, yerel arama ve hatırlatıcı.
3. FDE pilotunda yalnızca bir hedef sisteme, kullanıcı onayından sonra metin aktarımı ve aktarım sonucu takibi.

Akış: seç/paylaş → OCR → alan önerisi → insan kontrolü → kaydet/hatırlat → gerekiyorsa onaylı metni hedef sisteme aktar.

Kapsam dışı: bütün galeriyi otomatik tarama, tüm içerik türleri, iOS eşzamanlı geliştirme, genel amaçlı agent, otomatik hata teşhisi, ödeme ve takvim dahil çoklu entegrasyon. Tek kişilik uygulama ile kurumsal pilot birlikte iki ayrı ürün olarak geliştirilmez; 2. hafta tek pilot seçilir.

## 05. Gereksinimler ve başarı ölçütleri

- Kullanıcı OCR metnini düzeltebilmeli; görselde olmayan alan uydurulmamalı. Eksik tarih boş kalmalı; belirsiz tarih kullanıcı onayı istemeli.
- Görsel ve çıkarılan ham metin varsayılan olarak cihazda kalmalı. Kurum aktarımında kullanıcı gönderilecek metni ve hedefi görmeli; görüntü eki varsayılan kapalı olmalı.
- OCR, arama ve yerel kayıt, ilk kurulum/model hazırlığı sonrasında çevrimdışı denenmeli. Model indirme, izin ve cihaz farkları test edilmeli.
- Hatırlatma izni verilmezse uygulama açık bir durum göstermeli; kesin zamanda teslim garantisi verilmemeli.

Pilot hedefleri (ölçülmüş sonuç değil): en az 50 izinli/anonim örnekte temel alan doğruluğu %90; 10 kullanıcı görevinin en az 8'inin yardımsız tamamlanması; kayıt düzeltme dahil medyan hazırlama süresinin mevcut yönteme göre en az %30 azalması. Tarih hatalarının ayrıca sayılması gerekir; genel doğruluk bunları gizlememeli.

## 06. Teknik yaklaşım ve ekip katkısı

Önerilen mimari: Android istemci → cihazda OCR → basit alan çıkarımı → yerel veri deposu/arama → doğrulama ekranı. Kurumsal pilot için ince bir entegrasyon servisi ve yalnızca onaylı metni alan tek adapter. Teknoloji yığını ekipçe seçilecek; mobil geliştirme deneyimi ilk hafta kontrol edilecek.

AI yaklaşımı: önce OCR ve kurallarla ölçülebilir temel sürüm. Her telefonda güçlü yerel LLM çalıştığı varsayılmaz. Ücretli uzak model zorunlu olmaz; gerekirse yalnızca açık kullanıcı onayıyla, bütçe sınırı ve ayrı değerlendirme sonrası denenir. Görsel içindeki talimatlar veri olarak ele alınır.

| Alan | Önerilen katkı |
|---|---|
| Süleyman / AI ve sistem tasarımı | Veri modeli, alan çıkarımı ve değerlendirme kümesi |
| Web/istemci | Mobil paylaşım, kontrol ve arama ekranları; mobil rolünü ekip doğrular |
| Agent/backend | Onaylı taslak akışı, tek adapter, tekrar gönderimde çoğalmayı önleme |
| Siber güvenlik | Veri akışı, görsel gizliliği, token ve yetki incelemesi |
| Ağ/altyapı | Yerel/uzak sınırlar, kesinti testleri, kurumsal kurulum ve izleme |

## 07. SDLC ve üç aylık plan

- 1–2. hafta: bir ajans/ekiple süreç gözlemi; örnekler, başlangıç süreleri, hedef alanlar ve erişim sınırları. Pilot bulunamazsa FDE iddiası ertelenir.
- 3–4. hafta: Android üzerinde OCR, elle düzeltme ve yerel kayıt; müşteriye kısa demo.
- 5–6. hafta: alan çıkarımı, arama, hatırlatıcı ve veri silme; değerlendirme sonuçları.
- 7–8. hafta: seçilmiş tek adapter; müşterinin deneme ortamında alan eşleme ve onay akışı.
- 9–10. hafta: iki haftalık sınırlı gerçek kullanım; haftalık gözlem, hatalar ve geri dönüş prosedürü.
- 11–12. hafta: güvenlik/performans düzeltmeleri, kullanıcı eğitimi, kurulum ve bakım devri, önce/sonra raporu.

Kabul ölçütleri, tehdit modeli ve müşteri alan eşlemesi SDLC boyunca güncellenir. Müşteriye özgü alanlar yapılandırmayla tutulur; her müşteri için ayrı kod kopyası üretilmez.

## 08. SSDLC ve güvenlik riskleri

| Risk | Önlem / test |
|---|---|
| Görselde kişisel bilgi, parola veya müşteri kaydı | Kullanıcının seçtiği görsel; kırpma ve aktarım öncesi inceleme; ham görseli loglamama; test verisini anonimleştirme |
| Yanlış kayda/hedefe veri gönderme | Açık onay, sabit izinli hedef, en az yetki ve başka çalışma alanına erişim testleri |
| Aynı aksiyonun tekrar oluşması veya sahte içerik | İşlem kimliği, güvenli yeniden deneme; OCR içeriğini komut olarak yürütmeme |

Siber güvenlik sorumlusu tehdit modelini ve testleri koordine eder. Kullanıcı metni/tarihi doğrulamadan dış sisteme işlem yapılmaz. Yerel işletim sistemi yedeği, cihaz kaybı, silme ve kilit ekranı bildirim içeriği tasarımda ele alınır. OCR'ın cihazda yapılması, SDK telemetrisi dahil tüm ağ trafiğinin yokluğu anlamına gelmez.

## 09. Test, yayın ve işletim

Türkçe karakterler, küçük yazı, düşük kontrast, karanlık tema, eksik/yılı belirtilmemiş tarih ve yinelenen görsellerle test kümesi hazırlanır. En az iki farklı mevcut Android cihazında izin reddi, model hazırlığı, çevrimdışı çalışma ve uygulama yeniden başlatma denenir. İnternet tekrar geldiğinde aktarımın çift kayıt oluşturmadığı doğrulanır.

Pilot kurulum kaydı, hedef adapter yapılandırması, anonim hata metrikleri, önceki sürüme dönüş ve kullanıcı eğitim notu teslim edilir. FDE kanıtı çalışan API kadar, müşterinin gerçek akışında ölçülen sonuç ve devredilebilir işletim belgesidir. Mağaza yayını pilotun ön koşulu değildir; dağıtım yöntemi güncel platform koşullarıyla seçilir.

## 10. Pazar, maliyet ve uygulanabilirlik

Bireysel sürümde ödeme isteği belirsiz; kurumsal sürümde olası alıcı destek/operasyon yöneticisidir. İlk erişim yakın çevredeki küçük yazılım ekipleriyle görüşmeler; anlaşma veya erişim henüz yok. TAM/SAM, gelir ve müşteri sayısı iddiası üretilmedi.

Bireysel yerel sürümde merkezi sunucu ve ücretli LLM zorunlu değil. Kurumsal entegrasyon için aylık 0–30 USD altyapı ve 0–10 USD opsiyonel model denemesi bir bütçe hedefidir; satıcı teklifi veya garanti değildir. Aşımda deneme durdurulur. Mevcut bilgisayar/telefonlar kullanıldığı varsayılmıştır; yeni cihaz, emek, vergi ve mağaza ücretleri bu tahmine dahil değildir. Ortak karşılaştırma raporunda ayrıntı vardır.

Gelir hipotezi: sınırlı ücretli pilot/kurulum ve isteğe bağlı bakım; miktar müşteri zaman kazancı ölçüldükten sonra test edilir. Her müşteriye sınırsız özel entegrasyon satmak bu ekibin kapasitesine uygun değildir.

## 11. İlk doğrulama deneyi

Bir haftada üç destek/operasyon çalışanıyla son işlerini gözlemleyin; izinli ve anonim en az 20 örnekte elle oluşturulan aksiyonlarla taslağı karşılaştırın. Bir potansiyel müşteriden süreç sahibi, hedef sistem ve iki haftalık deneme zamanı netleşsin.

Devam koşulu: bir kurum pilotu kabul eder; en az iki çalışan tekrar kullanmak ister; doğrulama dahil hazırlama süresi %30 azalır ve hedef sistem erişimi mümkündür. Başarısızlık koşulu: erişim yok, görüntülerden gerekli alanlar çıkarılamıyor veya mevcut araç aynı ihtiyacı yeterince karşılıyor. Sorumlular ilk ekip toplantısında atanacak.

## 12. Kaynaklar, açık sorular ve karar isteği

Kaynak erişim tarihi: 27 Ekim 2026. Ürün sayfaları özellik/fiyat beyanlarıdır; bağımsız kullanım testi yapılmadı.

- [Pixel Screenshots: arama, aksiyonlar ve hatırlatma](https://support.google.com/pixelphone/answer/15312581?hl=en): cihaz/dil/bölge kısıtları sayfadan kontrol edilmeli.
- [mymind fiyatları](https://mymind.com/pricing): görsel metin tanıma ve etiketleme; 7,99 USD/ay başlangıç AI planı.
- [ML Kit Android OCR](https://developers.google.com/ml-kit/vision/text-recognition/v2/android) ve [diller](https://developers.google.com/ml-kit/vision/text-recognition/v2/languages): Türkçe OCR teknik adayı.
- [ML Kit veri işleme ve telemetri açıklaması](https://developers.google.com/ml-kit/terms).
- [Android bildirim izni](https://developer.android.com/develop/ui/compose/notifications/notification-permission).

Açık sorular: pilot ajans kim, gerçek akış ne, hangi tek adapter, mobil geliştirici kapasitesi var mı, kullanıcı onayı hangi alanlarda gerekli? İstenen karar: fikri seçmek değil; pilot görüşmesine ve teknik deneye alınması.
