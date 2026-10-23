# GitHub kurulum durumu ve hedef ayarlar

23 Ekim 2026 tarihinde GitHub API üzerinden doğrulandı: public repo, main üzerinde adminler dahil zorunlu PR, bir onay, son push için başka üyeden onay, eski onayların düşürülmesi, konuşmaların çözülmesi ve linear history etkin. Force push ve silme kapalı.

## İstenen yapı

- Organizasyon: fivefold-labs (oluşturuldu).
- Plan: GitHub Free; repo: project-hub, public.
- Varsayılan branch: main; katkı branch'leri PR ile birleşir.
- builders takımı: dört arkadaş ve repo sahibi; repo Write erişimi.
- Arkadaşlar: HilmiKilavuz, Ahmetyasarcan, ogulcannarin, MertSrtp.
- İlk hafta: docs/week-01 altındaki iki taslak GitHub issue olarak açılır.

## Main koruması

Public repo seçimiyle ücretsiz planda zorunlu branch protection kullanılabilir. Uzak repo oluşturuldu ve koruma etkin. Yerel git hook'ları sunucu koruması yerine geçmez.

Etkin korumalar ve sonraki CI adımı:

- Pull request zorunlu, en az bir başka üyenin onayı.
- Yeni commit'te eski onayları düşür; açık review konuşmaları çözülsün.
- Admin bypass kapalı; force push ve branch silme kapalı.
- Squash merge; mümkünse linear history.
- CI tanımlanıp başarıyla çalıştıktan sonra ilgili kontroller zorunlu yapılır. Henüz olmayan job adları eklenmez.

Etkin repo ayarları: squash merge açık, merge commit/rebase kapalı, birleşen branch'leri otomatik sil. Bu ayarlar tek başına main'e push'u engellemez.

## Kaynaklar

- https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/about-protected-branches
- https://docs.github.com/en/organizations/collaborating-with-groups-in-organizations/creating-a-new-organization-from-scratch
