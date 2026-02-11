# TeInvit – Production Codebase

Acest repository reprezintă codul custom utilizat în producție pentru site-ul https://teinvit.com.

Conținutul repo-ului este export 1:1 din mediul de producție și include:

- Plugin custom WordPress: `teinvit-core`
- Serviciu PDF bazat pe Puppeteer: `server.js`

Tema activă în producție este `Twenty Twenty-Four`.
Tema NU conține logică relevantă pentru randarea invitației, preview sau generarea PDF.

---

## Arhitectură generală

Pipeline-ul de randare este JS-first și trebuie păstrat ca atare.

Invitația trebuie să se afișeze identic în toate mediile:

- Preview din pagina de produs
- `/i/{token}`
- `/pdf/{token}`
- PDF final generat prin Puppeteer

Obiectiv obligatoriu: paritate vizuală 1:1 între HTML și PDF.

---

## Reguli de dezvoltare (nenegociabile)

1. Nu se modifică arhitectura JS-first.
2. Nu se introduce logică separată între preview, /i, /pdf și PDF.
3. Nu se afectează comportamentul pe mobile.
4. Nu se introduce drift vizual între HTML și PDF.
5. Nu se modifică ordinea blocurilor invitației.
6. Logica WAPF se modifică doar dacă este absolut necesar și justificat.

---

## Mod de lucru

- Orice modificare se face prin branch nou.
- PR obligatoriu înainte de merge în `main`.
- `main` este branch protejat.
- Codul trebuie analizat în raport strict cu fișierele existente în acest repository.
- Nu se utilizează alte repo-uri ca sursă de adevăr.

---

Acest repository este singura sursă validă pentru dezvoltările viitoare ale proiectului TeInvit.
