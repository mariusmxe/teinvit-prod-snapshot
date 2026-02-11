# TeInvit – Sursa unică de adevăr (Production Snapshot)

Acest repository (`teinvit-prod-snapshot`) este exportul 1:1 al codului din producție (teinvit.com).

Conținut:
- Plugin custom: `teinvit-core` (toate fișierele sunt la root în acest repo pentru ușurința analizelor)
- Serviciu PDF Puppeteer: `server.js`

Important:
- Nu există logică în tema WordPress (folosim Twenty Twenty-Four).
- Orice dezvoltare nouă se face DOAR prin PR-uri în acest repo (main protejat).
- Repo-urile vechi (`teinvit-audit`, `teinvit-audit-shadow`) sunt doar istorice/backup și NU reprezintă sursa curentă.
