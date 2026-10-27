# Proje önerisi: Ekran Görüntüsünden Aksiyon

Öneren: @suleymanssardogan · Tarih: 27 Ekim 2026 · Durum: ekip değerlendirmesine sunulan fikir.

## Amacımız

Telefonda biriktirdiğimiz ekran görüntülerini, sonradan kolayca bulabildiğimiz ve gerektiğinde bize ne yapacağımızı hatırlatan kayıtlara dönüştüren bir mobil uygulama geliştirmek istiyoruz.

Bir ilan, beğendiğimiz bir ürün veya katılmak istediğimiz bir etkinlik gördüğümüzde ekran görüntüsü alıyoruz. Fakat bu görüntüler galeride başka fotoğraflarla karışıyor. Bir süre sonra neyi neden kaydettiğimizi unutuyor, aradığımız görüntüyü bulmakta zorlanıyor veya içindeki tarihi kaçırabiliyoruz.

Uygulamamızın amacı ekran görüntüsünü yalnızca saklamak değil, içindeki bilgiyi kullanışlı hale getirmek: **kaydet → düzenle → bul → zamanı gelince harekete geç.**

## Kimler kullanabilir?

İnternette gördüklerini ekran görüntüsüyle kaydeden kişiler. Örneğin iş/staj ilanlarını biriktiren öğrenciler, ürün araştıran kullanıcılar veya etkinlik duyurularını daha sonra değerlendirmek isteyenler.

İlk denemede ulaşabildiğimiz öğrencilerle çalışabiliriz. Onların en sık kaydettiği içerik türünü gözlemleyerek ilk sürümün odağını netleştirebiliriz.

## Uygulama nasıl çalışacak?

1. Kullanıcı bir ekran görüntüsünü telefonun paylaş menüsünden uygulamaya gönderir veya uygulama içinden seçer.
2. Uygulama görseldeki metni okur ve bir kayıt taslağı oluşturur.
3. Kullanıcı başlığı, kategoriyi, notu ve varsa tarihi kontrol edip düzenler.
4. Kaydı saklar; isterse hatırlatıcı ekler.
5. Daha sonra başlık, metin veya etiket üzerinden arayarak kaydı ve orijinal görseli bulur.

Uygulama olmayan bir tarihi veya bağlantıyı uydurmaz. Görselden kesin çıkarılamayan bilgiler boş bırakılır veya kullanıcıya sorulur. Bir işleme geçmeden önce kullanıcı bilgileri doğrular.

## Örnek kullanım

Ayşe bir staj ilanının ekran görüntüsünü alıp uygulamaya paylaşır. Uygulama şirket ve pozisyon adını taslak olarak çıkarır. Görselde son başvuru tarihi varsa Ayşe bunu doğrular; yoksa kendisi ekleyebilir. Başvurmadan bir gün önce hatırlatma kurar.

Bir hafta sonra “geçen gün kaydettiğim yazılım stajı”nı ararken galeride yüzlerce fotoğraf arasında dolaşmak yerine uygulamadaki kayıtlar arasında arar. İlan görseline ulaşır, notunu okur ve başvuru adımına geçer. Başvuruyu otomatik olarak uygulama yapmaz.

Başka bir kullanıcı ürün ekran görüntüsünü “alınacaklar” etiketiyle kaydedebilir; etkinlik duyurusu kaydeden biri ise katılım için hatırlatıcı ekleyebilir. İlk sürümde bu kategorilerin ne kadarının otomatik tanınacağı örnek görsellerle denendikten sonra belirlenir.

## İlk sürümde neler olacak?

- Görsel seçme ve paylaş menüsünden içe aktarma.
- Görseldeki metni okuma ve kullanıcıya düzenlenebilir kayıt taslağı gösterme.
- Başlık, kategori, etiket ve kişisel not ekleme.
- Kayıt içeriğinde arama ve kategoriye göre filtreleme.
- Kullanıcının belirlediği tarihte hatırlatma.
- Orijinal görsele dönme, kaydı düzenleme ve silme.

Üç aylık hedefimiz bu akışın tek bir mobil platformda düzgün çalışması. İlk sürüme sosyal ağ, otomatik alışveriş, otomatik başvuru veya bütün galeriyi arka planda tarama eklemiyoruz.

## Yapay zekânın katkısı

Görseldeki yazıyı okumak ve bunu başlık/kategori gibi düzenlenebilir alanlara dönüştürmek için metin tanıma ve gerektiğinde AI yöntemleri araştıracağız. Her özelliğin bir LLM çağrısıyla yapılması gerekmiyor. Önce basit ve ölçülebilir yaklaşımı deneyip doğruluğuna bakacağız.

Görselleri ve metin okumayı mümkün olduğunca cihazda tutmak, hem gizlilik hem maliyet açısından hedefimiz. Bu hedefin seçilen cihazlarda uygulanabilirliğini küçük bir teknik denemeyle doğrulayacağız. Kullanıcı onayı olmadan görüntü veya metin dış servise gönderilmeyecek.

## Neden bu projeyi yapabiliriz?

İlk kullanıcıları yakın çevremizden bulabilir, kendi ekran görüntülerimizle örnekler hazırlayabiliriz. Tek platform ve sınırlı bir akışla başlarsak dosya işleme, arama, mobil deneyim ve hatırlatma üzerinde çalışabiliriz. Merkezi sunucu ve sürekli ücretli AI kullanımı zorunlu olmadan düşük maliyetli bir ilk sürüm hedefleyebiliriz.

Başarıyı “AI kullandık” diye değil, kullanıcının kaydını yeniden bulabilmesi, bilgiyi kolayca düzeltebilmesi ve uygulamayı tekrar kullanmasıyla değerlendireceğiz. Bunun kullanıcı için yeterince değerli olup olmadığını görüşmeler ve çalışan bir prototiple sınayacağız.

## Ekipçe konuşacağımız sorular

- İlk olarak hangi içerik türüne odaklanalım: ilan, ürün veya etkinlik?
- İlk mobil platform hangisi olsun; bu konuda deneyimimiz ne kadar?
- Metin tanıma ve kayıt oluşturma hangi cihazlarda yeterince iyi çalışıyor?
- Kullanıcılar mevcut galeri/not uygulamaları yerine bunu neden tekrar açsın?

Bu belge projeyi anlatan bir öneridir. Geliştirme kararı ve ayrıntılı iş bölümü ekip değerlendirmesinden sonra verilecek.
