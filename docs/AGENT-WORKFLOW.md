# Agent ile ekip çalışmasına başlama

## 1. Repo erişimini hazırla

Organizasyon davetini kabul edin. Herkes kendi GitHub hesabını ve kendi agent oturumunu kullanır. Public repoyu okumak için davet gerekmez; ekibin Write yetkisiyle branch göndermek için üyelik gerekir.

```bash
git clone https://github.com/fivefold-labs/project-hub.git
cd project-hub
```

Klasörü agent destekli editör veya terminal aracınızda açın. GitHub bağlantısı kullanan bir agent ile çalışıyorsanız `fivefold-labs/project-hub` erişimini kendi hesabınızdan sağlayın. Başkasının token'ını kullanmayın; token'ı sohbet veya issue'ya yazmayın.

## 2. Ortak bağlamı okut

Önce README.md, AGENTS.md, CONTRIBUTING.md ve bu belgeyi okutun. Her agent AGENTS.md dosyasını otomatik okumayabilir; dosyayı açıkça okumasını isteyin. GitHub bağlantısı dosyaları ve issue'ları kendiliğinden bağlama yüklediği anlamına gelmez.

Kopyalanabilir başlangıç mesajı:

> Bu repo fivefold-labs/project-hub. Önce README.md, AGENTS.md, CONTRIBUTING.md, docs/SDLC-SSDLC.md ve docs/proje-fikirleri/README.md dosyalarını oku. GitHub erişimin varsa #5, #2 ve #3 issue'larını incele; erişimin yoksa benden metinlerini iste. Amacımızı, mevcut aşamayı ve benim sıradaki işimi özetle. Göreve özel branch kullan, main'e doğrudan push yapma. Proje fikri ve teknoloji yığını henüz seçilmedi. Araştırmadaki gerçekleri varsayımlardan ayır. Kullanıcı adım: <GitHub hesabım>. Bu oturumdaki görevim: <tek somut görev>.

## 3. İlk katkını yap

- [#5 kurulum issue'suna](https://github.com/fivefold-labs/project-hub/issues/5) agent/repo erişim durumunu yazın.
- [#2 fikir havuzuna](https://github.com/fivefold-labs/project-hub/issues/2) alanınızı, haftalık zamanınızı ve en az bir problem önerinizi ekleyin.
- [Ortak şablonu](proje-fikirleri/sablonlar/proje-fikri-sablonu.md) kopyalayın ve `docs/proje-fikirleri/gonderimler/` altında kendi `.md` dosyanızı doldurun.
- Ayrı branch'ten PR açın; #2'ye PR bağlantısını ekleyin. Başka bir ekip üyesinden review isteyin.
- Başka bir öneriye gerekçeli geri bildirim verin. Adaylar [#3](https://github.com/fivefold-labs/project-hub/issues/3) üzerinden karşılaştırılacak.

## 4. Her görevde

Güncel main'i alın; kendi branch'inizi açın veya uygun mevcut görev branch'ini kontrol ederek sürdürün. Başka üyenin işini ezmeyin. Agent'a tek ve sınırları belli bir görev verin. Çıktıyı kendiniz inceleyin; ilgili doğrulamaları çalıştırın; PR açıklamasına sonuçları yazın. main'e birleşmek için yazar dışındaki en az bir üyenin onayı gerekir.

Henüz ürün kodu veya kurulum/test komutu yok. Şu an repoyu klonlamak ve Markdown belgelerini düzenlemek yeterlidir.
