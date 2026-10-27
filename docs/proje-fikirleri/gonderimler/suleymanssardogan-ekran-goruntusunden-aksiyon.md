# Proje Fikri Önerisi

> Şablon v1.1 · Durum: öneri (proje kararı değildir)

- Proje adı: Ekran Görüntüsünden Aksiyon
- Yazar / GitHub: Süleyman / @suleymanssardogan (agent desteğiyle hazırlanmıştır)
- Tarih: 2026-10-28
- Fikir sürümü: v02
- Şablon sürümü: 1.1
- İlgili issue: [#2](https://github.com/fivefold-labs/project-hub/issues/2)

## 01. Problem ve kullanıcı

**Amacımız:** Telefonda biriktirdiğimiz ekran görüntülerini, sonradan bulabildiğimiz ve zamanı geldiğinde hatırlatma alabileceğimiz kayıtlara dönüştüren bir mobil uygulama geliştirmek.

Bir staj ilanı, beğendiğimiz ürün veya etkinlik duyurusu gördüğümüzde ekran görüntüsü alıyoruz. Görsel galeride başka fotoğraflarla karışabiliyor; neyi neden kaydettiğimizi unutabiliyor veya içindeki tarihi kaçırabiliyoruz. Bu sorunun ne sıklıkta yaşandığını kullanıcılarla doğrulamamız gerekiyor.

**Hedef kullanıcı:** İlan, ürün ve duyuruları ekran görüntüsüyle kaydeden kişiler. İlk görüşmeler üniversite öğrencileriyle yapılabilir; ürün yalnızca üniversite etkinliklerine bağlı değildir.

**Örnek:** Ayşe bir staj ilanının görselini uygulamaya paylaşır. Uygulama şirket, pozisyon ve varsa son tarih için taslak çıkarır. Ayşe alanları düzeltir ve bir gün önce hatırlatma kurar. Daha sonra şirket adıyla arayıp orijinal görsele ve notuna ulaşır.

## 02. Kanıt ve varsayımlar

**Kaynaklarla doğrulananlar:**

- [Pixel Screenshots](https://support.google.com/pixelphone/answer/15312581?hl=en) zaten arama, önerilen aksiyonlar ve hatırlatma sunuyor; cihaz, dil ve bölge koşulları var.
- [mymind](https://mymind.com/pricing) görseldeki yazıyla arama ve AI etiketleme sunuyor.
- [ML Kit dil listesinde](https://developers.google.com/ml-kit/vision/text-recognition/v2/languages) Türkçe yer alıyor. Desteklenmesi, kendi görsellerimizde hedef doğruluğa ulaştığımız anlamına gelmez.

**Henüz doğrulanmayanlar:** Kullanıcıların mevcut galerilerinde yeterince zorlandığı, Türkçe alan çıkarımının yeterli çalışacağı, ayrı uygulama açmanın değeceği ve ödeme isteği. Henüz görüşme, prototip testi veya satış yapılmadı. Kendi deneyimimizi pazar kanıtı saymıyoruz.

## 03. Değer önerisi ve alternatifler

**Değer önerisi:** “Kaydettiğin ekran görüntüsünü kolayca bul; içindeki işi unutma.” Görseli yalnızca arşivlemek yerine kullanıcı tarafından doğrulanmış bir aksiyon kaydı oluşturmak istiyoruz.

| Alternatif | Neyi çözüyor? | Bizim sınayacağımız fark |
|---|---|---|
| [Pixel Screenshots](https://support.google.com/pixelphone/answer/15312581?hl=en) | Arama, koleksiyonlar, aksiyonlar ve hatırlatıcı | Hedef Android cihazlarda Türkçe ve az adımlı kayıt akışı yeterli değer yaratır mı? |
| [mymind](https://mymind.com/pricing) | Görsel içerik tanıma, etiketleme ve kişisel arşiv | Düzenlenebilir alanlar ve bir sonraki aksiyona odaklanmak yararlı mı? |
| Galeri + notlar/takvim | Kullanıcının mevcut yöntemi; görüşmede gözlemlenecek | Görseli bulma ve hatırlatma oluşturma süresi gerçekten azalıyor mu? |

**Rekabet riski:** “OCR ve hatırlatıcı” benzersiz bir özellik birleşimi değil. Hatırlatmayı tek başına farkımız diye sunamayız. Kullanıcı mevcut aracıyla rahatça çözüyorsa bu fikir ticari öncelik olmayabilir.

## 04. MVP kapsamı ve ana akış

**İlk sürümün üç temel özelliği:**

1. **Görselden kayıt:** Paylaş menüsü/görsel seçici, cihazda metin okuma ve düzenlenebilir başlık, kategori, tarih taslağı.
2. **Kayıtları bulma:** Metin, başlık ve etiketle arama; kayda not ekleme, orijinal görsele dönme, düzenleme ve silme.
3. **Aksiyon:** Kullanıcının doğruladığı tarih ve açıklamayla yerel hatırlatıcı; tamamlandı/ertelendi durumu.

**Ana akış:** Görseli seç → metni oku → alanları kontrol et → kaydet → hatırlatıcı kur → arayarak geri dön.

Başlangıçta tek mobil platform hedeflenir. Görüşmeler sonucunda bir içerik türü önceliklendirilir; ilan, ürün ve etkinliğin tamamını aynı anda kusursuz tanıma sözü verilmez.

**Kapsam dışı:** Tüm galeriyi otomatik tarama, sosyal ağ, satın alma veya başvuru yapma, iOS ile eşzamanlı geliştirme, bulut senkronizasyonu ve genel amaçlı sohbet agent'ı.

## 05. Gereksinimler ve başarı ölçütleri

**Kullanıcı hikâyeleri:**

- Kullanıcı olarak kaydettiğim ilanın başlığını ve son tarihini kontrol ederek hatırlatma kurabilmek istiyorum.
- Kaydımı bir kelimeyle arayıp orijinal görüntüyü bulmak istiyorum.
- Görsel ve çıkarılan metinleri istediğimde silebilmek istiyorum.

**Önerilen kabul ölçütleri; henüz ölçülmedi:**

- Kaynakta olmayan tarih oluşturulmaz; belirsiz/eksik tarih kullanıcıya sorulur veya boş kalır.
- 50 izinli/sentetik görselde başlık/kategori/tarih için alan bazında sonuç raporlanır. Kaynakta açık olan tarihlerde en az %90 doğru çıkarım ilk teknik hedeftir; yanlış ve boş sonuçlar ayrı sayılır.
- Beş pilot kullanıcının en az dördü kaydetme, arama ve hatırlatıcı oluşturma görevlerini yardım almadan tamamlar.
- Hatırlatıcı izni reddedilirse bu durum açıkça gösterilir. Cihaz ve işletim sistemi kısıtları nedeniyle kesin teslim garantisi verilmez.
- Temel kayıt ve arama çevrimdışı çalışır; kullanıcı içerikleri varsayılan olarak dış servise gönderilmez.

## 06. Teknik yaklaşım ve ekip katkısı

**Teknik yaklaşım önerisi:** Mobil istemci → cihazda OCR → alan çıkarımı → kullanıcı doğrulaması → yerel veri deposu/arama → yerel hatırlatma.

[Android ML Kit OCR](https://developers.google.com/ml-kit/vision/text-recognition/v2/android) teknik adaylardan biri. Önce OCR ve basit kurallarla bir başlangıç sonucu ölçülür. Güçlü bir yerel LLM'nin her telefonda çalışacağı varsayılmaz; ücretli AI çağrısı temel akışın şartı değildir. Teknoloji seçimi ilk haftadaki cihaz denemesinden sonra yapılır.

| Alan | Anlamlı katkı önerisi |
|---|---|
| Süleyman / AI ve sistem tasarımı | Alan modeli, çıkarım yaklaşımı ve doğruluk değerlendirmesi |
| Mobil/web | Paylaşım, doğrulama, arama ve hatırlatma ekranları |
| Agent/backend | Araçlardan oluşan onaylı işlem akışı; ayrı agent yarar sağlamazsa eklenmez |
| Siber güvenlik | Yerel veri, dosya yükleme, izin ve silme testleri |
| Ağ/altyapı | Çevrimdışı/model indirme davranışı, ağ trafiği doğrulaması ve sürüm dağıtımı |

**Ekip uyumu sınırı:** Bu fikir mobil ve AI ağırlıklı. Ağ/altyapı ve backend işi daha dar kalabilir. Beş kişinin de derin uzmanlık işi yapması öncelikse bu dezavantajı seçimde hesaba katmalıyız; sırf görev üretmek için sunucu eklememeliyiz.

## 07. SDLC ve üç aylık plan

| Hafta | Somut çıktı |
|---|---|
| 1–2 | Kullanıcı görüşmeleri, mevcut yöntemle karşılaştırma, OCR deneyi; ilk içerik ve platform seçimi |
| 3–4 | Görsel seçme → metin → elle düzeltme → kayıt akışının çalışan sürümü |
| 5–6 | Arama, etiket, tarih doğrulama ve hatırlatma |
| 7–8 | İzin, silme, çevrimdışı davranış ve cihaz testleri |
| 9–10 | Sınırlı pilot; tekrar kullanım ve hata ölçümü |
| 11–12 | Düzeltmeler, stabil demo, kurulum ve bakım notları |

Analiz ve tasarım kararları yazılı tutulur; güvenlik kontrolleri her aşamada uygulanır. Bu plan ürün seçilirse detaylandırılacak bir öneridir. Fikir onayı olmadan uygulama geliştirmeye başlanmış sayılmaz.

## 08. SSDLC ve güvenlik riskleri

**Temel güvenlik gereksinimi:** Kullanıcının seçtiği görsel ve çıkarılan metin varsayılan olarak cihazda işlenir/saklanır; içerik dış servise gönderilmez. Bir sağlayıcı kullanılırsa model/SDK indirme ve telemetri trafiği ayrıca incelenir. Cihazda OCR, hiç ağ trafiği olmadığı anlamına gelmez.

| Risk | Önlem ve doğrulama |
|---|---|
| Görselde kimlik, mesaj, banka veya parola bulunması | Yalnızca seçilen görsele erişim; ham içeriği loglamama; testlerde gerçek hassas veri kullanmama; bildirimde özel içeriği varsayılan gizleme |
| Cihaz kaybı/yedeği üzerinden veri açılması | Uygulama depolama/yedekleme davranışını inceleme; silinen kayda ve kopyalarına erişim testi |
| Yanlış tarihten aksiyon veya görsel metninden komut çalıştırma | Tarih doğrulaması, kullanıcı onayı; OCR çıktısını veri olarak işleme, otomatik dış işlem yapmama |

Siber güvenlik sorumlusu veri akışını, izinleri ve silme gereksinimlerini inceler. Fotoğraflar public repoya yüklenmez. SSDLC bu gereksinimlerin geliştirme ve test boyunca izlenmesidir.

## 09. Test, yayın ve işletim

**Testler:** Türkçe karakter, küçük yazı, karanlık tema, bir görselde birden fazla tarih, yılı olmayan tarih, düşük kontrast ve aynı görselin tekrar eklenmesi. En az iki mevcut Android cihazında çevrimdışı çalışma, izin reddi, yeniden başlatma ve model hazırlığı denenir.

**AI değerlendirmesi:** Sabit ve izinli/sentetik örnek kümesinde çıkarılan her alan kaynakla karşılaştırılır. Kritik tarih hataları genel ortalamada gizlenmez. Kullanıcının düzeltme süresi de ölçülür.

**Yayın ve işletim:** Önce küçük bir gönüllü test grubu; dağıtım yöntemi güncel platform koşullarıyla seçilir. Sürüm, anonim hata kaydı, maliyet ve geri dönüş yöntemi belgelenir. Mağaza yayını ilk deneyin zorunlu çıktısı değildir. Şu an uygulama veya çalıştırılmış ürün testi yok.

## 10. Pazar, maliyet ve uygulanabilirlik

**İlk kullanıcı:** Ekran görüntüsüyle ilan/ürün/duyuru biriktiren kişiler; ilk erişim öğrenciler ve yakın çevre. **Olası ödeme yapan:** Bireysel kullanıcı. Ödeme isteği doğrulanmadı; ücretsiz yerleşik alternatifler önemli bir engel.

Olası gelir modeli, temel kullanım ücretsizken ileride gelişmiş düzenleme/yedekleme özellikleri için ücret alınması olabilir; henüz karar veya gelir tahmini değildir. Önce tekrar kullanım kanıtı gerekir.

| Kalem | İlk sürüm yaklaşımı |
|---|---|
| OCR ve arama | Cihazda çalışma; merkezi görsel depolama yok |
| AI API | Zorunlu değil; eklenirse onaylı kullanım ve bütçe sınırı gerekir |
| Sunucu | Yerel MVP için gerekli değil |
| Diğer maliyet | Mevcut cihaz/ekipman varsayımı; yeni cihaz, mağaza, bakım emeği ayrıca hesaplanır |

Düşük maliyet hedefi sıfır toplam maliyet garantisi değil. Hazır araçların fiyat/koşulları teknoloji seçimi sırasında teyit edilir. En büyük belirsizlik geliştirme giderinden çok kullanıcıya mevcut araçlardan daha değerli gelmesi ve beş kişiye uygun kapsam oluşturmasıdır.

## 11. İlk doğrulama deneyi

**Önerilen sorumlu:** @suleymanssardogan; ilk deney koordinasyonu. Mobil/güvenlik desteği verecek üyeler ekipçe belirlenecek.

**Bir haftalık deney:**

1. Düzenli ekran görüntüsü kaydeden beş kişiyle son kaydettikleri içerikleri nasıl bulduklarını gözlemle.
2. Her katılımcıyla hassas içeriği çıkarılmış beş örnekte mevcut yöntemle bulma/hatırlatma süresini ölç.
3. Basit etkileşimli akış veya teknik taslakla aynı görevleri denet; görev sırasını değiştirerek öğrenme etkisini azalt.
4. Mevcut galeri/not yöntemi ile yeni akışı süre ve düzeltme ihtiyacı açısından karşılaştır. Yalnızca “beğendim” yanıtını talep kanıtı sayma.

**İlerleme eşiği:** En az 4/5 kişi görevi yardımsız tamamlar; kullanıcıların medyan görev süresi en az %30 azalır; en az üç kişi bir hafta içinde ikinci kez kullanmayı dener. Bunlar deney öncesi önerilen hedeflerdir.

**Vazgeçme/daraltma koşulu:** Mevcut araç aynı işi yeterince iyi yapıyor, kullanıcı uygulamaya geçmiyor veya tarih düzeltme yükü kazancı ortadan kaldırıyorsa genel arşiv fikri daraltılır ya da elenir. İlan türü belirgin şekilde daha yararlıysa yalnızca o akış değerlendirilir.

## 12. Kaynaklar, açık sorular ve karar isteği

**Kaynaklar — son kontrol: 28 Ekim 2026.** Ürün sayfaları resmî özellik beyanıdır; uygulamaları bağımsız olarak denemedik.

- [Pixel Screenshots](https://support.google.com/pixelphone/answer/15312581?hl=en): arama, aksiyon ve hatırlatıcı özellikleri.
- [mymind](https://mymind.com/pricing): görüntü metniyle arama ve etiketleme.
- [ML Kit Android OCR](https://developers.google.com/ml-kit/vision/text-recognition/v2/android) ve [dil listesi](https://developers.google.com/ml-kit/vision/text-recognition/v2/languages): teknik araştırma adayları.
- [ML Kit veri işleme açıklaması](https://developers.google.com/ml-kit/terms): cihazda işlem ve SDK trafiği ayrımı.

**Açık sorular:** Hangi içerik türü, hangi mobil platform, mevcut araçlara karşı hangi ölçülebilir fark, beş kişilik ekip için yeterli teknik kapsam var mı?

**Ekipten istediğim:** Önce bir haftalık deneye alınmasını ve kapsamın tartışılmasını değerlendirelim. [Başvuru takipçisiyle](suleymanssardogan-is-staj-basvuru-takipcisi.md) birleştirme, ileride ekran görüntüsünden başvuru kaydı üretme şeklinde düşünülebilir; şu an iki ayrı öneri ve tek ürün kararı alınmadı. Kabul, [seçim ölçütleriyle](../../SELECTION.md) ve [issue #3'te](https://github.com/fivefold-labs/project-hub/issues/3) değerlendirilecek.
