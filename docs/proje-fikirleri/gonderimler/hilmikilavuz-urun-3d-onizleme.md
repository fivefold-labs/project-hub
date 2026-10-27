# Proje Fikri Önerisi

> Şablon v1.1 · Durum: öneri (proje kararı değildir)

- Proje adı: Ürün Görselinden 3D Önizleme (çalışma adı)
- Yazar / GitHub: Hilmi Kılavuz / @HilmiKilavuz
- Tarih: 2026-10-27
- Fikir sürümü: v01
- Şablon sürümü: 1.1
- İlgili issue: [#2](https://github.com/fivefold-labs/project-hub/issues/2)

## 01. Problem ve kullanıcı

Online alışveriş yapan kullanıcılar, ürünü yalnızca birkaç düz fotoğraftan değerlendiriyor. Bu yüzden şu soruların cevabını bulmakta zorlanıyorlar:

- Ürün gerçekte ne kadar büyük? Masama, odama veya üzerime nasıl oturur?
- Fotoğrafta görünmeyen açılardan nasıl görünüyor?
- İkinci el ürünlerde (örneğin araç) hasar, çizik ya da boya tam olarak nerede?

Bugün kullanıcılar bunu ölçü tablosunu okuyarak, yorumlara bakarak ya da satıcıya soru sorarak çözmeye çalışıyor. Ürün beklentiyi karşılamadığında iade ediyor. Satıcı tarafında ise 3D model hazırlatmak pahalı ve zaman alıcı olduğu için çoğu küçük ve orta ölçekli e-ticaret işletmesi 3D/AR içerik sunmuyor.

Problem: satıcının elindeki mevcut ürün görselleri, alıcının boyut, şekil ve durumla ilgili sorularına yeterli cevap vermiyor.

Hedef kullanıcılar:

- **Alıcı:** Online alışveriş yapan son kullanıcı.
- **Müşteri (ödeme yapan):** Küçük ve orta ölçekli e-ticaret satıcıları, ikinci el ilan platformları ve araç galerileri.

## 02. Kanıt ve varsayımlar

**Doğrulanan bulgular (kaynaklı):**

- Shopify'ın yayımladığı Gunner Kennels vaka çalışmasında 3D/AR eklendikten sonra sipariş dönüşüm oranında %40 artış ve iadelerde %5 düşüş raporlanmış. ([Shopify vaka çalışması](https://www.shopify.com/es/case-studies/gunner-kennels), erişim 2026-10-27)
- Görselden 3D model üretme alanında yatırım almış şirketler var. Örneğin RECON Labs, tek 2D görselden 3D görünüm üreten aracı için 4,4 milyon dolar Seri A yatırımı almış. ([TechCrunch](https://techcrunch.com/?p=2310240), erişim 2026-10-27)
- Araç hasar tespitinde fotoğraf ve 3D yeniden oluşturmayı birleştiren şirketler (Click-Ins, Fyusion, Tchek, Ravin) sigorta, kiralama ve bayi pazarına satış yapıyor. Bu, alanda ödeme yapan müşteri olduğunu gösteriyor. (Kaynaklar 03. bölümde.)

**Henüz doğrulanmadı (varsayımlar):**

- Türkiye'deki küçük satıcıların 3D önizleme için ödeme yapmaya istekli olduğu. Araştırma: tanıdığım esnaf ve e-ticaret satıcılarıyla görüşme.
- Alıcıların 3D önizleme olduğunda satın alma kararını daha kolay verdiği. Araştırma: öğrencilerle kısa görüşme ve basit bir prototip denemesi.
- Satıcının elindeki 2–5 sıradan ürün fotoğrafından kullanılabilir kalitede bir 3D model üretilebildiği. Araştırma: 06. bölümdeki teknik deney.
- Sıklıkla tekrarlanan "3D/AR dönüşümü %94 artırır" gibi rakamlar satıcı bloglarından geliyor ve birincil kaynakları bulunamadı. Bu rakamlar kanıt olarak kullanılmayacak.

Henüz kullanıcı görüşmesi yapılmadı.

## 03. Değer önerisi ve alternatifler

**Değer önerisi:** Satıcının zaten elinde olan ürün fotoğraflarından, alıcının ürünün boyutunu, şeklini ve durumunu tarayıcıda döndürerek ve gerçek ölçekte görerek anlayabileceği bir 3D önizleme üretmek.

**Mevcut alternatifler:**

| Alternatif | Ne yapıyor | Bizim olası farkımız |
|---|---|---|
| [Shopify 3D/AR medya](https://www.pictureit.co/blog/top-augmented-reality-for-ecommerce-apps-2026) | Ürün sayfasında 3D model ve AR gösterimi | Yalnızca Shopify satıcılarına açık ve modeli satıcının ayrıca hazırlaması gerekiyor |
| [CGTrader ARsenal](https://www.furnituretoday.com/technology/cgtrader-offers-free-version-to-speed-up-retail-e-commerce-adoption), [Hexa](https://app.dealroom.co/companies/hexa), [Sayduck](https://www.sayduck.com/post/best-3d-product-viewers-for-ecommerce-in-2026) | 3D model üretimi/barındırma ve AR görüntüleyici | Kurumsal odaklı ve yabancı pazar için tasarlanmış; Türkiye'deki küçük satıcı ve pazar yeri entegrasyonu belirsiz |
| [artlabs](https://artlabs.ai/), [123D](https://startupim.com/company/123d), [RECON Labs](https://techcrunch.com/?p=2310240) | Ürün görselinden yapay zekâ ile 3D üretimi | Doğrudan rakip. Farkımız boyut doğrulama ve ikinci el durum/hasar işaretleme olabilir. Henüz doğrulanmadı |
| [Click-Ins](https://startupim.com/company/Click-Ins/raw), [Fyusion](https://www.geoweeknews.com/articles/fyusion-inspect-pairs-3d-and-ai-to-inspect-vehicle-damage-with-mobile-devices/), [Tchek](https://www.uktech.news/news/tchek-a-french-startup-that-detects-car-damage-with-ai-bags-26m-20210127), [Ravin](https://techcrunch.com/?p=1829746) | Araç hasarını fotoğraf ve 3D ile tespit ve raporlama | Sigorta ve kiralama şirketlerine yönelik. Bireysel ilan sahibi ve alıcıya yönelik basit bir hasar haritası boşluk olabilir |

Bu alanda güçlü rakipler var. Bu yüzden farkımızı dar bir nişte göstermemiz gerekiyor (bkz. 12. bölüm).

## 04. MVP kapsamı ve ana akış

**Üç temel özellik:**

1. **Görselden 3D üretim:** Satıcı 2–5 ürün fotoğrafı ve ürünün gerçek ölçülerini (en, boy, yükseklik) yükler. Sistem 3D modeli üretir ve gerçek ölçüye göre ölçekler.
2. **Web/mobil 3D görüntüleyici:** Alıcı, ürünü tarayıcıda döndürür, yakınlaştırır ve destekleyen cihazlarda AR ile gerçek ortamda gerçek boyutunda görür.
3. **Not/hasar işaretleme:** Satıcı, model üzerinde belirli noktalara not ekler (örneğin "sol kapıda çizik"). Alıcı bu noktalara tıklayıp ilgili fotoğrafı görür.

**Ana akış:**

1. Satıcı ürün fotoğraflarını ve ölçülerini yükler.
2. 3D model üretilir. Satıcı modeli önizler, beğenmezse yeniden dener.
3. Satıcı isterse modelin üzerine not veya hasar işareti ekler.
4. Sistem, ürün sayfasına eklenebilecek bir bağlantı veya gömme kodu verir.
5. Alıcı bağlantıdan 3D/AR önizlemeyi açar.

**İlk sürümün dışında kalacaklar:**

- Yapay zekâ ile otomatik hasar tespiti (ilk sürümde hasar noktalarını satıcı elle işaretler).
- Tam araç gibi büyük ve karmaşık nesneler. İlk sürüm tek parça, küçük ve orta boy ürünlere (ayakkabı, çanta, küçük mobilya gibi) odaklanır.
- Trendyol, Hepsiburada gibi pazar yerleriyle doğrudan entegrasyon.
- Ödeme ve abonelik sistemi.
- Ürünü giyme/üzerinde deneme (virtual try-on).

## 05. Gereksinimler ve başarı ölçütleri

**Kullanıcı hikâyeleri:**

- Satıcı olarak, 3D modelleme bilmeden mevcut fotoğraflarımdan 3D önizleme oluşturmak istiyorum.
- Alıcı olarak, ürünün gerçek boyutunu kendi ortamımda görmek istiyorum.
- İkinci el alıcısı olarak, hasarın ürünün neresinde olduğunu tek bakışta görmek istiyorum.

**İşlevsel olmayan beklentiler:**

- Görüntüleyici orta segment bir telefonda akıcı çalışmalı ve sayfayı belirgin şekilde yavaşlatmamalı.
- Model dosyası mobil veri ile makul sürede yüklenmeli.
- Yüklenen görseller yalnızca model üretimi için kullanılmalı ve açıkça belirtilen süre boyunca saklanmalı.

**Kabul ölçütleri (hedefler henüz varsayımdır):**

- Test için seçilen 10 ürünün en az 7'sinde kullanılabilir 3D model üretilmesi.
- Modelden ölçülen boyutların, satıcının girdiği ölçülerle en fazla %5 farklı olması.
- Pilot alıcıların çoğunluğunun önizlemeyi "boyutu ve şekli anlamama yardımcı oldu" diye değerlendirmesi.

## 06. Teknik yaklaşım ve ekip katkısı

**Olası bileşenler (karar değil, araştırma konusudur):**

- **3D üretim:** Hazır bir görselden 3D API'si ya da açık kaynak bir model. Çok fotoğraf varsa fotogrametri ve Gaussian splatting gibi yöntemler de değerlendirilebilir. Kaynaklara göre tek görselli yapay zekâ hızlı, fotogrametri ise daha doğru ama daha çok ve daha iyi fotoğraf istiyor. ([3D AI Studio rehberi](https://www.3daistudio.com/blog/best-ai-tools-for-product-visualization-ecommerce-3d-2026), satıcı kaynağıdır)
- **Görüntüleyici:** Web tabanlı bir 3D/AR görüntüleyici, GLB/USDZ dosya formatları.
- **Arka uç:** Görsel yükleme, iş kuyruğu (3D üretim uzun sürebilir), model depolama ve paylaşım bağlantısı.

**En büyük teknik belirsizlik:** Sıradan satıcı fotoğraflarından üretilen modelin kalitesi ve ölçü doğruluğu. İlk haftanın teknik deneyi bunu ölçmeli.

**Ekip katkısı:**

- **Web/mobil (Hilmi):** Görüntüleyici, satıcı paneli, mobil uyum.
- **AI (Süleyman, Oğulcan):** 3D üretim modelinin seçimi ve değerlendirilmesi, ileride hasar tespiti.
- **Agent:** Satıcının fotoğraf yükleme sürecini yönlendiren yardımcı (örneğin "arka açıdan bir fotoğraf daha çek"). Gereksizse eklenmez.
- **Ağ/altyapı (Ahmet):** Büyük dosya depolama, CDN, iş kuyruğu ve düşük maliyetli dağıtım.
- **Siber güvenlik (Hilmi):** Dosya yükleme güvenliği, erişim kontrolü, SSDLC koordinasyonu.

## 07. SDLC ve üç aylık plan

| Hafta | Çıktı |
|---|---|
| 1–2 | Kullanıcı görüşmeleri (satıcı ve alıcı), teknik deney: 10 üründen 3D üretim kalitesi ölçümü |
| 3–4 | Mimari ve tehdit modeli; görsel yükle → model üret → görüntüle akışının ilk uçtan uca sürümü |
| 5–8 | Ölçekleme, not/hasar işaretleme, satıcı paneli, testler, güvenlik kontrolleri |
| 9–10 | Tanıdık esnaf ve satıcılarla pilot; geri bildirim ve hata düzeltmeleri |
| 11–12 | Stabil demo, kurulum rehberi, ölçüm sonuçları ve vaka yazısı |

Sorumluluklar öneri niteliğindedir ve proje seçilirse ekipçe belirlenir.

## 08. SSDLC ve güvenlik riskleri

**Hassas veriler ve güven sınırları:** Satıcının yüklediği görseller, satıcı hesabı, paylaşım bağlantıları. Görsel üçüncü taraf bir 3D API'sine gönderilirse veri sistemimizin dışına çıkmış olur. Bu da bir güven sınırıdır.

**En önemli üç risk:**

1. **Zararlı dosya yükleme:** Görsel gibi görünen zararlı dosyalar ya da çok büyük dosyalarla servisi yorma. Önlem: dosya türünü içerikten doğrulama, boyut sınırı, görseli yeniden kodlama, meta verileri (EXIF, konum bilgisi) silme, hız sınırlama.
2. **Yetkisiz erişim:** Başka bir satıcının modeline veya görseline erişme ya da onu değiştirme. Önlem: nesne bazında yetki kontrolü, tahmin edilemez paylaşım bağlantıları, IDOR testleri.
3. **Yanıltıcı içerik:** Satıcının hasarı gizleyen veya ürünü olduğundan farklı gösteren bir model sunması. Önlem: modelin kaynak fotoğraflarla birlikte gösterilmesi, kullanıcıya "yapay zekâ ile üretilmiştir" uyarısı.

**Güvenlik testleri:** Dosya yükleme testleri, yetki testleri, bağımlılık ve secret taraması.

**Koordinatörün inceleyeceği açık sorular:** Görseller üçüncü taraf bir API'ye gönderilecekse KVKK açısından ne gerekir? Görseller ve modeller ne kadar süre saklanmalı?

## 09. Test, yayın ve işletim

- **İşlevsel testler:** Yükleme, üretim kuyruğu, görüntüleyici ve paylaşım bağlantısı akışları.
- **AI değerlendirmesi:** Sabit bir 10–20 ürünlük test seti. Her modelde ölçü hatası ölçülür ve görsel kalite ekip tarafından 1–5 arası puanlanır.
- **Pilot kullanıcılar:** Tanıdığım esnaf ve satıcılar (satıcı tarafı), öğrenciler (alıcı tarafı).
- **Yayın ve bakım:** Tek bir bulut ortamına basit dağıtım, sorun olursa önceki sürüme dönüş, hata ve maliyet takibi.

## 10. Pazar, maliyet ve uygulanabilirlik

- **Kullanıcı:** Online alışveriş yapan alıcılar.
- **Ödeme yapan taraf:** E-ticaret satıcıları, ikinci el ilan platformları, araç galerileri. Olası gelir modeli ürün başına ücret ya da aylık abonelik. Henüz doğrulanmadı.
- **Nasıl ulaşırız:** İlk aşamada tanıdığım esnaf ve bir şirketteki bağlantılarım, ardından küçük e-ticaret satıcıları.
- **Maliyet varsayımları:** Hazır bir 3D API kullanılırsa model başına ücret ödenir. Açık kaynak model kullanılırsa GPU maliyeti oluşur. 3D dosyaları büyük olduğu için depolama ve aktarım maliyeti de hesaba katılmalı. Gerçek rakamlar henüz araştırılmadı, teknik deneyde ölçülecek.
- **Uygulanabilirlik:** Model üretimini sıfırdan geliştirmek üç ayda gerçekçi değil. MVP, hazır modeller veya API'ler üzerine ölçekleme, görüntüleme ve işaretleme katmanı kurarsa yapılabilir görünüyor.

## 11. İlk doğrulama deneyi

**Sorumlu:** @HilmiKilavuz (teknik kısım için AI tarafından bir ekip arkadaşıyla birlikte).

**Bir haftalık deney:**

1. **Teknik:** Farklı türlerden 10 ürün seç ve her biri için 2–5 sıradan telefon fotoğrafı çek. En az iki farklı görselden 3D aracıyla model üret. Kaliteyi 1–5 arası puanla ve ölçü hatasını ölç.
2. **Kullanıcı:** En az 3 satıcı/esnaf ve 5 öğrenciyle kısa görüşme yap. Sorular: Bu sorunu en son ne zaman yaşadın? Nasıl çözdün? İade ettin mi? Satıcıysan böyle bir araca ödeme yapar mıydın?

**Başarı eşiği:**

- 10 ürünün en az 6'sında kullanılabilir model üretilmesi.
- Görüşülen satıcıların en az 2'sinin pilot denemeye gönüllü olması.

**Fikri değiştirecek sonuç:** Model kalitesi yetersiz çıkarsa fikir "çok açılı fotoğraf çekim rehberi ve 360° görüntüleyici" yönüne daraltılır. Satıcı ilgisi yoksa ikinci el ilan ve hasar haritası yönü öne alınır.

## 12. Kaynaklar, açık sorular ve karar isteği

**Kaynaklar (erişim tarihi: 2026-10-27):**

- [Shopify — Gunner Kennels vaka çalışması](https://www.shopify.com/es/case-studies/gunner-kennels)
- [3D AI Studio — 2026 e-ticaret 3D araçları rehberi](https://www.3daistudio.com/blog/best-ai-tools-for-product-visualization-ecommerce-3d-2026) (satıcı kaynağı)
- [Sayduck — 2026 3D ürün görüntüleyicileri](https://www.sayduck.com/post/best-3d-product-viewers-for-ecommerce-in-2026) (satıcı kaynağı)
- [PictureIt — 2026 e-ticaret AR uygulamaları](https://www.pictureit.co/blog/top-augmented-reality-for-ecommerce-apps-2026)
- [artlabs](https://artlabs.ai/)
- [123D](https://startupim.com/company/123d)
- [TechCrunch — RECON Labs yatırımı](https://techcrunch.com/?p=2310240)
- [Furniture Today — CGTrader ARsenal](https://www.furnituretoday.com/technology/cgtrader-offers-free-version-to-speed-up-retail-e-commerce-adoption)
- [Dealroom — Hexa](https://app.dealroom.co/companies/hexa)
- [Click-Ins](https://startupim.com/company/Click-Ins/raw)
- [Geo Week News — Fyusion Inspect](https://www.geoweeknews.com/articles/fyusion-inspect-pairs-3d-and-ai-to-inspect-vehicle-damage-with-mobile-devices/)
- [UKTN — Tchek](https://www.uktech.news/news/tchek-a-french-startup-that-detects-car-damage-with-ai-bags-26m-20210127)
- [TechCrunch — Ravin.ai](https://techcrunch.com/?p=1829746)

**Açık sorular:**

- Hangi niş ile başlamalıyız: genel e-ticaret ürünleri mi, ikinci el eşya ve hasar haritası mı?
- Türkiye'deki satıcılar için mevcut alternatifler neden yeterli değil? Görüşmelerle araştırılacak.
- Görsel kalitesi düşük olduğunda kullanıcıya nasıl bir fotoğraf rehberi sunmalıyız?

**Ekipten beklenen geri bildirim:**

- Hangi kullanım alanını daha anlamlı buluyorsunuz?
- Oğulcan'ın ikinci el araç değerleme fikriyle (#2) birleştirilebilir mi? Araç fotoğraflarından hasar haritası, değerleme sistemine görsel bir katman olabilir.
- Teknik deneye kim destek olabilir?

Bu metin bir öneridir; proje seçimi [değerlendirme yöntemi](../../SELECTION.md) ve karar kaydıyla yapılır.
