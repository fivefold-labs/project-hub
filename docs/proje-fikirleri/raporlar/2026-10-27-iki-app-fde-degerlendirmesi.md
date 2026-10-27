# İki mobil uygulama fikri: pazar, maliyet ve Forward Deployed Engineering değerlendirmesi

- Tarih: 27 Ekim 2026
- Öneren: @suleymanssardogan; agent desteğiyle hazırlanmıştır.
- Durum: masa başı araştırması ve pilot önerisi; seçilmiş proje değildir.
- Kısıtlar: beş kişilik öğrenci ekibi, üç ayda MVP, düşük hizmet gideri, gerçek müşteriyle FDE deneyimi.
- İlgili işler: [#2 fikir havuzu](https://github.com/fivefold-labs/project-hub/issues/2), [#3 değerlendirme](https://github.com/fivefold-labs/project-hub/issues/3).

## Okuma rehberi

1. [Ekran Görüntüsünden Aksiyon önerisi](../gonderimler/suleymanssardogan-ekran-goruntusunden-aksiyon.md).
2. [İş / Staj Başvuru Takipçisi önerisi](../gonderimler/suleymanssardogan-is-staj-basvuru-takipcisi.md).

İki öneri ortak şablonun 12 bölümünü izler. İkisi birden üç aylık geliştirme planına alınmaz. Birleştirme veya uygulama geliştirme kararı alınmadı. Araştırmada gerçek kullanıcı görüşmesi, ürün denemesi, ödeme veya kurum anlaşması yapılmadı.

## FDE için neyi başarmamız gerekiyor?

Forward Deployed Engineering, müşterinin süreçlerini yerinde/beraber çalışarak anlamak, gerçek veri ve sistemlerle çözüm kurmak, dağıtmak ve kullanım sonuçlarını izlemektir. Palantir ve Anthropic'in resmî işe alım açıklamaları müşteriyle birlikte geliştirme, kurum sistemleri ve uçtan uca teslim sorumluluğunu vurguluyor. Bu açıklamalar bizim bir müşteri bulduğumuzun veya o firmalarla eşdeğer ölçekte iş yaptığımızın kanıtı değildir. [Palantir FDSE rolü](https://jobs.lever.co/palantir/dab396d4-2f14-4796-aac0-0d82883dccf0), [Anthropic FDE rolü](https://job-boards.greenhouse.io/anthropic/jobs/5391016008).

Bu ekip için somut teslimler:

- Bir pilot kurum, süreç sahibi ve haftalık görüşme takvimi.
- Mevcut iş akışı, başlangıç süresi/hata ölçümü ve kabul ölçütleri.
- İzinli örnek veriler; veri akışı ve hedef alan eşlemesi.
- Tek bir gerçek entegrasyon veya kurumun mevcut veri iş akışına kanıtlanmış uyarlama.
- Müşteri ortamı veya onaylı pilot ortamında kurulum, güvenlik testi ve kabul oturumu.
- En az iki haftalık kullanım, hata takibi, kullanıcı eğitimi ve bakım devri.
- Anonim önce/sonra vaka raporu. Başarısız deneyler de açıkça yazılır.

CSV'yi yalnızca indirmek entegrasyon kanıtı sayılmaz: müşteri dosyayı kendi sürecine gerçekten almalı, alan eşlemesi ve çoğaltma/hata davranışı birlikte doğrulanmalıdır. Gerçek müşteri bulunamazsa yapılan iş ürün prototipidir; FDE pilotu tamamlandı diye sunulmaz.

## Karşılaştırma

| Boyut | Ekran Görüntüsünden Aksiyon | İş / Staj Başvuru Takipçisi |
|---|---|---|
| Bireysel değer | Kaydedilen görseli bulunabilir kayda ve hatırlatıcıya dönüştürme | Başvuruyu, görüşmeyi ve sonraki adımı bir arada takip |
| FDE pilotu | Küçük ajansın destek ekran görüntüsünü onaylı iş kaydına dönüştürme | Kariyer/mentorluk ekibinin izinli aday takibine uyarlama |
| Pilot sahibi | Destek/operasyon sorumlusu | Kariyer danışmanı veya bootcamp koordinatörü |
| Gerçek uyarlama | Tek issue/görev sistemi; zorunlu alanlar ve onay akışı | Kurumun aşamaları, danışman paylaşımı ve tek CSV akışı |
| Ana teknik belirsizlik | OCR, tarih/alan çıkarımı, mobil deneyim | Veri sahipliği, kayıt paylaşımı ve kurum erişimi |
| Asgari tüketici işletimi | Cihazda işleme; merkezi servis gerekmeyebilir | Yerel kişisel kayıt mümkün; kurumsal sürüm sunucu gerektirir |
| Rakip baskısı | Pixel Screenshots ve mymind mevcut | Teal/Huntr ücretsiz takip; JobTeaser/Symplicity kurum pazarı |
| Ticari belirsizlik | Kişisel kullanımın aciliyeti ve kurumun zaman kaybı | Ücretsiz alternatiflere karşı değer ve kurum satın alma süresi |
| İlk doğrulama | Bir ajansla anonim görseller ve tek iş akışı | Bir danışman ekibiyle mevcut takip tablosu ve gönüllü adaylar |

Bu tablo bir değerlendirmedir, ölçülmüş puanlama değildir. İki fikrin de tüketici sürümüne tek başına FDE etiketi vermek doğru olmaz.

## Rakip ve pazar bulguları

| Kaynak | Doğrulanan resmî özellik/fiyat | Çıkarımımız |
|---|---|---|
| [Pixel Screenshots](https://support.google.com/pixelphone/answer/15312581?hl=en) | Arama, aksiyonlar ve hatırlatıcı; destek sınırları var | Ekran görüntüsünü anlamlandırma başlı başına yeni değil |
| [mymind](https://mymind.com/pricing) | Görüntü metni tanıma ve etiketleme; Student of Life 7,99 USD/ay | Arşivleme pazarı ücretli ürüne sahip; bizim ödeme isteğimiz bilinmiyor |
| [Teal](https://www.tealhq.com/pricing) | Ücretsiz sınırsız iş takibi; Teal+ 29 USD/30 gün | Temel takip için abonelik satmak zor olabilir |
| [Huntr](https://help.huntr.co/en/articles/9806024-faq) | Ücretsiz 100 iş takibi; Pro 40 USD/ay | Aynı özellikleri daha azıyla sunmak yeterli farklılaşma değil |
| [JobTeaser](https://www.jobteaser.com/en) / [Symplicity](https://www.symplicity.com/uk/csm) | Üniversitelere yönelik kariyer platformları | Kurumsal sürümde de mevcut rakipler var |

Bunlar satıcı beyanlarıdır; aktif ücretli kullanıcı sayısı ve ticari performans bağımsız olarak doğrulanmadı. Bütün rakiplerin tüm özellikleri denenmedi. Rakipte belirli bir özelliğin olmadığı varsayılmıyor. Toplam pazar büyüklüğü, Türkiye ücretli kullanıcı sayısı, TAM/SAM veya gelir tahmini için yeterli veri yok; sayı üretilmedi.

Araştırılacak ticari yaklaşım: bir dar kurumsal sürece yönelik, kapsamı belli ücretli kurulum/pilot ve isteğe bağlı bakım. Müşteri başına sınırsız özel iş yerine ortak ürün çekirdeği + yapılandırma + tek adapter. Her iki fikirde de satın alma isteği müşteri görüşmesi ve somut pilot teklifiyle test edilmeli.

## Düşük maliyet tasarımı

| Kalem | Ekran görüntüsü fikri | Başvuru takipçisi |
|---|---|---|
| OCR / AI | Cihazda OCR adayı; ücretli LLM temel akış için zorunlu değil | Manuel/link/metin girişi temel akışı çalıştırır |
| Merkezi altyapı | Kişisel kullanımda gerekmeyebilir; kurumsal adapter için küçük servis | Kurumsal pilotta uygulama, veritabanı ve yedekleme |
| Veri | Ham görsel varsayılan cihazda; yalnız onaylı metin paylaşımı | Gereken başvuru alanları; ilk sürümde CV dosyası saklama yok |
| Entegrasyon | Bir hedef; hedef aracın lisans/kota maliyeti ayrıca teyit edilecek | Bir kurum CSV biçimi; ilk sürümde SSO/ATS/e-posta yok |

Planlama bütçesi: seçilen tek kurumsal pilot için 0–30 USD/ay altyapı hedefi ve 0–10 USD/ay opsiyonel AI deneme sınırı. Üç aylık üst planlama toplamı 120 USD olur; bu, onaylanmış harcama veya sağlayıcı fiyat teklifi değildir. Ücretsiz kota ve müşteri altyapısının uygunluğu teyit edilmeden sıfır maliyet vaat edilmez. Model denemesi temel gereksinim değil; müşteriye uygun değilse kaldırılır. İki fikir aynı anda bu bütçeyle kurulacak diye varsayılmıyor.

Varsayımlar: mevcut bilgisayar ve Android test cihazı var; emek ücretsiz öğrenci emeği olarak değerlendirilmiş. Yeni cihaz, iOS donanımı, internet/elektrik, vergi, alan adı, mağaza üyeliği, ücretli hedef sistem ve destek emeği bu rakamlara dahil değil. Doğruluk ve kullanıcı kontrolü için harcanan zaman da maliyettir.

Mağaza yayını opsiyoneldir: [Google Play](https://support.google.com/googleplay/android-developer/answer/6112435) geliştirici kaydı 25 USD tek seferlik; [Apple Developer Program](https://developer.apple.com/programs/whats-included/) yıllık 99 USD veya yerel para tutarı listeliyor. Test/kimlik doğrulama gereklilikleri ayrıca uygulanabilir. Bu ücretler ödenmedi ve ödeme yetkisi istenmiyor. İlk pilotun dağıtım yöntemi platform koşullarına göre belirlenir.

Teknik araştırma: [ML Kit OCR](https://developers.google.com/ml-kit/vision/text-recognition/v2/android), [Türkçe dil desteği](https://developers.google.com/ml-kit/vision/text-recognition/v2/languages) ve [işleme/telemetri açıklaması](https://developers.google.com/ml-kit/terms). OCR girdisi cihazda işlenebilir; bu, serbest biçimdeki her bilginin doğru anlaşılacağı veya SDK'nın hiç ağ trafiği üretmeyeceği anlamına gelmez. [Android bildirim izni](https://developer.android.com/develop/ui/compose/notifications/notification-permission) de hatırlatma testlerine dahil edilir.

## Beş kişi ve üç ay: uygulanabilirlik

Bilinen kapasite: Süleyman AI/sistem tasarımı, Ahmet ağ/altyapı ve Oğulcan AI/entegrasyon alanlarını issue #2'de ifade etti; bu yorumlarda haftalık 10 saat yer alıyor. Diğer üyelerin güncel rol ve süreleri teyit edilmeden toplam kapasite kesinleştirilmez. Herkes 10 saat ayırırsa 12 haftada 600 saat brüt kapasite oluşur; bu bir senaryodur. Görüşme, öğrenme, test ve yeniden çalışma geliştirme süresini azaltır.

İş dağılımı önerisi: AI/veri değerlendirme, mobil/web, backend/tek adapter, güvenlik/SSDLC, dağıtım/izleme. Roller ekipçe atanır. FDE'yi tek kişiye bırakmayın; herkes en az bir müşteri gözlemi, geri bildirim değerlendirmesi veya kabul oturumuna katılsın. Mobil deneyim eksikse ilk hafta teknik deneme ve kapsam indirimi gerekir.

Ürün seçimi sonrası: 1–2. hafta keşif ve anlaşılmış ölçütler; 3–6. hafta tek uçtan uca akış; 7–8. hafta kurum uyarlaması; 9–10. hafta gerçek pilot; 11–12. hafta iyileştirme, işletim devri ve vaka yazısı. Müşteri izin süreçleri üç ayı aşabilir. İkinci hafta sonunda süreç sahibi ve erişim yoksa FDE hedefi için aday yeniden değerlendirilir.

## Ekipten istenen karar ve bir haftalık plan

Bu rapor iki fikirden birini seçmez. FDE açısından öncelik, önce gerçek pilot kurumu bulunabilen fikre verilsin.

- Bir kişi üç küçük ajansın destek/operasyon sürecine erişim arasın.
- Bir kişi iki kariyer/mentorluk ekibi ve beş aktif adayla görüşme arasın.
- Süleyman alan çıkarımı ve mimari riskleri; ağ/altyapı sorumlusu kurulum ve maliyet senaryosunu; güvenlik sorumlusu veri erişimi/izin risklerini incelesin. İsim bazlı görevler ekip toplantısında kesinleştirilsin.
- Her aday için bir mevcut iş örneği, başlangıç süre ölçümü ve pilot sahibi kaydedilsin. Kişisel veriler public repoya konmasın.
- Hafta sonunda #3'te kanıtları karşılaştırın: bir süreç sahibi, izinli veri, tek uygulanabilir entegrasyon ve iki haftalık deneme zamanı var mı?

Birinin FDE koşulları sağlanırsa o adayın ürün kapsamını kesinleştirin. İkisi de sağlamıyorsa üçüncü aday araştırılır; gerçek müşteri olmadan saha deneyimi tamamlandı diye sunulmaz. Tüketici prototipi seçilirse FDE hedefinin henüz karşılanmadığı açıkça kaydedilir.
