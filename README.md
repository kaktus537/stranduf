# Strand UF

Enkel hemsida för Strand UF — klippning med utkörning i Kalix.

## Innehåll

- `index.html` — startsida: logga, pris, gruppboenden och länk till produkterna
- `gruppboenden.html` — info för gruppboenden + kontaktvägar (mejl, telefon, Instagram)
- `produkter.html` — hårprodukter med bild och pris
- `boka.html` — bokning via inbäddad cal.com-kalender
- `css/style.css` — gemensam stilmall

## Att fylla i

- **Kontaktuppgifter** — klart. Telefon `072-531 2600`, mejl `Strand.uf@gmail.com`,
  Instagram `@strand.uf` och adressen Flygfältsvägen 35, Kalix finns i sidfoten på
  alla sidor och i kontaktkorten på `gruppboenden.html`.
- **Priser** — 280 kr med utkörning, 250 kr om kunden kommer till Flygfältsvägen 35.
- **cal.com** — klart. `CAL_LINK` längst ner i `boka.html` pekar på
  `harklippning` (dvs. https://cal.com/harklippning). Byter ni eventtyp är det den
  variabeln som ska ändras.
- **Produkterna** — `produkter.html` innehåller sex platshållarkort. Byt namn och
  pris, lägg produktbilderna i `images/produkter/` och peka om `src` på varje
  `<img>`. Kopiera ett `<article class="product">`-block för att lägga till fler.
- **Loggan** — startsidan visar originalloggan, oredigerad. Spara logotypfilen
  som `images/logo.png` så syns den på startsidan. Är filen en jpg heter den
  `images/logo.jpg` — ändra då `src` i `index.html` till det.

## Kör lokalt

Öppna `index.html` i webbläsaren, eller kör en lokal server:

```
python -m http.server 8000
```

## Gruppboenden

Gruppboenden bokar **inte** via cal.com-kalendern. `gruppboenden.html` förklarar
hur det går till och listar de tre kontaktvägarna. Länkar dit finns i menyn, som
en banner på startsidan, i raden «Klippning på gruppboenden» och överst på
`boka.html`.


## SEO

Adressen `https://stranduf.se` är inbakad på flera ställen. Byter ni domän måste
den bytas i `sitemap.xml`, `robots.txt`, `CNAME` och i varje sidas `<head>`
(`canonical`, `og:url`, `og:image` och den strukturerade datan på startsidan).

- **Varje sida** har egen `<title>`, `description`, `canonical` och
  Open Graph-taggar (rubrik och logga när länken delas i sociala medier).
- **`sitemap.xml`** listar de fem sidorna. Lägg till nya sidor här och uppdatera
  `lastmod` när en sida ändras.
- **`robots.txt`** släpper in alla sökmotorer och pekar på sitemapen.
- **`CNAME`** talar om för GitHub Pages att sidan ligger på `stranduf.se`.
- **`404.html`** visas vid felaktig adress och är märkt `noindex`.
- **Strukturerad data** (JSON-LD) i `index.html` beskriver företaget för Google:
  adress, telefon, Instagram och de tre priserna. Ändras priser eller
  kontaktuppgifter ska de ändras där också. Övriga sidor har brödsmulor.

Efter publicering: lägg till sidan i [Google Search Console](https://search.google.com/search-console)
och skicka in `https://stranduf.se/sitemap.xml`. Skapa gärna även en
Google Företagsprofil — för lokala sökningar som «frisör Kalix» väger den tyngst.
