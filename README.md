# RKN Motors — website

De website van RKN Motors (Waasmunster). Statische site, gehost via GitHub Pages.

## Structuur

| Pad | Inhoud |
| --- | --- |
| `index.html` | De volledige site: HTML, CSS en JavaScript in één bestand |
| `stock.json` | De wagens in stock — merk, model, prijs, status, specificaties en fotolijst |
| `fotos/<wagen>/` | Foto's per wagen: `01.jpg` … (groot) en `t01.jpg` … (thumbnail) |
| `img/` | Panden, sfeerbeelden en de oudere fotosets |
| `vid/` | Video's voor de dienstenpanelen (import, detailing, studio) |

## Een wagen toevoegen of aanpassen

Alles staat in `stock.json`. Eén wagen ziet er zo uit:

```json
{
  "id": "c11",
  "merk": "Volkswagen",
  "model": "Golf 1.5 TSI",
  "type": "Hatchback",
  "jaar": 2021,
  "km": 64000,
  "brandstof": "Benzine",
  "bak": "Manueel",
  "prijs": 18500,
  "status": "te koop",
  "len": 0.86,
  "pluspunten": ["12 maanden garantie"],
  "info": [["Eerste inschrijving", "03/2021"]],
  "uitrusting": ["Airco"],
  "fotos": [
    { "src": "fotos/vw-golf/01.jpg", "thumb": "fotos/vw-golf/t01.jpg", "alt": "Vooraanzicht" }
  ]
}
```

- `status` is `te koop`, `binnenkort` of `verkocht`
- `prijs` is een getal zonder euroteken, of `null` als er nog geen prijs is
- `len` bepaalt hoe breed de getekende wagen op de kaart staat (0,76 tot 0,92)
- Zet de foto's in een nieuwe map onder `fotos/` met zowel een grote als een thumbnail-versie

## Publiceren

Elke push naar `main` zet de site automatisch live via GitHub Pages. Een wijziging staat
doorgaans binnen één à twee minuten online.
