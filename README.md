# Strand UF

Enkel hemsida för Strand UF — klippning med utkörning i Kalix.

## Innehåll

- `index.html` — startsida: logga, pris, äldreboenden och länk till produkterna
- `produkter.html` — hårprodukter med bild och pris
- `boka.html` — bokning via inbäddad cal.com-kalender
- `css/style.css` — gemensam stilmall

## Att fylla i

- **Telefon och mejl** — placeholders `070 – 123 45 67` och `hej@stranduf.se`
  finns i sidfoten på båda sidorna.
- **cal.com** — variabeln `CAL_LINK` längst ner i `boka.html`.
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
