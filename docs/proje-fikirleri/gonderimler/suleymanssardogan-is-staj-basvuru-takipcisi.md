# Proje Fikri Önerisi

> Şablon v1.1 · Durum: öneri (proje kararı değildir)

- Proje adı: İş / Staj Başvuru Takipçisi (çalışma adı)
- Yazar / GitHub: Süleyman / @suleymanssardogan
- Tarih: 2026-10-28
- Fikir sürümü: v03
- Şablon sürümü: 1.1
- İlgili issue: [#2](https://github.com/fivefold-labs/project-hub/issues/2)

## 01. Problem ve kullanıcı

İş ve staj ararken farklı şirketlere, farklı siteler üzerinden başvurabiliyoruz. Başvurular çoğaldıkça şu soruları takip etmek zorlaşıyor:

- Hangi şirkete ne zaman başvurdum; cevap bekliyor muyum?
- O başvuruda hangi CV sürümünü kullandım?
- Görüşme ne zaman ve öncesinde ne hazırlamalıyım?
- Henüz başvurmadığım hangi ilanın son tarihi yaklaşıyor?

Bugün bu bilgileri Excel, notlar, e-posta ve takvim arasında takip edebiliyoruz. Başvurunun kaydı ile sonraki adımı aynı yerde görmek için bu bilgileri bir araya getirmek gerekiyor.

**Amacımız:** Başvuruları, görüşmeleri ve sonraki yapılacak işleri tek yerde gösteren bir mobil uygulama geliştirmek.

**Hedef kullanıcılar:** Staj arayan üniversite öğrencileri, ilk işine başvuran mezunlar ve aynı anda birden fazla başvuru yürüten kişiler. İlk denemeleri kendimiz ve aktif iş/staj arayan arkadaşlarımızla yapabiliriz.

## 02. Kanıt ve varsayımlar

**Doğrulanan bulgular (kaynaklı):**

- [Teal](https://www.tealhq.com/pricing), ücretsiz sınırsız başvuru takibi sunuyor.
- [Huntr](https://help.huntr.co/en/articles/9806024-faq), ücretsiz planda 100 işe kadar takip sunuyor.

Bu nedenle başvuru panosu yeni bir fikir değil; mevcut ürünlerden hangi noktada ayrılacağımızı göstermemiz gerekiyor.

**Henüz doğrulanmadı (varsayımlar):**

- Hedef öğrencilerin mevcut takip yönteminde sorun yaşadığı. Araştırma: son başvuruları üzerinden görüşme.
- Türkçe ve hızlı kayıt akışının mevcut ürünlerden daha kullanışlı bulunacağı. Araştırma: aynı görevleri karşılaştıran prototip testi.
- Kullanıcıların durumları düzenli güncelleyeceği veya ücretli özellik isteyeceği. Araştırma: bir haftalık tekrar kullanım denemesi.

Henüz kullanıcı görüşmesi, ürün testi veya satış yapılmadı.

## 03. Değer önerisi ve alternatifler

**Değer önerisi:** Kullanıcının “hangi başvurum ne durumda, sırada ne yapmalıyım?” sorusunu tek ekranda cevaplamak.

**Mevcut alternatifler:**

| Alternatif | Ne yapıyor? | Bizim olası farkımız |
|---|---|---|
| [Teal](https://www.tealhq.com/pricing) | İş takibi ve CV araçları | Türkçe staj akışında kısa kayıt/güncelleme deneyimi |
| [Huntr](https://help.huntr.co/en/articles/9806024-faq) | Başvuru panosu, ilan kaydetme ve CV araçları | Kullanıcının getirdiği ilan metninden düzenlenebilir kayıt ve sonraki adıma odaklanma |
| Excel / Notion / takvim | Kişinin kurduğu başvuru listesi ve hatırlatmalar | Kayıt, görüşme ve sonraki adımı ayrı araçlar yerine tek akışta toplama |

Kariyer.net veya LinkedIn gibi kaynaklardan kullanıcı tarafından yapıştırılan metin/linkle çalışmak düşünülebilir. Bu, sitelerle resmî entegrasyon veya otomatik içerik okuma taahhüdü değildir. Türkçe arayüz tek başına yeterli fark sayılmaz.

## 04. MVP kapsamı ve ana akış

**Üç temel özellik:**

1. **Başvuru kaydı:** Şirket, pozisyon, ilan kaynağı, başvuru/son tarih ve kullanılan CV sürümünün etiketi. Kullanıcı elle veya yapıştırdığı metin/link üzerinden kayıt oluşturur.
2. **Durum panosu:** Kaydedildi, başvuruldu, görüşme, teklif, olumsuz ve geri çekildi aşamaları; her başvuruya özel not ve filtreler.
3. **Görüşme ve sonraki adım:** Tarih, hazırlık notu ve hatırlatma; yapılacak işi tamamlandı olarak işaretleme.

**Ana akış:**

1. Mehmet sekiz staj ilanını kaydeder.
2. Başvurduğu üçünü “başvuruldu” aşamasına taşır; birine “İngilizce CV v2” notunu ekler.
3. Görüşme daveti geldiğinde tarih, bağlantı ve hazırlık notunu girer.
4. Hatırlatma alır; görüşme sonrasında sonucu günceller.
5. Panodan kimden cevap beklediğini ve sıradaki işlerini görür.

**İlk sürümün dışında kalacaklar:**

- Otomatik başvuru ve e-posta hesabını okuma.
- İlan sitelerini topluca tarama ve tüm sitelerle entegrasyon.
- CV üretimi, AI mülakatı ve aday puanlama.
- CV dosyası depolama; ilk aşamada kullanıcı etiketi yeterli olabilir.
- Birden fazla mobil platformu aynı anda geliştirme.

Başvuru durumunu kullanıcı günceller; sistem şirketin yanıt verdiğini kendi kendine varsaymaz.

## 05. Gereksinimler ve başarı ölçütleri

**Kullanıcı hikâyeleri:**

- Aday olarak hangi başvurularımın açık olduğunu ve hangi CV etiketiyle başvurduğumu görmek istiyorum.
- Görüşmemin tarihini ve hazırlık notunu tek kayıtta tutmak istiyorum.
- Kayıtlarımı dışa aktarmak veya silmek istiyorum.

**İşlevsel olmayan beklentiler:**

- Elle kayıt ve durum takibi AI olmadan çalışmalı.
- Eksik tarih veya başvuru sonucu uydurulmamalı.
- Kayıtlar kullanıcıya ait olmalı; dışa aktarma/silme yapılabilmeli.
- Bildirim izni verilmezse kullanıcı bunu görebilmeli.

**Kabul ölçütleri (önerilen hedefler):**

- Beş kişiden en az dördünün kayıt, durum güncelleme ve hatırlatma görevlerini yardımsız tamamlaması.
- Kayıt/güncelleme görev süresinin mevcut yöntemlerine göre medyan %25 kısalması.
- En az üç kişinin yedi gün içinde ikinci bir gün kayıt veya durum güncellemesi yapması.

Bunlar pilotta ölçülecek hedeflerdir. İşe girme oranı gibi uzun vadeli sonuçlar MVP'nin garanti ettiği bir başarı olarak sunulmayacak.

## 06. Teknik yaklaşım ve ekip katkısı

**Olası bileşenler:**

- **Mobil uygulama:** Başvuru formu, durum panosu, arama ve hatırlatıcılar.
- **Veri modeli:** İlan kaydı, başvuru durumu, durum geçmişi, not ve sonraki adım.
- **Yerel veri deposu:** İlk sürümde hesap/senkronizasyon zorunlu olmadan kayıtları saklama.
- **AI desteği:** Kullanıcının yapıştırdığı ilan metninden şirket, rol ve tarih taslağı çıkarma; sonuçları kullanıcıya doğrulatma.

**En büyük teknik belirsizlik:** Farklı ilan metinlerinden doğru alan çıkarırken elle kayıt akışını yavaşlatmamak. Önce basit yöntemle başlangıç sonucu ölçülür. Link eklemek için her sitenin içeriğini otomatik okuyabildiğimiz varsayılmaz.

**Ekip katkısı önerisi:**

- **Mobil/web:** Başvuru formu, pano ve görüşme ekranları.
- **AI ve sistem tasarımı (Süleyman):** Veri modeli, alan çıkarımı ve değerlendirme.
- **Agent/entegrasyon:** İlan metni → taslak → onaylı kayıt akışı; ayrı agent gerekmezse eklememe.
- **Ağ/altyapı:** Çevrimdışı çalışma, dağıtım ve ileride senkronizasyon ihtiyacının analizi.
- **Siber güvenlik:** Kişisel veri saklama, izinler, silme ve dışa aktarma güvenliği.

Ağ/backend katkısı yerel bir uygulamada daha dar kalabilir. Her uzmanlığa derin iş çıkarmak ekip için temel koşulsa bu dezavantaj seçimde dikkate alınmalı. Roller proje seçildiğinde kesinleşir.

## 07. SDLC ve üç aylık plan

| Hafta | Çıktı |
|---|---|
| 1–2 | Aktif adaylarla görüşme; mevcut yöntem karşılaştırması; veri modeli ve ilk platform |
| 3–4 | İlan ekle → aşama değiştir → sonraki adım oluştur akışının çalışan sürümü |
| 5–8 | Notlar, filtreler, hatırlatıcı, ilan metni deneyi ve veri güvenliği testleri |
| 9–10 | Küçük pilot grup; kayıt güncelleme ve tekrar kullanım ölçümü |
| 11–12 | Düzeltmeler, stabil demo, kurulum rehberi ve sonuç raporu |

Planlama, gereksinim, tasarım ve test kararları süreç boyunca güncellenir. Güvenlik kontrolleri geliştirme sonunda bırakılmaz. Bu takvim proje seçilirse detaylandırılacak taslaktır.

## 08. SSDLC ve güvenlik riskleri

**Hassas veriler ve güven sınırları:** Başvuru geçmişi, görüşme notları, kişi bilgileri ve ilan metni. Kullanıcı cihazı, işletim sistemi yedeği ve olası AI servisi ayrı değerlendirilir.

**En önemli üç risk:**

1. **Kişisel verinin açığa çıkması:** İlk sürümde CV dosyası yerine etiket tutulur. Ham başvuru/notlar loglara yazılmaz; yedekleme, silme ve dışa aktarma test edilir.
2. **Zararlı ilan metni veya bağlantı:** İçerik güvenli görüntülenir; metin komut olarak yürütülmez. Link kullanıcı onayıyla açılır; sunucudan rastgele URL getirme yapılmaz.
3. **Dış AI servisine gereksiz veri aktarımı:** Temel akış uzak modele bağlı olmaz. Dış servis denenirse gönderilecek alanlar gösterilir ve kullanıcı onayı alınır.

**Güvenlik testleri:** Kayıt silme, dışa aktarma, bildirimde özel notların görünmesi, izin reddi ve zararlı metin/link örnekleri.

**Açık sorular:** Cihaz yedekleri ve veri saklama nasıl çalışacak? Hesap/senkronizasyon eklenirse sahiplik kontrolü ve kullanıcılar arası erişim testleri nasıl uygulanacak?

## 09. Test, yayın ve işletim

- **İşlevsel testler:** Başvuru oluşturma/düzenleme, aşama değişikliği, tekrarlanan ilan, arama, görüşme hatırlatması, silme ve dışa aktarma.
- **AI değerlendirmesi:** Kullanımına izin verilen/sentetik ilan metinlerinde şirket, rol ve tarih alanlarını ayrı ölçme. Yanlış tarih hata sayılır; belirsiz tarihin boş kalması kabul edilebilir.
- **Pilot kullanıcılar:** Şu anda iş/staj başvurusu yapan en az beş gönüllü; ilk hafta sonrası tekrar kullanım gözlemi.
- **Yayın ve bakım:** Tek platformda sınırlı test sürümü, anonim hata takibi ve önceki sürüme dönüş rehberi.

En az iki mevcut cihazda yeniden başlatma, çevrimdışı çalışma ve bildirim izni kontrol edilir. Gerçek aday kayıtları veya görüşme notları repoya konmaz.

## 10. Pazar, maliyet ve uygulanabilirlik

- **Kullanıcı:** Staj veya iş başvurusu yürüten bireyler.
- **Ödeme yapan taraf:** Olası bireysel kullanıcı. Gelişmiş özellikler için ücretli model düşünülebilir; ödeme isteği henüz araştırılmadı.
- **Nasıl ulaşırız:** Aktif başvuru yapan öğrenciler, mezunlar ve yakın çevremiz.
- **Maliyet yaklaşımı:** Yerel veri saklama, elle giriş ve hatırlatma ile ilk sürüm merkezi sunucu olmadan denenebilir. AI desteği zorunlu olmaz. Yeni cihaz, mağaza yayını ve destek emeği ayrıca hesaplanır.
- **Uygulanabilirlik:** Üç temel özellik ve tek platformla üç aylık bir MVP hedeflenebilir. Otomatik başvuru, bütün ilan siteleri ve e-posta entegrasyonu kapsamı ciddi büyütür.

Teal ve Huntr'ın ücretsiz takip sunması gelir modeli için önemli bir risk. Kullanıcıların uygulamayı tekrar açıp kayıtlarını güncellemesi, ücretli özellik düşünmeden önce doğrulanması gereken davranıştır.

## 11. İlk doğrulama deneyi

**Önerilen sorumlu:** @suleymanssardogan; mobil prototip ve güvenlik desteği ekipçe belirlenecek.

**Bir haftalık deney:**

1. **Kullanıcı:** Aktif başvuru yapan beş kişiyle son başvurularını nasıl takip ettiklerini gözlemle. Hangi bilgileri kaybettiklerini ve mevcut araçlarını sor.
2. **Prototip:** Kayıt ekleme, durum güncelleme ve görüşme hatırlatma görevlerini basit prototipte denet. Aynı görevleri mevcut yöntemleriyle karşılaştır.
3. **Tekrar kullanım:** Bir hafta içinde ikinci bir gün kayıt/güncelleme yapıp yapmadıklarını izle.

**Başarı eşiği:**

- En az 4/5 kişinin temel görevleri yardımsız tamamlaması.
- Medyan görev süresinin mevcut yönteme göre %25 azalması.
- En az üç kişinin ikinci bir gün kayıt veya durum güncellemesi yapması.

**Fikri değiştirecek sonuç:** Kullanıcılar panoyu güncellemiyor veya mevcut ücretsiz araçları yeterli buluyorsa genel takip fikri yeniden değerlendirilir. Asıl ihtiyaç ekran görüntüsünden hızlı kayıt çıkarsa kapsam o akışa daraltılabilir.

## 12. Kaynaklar, açık sorular ve karar isteği

**Kaynaklar (kontrol tarihi: 2026-10-28):**

- [Teal — takip ve planlar](https://www.tealhq.com/pricing)
- [Huntr — resmî yardım ve planlar](https://help.huntr.co/en/articles/9806024-faq)

Kaynaklar resmî ürün açıklamalarıdır; rakip uygulamalar bağımsız test edilmedi.

**Açık sorular:**

- Staj arayan kullanıcı için mevcut ürünlerin çözemediği somut iş ne?
- Veri girişini ve durum güncellemeyi nasıl kolaylaştırabiliriz?
- Beş kişilik ekip için teknik kapsam yeterli mi?

**Ekipten beklenen geri bildirim:**

- Başvurularınızı bugün nasıl takip ediyorsunuz; en çok nerede zorlanıyorsunuz?
- İlk kullanıcı/prototip denemesine kim destek olabilir?
- [Ekran Görüntüsünden Aksiyon](suleymanssardogan-ekran-goruntusunden-aksiyon.md) fikriyle birleşip “ilan görseli → başvuru kaydı” akışı oluşturması daha yararlı olur mu?

Bu iki öneriyi aynı anda iki ürün olarak geliştirme kararı alınmadı. Proje seçimi [değerlendirme yöntemi](../../SELECTION.md) ve ekip kararıyla yapılacak.
