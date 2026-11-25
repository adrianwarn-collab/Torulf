# Instruktioner för Claude Code – Torulf

- Torulf är en träningsapp (PWA) för en 14-årig kille. Gränssnitt och texter på **svenska**, rak och peppande ton.
- Hela appen ligger i `index.html` (vanilla HTML/CSS/JS, inget ramverk, ingen byggprocess). Behåll det så.
- Säkerhet för ungdom: inga set under 6 reps, inga maxlyft, teknik före vikt, inga bantningsråd eller kalorital, inga kosttillskott.
- Data sparas i localStorage under nyckeln `torulf.v1`. Ändra aldrig formatet så att gammal data går förlorad – lägg till fält med standardvärden i `fresh()`.
- Användarinmatad text ska alltid gå genom `esc()` innan den hamnar i HTML.
- Höj `VERSION` i `sw.js` vid varje ändring som ska ut till mobilen.
- Testa i mobilstorlek (390×844) innan du är klar.
