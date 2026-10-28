# Proje Fikri Önerisi

> Şablon v1.1 · Durum: öneri (proje kararı değildir)

- Proje adı: Ekran Görüntüsünden Aksiyon (çalışma adı)
- Yazar / GitHub: Süleyman / @suleymanssardogan
- Tarih: 2026-10-28
- Fikir sürümü: v03
- Şablon sürümü: 1.1
- İlgili issue: [#2](https://github.com/fivefold-labs/project-hub/issues/2)

## 01. Problem ve kullanıcı

İnternette gördüğümüz bir ilanı, ürünü veya duyuruyu daha sonra değerlendirmek için ekran görüntüsü alıyoruz. Ancak görüntü galeride kaldığında şu soruların cevabını bulmak zorlaşıyor:

- Kaydettiğim ilan hangi şirketindi ve son başvuru tarihi neydi?
- Beğendiğim ürünün ekran görüntüsü nerede?
- Bu görseli neden kaydetmiştim; yapmam gereken bir şey var mıydı?

Bugün bunları galeride arayarak, ayrı bir not yazarak veya takvime elle hatırlatma ekleyerek çözebiliyoruz. Görseli saklamakla sonraki adımı takip etmek birbirinden ayrı kalıyor.

**Amacımız:** Kullanıcının seçtiği ekran görüntüsünü okuyup düzenlenebilir bir kayda dönüştüren; kaydı arayarak bulmayı ve ilgili iş için hatırlatma kurmayı sağlayan bir mobil uygulama geliştirmek.

**Hedef kullanıcılar:** İlan, ürün ve duyuruları ekran görüntüsüyle biriktiren kişiler. İlk kullanıcı denemelerini ulaşabildiğimiz öğrenciler ve arkadaş çevremizle yapabiliriz.

## 02. Kanıt ve varsayımlar

**Doğrulanan bulgular (kaynaklı):**

- [Pixel Screenshots](https://support.google.com/pixelphone/answer/15312581?hl=en), ekran görüntülerinde arama, aksiyon önerileri ve hatırlatıcı sunuyor. Resmî sayfada cihaz, dil ve bölge sınırları bulunuyor.
- [mymind](https://mymind.com/pricing), görüntü metni tanıma ve otomatik etiketleme sunuyor. Yani bu alanda mevcut ürünler var.
- [ML Kit](https://developers.google.com/ml-kit/vision/text-recognition/v2/languages), Türkçe metin tanımayı destekliyor. Kendi görsellerimizdeki doğruluk teknik deneyle ölçülecek.

**Henüz doğrulanmadı (varsayımlar):**

- Kullanıcıların galeride arama ve ayrı hatırlatıcı oluşturma işini önemli bir sorun olarak gördüğü. Araştırma: son kaydettikleri görseller üzerinden kullanıcı görüşmesi.
- Türkçe ilanlardan yeterince doğru başlık/tarih çıkarılabildiği. Araştırma: farklı görsellerle OCR deneyi.
- Kullanıcıların mevcut araçları yerine bu uygulamayı düzenli kullanacağı veya ücretli özellik isteyeceği. Araştırma: bir haftalık kullanım denemesi.

Henüz kullanıcı görüşmesi veya çalışan ürün testi yapılmadı.

## 03. Değer önerisi ve alternatifler

**Değer önerisi:** Ekran görüntüsünü yalnızca saklamak yerine içindeki bilgiyi, kullanıcının kontrol edebildiği bir kayda ve sonraki adıma dönüştürmek.

**Mevcut alternatifler:**

| Alternatif | Ne yapıyor? | Bizim olası farkımız |
|---|---|---|
| [Pixel Screenshots](https://support.google.com/pixelphone/answer/15312581?hl=en) | Arama, koleksiyon, aksiyon ve hatırlatma | Hedeflediğimiz Android cihazlarda Türkçe alanlar ve tek akışta kayıt; kullanım değeri test edilecek |
| [mymind](https://mymind.com/pricing) | Görselleri okuyup etiketleyen kişisel arşiv | Kaydı başlık/tarih/not olarak düzenleme ve yapılacak işe odaklanma |
| Galeri + not/takvim | Görseli bulma ve hatırlatmayı ayrı araçlarda yapma | Bu adımları aynı kayıtta toplama |

Arama ve hatırlatma rakiplerde de var. Farkımızın “Türkçe, kolay ve düzenlenebilir bir aksiyon akışı” olup olamayacağını ilk kullanıcı denemesinde araştıracağız.

## 04. MVP kapsamı ve ana akış

**Üç temel özellik:**

1. **Görselden kayıt oluşturma:** Kullanıcı ekran görüntüsünü seçer veya paylaş menüsünden gönderir. Metin okunur; başlık, kategori ve varsa tarih için düzenlenebilir taslak hazırlanır.
2. **Arama ve düzenleme:** Başlık, metin ve etiketle kayıt aranır. Kullanıcı not ekler, orijinal görsele döner, kaydı düzenler veya siler.
3. **Hatırlatma ve aksiyon takibi:** Kullanıcı doğruladığı tarih için hatırlatıcı kurar; işi tamamlandı olarak işaretler veya erteler.

**Ana akış:**

1. Ayşe bir staj ilanının ekran görüntüsünü uygulamaya paylaşır.
2. Şirket, pozisyon ve son tarih taslak olarak çıkarılır; Ayşe kontrol edip düzeltir.
3. “Başvuru yap” notunu ekleyip bir gün öncesine hatırlatma kurar.
4. Daha sonra şirket adıyla arayarak ilan görseline ve notuna ulaşır.

**İlk sürümün dışında kalacaklar:**

- Tüm galeriyi otomatik tarama ve bulut senkronizasyonu.
- Otomatik alışveriş, başvuru veya mesaj gönderimi.
- Sosyal ağ ve genel amaçlı sohbet asistanı.
- Android ve iOS'u aynı anda geliştirme. İlk platform ekip kapasitesiyle seçilir.

İlk denemede tek bir içerik türü önceliklendirilir. İlan, ürün ve etkinliğin hepsini aynı anda kusursuz tanımak MVP hedefi değildir.

## 05. Gereksinimler ve başarı ölçütleri

**Kullanıcı hikâyeleri:**

- Kaydettiğim ilanın son tarihini kontrol ederek hatırlatma kurmak istiyorum.
- Görseli bir kelimeyle arayıp bulmak ve neden kaydettiğimi görmek istiyorum.
- İçeriğimi istediğimde düzenlemek ve tamamen silmek istiyorum.

**İşlevsel olmayan beklentiler:**

- Temel kayıt ve arama, model hazırlığından sonra çevrimdışı çalışmalı.
- Görsel ve çıkarılan metin varsayılan olarak cihazda kalmalı.
- Eksik tarih uydurulmamalı; belirsiz bilgi kullanıcıya sorulmalı.
- Bildirim izni yoksa kullanıcı bunu görebilmeli.

**Kabul ölçütleri (önerilen hedefler):**

- 50 izinli/sentetik görselde, açıkça yazılmış tarihler için en az %90 doğru çıkarım.
- Beş pilot kullanıcının en az dördünün kayıt, arama ve hatırlatma görevlerini yardımsız tamamlaması.
- Kullanıcıların medyan görev süresinin mevcut yöntemlerine göre en az %30 kısalması.

Bu değerler test sonucu değil; ürün seçilirse ölçülecek hedeflerdir.

## 06. Teknik yaklaşım ve ekip katkısı

**Olası bileşenler:**

- **Mobil uygulama:** Görsel paylaşımı, kayıt ekranı, arama ve hatırlatıcılar.
- **Metin tanıma:** [Android ML Kit OCR](https://developers.google.com/ml-kit/vision/text-recognition/v2/android) gibi cihazda çalışan bir çözüm.
- **Alan çıkarımı:** Metinden başlık, kategori ve tarih önerisi; önce basit kurallar, gerekirse AI yaklaşımı.
- **Yerel veri deposu:** Görsel bağlantısı, çıkarılan metin, not, etiket ve aksiyon durumu.

**En büyük teknik belirsizlik:** Farklı tasarımlardaki Türkçe ekran görüntülerinden doğru tarih ve başlık çıkarabilmek. Her telefonda güçlü bir yerel LLM çalıştığı varsayılmayacak; AI olmadan düzeltme/kayıt akışı çalışacak.

**Ekip katkısı önerisi:**

- **Mobil/web:** Paylaş menüsü, doğrulama ekranı ve arama deneyimi.
- **AI ve sistem tasarımı (Süleyman):** Alan modeli, OCR/çıkarım yaklaşımı ve değerlendirme.
- **Agent/entegrasyon:** Metin → taslak → kullanıcı onayı → kayıt adımlarını yönetme; ayrı agent gerekmiyorsa eklememe.
- **Ağ/altyapı:** Çevrimdışı çalışma, model indirme/ağ kesintisi testleri ve sürüm dağıtımı.
- **Siber güvenlik:** İzinler, cihazda saklama, silme ve bildirim gizliliği.

Bu proje mobil ve AI ağırlıklı; ağ/backend tarafında daha sınırlı iş çıkarabilir. Beş kişinin uzmanlık beklentisi değerlendirilirken bu nokta hesaba katılmalı. Kişi bazında son görev dağılımı ekipçe yapılacak.

## 07. SDLC ve üç aylık plan

| Hafta | Çıktı |
|---|---|
| 1–2 | Kullanıcı görüşmeleri; 50 görselde OCR/alan çıkarımı deneyi; ilk platform ve içerik türü |
| 3–4 | Görsel seç → metni oku → düzelt → kaydet akışının çalışan sürümü |
| 5–8 | Arama, etiketler, hatırlatma, silme ve cihaz/güvenlik testleri |
| 9–10 | Küçük pilot grup; geri bildirim, tekrar kullanım ve hata ölçümü |
| 11–12 | Düzeltmeler, stabil demo, kurulum rehberi ve sonuç raporu |

Planlama, analiz, tasarım, geliştirme, test, yayın ve bakım çıktıları kısa iterasyonlarla tutulur. Güvenlik çalışmaları sürece eşlik eder. Takvim ve sorumluluklar proje seçilirse ekipçe kesinleştirilir.

## 08. SSDLC ve güvenlik riskleri

**Hassas veriler ve güven sınırları:** Ekran görüntüsünde mesaj, kimlik, banka bilgisi veya parola bulunabilir. Görsel seçimi, uygulama deposu, cihaz yedeği ve olası dış servisler incelenecek.

**En önemli üç risk:**

1. **Gereksiz veri erişimi:** Yalnızca kullanıcının seçtiği görsel işlenir; tüm galeriye otomatik erişilmez. Ham görüntü/metin loglara yazılmaz.
2. **Verinin cihaz veya bildirim üzerinden açılması:** Depolama/yedekleme ve silme davranışı test edilir; kilit ekranında özel içerik varsayılan gizlenir.
3. **Yanlış bilgiyle işlem yapılması:** Tarih ve alanlar kullanıcıya doğrulatılır; görseldeki metin komut olarak yürütülmez; otomatik dış işlem yapılmaz.

**Güvenlik testleri:** İzin reddi, desteklenmeyen/büyük görsel, veri silme, bildirim gizliliği ve ağ trafiğinde içerik sızıntısı testleri.

**Açık sorular:** Cihaz yedeğine hangi veriler girecek? SDK telemetrisi ne içeriyor? [ML Kit açıklaması](https://developers.google.com/ml-kit/terms) cihazda işleme ile SDK ağ/telemetri davranışını ayırıyor; bu ayrım seçilecek çözümde doğrulanacak.

## 09. Test, yayın ve işletim

- **İşlevsel testler:** Görsel ekleme, düzenleme, arama, hatırlatma, tamamlandı/ertelendi ve silme akışları.
- **AI değerlendirmesi:** Türkçe karakter, küçük yazı, karanlık tema, eksik/yılı olmayan tarih içeren sabit görsel kümesi. Başlık, kategori ve tarih ayrı ölçülür; yanlış ve boş sonuçlar ayrı raporlanır.
- **Pilot kullanıcılar:** Düzenli ekran görüntüsü kaydeden en az beş gönüllü.
- **Yayın ve bakım:** Önce tek platformda sınırlı test sürümü; anonim hata takibi, sürüm kaydı ve önceki sürüme dönüş rehberi.

En az iki mevcut cihazda çevrimdışı çalışma, uygulama yeniden başlatma ve bildirim izni reddi kontrol edilir. Gerçek hassas ekran görüntüleri public repoya eklenmez.

## 10. Pazar, maliyet ve uygulanabilirlik

- **Kullanıcı:** İlan, ürün ve duyuru ekran görüntülerini saklayan kişiler.
- **Ödeme yapan taraf:** Olası bireysel kullanıcı. Ücretli gelişmiş özellik modeli düşünülebilir; ödeme isteği henüz doğrulanmadı.
- **Nasıl ulaşırız:** İlk aşamada öğrenciler ve yakın çevremiz; ardından aynı davranışı gösteren daha geniş bir test grubu.
- **Maliyet yaklaşımı:** OCR, arama ve kayıt cihazda çalışırsa merkezi sunucu ve sürekli ücretli AI çağrısı zorunlu olmaz. Yeni cihaz, mağaza yayını ve destek emeği ayrıca hesaplanır. Hazır araçların lisans/dağıtım koşulları seçilmeden önce kontrol edilir.
- **Uygulanabilirlik:** Tek platform ve üç temel özellik üzerinde üç aylık bir MVP denenebilir. Her tür görseli anlayan genel asistan kapsamı bu süreyi aşar.

Ücretsiz yerleşik özellikler güçlü rekabet oluşturuyor. Bu nedenle ilk başarı ölçütü gelir tahmini değil, kullanıcının mevcut yöntemi yerine uygulamayı tekrar açmasıdır.

## 11. İlk doğrulama deneyi

**Önerilen sorumlu:** @suleymanssardogan; mobil ve güvenlik desteği ekipçe belirlenecek.

**Bir haftalık deney:**

1. **Teknik:** İzinli/sentetik 50 ekran görüntüsünde metin ve tarih çıkarımını dene. Hangi alanların yanlış veya eksik geldiğini kaydet.
2. **Kullanıcı:** Beş kişiyle kendi galeri/not yöntemlerinde görsel bulma ve hatırlatma oluşturma görevlerini gözlemle. Aynı görevleri basit prototipte denet; süre ve düzeltme ihtiyacını karşılaştır.
3. **Tekrar kullanım:** Hafta içinde ikinci kez kayıt ekleyip eklemediklerini gözlemle.

**Başarı eşiği:**

- Beş kişiden en az dördünün temel görevleri yardımsız tamamlaması.
- Medyan görev süresinin mevcut yönteme göre en az %30 azalması.
- En az üç kişinin hafta içinde ikinci kez kullanması.

**Fikri değiştirecek sonuç:** Mevcut araçlar aynı işi yeterince kolay yapıyorsa genel arşiv fikri elenir veya tek içerik türüne daraltılır. En belirgin ihtiyaç staj ilanlarında çıkarsa başvuru takipçisiyle bağlantı ayrıca değerlendirilir.

## 12. Kaynaklar, açık sorular ve karar isteği

**Kaynaklar (kontrol tarihi: 2026-10-28):**

- [Google — Pixel Screenshots](https://support.google.com/pixelphone/answer/15312581?hl=en)
- [mymind — özellik ve planlar](https://mymind.com/pricing)
- [Google — Android ML Kit OCR](https://developers.google.com/ml-kit/vision/text-recognition/v2/android)
- [Google — OCR desteklenen diller](https://developers.google.com/ml-kit/vision/text-recognition/v2/languages)
- [Google — ML Kit veri işleme açıklaması](https://developers.google.com/ml-kit/terms)

Kaynaklar resmî ürün/teknik açıklamalardır; rakip uygulamalar bağımsız test edilmedi.

**Açık sorular:**

- İlk içerik türü ilan mı, ürün mü, etkinlik mi olsun?
- Galeri/not uygulamasına göre kullanıcının hissedeceği fark ne olacak?
- Mobil kapasitemiz ve beş kişilik ekip için iş dağılımı uygun mu?

**Ekipten beklenen geri bildirim:**

- Bu problemi siz yaşıyor musunuz; en son nasıl çözdünüz?
- İlk görsel/cihaz denemesine kim destek olabilir?
- [Başvuru takipçisiyle](suleymanssardogan-is-staj-basvuru-takipcisi.md) “ilan görseli → başvuru kaydı” şeklinde birleşmesi daha anlamlı olur mu?

Bu metin bir öneridir. Proje seçimi [değerlendirme yöntemi](../../SELECTION.md) ve ekip kararıyla yapılacak.
