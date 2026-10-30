# Proje Fikri Önerisi

> Şablon v1.1 · Durum: öneri (proje kararı değildir)

- Proje adı: Akıllı Toprak Nemi ve Sulama Karar Sistemi (Tek Bitki PoC)
- Yazar / GitHub: Mert Sarıtop / @MertSrtp
- Tarih: 2026-10-30
- Fikir sürümü: v01
- Şablon sürümü: 1.1
- İlgili issue: [#2](https://github.com/fivefold-labs/project-hub/issues/2)

## 01. Problem ve kullanıcı

Bitki yetiştiriciliğinde (seralar, yerel fide üreticileri ve kapalı alan tarımı) aşırı veya yetersiz sulama mahsul verimini doğrudan düşürmekte, kök çürümesine ya da bitki stresine yol açmaktadır. Ayrıca geleneksel tarımsal sulama yöntemleri yüksek miktarda su ve elektrik/enerji israfına neden olmaktadır.

Bugün üreticiler sulamayı çoğunlukla sabit zamanlayıcılarla (örneğin günde 2 kez sabit süre) ya da toprağın üst yüzeyini gözle/elle kontrol ederek yapmaktadır. Bu yöntemler; toprak altındaki gerçek kök nemini, ortam sıcaklığını, anlık buharlaşma oranını ve hava tahminlerini dikkate almadığı için dinamik ihtiyaçlara cevap verememektedir.

Problem: Üreticinin elinde toprak altı nemini ve bitkinin dinamik su ihtiyacını anlık izleyen, mikroklima ve hava tahminleriyle birlikte değerlendiren ve sulamayı akıllı şekilde yöneten düşük maliyetli, güvenilir bir karar ve otomasyon mekanizması bulunmamaktadır.

Hedef kullanıcılar:
- **Birincil (MVP / PoC):** Tek bir bitki/fide (örneğin sera domatesi) yetiştiren yerel sera üreticileri, fide yetiştiricileri veya kapalı alan bitki yetiştiricileri.
- **İkincil (Gelecek Vizyonu):** Çoklu parsel ve açık tarla işletmecileri, modern tarım girişimleri.

## 02. Kanıt ve varsayımlar

**Doğrulanan bulgular (kaynaklı):**
- Birleşmiş Milletler Gıda ve Tarım Örgütü (FAO) verilerine göre küresel tatlı su tüketiminin yaklaşık %70'i tarımda kullanılmakta ve geleneksel sulama yöntemlerinde suyun %30 ila %50'si aşırı sulama ve buharlaşma nedeniyle israf edilmektedir. ([FAO Su Yönetimi Raporu](https://www.fao.org/land-water/water/water-management/irrigation/en/))
- Toprak nemi sensörleri ve veri odaklı sulama optimizasyonunun su tüketiminde %20–40 arasında tasarruf sağladığı ve bitki gelişimini iyileştirdiği akademik ve saha araştırmalarında gösterilmiştir. ([Smart Irrigation Systems Review - ScienceDirect](https://doi.org/10.1016/j.agwat.2020.106649))

**Henüz doğrulanmadı (varsayımlar):**
- Yerel üreticilerin sulama vanalarını otonom bir yapay zekâ modeline veya algoritmaya teslim etme güveni. Araştırma: Yerel üreticilerle yüz yüze kısa görüşme.
- Düşük maliyetli kapasitif toprak nem sensörünün 3 aylık süreçte korozyon veya tuzlanma yaşamadan stabil veri üretip üretemeyeceği. Araştırma: 11. bölümdeki ilk doğrulama deneyi.
- Tek bitki (ör. saksı domates fidesi) üzerinde toplanacak nem düşüş verisiyle eğitilecek bir yapay zekâ tahmin/anomali modelinin sulama zamanını insan tahmininden daha isabetli kestirebileceği.

## 03. Değer önerisi ve alternatifler

**Değer önerisi:** Toprak altı nem sensörü ve mikroklima verilerini yapay zekâ destekli analizle işleyerek, tek bir bitkinin su ihtiyacını doğru zamanda tespit eden ve sulama aksiyonunu optimize eden düşük maliyetli, güvenli bir akıllı karar ve otomasyon sistemi.

**Mevcut alternatifler:**

| Alternatif | Ne yapıyor | Bizim olası farkımız |
|---|---|---|
| [Doktar](https://www.doktar.com/) / [CropX](https://cropx.com/) | Büyük ölçekli tarım için kurumsal IoT sensörleri ve uydu analitiği sunar | Yüksek donanım ve lisans maliyeti gerektirir; küçük/yerel üretici veya tekil sera için erişilebilir değildir. |
| Mekanik Zamanlayıcılar (Hunter, Gardena vb.) | Belirlenen saatte vanayı sabit süre açıp kapatır | Toprak nemini, bitkinin gerçek ihtiyacını ve hava durumunu bilmez; yağmurlu veya aşırı nemli günde de gereksiz sular. |
| Akıllı Bahçe Vanaları (Tuya, Sonoff) | Wi-Fi/Zigbee ile uzaktan telefonla vana kontrolü sağlar | Sadece uzaktan kumandadır; yapay zekâ analitiği, nem öngörüsü ve bitki sağlığı kararı üretmez. |

## 04. MVP kapsamı ve ana akış

Üç aylık süreçte amaç, sistemi tek bir bitki üzerinde uçtan uca doğrulamaktır (PoC). Tek bitkide başarı sağlandıktan sonra çoklu bitki ve seri üretime geçiş hedeflenir.

**Üç temel özellik:**
1. **Telemetri ve Nem Takibi:** Toprak altı kapasitif nem sensörü ve ortam sensöründen (sıcaklık/nem) alınan verilerin mikrodenetleyici (ESP32) aracılığıyla güvenli şekilde backend'e iletilmesi ve web arayüzünde canlı grafiklerle sunulması.
2. **Yapay Zekâ Destekli Sulama Karar Motoru:** Nem düşüş hızını, ortam koşullarını ve hava tahminini analiz ederek sulama ihtiyacını önceden tahmin eden ve sulama süresini/zamanını dinamik belirleyen AI karar algoritması.
3. **Güvenli Vana Kontrolü ve Fail-Safe Koruması:** Eşik değer veya AI kararıyla 12V solenoid vanayı/röleyi tetikleyen, ağ kopması ya da sensör bozulmasında vanayı kapatarak su baskınını önleyen güvenlik mekanizması.

**Ana akış:**
1. Sensör toprak nemi ve ortam verilerini periyodik olarak okur ve backend'e iletir.
2. Yapay zekâ modeli nem trendini analiz eder, hava tahminiyle birleştirerek sulama gerekip gerekmediğini hesaplar.
3. Sulama gerekiyorsa sistem vanayı açar; toprak hedeflenen doygunluğa ulaştığında veya maksimum emniyet süresi (timeout) dolduğunda vanayı kapatır.
4. Kullanıcı panel üzerinden anlık toprak durumunu, AI tahminlerini ve sulama geçmişini izler.

**İlk sürümün dışında kalacaklar:**
- Açık tarla tipi uzun menzilli LoRaWAN ağları.
- Yüksek voltajlı endüstriyel dalgıç motor kontrolleri.
- Çoklu tarla/parsel yönetimi ve ticari abonelik altyapısı.
- Uydu görüntüsü (Sentinel-2) entegrasyonu (ileri faz).

## 05. Gereksinimler ve başarı ölçütleri

**Kullanıcı hikâyeleri:**
- Üretici olarak, bitkimin toprak altı nemini ve sulama geçmişini cep telefonumdan/webden anlık görmek istiyorum.
- Üretici olarak, yapay zekânın bitkimin ne zaman sulanması gerektiğini önceden tahmin etmesini ve vanayı doğru miktarda açmasını istiyorum.
- Üretici olarak, internet koptuğunda veya sensör bozulduğunda vananın açık kalıp bitkiyi çürütmesini engelleyen bir donanımsal emniyet istiyorum.

**İşlevsel olmayan beklentiler:**
- Düşük gecikme: Sulama kararı ile vananın tetiklenmesi arasındaki gecikme < 10 saniye olmalıdır.
- Güvenilirlik: Donanım tarafında "watchdog timer" bulunmalı, bağlantı kopsa dahi vana açık kalmamalıdır.
- Düşük veri tüketimi ve şifreli veri aktarımı (TLS/HTTPS veya MQTT over TLS).

**Kabul ölçütleri (hedefler henüz varsayımdır):**
- 1 test bitkisi (ör. saksı domates fidesi) üzerinde 14 gün boyunca kesintisiz sensör veri akışı sağlanması.
- Yapay zekâ modelinin nem düşüş trendini analiz ederek sulama ihtiyacını en az %80 doğrulukla önceden tahmin edebilmesi.
- Fail-safe senaryolarında (ağ kesintisi simülasyonu) vananın belirlenen emniyet süresi içinde (maks. 2 dakika) kapanması (%100 başarı).

## 06. Teknik yaklaşım ve ekip katkısı

**Olası bileşenler (karar değil, araştırma konusudur):**
- **Mikrodenetleyici & Donanım:** ESP32, Kapasitif Toprak Nemi Sensörü v1.2, DHT22 (sıcaklık/nem), 5V/12V Röle ve Solenoid Vana.
- **Yapay Zekâ ve Karar Modeli:** Nem azalma eğrisini modelleyen zaman serisi analitiği (regresyon / LSTM veya hafif ML modeli), anomali tespiti (sensör arızası/aşırı nem tespiti) ve meteoroloji API verisiyle sulamayı optimize eden kural/tahmin motoru.
- **Haberleşme & Altyapı:** MQTT (Mosquitto) veya REST API, zaman serisi veritabanı (TimescaleDB / InfluxDB / PostgreSQL).
- **Arayüz:** Hafif bir web paneli (telemetri grafikleri, vana durum kontrolü, AI tahmin kartları).

**Ekip katkısı:**
- **Yapay Zekâ ve Akıllı Sistemler (Ana Odak - Mert):** Toprak nemi düşüş tahmini, dinamik sulama süresi optimizasyon algoritması, sensör anomali tespiti ve AI karar motorunun geliştirilmesi. İhtiyaç halinde web/backend entegrasyonuna destek.
- **Web, Ağ, Siber Güvenlik ve Altyapı:** Bu projenin seçilmesi durumunda teknik roller ekip üyelerinin ilgi ve yetkinliklerine göre ekipçe belirlenecektir (Ağ yönetimi, IoT haberleşmesi, SSDLC güvenlik doğrulamaları ve arayüz geliştirme).

## 07. SDLC ve üç aylık plan

| Hafta | Aşama | Çıktı |
|---|---|---|
| 1–2 | Analiz & Keşif | Sensör ve donanım seçimi, test ortamı hazırlığı, yerel üretici görüşmesi |
| 3–4 | Tasarım & PoC | ESP32 sensör okuma, MQTT/HTTP veri aktarımı, temel backend ve veri kaydı |
| 5–6 | Yapay Zekâ & Karar Motoru | Nem düşüş verileriyle AI tahmin modelinin geliştirilmesi ve karar motoru entegrasyonu |
| 7–8 | Otomasyon & Güvenlik | Solenoid vana/röle entegrasyonu, fail-safe ve güvenlik kontrolleri (SSDLC) |
| 9–10 | Canlı Test (Tek Bitki) | 14 günlük kesintisiz canlı bitki sulama denemesi, model doğrulama |
| 11–12 | Değerlendirme & Yayın | Karşılaştırmalı su tasarrufu analizi, demo sunumu, teknik vaka raporu |

## 08. SSDLC ve güvenlik riskleri

**En önemli üç risk ve önlemleri:**
1. **Yetkisiz Vana Tetikleme (Replay veya Spoofing Saldırısı):** Saldırganın vanayı sürekli açık tutarak su baskını yaratması veya vanayı kilitleyerek mahsulü kurutması.
   * *Önlem:* Cihaz ile sunucu arasında TLS şifreleme, tek kullanımlık token (nonce) ve kimlik doğrulama.
2. **Sensör Verisi Manipülasyonu veya Donanım Arızası:** Sensörün toprağı sürekli kuru göstermesi durumunda sistemin aralıksız sulama yapması.
   * *Önlem:* Yazılımsal ve donanımsal "maksimum çalışma süresi" (hard limit / watchdog) koyarak tek seferde belirlenen süreden fazla su akışını engellemek; yapay zekâ anomali tespiti ile ani/tutarsız sensör verilerini filtrelemek.
3. **Ağ Kesintisi Riskleri:** Cihazın internet bağlantısı koptuğunda vana durumunun belirsiz kalması.
   * *Önlem:* ESP32 tarafında yerel fail-safe kuralı: Bağlantı koptuğu anda aktif sulama varsa vana otomatik kapatılır.

## 09. Test, yayın ve işletim

- **Donanım & Birim Testleri:** Sensörün kuru toprak, nemli toprak ve su içindeki analog değer aralıklarının kalibrasyon testleri.
- **Yapay Zekâ Değerlendirmesi:** Modelin tahmin ettiği sulama ihtiyacı ile gerçek nem eğrisi arasındaki farkın (RMSE / MAE) hesaplanması.
- **Güvenlik Testleri:** Ağ kesintisi simülasyonu, hatalı veri enjeksiyonu ve yetkisiz API çağrısı denemeleri.
- **Canlı Pilot:** Tek bir saksı bitkisi üzerinde 2 hafta boyunca sistemin gözetimli çalıştırılması.

## 10. Pazar, maliyet ve uygulanabilirlik

- **Prototip Donanım Maliyeti:**
  - ESP32 Geliştirme Kartı: ~$5
  - Kapasitif Nem Sensörü (v1.2 korozyona dayanıklı): ~$2–3
  - 12V Selenoid Vana + Röle Kartı: ~$5–8
  - Güç adaptörü ve kablolama: ~$3–5
  - *Toplam Donanım Bütçesi:* ~$15–20 (öğrenci bütçesiyle kolaylıkla temin edilebilir).
- **Yazılım & Sunucu:** Düşük veri hacmi nedeniyle ücretsiz veya çok düşük maliyetli bulut hizmetleri (Cloud Free Tier / VPS).
- **Pazar Potansiyeli:** Tek bitkide doğrulanacak PoC, ileride çoklu vana kontrol kartları ile seralara ve hobi bahçelerine ölçeklenebilir ürün prototipine dönüştürülebilir.

## 11. İlk doğrulama deneyi

- **Deney (1. Hafta):** 1 adet saksıda kapasitif nem sensörü ile 3 gün boyunca toprak sulandıktan sonra kuruma sürecindeki analog değer değişimini ölçmek. Eş zamanlı olarak yerel 1 üretici/seracı ile görüşüp otomasyona güven şartlarını sormak.
- **Sorumlu:** Mert Sarıtop (@MertSrtp)
- **Başarı Eşiği:** Sensörün doygun ve kuru toprak arasında en az %40'lık belirgin bir voltaj/değer farkı göstermesi ve üreticinin "fail-safe varsa denerim" geri bildirimi.
- **Fikri Değiştirme Kriteri:** Ucuz sensörün tutarsız/gürültülü değerler vermesi veya üreticilerin böyle bir otomasyona kesinlikle güvenmeyeceğini belirtmesi durumunda donanımsız uydu/hava durumu odaklı karar destek modeline pivot edilir.

## 12. Kaynaklar, açık sorular ve karar isteği

**Kaynaklar:**
- FAO Tarımsal Su Yönetimi ve Sulama Kılavuzları (Erişim: 2026-10-30).
- MDPI Sensors, "IoT-Based Smart Irrigation Systems: An Overview" (Erişim: 2026-10-30).
- ESP32 ve MQTT Güvenlik Dokümantasyonu (Espressif Docs, Erişim: 2026-10-30).

**Açık Sorular:**
- Kapasitif sensörün toprak tuzluluğuna bağlı sapmaları yapay zekâ tarafında bir katsayıyla düzeltilebilir mi?
- Ekip üyeleri donanım PoC'si için fiziksel test ortamı oluşturmayı destekliyor mu?

**Ekipten Geri Bildirim İsteği:**
- Tek bitki PoC yaklaşımı 3 aylık MVP süresi için uygulanabilir bulunuyor mu?
- Yapay zekâ tahmin ve anomali tespiti modeline ek olarak hangi analitik özellikler önerilir?
