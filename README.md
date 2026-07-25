# Capital Automotive Berlin — Website

Live unter: **https://holtinnercircle.github.io/automotive-capital/**

Jede Seite liegt in einem eigenen Ordner mit `index.html` → saubere URLs ohne `.html` (z. B. `/automotive-capital/kontakt/`). Alle Pfade sind fest auf den GitHub-Pages-Unterordner `/automotive-capital/` eingestellt.

## ⚠️ Wichtig: Base-Path fest verdrahtet

Diese Version ist speziell für die URL `https://holtinnercircle.github.io/automotive-capital/` gebaut. Alle Pfade beginnen mit `/automotive-capital/...`.

Falls sich der Repo-Name jemals ändert, oder eine eigene Domain (z. B. `capital-automotive-berlin.de`) eingerichtet wird, müssen alle Pfade entsprechend angepasst werden (Bescheid geben, dann baue ich das neu).

## Struktur

```
/
├── index.html                          → /automotive-capital/
├── fahrzeuge/
│   ├── index.html                      → /automotive-capital/fahrzeuge/
│   └── <slug>/index.html               → /automotive-capital/fahrzeuge/<slug>/
├── marken/index.html                   → /automotive-capital/marken/
├── ueber-uns/index.html                → /automotive-capital/ueber-uns/
├── faq/index.html                      → /automotive-capital/faq/
├── kontakt/index.html                  → /automotive-capital/kontakt/
├── bewertungen/index.html              → /automotive-capital/bewertungen/
├── impressum/index.html                → /automotive-capital/impressum/
├── datenschutz/index.html              → /automotive-capital/datenschutz/
├── agb/index.html                      → /automotive-capital/agb/
├── css/style.css
└── images/  (alle Fahrzeugfotos + Logos + reviews/)
```

## Deployment

Diesen kompletten Ordnerinhalt 1:1 ins Root des Repos `automotive-capital` pushen/hochladen (nicht in einen Unterordner). In den Repo-Settings unter „Pages" → Branch `main` / `/ (root)` auswählen. Nach 1–3 Minuten Build-Zeit ist die Seite unter der URL oben live.

## Bekannte Lücke

Auf der Rolls-Royce-Ghost-Detailseite (`/automotive-capital/fahrzeuge/rolls-royce-ghost/`) gibt es eine 4er-Bildergalerie, für die nie Fotos hochgeladen wurden (`Rolls-Royce-Ghost-Weiss-01.jpg` bis `-04.jpg`). War schon im Original so — die Hauptkachel ist vorhanden, nur die Zusatzgalerie fehlt.
