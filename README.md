# Capital Automotive Berlin — Website (finale Struktur)

Jede Seite liegt in einem eigenen Ordner mit `index.html` → saubere URLs ohne `.html` (z. B. `/kontakt/`). Alle Pfade sind absolut (`/css/...`, `/images/...`) und funktionieren dadurch auf jeder Ebene identisch — direkt so hochladbar auf GitHub Pages oder jeden anderen Webhost.

## Struktur

```
/
├── index.html                          Startseite (/)
├── fahrzeuge/
│   ├── index.html                      /fahrzeuge/
│   ├── lamborghini-revuelto-weiss/index.html
│   ├── lamborghini-revuelto-schwarz/index.html
│   ├── lamborghini-huracan-evo-spyder/index.html
│   ├── lamborghini-urus-performante/index.html
│   ├── ferrari-812-gts/index.html
│   ├── ferrari-sf90-spider/index.html
│   ├── ferrari-purosangue/index.html
│   ├── ferrari-12cilindri/index.html
│   ├── ferrari-296-gtb/index.html
│   ├── porsche-911-turbo-s/index.html
│   ├── porsche-911-gt3-rs/index.html
│   └── rolls-royce-ghost/index.html
├── marken/index.html                    /marken/
├── ueber-uns/index.html                 /ueber-uns/
├── faq/index.html                       /faq/
├── kontakt/index.html                   /kontakt/
├── bewertungen/index.html               /bewertungen/
├── impressum/index.html                 /impressum/
├── datenschutz/index.html               /datenschutz/
├── agb/index.html                       /agb/
├── css/
│   └── style.css
└── images/
    ├── logo-weiss.png, logo-schwarz.png
    ├── alle Fahrzeugfotos (hero.png, ferrari-*, lamborghini-*, porsche-*, rolls_royce-*...)
    └── reviews/
        ├── 296gtb-gelb.png
        ├── urus_perfomante-gelb.png
        └── rr-ghost-abgabe.mp4
```

## Status: vollständig ✅

Alle Bilder sind eingebunden, alle Links auf absolute Pfade umgestellt, alle Seiten haben eigene Ordner. Dieser Ordnerinhalt kann 1:1 als Root eines GitHub-Pages-Repos (oder jedes anderen Hostings) hochgeladen werden.

## Bekannte Lücke (unabhängig von der Umstrukturierung)

Auf der Rolls-Royce-Ghost-Detailseite (`/fahrzeuge/rolls-royce-ghost/`) gibt es eine Bildergalerie mit 4 Plätzen (`Rolls-Royce-Ghost-Weiss-01.jpg` bis `-04.jpg`), für die im Original nie Fotos hochgeladen wurden. Das war schon vor der Umstrukturierung so — die Haupt-Kachel (Seitenansicht) ist vorhanden, nur die zusätzliche Galerie fehlt. Falls gewünscht, einfach 4 Fotos mit genau diesen Dateinamen in `/images/` ablegen.

## Was sich geändert hat

- Jede Seite bekam einen eigenen Ordner mit `index.html` → saubere URLs ohne `.html`
- Alle internen Links, Nav, Footer, Dropdown-Menü, Buttons → absolute Pfade (`/kontakt/` statt `kontakt.html` bzw. `../kontakt.html`)
- Logos und alle Fahrzeugbilder zentral in `/images/` (inkl. `/images/reviews/`)
- CSS-Pfad auf `/css/style.css` umgestellt
- `marken.html#lamborghini` etc. → `/marken/#lamborghini` (Anker bleiben erhalten)
- Design, Inhalte, Texte, Preise, Funktionen (Buchungsformular, WhatsApp-Link, Reviews-Slider) unverändert

## Deployment auf GitHub Pages

1. Neues Repository anlegen (oder bestehendes nutzen)
2. Diesen kompletten Ordnerinhalt (alles, was hier liegt — `index.html`, `fahrzeuge/`, `css/`, `images/` usw.) direkt ins Root-Verzeichnis des Repos hochladen/pushen
3. In den Repo-Einstellungen unter „Pages" als Quelle den `main`-Branch (Root) auswählen
4. Fertig — GitHub Pages liefert `ordner/index.html` automatisch als `/ordner/` aus, die absoluten Pfade greifen direkt
