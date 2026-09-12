# Strand UF

Enkel hemsida för Strand UF — klippning med utkörning i Kalix.

## Innehåll

- `index.html` — startsida: erbjudandet (hembesök 250 kr) och äldreboenden
- `boka.html` — bokning via inbäddad cal.com-kalender
- `css/style.css` — gemensam stilmall

## Att fylla i

- **Telefon och mejl** — placeholders `070 – 123 45 67` och `hej@stranduf.se`
  finns i sidfoten på båda sidorna.
- **cal.com** — variabeln `CAL_LINK` längst ner i `boka.html`.
- **Loggan** — startsidan ritar loggan som SVG. Vill ni använda originalfilen,
  lägg den som `images/logo.png` och byt ut `<svg class="mark">`-blocket mot
  `<img class="mark" src="images/logo.png" alt="Strand UF">`.

## Kör lokalt

Öppna `index.html` i webbläsaren, eller kör en lokal server:

```
python -m http.server 8000
```
