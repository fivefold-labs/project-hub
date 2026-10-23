# Proje fikirleri

Burada ekip üyelerinin standart formatta hazırladığı fikir PDF'leri toplanır. Proje henüz seçilmedi.

## Klasörler

- `sablonlar/proje-fikri-sablonu.md`: kopyalayıp doldurulacak düzenlenebilir kaynak.
- `sablonlar/proje-fikri-sablonu.pdf`: başlık sırası ve sayfa düzeni için referans; interaktif form değildir.
- `gonderimler/`: üyelerin tamamladığı PDF'ler ve isteğe bağlı düzenlenebilir kaynakları.

## Ortak format v1.0

A4 dikey, yaklaşık 20 mm kenar boşluğu, okunabilir 10–12 punto gövde metni. Hedef 4 sayfa, gerekirse en fazla 6 sayfa. 12 bölümün adını ve sırasını koruyun; Markdown'daki `[Doldurun]` alanlarını değiştirin, açıklama yönergelerini teslimden önce kaldırın. Bilmediğiniz alanlara `Henüz doğrulanmadı` ve nasıl araştıracağınızı yazın. Türkçe yazın; teknik terimlerin İngilizcesini kullanabilirsiniz.

Başlıkları ve sırayı koruyarak Word, Google Docs veya Markdown editöründe hazırlayıp PDF olarak dışa aktarabilirsiniz. PDF metni seçilebilir olmalı; ekran görüntüsü veya tarama olarak göndermeyin. Başlık bilgilerine yazarın GitHub hesabını, tarihi, fikir sürümünü ve şablon sürümünü ekleyin. E-posta/telefon gibi kişisel bilgiler eklemeyin.

Dosya adı: `kullaniciadi-fikir-kisa-adi-v01.pdf`. Küçük harf, ASCII karakter ve tire kullanın. Örnek: `hilmikilavuz-ornek-fikir-v01.pdf` (yalnızca dosya adı örneğidir).

## Teslim akışı

1. Şablonu kopyalayın ve tüm bölümleri doldurun.
2. PDF'yi açıp sayfa taşması, Türkçe karakterler ve kaynak bağlantılarını kontrol edin.
3. Repoda `idea/kullaniciadi-kisa-ad` branch'i açın.
4. PDF'yi `docs/proje-fikirleri/gonderimler/` içine ekleyin. Düzenlenebilir kaynağı aynı kök adla ekleyebilirsiniz; ortak şablonu değiştirmeyin.
5. PR açın; özet, dosya bağlantısı, açık sorular ve ilgili issue'yu belirtin. İlk hafta [#2 fikir havuzuna](https://github.com/fivefold-labs/project-hub/issues/2) bağlantı verin.
6. Başka bir ekip üyesinin onayından sonra squash merge yapılır. Sonraki revizyon yeni sürüm numarası ve yeni PR ile gelir.

Tarayıcıdan yüklerken önce branch seçin; `Add file → Upload files` ile yükleyin, sonra PR açın. main'e doğrudan yükleme/commit yapılmaz.

## İnceleme ölçütleri

12 bölüm mevcut mu? Problem ve kullanıcı net mi? Kanıt ve varsayım ayrılmış mı? Üç ayda yapılabilir bir MVP var mı? SDLC ve SSDLC planlanmış mı? Mevcut alternatifler ve kaynaklar yazılmış mı? PDF okunabilir mi?

Biçim incelemesi, fikrin ürün olarak kabulü değildir. Ürün seçimi [değerlendirme yöntemi](../SELECTION.md) ve karar kaydıyla yapılır. Repo public olduğu için kullanıcı görüşmelerini anonimleştirin; gizli bilgi yüklemeyin.
