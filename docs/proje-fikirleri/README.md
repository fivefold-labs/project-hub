# Proje fikirleri

Ekip önerilerini aynı başlıklarla hazırlanmış Markdown metinleri olarak topluyoruz. Proje henüz seçilmedi.

## Ortak şablon

[sablonlar/proje-fikri-sablonu.md](sablonlar/proje-fikri-sablonu.md) dosyasını kopyalayın ve [gonderimler/](gonderimler/README.md) altına `kullaniciadi-fikir-kisa-adi.md` adıyla kaydedin. Küçük harf, ASCII karakter ve tire kullanın. Örnek: `hilmikilavuz-ornek-fikir.md`.

Bölüm başlıklarını ve sırasını koruyun. `[Doldurun]` alanlarını değiştirin; kısa ve somut yazın. Bilinmeyenlere `Henüz doğrulanmadı` yazıp nasıl araştırılacağını ekleyin. Türkçe yazın; teknik terimler İngilizce olabilir. Şablon sürümü 1.1'dir; güncellemeler aynı dosyanın Git geçmişinde takip edilir.

## Teslim akışı

1. En az bir problem önerisini [fikir havuzu #2'ye](https://github.com/fivefold-labs/project-hub/issues/2) yazın.
2. `idea/kullaniciadi-kisa-ad` gibi kendi branch'inizi açın.
3. Şablonu kendi `.md` dosyanıza kopyalayıp doldurun; ortak şablonu değiştirmeyin.
4. PR açın; özet, dosya bağlantısı, açık sorular ve `Refs #2` ekleyin.
5. Başka bir ekip üyesi incelesin. Biçim ve içerik düzeltmeleri tamamlanınca squash merge yapılır.
6. PR bağlantısını #2'ye ekleyin. Sonraki revizyonları aynı dosyada yeni PR ile yapın.

GitHub web arayüzünden dosya eklerken kendi branch'inizi seçin; `Add file → Create new file` üzerinden `.md` dosyası açıp metni yapıştırabilirsiniz. main'e doğrudan commit yapılmaz.

## İnceleme ölçütleri

Tüm bölümler mevcut mu? Problem ve kullanıcı net mi? Kanıt ve varsayım ayrılmış mı? Üç ayda yapılabilir bir MVP var mı? SDLC ve SSDLC düşünülmüş mü? Alternatifler ve kaynaklar yazılmış mı?

Metnin repoya alınması ürün seçimi değildir. Seçim [değerlendirme yöntemi](../SELECTION.md) ve karar kaydıyla yapılır. Repo public; kullanıcı görüşmelerini anonimleştirin ve gizli bilgi paylaşmayın.
