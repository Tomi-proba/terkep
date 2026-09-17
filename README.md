# Utazási idő / sebességkorlátozás-térkép

Hobbi projekt: megadod A és B pontot, az app kiszámolja az autós útvonalat, a sebességkorlátozás
szerint színezett szakaszokra bontja, és lehetővé teszi, hogy szakaszonként megadd a saját tempódat
— a végén összehasonlítja a hivatalos limittel számolt menetidőt azzal, amennyit a saját sebességeiddel
spórolnál (vagy vesztenél).

Egyetlen `index.html` fájl, build lépés nélkül. Használt szolgáltatások (mind ingyenes, kulcs nélküli):

- **Nominatim** — geokódolás (helynév/cím → koordináta)
- **OSRM** (`router.project-osrm.org` demó szerver) — útvonaltervezés
- **Overpass API** — OpenStreetMap `maxspeed` adatok
- **Leaflet** + **CARTO** csempék — térkép megjelenítés

## Futtatás

Nincs build lépés — egyszerűen nyisd meg az `index.html`-t böngészőben, vagy deployold statikus
oldalként (pl. Vercel, Netlify, GitHub Pages).

## Megjegyzés

Ez egy kedvtelésből épített, oktatási/hobbi célú eszköz, nem production-szintű. Ahol nincs
`maxspeed` adat az OSM-ben, az app "nincs adat"-ként jelzi és egy becsült sebességgel számol tovább,
nem akad el rajta.
