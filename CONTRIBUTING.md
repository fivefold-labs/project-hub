# Katkı rehberi

## Günlük akış

1. İlgili issue'yu okuyun; yapmak istediğiniz işi yorumla belirtin.
2. Güncel main'den branch açın: `docs/fikir-onerisi`, `feat/oturum-akisi`, `fix/baglanti-hatasi` gibi.
3. Küçük, tek amacı olan değişiklikler yapın. Commit mesajı değişikliği açıklasın.
4. main hedefli pull request açın; ilgili issue'yu, değişikliğin nedenini ve doğrulamasını yazın.
5. Başka bir ekip üyesinden review isteyin. En az bir onay alın; açık yorumları çözün.
6. Yeni değişiklik sonrası gerekirse tekrar review isteyin. Uygun PR'ları squash merge yapın ve branch'i silin.

main'e doğrudan push, force push ve main'i silmek ekip kurallarına aykırıdır. Public repoda bu kısıtlamalar GitHub branch protection ile uygulanıyor; etkinleştirme durumu setup/README.md içinde izlenir. İlk repo oluşturma işlemi dışında normal katkılar daima PR ile yapılır.

## Review

Kişiyi değil değişikliği değerlendirin. Sorunu, nedenini ve mümkünse bir öneriyi yazın. Yazar kendi PR'ını onaylayamaz. İnceleme sorumluluğunu ekip içinde dönüşümlü paylaşın.

## Tamamlanma ölçütü

- Issue'nun kabul ölçütleri karşılandı.
- Davranışı etkileyen değişiklikler uygun şekilde doğrulandı; sonuç PR'a yazıldı.
- Gerekli dokümanlar güncellendi, gizli bilgi veya kişisel kullanıcı verisi eklenmedi.
- Başka bir ekip üyesi inceledi ve önemli yorumlar çözüldü.

Henüz uygulama veya test altyapısı yok; çalıştırılmamış testleri geçmiş gibi göstermeyin. Teknoloji yığını seçilince kurulum, test ve CI komutları eklenecek.

## Fikir metinleri, agent kullanımı ve güvenlik etkisi

Fikir metinleri [ortak format](docs/proje-fikirleri/README.md) ile `docs/proje-fikirleri/gonderimler/` klasörüne `.md` dosyası olarak PR üzerinden eklenir. Metnin birleştirilmesi, proje fikrinin seçildiği anlamına gelmez.

PR'larda güvenlik etkisini açıklayın. Kimlik/yetki, veri işleme, dış araç çağrıları veya ağ sınırları değişiyorsa güvenlik koordinatöründen inceleme isteyin. Ayrıntılar: [SDLC ve SSDLC](docs/SDLC-SSDLC.md).

Agent ile çalışırken [AGENTS.md](AGENTS.md) ve [başlangıç rehberini](docs/AGENT-WORKFLOW.md) izleyin. Her üye kendi agent oturumunu repo klasörüne bağlar; yaptığı değişikliği inceleme ve doğrulama sorumluluğunu taşır.
