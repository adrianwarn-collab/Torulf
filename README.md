# Torulf

Träningsapp för en 14-åring: veckoprogram efter valda dagar (gym eller hemma med kroppsvikt/kettlebell), övningsbank, egna övningar och pass, guidad uppvärmning och stretch, fullt/kort/lätt pass, märken, sömn/vatten/mat och en veckorapport till pappa.

Hela appen är en enda fil (`index.html`) – ingen byggprocess behövs.

## Publicera gratis (enklast)
1. Packa upp `torulf-app.zip` så att du får mappen `torulf-app`.
2. Gå till https://app.netlify.com/drop och dra in mappen.
3. Öppna adressen du får i **Safari** på sonens iPhone → Dela → **Lägg till på hemskärmen**.

(Skapa gärna ett gratis Netlify-konto så att adressen inte försvinner och du kan uppdatera samma sida senare.)

## Uppdatera appen
1. Ändra filerna.
2. Höj `VERSION` i `sw.js` (t.ex. `torulf-v2`) – annars kan mobilen visa den gamla versionen.
3. Dra in mappen igen på samma Netlify-sida (Deploys → dra och släpp).

## Struktur
- `index.html` – hela appen: övningsbank (`BANK`), passmallar (`TPL`), uppdelningar (`SPLIT`), rep-scheman (`SCHEMES`), tips (`TIPS`), uppvärmning/stretch (`ROUT`), märken (`BADGES`), veckorapport (`report()`).
- `sw.js` – gör att appen fungerar utan nät.
- `manifest.webmanifest` + `icons/` – namn och ikon på hemskärmen.

## Data
Allt sparas lokalt i mobilen (localStorage). Under Logg → Säkerhetskopia kan han spara en backupfil, t.ex. i iCloud Drive, och läsa in den på en ny mobil.

## Testa lokalt
```
python -m http.server 8000
```
Öppna http://localhost:8000
