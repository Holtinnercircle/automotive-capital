# Capital Automotive Berlin — Website

Läuft auf der eigenen Domain: **https://capital-automotive.de**

Jede Seite liegt in einem eigenen Ordner mit `index.html` → saubere URLs ohne `.html` (z. B. `capital-automotive.de/kontakt/`). Alle Pfade sind root-relativ (`/css/style.css`, `/images/...`), das funktioniert korrekt, sobald die Domain eingerichtet ist.

## ⚠️ So richtest du die eigene Domain bei GitHub Pages ein

Die Datei `CNAME` (liegt bereits im Root dieser ZIP, Inhalt: `capital-automotive.de`) sorgt dafür, dass GitHub Pages weiß, unter welcher Domain die Seite laufen soll. Zusätzlich musst du noch zwei Dinge selbst erledigen:

**1. DNS bei deinem Domain-Anbieter einrichten** (da, wo du `capital-automotive.de` gekauft/registriert hast — z. B. IONOS, Namecheap, denic-Partner etc.):

Für die nackte Domain (`capital-automotive.de` ohne `www`) vier A-Records anlegen, die auf GitHub zeigen:
```
A     @     185.199.108.153
A     @     185.199.109.153
A     @     185.199.110.153
A     @     185.199.111.153
```
Falls du zusätzlich `www.capital-automotive.de` willst, noch einen CNAME-Record:
```
CNAME   www   holtinnercircle.github.io.
```

**2. In den GitHub-Repo-Settings bestätigen:**
Settings → Pages → unter "Custom domain" `capital-automotive.de` eintragen (falls nicht schon durch die CNAME-Datei automatisch erkannt) → "Enforce HTTPS" aktivieren, sobald das Zertifikat ausgestellt wurde (kann nach DNS-Umstellung bis zu 24h dauern, meist aber schneller).

DNS-Änderungen brauchen manchmal ein paar Stunden bis sie überall greifen — falls die Seite nicht sofort unter der neuen Domain lädt, kurz Geduld haben.

## Struktur

```
/
├── CNAME                               → enthält "capital-automotive.de"
├── index.html                          → /
├── fahrzeuge/
│   ├── index.html                      → /fahrzeuge/
│   └── <slug>/index.html               → /fahrzeuge/<slug>/
├── marken/index.html                   → /marken/
├── ueber-uns/index.html                → /ueber-uns/
├── faq/index.html                      → /faq/
├── kontakt/index.html                  → /kontakt/
├── bewertungen/index.html              → /bewertungen/
├── impressum/index.html                → /impressum/
├── datenschutz/index.html              → /datenschutz/
├── agb/index.html                      → /agb/
├── css/style.css
└── images/  (alle Fahrzeugfotos + Logos + reviews/)
```

## Deployment

Kompletten Ordnerinhalt (inkl. der `CNAME`-Datei — die ist unsichtbar/leicht zu übersehen, aber wichtig!) 1:1 ins Root des Repos pushen/hochladen. Dann DNS wie oben beschrieben einrichten.

## Bekannte Lücke

Auf der Rolls-Royce-Ghost-Detailseite (`/fahrzeuge/rolls-royce-ghost/`) gibt es eine 4er-Bildergalerie, für die nie Fotos hochgeladen wurden (`Rolls-Royce-Ghost-Weiss-01.jpg` bis `-04.jpg`). War schon im Original so — die Hauptkachel ist vorhanden, nur die Zusatzgalerie fehlt.
