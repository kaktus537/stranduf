# Strand UF

Webbsida för Strand UF — en frisörsalong driven inom Ung Företagsamhet.

Statisk sajt, ingen byggprocess. Öppna `index.html` i webbläsaren, eller kör en
lokal server för att slippa cache-strul:

```
python -m http.server 8000
```

## Sidor

| Fil | Sida |
| --- | --- |
| `index.html` | Startsida — om företaget, vad vi erbjuder, tjänstepriser |
| `boka.html` | Bokning via inbäddad cal.com-kalender |
| `priser.html` | Prislista på hårprodukter (endast visning, ingen beställning) |
| `css/style.css` | Gemensam stilmall för alla sidor |

## Koppla ihop bokningen med cal.com

1. Skapa ett konto på [cal.com](https://cal.com) och lägg upp era tjänster som
   *event types* (t.ex. "Klippning kort hår, 45 min").
2. Öppna `boka.html` och byt ut värdet längst ner i filen:

   ```js
   var CAL_LINK = "stranduf";
   ```

   Skriv ert eget användarnamn — `"stranduf"` visar alla tjänster, medan
   `"stranduf/klippning"` går direkt till en specifik tjänst.
3. Byt även ut de två `https://cal.com/stranduf`-länkarna i samma fil
   (reservlänkar om skriptet inte laddas).

Öppettider i cal.com styr vilka tider som går att boka — uppdatera dem där,
inte i koden.

## Innehåll att byta ut

Adress, telefonnummer, mejladress, org.nr och priser finns direkt i HTML-filerna
(sök på `Strandvägen`, `070 – 123 45 67` eller `hej@stranduf.se`).
