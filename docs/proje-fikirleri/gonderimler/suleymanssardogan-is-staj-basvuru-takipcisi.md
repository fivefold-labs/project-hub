# Proje Fikri Önerisi

> Şablon v1.1 · Durum: öneri (proje kararı değildir)

- Proje adı: İş / Staj Başvuru Takipçisi
- Yazar / GitHub: Süleyman / @suleymanssardogan (agent desteğiyle hazırlanmıştır)
- Tarih: 2026-10-28
- Fikir sürümü: v02
- Şablon sürümü: 1.1
- İlgili issue: [#2](https://github.com/fivefold-labs/project-hub/issues/2)

## 01. Problem ve kullanıcı

**Amacımız:** İş ve staj başvurularını, görüşmeleri ve sonraki yapılacakları tek yerde takip edebileceğimiz bir mobil uygulama geliştirmek.

Farklı sitelerden birden fazla başvuru yaptığımızda hangi ilana ne zaman başvurduğumuzu, hangi CV sürümünü kullandığımızı ve hangi şirketten cevap beklediğimizi karıştırabiliyoruz. Başvuru bilgileri notlara, e-postalara ve takvimlere dağılabiliyor. Bunun hedef kullanıcıda ne kadar önemli olduğunu araştıracağız.

**Hedef kullanıcı:** Staj arayan öğrenciler, ilk işine başvuran mezunlar ve aynı anda birden fazla başvuru yürüten kişiler.

**Örnek:** Mehmet sekiz ilanı kaydeder, üçüne başvurunca durumlarını günceller. Bir kayda “İngilizce CV v2” etiketini ekler. Görüşme daveti geldiğinde tarih, bağlantı ve hazırlık notunu kaydeder; hatırlatma kurar. Ana ekranda “hangi başvurum ne durumda, sırada ne yapmalıyım?” sorusunun yanıtını görür.

## 02. Kanıt ve varsayımlar

**Kaynaklarla doğrulananlar:**

- [Teal](https://www.tealhq.com/pricing) ücretsiz sınırsız başvuru takibi sunuyor.
- [Huntr](https://help.huntr.co/en/articles/9806024-faq) ücretsiz planda 100 işe kadar takip sunuyor.

**Varsayımlar:** Türkiye'deki öğrencilerin mevcut çözümlerden memnun olmadığı, Türkçe ve hızlı girişin fark yaratacağı, kullanıcıların durumları düzenli güncelleyeceği ve ücretli özellik isteyeceği. Bunlar henüz doğrulanmadı.

Henüz kullanıcı görüşmesi, prototip denemesi veya ödeme kanıtı yok. Son sınıf öğrencisi olmamız ilk kullanıcıya ulaşmayı kolaylaştırabilir; tek başına pazar talebi göstermez.

## 03. Değer önerisi ve alternatifler

**Değer önerisi:** “Başvurduğun işleri, görüşmeleri ve bir sonraki adımını tek yerde gör.” Hızlı kayıt ve düzenli güncellemeyi kolaylaştıran dar bir mobil deneyim hedefleniyor.

| Alternatif | Neyi çözüyor? | Bizim sınayacağımız fark |
|---|---|---|
| [Teal](https://www.tealhq.com/pricing) | Başvuru takibi ve CV araçları; ücretsiz takip | Türkçe staj akışında daha az adımla kayıt ve güncelleme |
| [Huntr](https://help.huntr.co/en/articles/9806024-faq) | Takip panosu, ilan kaydetme ve CV araçları | Öğrencinin kullandığı ilan metninden kolayca düzenlenebilir kayıt |
| Excel / Notion / takvim | Kullanıcının kurduğu takip yöntemi | Görüşme ve sonraki aksiyonları yönetmede süre/çaba azalması |

Türkçe arayüz veya pano tek başına üstünlük değildir. Teal/Huntr gibi ücretsiz ürünler ciddi rakip. Kullanıcının “neden mevcut aracımı bırakayım?” sorusuna deneyle yanıt veremiyorsak projeyi seçmemeliyiz.

## 04. MVP kapsamı ve ana akış

**İlk sürümün üç temel özelliği:**

1. **Başvuru kaydı:** Elle veya kullanıcının yapıştırdığı ilan metni/linkiyle şirket, rol, kaynak, tarih ve CV sürümü etiketi.
2. **Süreç panosu:** Kaydedildi, başvuruldu, görüşme, teklif, olumsuz ve geri çekildi gibi aşamalar; başvuruya özel not ve arama.
3. **Sonraki adım:** Görüşme/takip tarihi, hazırlık notu ve kullanıcının seçtiği hatırlatma.

**Ana akış:** İlanı ekle → alanları doğrula → aşamayı güncelle → not/sonraki adım ekle → hatırlatma al → sonucu kaydet.

Başvuru durumunu kullanıcı belirler; uygulama bir şirketin yanıt verdiğini varsaymaz. İlan bağlantısını saklamak, o sitenin içeriğini otomatik okuyabildiğimiz anlamına gelmez; elle giriş ve metin yapıştırma temel akışı çalıştırır.

**Kapsam dışı:** Otomatik başvuru, toplu ilan kazıma, e-posta hesabını tarama, CV üretimi, AI mülakatı, aday puanlama, tüm iş siteleriyle entegrasyon ve eşzamanlı çoklu platform geliştirme.

## 05. Gereksinimler ve başarı ölçütleri

**Kullanıcı hikâyeleri:**

- Aday olarak başvurumun durumunu ve hangi CV etiketiyle başvurduğumu görmek istiyorum.
- Görüşme tarihini ve hazırlık notunu tek kayıtta tutmak istiyorum.
- Kayıtlarımı dışa aktarmak ve silmek istiyorum.

**Önerilen kabul ölçütleri; henüz ölçülmedi:**

- Eksik son tarih veya şirket yanıtı uydurulmaz; kullanıcı verileri düzenleyebilir.
- İlk pilotta beş kullanıcının en az dördü kayıt, aşama güncelleme ve hatırlatma görevlerini yardımsız tamamlar.
- Yedi gün içinde en az üç kullanıcı ikinci bir gün gerçek bir başvuru kaydı veya durum güncellemesi yapar.
- Görüşme/hatırlatma izni kapalıysa görünür durum sunulur; bildirimlerin kesin teslimi vaat edilmez.
- Dışa aktarılan kayıtlar tekrar okunabilir; silme ve izin akışları test edilir. Bu hedefler ürün seçilirse ayrıntılı kabul testlerine dönüştürülecek.

## 06. Teknik yaklaşım ve ekip katkısı

**Teknik yaklaşım önerisi:** Mobil istemci, yerel kayıtlar ve durum modeli, arama ve hatırlatma. Düşük maliyet için ilk sürümde hesap ve bulut senkronizasyonu zorunlu değil. Mevcut mobil geliştirme kapasitesi ilk hafta doğrulanacak.

**AI katkısı:** Yapıştırılan ilan metninden şirket, pozisyon ve tarih taslağı araştırılabilir. Başlangıçta kurallar ve kullanıcı girişiyle ölçülebilir temel sürüm kurulur. AI devre dışıyken de takip çalışır. Kaynakta olmayan alan üretilmez; adayları değerlendiren veya işe alınma olasılığı veren model yapılmaz.

| Alan | Anlamlı katkı önerisi |
|---|---|
| Süleyman / AI ve sistem tasarımı | Başvuru veri modeli, alan çıkarımı ve ölçümü |
| Mobil/web | Kayıt, pano, filtre ve takvim/hatırlatma deneyimi |
| Agent/backend | Durum akışı ve onaylı alan çıkarımı; agent gereksizse eklenmez |
| Siber güvenlik | Kişisel veri, saklama, dışa aktarma/silme ve izin testleri |
| Ağ/altyapı | Cihaz/ağ kesinti davranışı, dağıtım ve ileride senkronizasyon gereksinimi analizi |

**Ekip uyumu sınırı:** Yerel takip uygulamasında ağ ve backend uzmanlığına ayrılan iş daha az olabilir. Ağır altyapı kurarak bu açığı yapay biçimde büyütmek yerine seçim değerlendirmesine dürüstçe yazmalıyız. Tüm üyelerin derin uzmanlık işi yapması temel koşulsa bu fikir daha zayıf kalabilir.

## 07. SDLC ve üç aylık plan

| Hafta | Somut çıktı |
|---|---|
| 1–2 | Aktif aday görüşmeleri, mevcut yöntem karşılaştırması, veri modeli ve tek platform seçimi |
| 3–4 | İlan kaydı → aşama → sonraki adım akışının çalışan sürümü |
| 5–6 | Notlar, filtreler, tarih ve hatırlatma |
| 7–8 | İlan metninden taslak deneyi, silme/dışa aktarma ve cihaz testleri |
| 9–10 | Aktif başvuru yapan küçük grupla pilot ve tekrar kullanım ölçümü |
| 11–12 | Düzeltmeler, stabil demo ve kurulum/bakım rehberi |

Gereksinim, mimari ve güvenlik kararları küçük iterasyonlarla güncellenir. Bu, proje seçildikten sonra kesinleştirilecek taslak SDLC planıdır; uygulama kodu henüz yok.

## 08. SSDLC ve güvenlik riskleri

Başvuru geçmişi, görüşme notu ve iletişim bilgileri kişisel veri içerebilir. İlk sürümde CV dosyası depolamak yerine kullanıcı etiketini tutarak veri miktarını azaltırız.

| Risk | Önlem ve doğrulama |
|---|---|
| Başvuru/notların cihaz veya yedekten açılması | Uygulama depolama ve yedekleme davranışı; silme/dışa aktarma testleri; kilit ekranında özel not göstermeme |
| İlan linki veya metni üzerinden zararlı içerik | Güvenli metin gösterimi; linki kullanıcı onayıyla açma; sunucudan rastgele URL çekmeme; metni komut gibi çalıştırmama |
| Opsiyonel AI'a kişisel veri gönderimi | İlk akışta dış model zorunlu değil; eklenirse açık onay, gönderilen alanları gösterme ve loglarda içerik tutmama |

Siber güvenlik sorumlusu veri akışını, izinleri, saklamayı ve silme gereksinimlerini koordine eder. Gerçek aday kayıtları public repoya veya test loglarına konmaz. İleride hesap/senkronizasyon eklenirse sahiplik kontrolü ve kullanıcılar arası erişim testleri yeni gereksinim olur.

## 09. Test, yayın ve işletim

**İşlevsel testler:** Başvuru ekleme/düzenleme, aşama geçişi, tekrarlanan ilan, tarih/saat dilimi, arama, hatırlatma izni ve veri silme. Dışa aktarılan örnek kayıtların eksiksiz okunabildiği doğrulanır.

**AI denemesi:** Kullanımına izin verilen/sentetik ilan metinleriyle şirket, rol ve tarih alanları ayrı ayrı değerlendirilir. Belirsiz tarihlerde boş bırakma kabul edilir; yanlış tarih önerisi hata sayılır. Başarısız çıkarımda manuel akış açık kalır.

**Pilot:** En az beş aktif iş/staj arayan kişiyle bir hafta; sonraki aşamada iki haftalık tekrar kullanım gözlemi. İlk kayıt sayısına ek olarak ikinci gün/hafta güncellemesi ölçülür.

**Yayın ve işletim:** Küçük test grubu, sürüm takibi, anonim hata bilgisi ve önceki sürüme dönüş rehberi. Mağaza yayını için koşullar ayrıca kontrol edilir. Kullanıcının gerçek başvuru içeriği izleme sistemine gönderilmez. Şu an test sonucu veya aktif kullanıcı olduğu iddia edilmiyor.

## 10. Pazar, maliyet ve uygulanabilirlik

**Kullanıcı ve olası ödeme yapan:** İş/staj arayan birey. Üniversite öğrencileri ve yakın çevreden ilk deneme grubu bulunabilir. Kurumsal müşteriye erişim veya anlaşma olduğu varsayılmıyor.

Temel takip için güçlü ücretsiz rakipler olduğu için ücretli abonelik satmak zor olabilir. Olası ücretli özellikler ileride değerlendirilebilir; önce tekrar kullanım ve mevcut araçlara karşı değer kanıtlanmalıdır. Gelir, pazar büyüklüğü ve ödeme isteği henüz doğrulanmadı.

| Kalem | İlk sürüm yaklaşımı |
|---|---|
| Veri saklama ve hatırlatma | Cihazda; merkezi sunucu zorunlu değil |
| AI | İsteğe bağlı deney; manuel giriş temel işlevi sağlar |
| İlan verisi | Kullanıcının girdiği metin/link; ücretli ilan API'si veya scraping altyapısı yok |
| Diğer maliyet | Mevcut cihazlar varsayılır; yayın, yeni cihaz ve destek emeği ayrıca hesaplanır |

Üç ayda dar bir takip akışı teknik olarak denenebilir; bütün iş arama sürecini otomatikleştirmek kapsamı aşar. Seçim için asıl soru, yeni uygulamanın tablo veya mevcut ücretsiz araca göre daha düzenli kullanılacak olmasıdır.

## 11. İlk doğrulama deneyi

**Önerilen sorumlu:** @suleymanssardogan; kullanıcı deneyi koordinasyonu. Mobil prototip ve veri güvenliği desteği ekipçe atanacak.

**Bir haftalık deney:**

1. Şu anda iş/staj başvurusu yapan beş kişiyle görüş; son başvurularını nasıl takip ettiklerini gözlemle.
2. Gerçek kişisel içerikleri toplamadan kayıt, aşama güncelleme ve görüşme hatırlatma akışının basit taslağını denet.
3. Kullanıcının mevcut yöntemiyle aynı görevleri karşılaştır; süreyi, düzeltmeleri ve unutulan sonraki adımları kaydet.
4. Bir hafta boyunca ikinci bir günde tekrar kayıt/güncelleme yapıp yapmadıklarını gözlemle; yalnızca beğeni yorumlarını başarı sayma.

**İlerleme eşiği:** En az 4/5 kişi temel görevleri yardımsız yapar; medyan kayıt+güncelleme süresi mevcut yöntemden %25 kısa olur; en az üç kişi bir haftada ikinci kez kullanır. Bunlar önceden önerilen ölçütlerdir, elde edilmiş sonuçlar değil.

**Vazgeçme/daraltma koşulu:** Kullanıcılar panoyu güncellemiyor veya Teal/Huntr/tablolarla aynı işi yeterince kolay yapıyorsa genel takip fikri yeniden değerlendirilir. Ekran görüntüsünden hızlı kayıt belirgin ihtiyaç çıkarsa yalnızca o akış için teknik deney önerilir.

## 12. Kaynaklar, açık sorular ve karar isteği

**Kaynaklar — son kontrol: 28 Ekim 2026.** Resmî ürün beyanlarıdır; uygulamalar bağımsız olarak denenmedi.

- [Teal fiyat ve özellikleri](https://www.tealhq.com/pricing): ücretsiz sınırsız iş takibi; geniş CV/başvuru araçları.
- [Huntr resmî yardım / planlar](https://help.huntr.co/en/articles/9806024-faq): ücretsiz 100 işe kadar takip, ilan kaydetme ve ücretli ek araçlar.

**Açık sorular:** Türkçe staj akışında hangi fark değerli, kullanıcı neden mevcut araçtan geçer, veri girişini nasıl azaltırız, beş uzmanlık alanı için kapsam yeterli mi?

**İki fikrin ilişkisi:** [Ekran Görüntüsünden Aksiyon](suleymanssardogan-ekran-goruntusunden-aksiyon.md), başvuru kaydı oluşturmanın başka bir girişi olabilir. Bu seçenek birleştirme kararı değildir; önce her fikrin kullanım değerini ayrı sınayacağız. İki tam ürünü aynı anda geliştirmeyeceğiz.

**Ekipten istediğim:** Bir haftalık deneyi ve ekip uyumunu değerlendirelim. Fikrin belgelenmesi proje seçimi anlamına gelmez; [seçim ölçütleri](../../SELECTION.md) ve [issue #3](https://github.com/fivefold-labs/project-hub/issues/3) üzerinden birlikte karar verilecek.
