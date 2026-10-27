# Project Hub · Fivefold Labs

Beş yazılım mühendisliği son sınıf öğrencisi; web, agent, yapay zekâ, siber güvenlik ve ağ alanlarını birleştirerek üç ayda gerçek kullanıcılarla denenebilen bir MVP geliştirmeyi hedefliyoruz.

**Durum: keşif aşaması. Proje fikri, hedef kitle ve teknoloji yığını henüz seçilmedi.** Bu repo fikirleri, araştırmayı, kararları ve daha sonra ürün geliştirmeyi ortak bir yerde toplar. Organizasyon adı bir çalışma adıdır.

## Vizyonumuz

Gerçek kullanıcıların hayatını kolaylaştıran, güvenilir ve sürdürülebilir yazılım ürünleri geliştiren; teknik yetkinliğini ekip çalışmasıyla görünür kılan bir mühendislik ekibi olmak.

## Misyonumuz

Web, agent, yapay zekâ, siber güvenlik ve ağ uzmanlıklarımızı ortak bir problem etrafında birleştirmek; kullanıcı araştırmasından bakım sürecine kadar yazılım geliştirme yaşam döngüsünü (SDLC) uygulayarak üç ayda test edilebilir bir MVP üretmek. Güvenliği her aşamaya entegre etmek, kararlarımızı belgelemek ve kullanıcı geri bildirimiyle iyileştirmek.

## Amacımız

- Gerçek bir kullanıcı problemini kanıtlarla belirlemek; fikri ve hedef kitleyi birlikte seçmek.
- Üç ayda sınırlı kapsamlı, çalışan ve gerçek kullanıcılarla denenebilen bir MVP geliştirmek.
- İş başvurularında gösterebileceğimiz güçlü bir portföy ve her üyenin katkısının izlenebildiği bir çalışma ortaya koymak.
- Ürünün pazara giriş ve sürdürülebilir gelir ihtimalini araştırmak; varsayımları doğrulanmış sonuç gibi sunmamak.
- Kod incelemesi, test, güvenlik ve dokümantasyon alışkanlıklarını birlikte geliştirmek.

## Herkes repoyu kendi agent'ına bağlasın

Her ekip üyesi repoyu bilgisayarına klonlayıp kullandığı agent/editörde proje olarak açar. GitHub entegrasyonu kullanıyorsa bu repoya erişimini de doğrular. Ortak kurallar [AGENTS.md](AGENTS.md) içinde; agent'ın bu dosyayı okuduğunu kontrol edin.

```bash
git clone https://github.com/fivefold-labs/project-hub.git
cd project-hub
```

Agent'a verebileceğiniz başlangıç mesajı:

> Önce README.md, AGENTS.md, CONTRIBUTING.md ve docs/AGENT-WORKFLOW.md dosyalarını oku. Projenin amacını ve mevcut aşamasını özetle. GitHub erişimin varsa #5 kurulum, #2 fikir havuzu ve #3 değerlendirme issue'larını incele; erişimin yoksa benden metinlerini iste. Benim görevime uygun bir branch üzerinde çalış; main'e doğrudan push yapma. Fikir önerimi ortak Markdown şablonuyla hazırlamama yardım et. Bulguları ve varsayımları ayır; proje veya teknoloji seçimini ekip adına yapma.

Herkes [kurulum ve ilk katkı issue'suna #5](https://github.com/fivefold-labs/project-hub/issues/5) kurulum durumunu yazsın. [Adım adım agent çalışma rehberi](docs/AGENT-WORKFLOW.md).

## Proje fikrini nasıl sunarız?

[Ortak metin şablonunu](docs/proje-fikirleri/sablonlar/proje-fikri-sablonu.md) kopyalayın ve [gönderimler klasöründe](docs/proje-fikirleri/gonderimler/README.md) `kullaniciadi-fikir-kisa-adi.md` adıyla doldurun. Fikirler doğrudan Markdown (`.md`) olarak teslim edilir.

Her öneri ayrı branch ve PR üzerinden, başka bir ekip üyesinin incelemesiyle alınır. PR bağlantısını [fikir havuzu #2'ye](https://github.com/fivefold-labs/project-hub/issues/2) ekleyin. [Teslim kuralları](docs/proje-fikirleri/README.md).

Bir fikrin belgelenmesi, projenin seçildiği anlamına gelmez. Ürün kararı araştırma, ekip değerlendirmesi ve karar kaydıyla verilir.

## Değerlendirmeye sunulan iki uygulama fikri

- **[Ekran Görüntüsünden Aksiyon](docs/proje-fikirleri/gonderimler/suleymanssardogan-ekran-goruntusunden-aksiyon.md):** Telefonda kaydettiğimiz ekran görüntülerini aranabilir kayıtlara ve hatırlatıcılara dönüştüren mobil uygulama.
- **[İş / Staj Başvuru Takipçisi](docs/proje-fikirleri/gonderimler/suleymanssardogan-is-staj-basvuru-takipcisi.md):** Başvuruları, görüşmeleri ve sonraki adımları tek yerde takip etmeyi sağlayan mobil uygulama.

İki belgede projenin amacı, hedef kullanıcıları, örnek kullanımı ve ilk sürüm kapsamı anlatılıyor. Bunlar Süleyman'ın önerileri; proje henüz seçilmedi. Diğer öneriler ve ekip yorumları [issue #2'de](https://github.com/fivefold-labs/project-hub/issues/2).

## Geliştirme yaklaşımımız: SDLC + SSDLC

Planlama → gereksinim analizi → tasarım → geliştirme → test → yayın → bakım ve geri bildirim. Bu aşamalar kısa iterasyonlarla tekrar edilir; proje seçilmeden teknoloji yığını sabitlenmez.

Siber güvenlik sorumlusu, güvenli yazılım geliştirme yaşam döngüsünü (SSDLC) koordine eder: güvenlik gereksinimleri, tehdit modelleme, güvenli tasarım, güvenlik incelemeleri ve testleri, yayın kontrolleri ve zafiyet takibi. **Güvenlik tüm ekibin sorumluluğudur; yalnızca en sonda yapılan bir test değildir.** [Aşamalar, çıktılar ve sorumluluklar](docs/SDLC-SSDLC.md).

## İlk hafta

1. **Ekibi tanıyalım ve problem/fikir havuzu oluşturalım:** Herkes haftalık müsaitliğini, güçlü alanlarını ve 1–2 problem önerisini ilk issue'ya yorum olarak ekler.
2. **Fikirleri kullanıcı kanıtıyla değerlendirelim:** En fazla üç adayı karşılaştırır, ulaşabildiğimiz kullanıcılarla kısa görüşmeler yaparız. Hafta sonunda en güçlü adayları ve açık soruları kaydederiz; kanıt yetersizse seçim yapmayız.

Aktif işler: [kurulum ve ilk katkı #5](https://github.com/fivefold-labs/project-hub/issues/5), [fikir havuzu #2](https://github.com/fivefold-labs/project-hub/issues/2) ve [değerlendirme #3](https://github.com/fivefold-labs/project-hub/issues/3).

## Nasıl katkı yapıyoruz?

**Ekip kuralı: main'e doğrudan push yok.** Her değişiklik ayrı branch ve pull request üzerinden, yazarı dışındaki en az bir ekip üyesinin incelemesiyle ilerler.

> Kurulum doğrulandı (23 Ekim 2026): public repo, adminler dahil zorunlu PR ve en az bir başka üyeden onay; force push ve main silme kapalı. Ayrıntılar: [koruma ayarları](setup/README.md).

- [Katkı rehberi](CONTRIBUTING.md)
- [Ekip ve çalışma anlaşması](docs/TEAM.md)
- [Fikir önerisi şablonu](docs/proje-fikirleri/sablonlar/proje-fikri-sablonu.md)
- [Agent çalışma kuralları](AGENTS.md)
- [Değerlendirme yöntemi](docs/SELECTION.md)
- [12 haftalık yol haritası](docs/ROADMAP.md)
- [Karar kayıtları](docs/decisions/README.md)
- [Güvenlik](SECURITY.md)

## Başarıyı nasıl göstereceğiz?

Çalışan demo, tekrar kurulabilir ortam, kullanıcı geri bildirimi, anlamlı testler, açıklanmış mimari kararlar ve herkesin yaptığı katkıyı gösteren issue/PR geçmişi. Ürün seçildikten sonra başarı ölçütleri sayısal hale getirilecek.

## Kullanım ve lisans

Lisans ve ürünün dağıtım modeli ekipçe henüz belirlenmedi. Repo public olarak yayımlandı; bu, otomatik olarak bir açık kaynak lisansı verildiği anlamına gelmez. Üçüncü taraf kodların lisanslarını koruruz.
