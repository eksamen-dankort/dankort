# Teknisk dokumentation for 2. semester eksamen  
Dette projekt er udviklet som et studieprojekt og er bygget i Astro med dynamisk indhold hentet fra Supabase via REST API. Formålet med denne README er at gøre projektet nemt at forstå og arbejde videre på, især når flere bidrager til samme kodebase.

## Projektstruktur:
Projektet følger Astro’s standardstruktur:

public/
images/ - billeder der kan tilgås direkte af sitet
src/
components/ - genanvendelige komponenter (fx Header/Footer/knapper/sektioner)
font/ - lokale fonte
layouts/ - layout-filer (fx Layout.astro)
pages/ - sidernes routede filer
index.astro - forside
forbrugspause.astro - konceptside
forms.astro - login/opret (eller formularside)
cafes/ - cafésider (oversigt + dynamiske detaljer, [id].astro)
styles/
global.css - fælles styling + CSS-variabler i :root

## Styling (global CSS)
Der bruges en fælles global.css med :root variabler til farver og typografi. Det gør det nemt at holde et konsistent udtryk og ændre tema uden at skulle rette mange steder i koden.

## Navngivning:
Dette punkt kan forbedres til næste gang, da vi ikke har navngivet filer og mapper konsekvent på engelsk, men har en lidt blandet struktur, hvilket ville kunne skabe unødig forvirring. 

## Git branches:
Vi har navngivet vores branches, efter hvad der er blevet arbejdet med i den individuelle branch og ikke hvem, der har arbejdet på den. 

## Commits:
Korte, beskrivende commits på engelsk.
Kan forbedres, da vi primært har skrevet på dansk, samt vi bør lave commits oftere, når noget virker.

## Samarbejde:
Undgå at arbejde i de samme filer samtidig (især under src/pages/).
Kommunikér merges/ændringer der påvirker andre.


## Funktionalitet:
Projektet indeholder bl.a.:
- Dynamisk cafédata fra Supabase
- Caféer hentes fra Supabase REST API og vises på sitet.

## Komponentbaseret opbygning
- UI er opdelt i genanvendelige komponenter for at holde kodebasen overskuelig.
- Global styling
- Farver/typografi styres centralt via global.css og :root.

## Supabase
- Supabase bruges som backend/databasen til caféindhold.
- Tabel: cafeFelter: id, created_at, name, description, img
- Cafédata hentes via Supabase REST API og bruges til at bygge både oversigt og (evt.) detaljesider.

# API endpoints
Dette afsnit skal liste de endpoints fra API'et i har benyttet:
- (fx. https://dummyjson.com/products)

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
| `npm run astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `npm run astro -- --help` | Get help using the Astro CLI                     |