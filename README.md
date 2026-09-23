# oswaldkoenig.ch — V1 «Quipu»

Statische Website, kein Build-Schritt, keine Abhängigkeiten. HTML, CSS, ein bisschen JS.
Webfonts selbst gehostet (`assets/fonts/`), keine externen CDNs.

## Hosting & Domain

- **GitHub Pages** aus Branch `main`, Ordner `/ (root)` → Repo `siio-kunto/ohkt`
- **Custom Domain:** `oswaldkoenig.ch` (Datei `CNAME`), `www` leitet auf die Apex-Domain um
- **DNS:** Hostpoint. A-Records auf GitHub Pages (185.199.108–111.153), `www` als CNAME auf `siio-kunto.github.io`.
  MX bleibt bei Google Workspace. Nichts anderes anfassen.
- **HTTPS:** GitHub stellt das Zertifikat nach dem DNS-Umzug selbst aus (Minuten bis ~1h).
  Danach in Settings → Pages «Enforce HTTPS» aktivieren.

## Struktur

- `index.html` — Hauptschnur: Hero, die Stränge (5 + 3 eingeholte), «Gerade», Colophon
- `strang.html` — alle acht Strangseiten aus einer Datei; Inhalt als Daten in `STRAENGE`
  (dort pflegen, nicht im Markup). Adressierung per Hash: `strang.html#space` usw.
- `strang.html#buchen` — Buchung `<sp_ce>` (Cal.com-Inline-Embed, lazy geladen,
  Fallback-Link, Kurzfristig-Mail). Konfiguration von Verfügbarkeit und Kalender
  liegt in Cal.com, nicht hier.
- `404.html` — Kein Knoten an dieser Stelle; leitet bekannte alte Pfade auf den passenden Strang.
- `style.css` — Designsystem «Quipu» (Papier `#EEEDF5`, Newsreader / Hanken Grotesk / IBM Plex Mono)
- `assets/` — Kachelbilder, Porträt, Marken-Loop, Fonts
- `CNAME`, `.nojekyll` — Deploy-Steuerung für GitHub Pages

## Buchung `<sp_ce>`

Cal.com, Event `spce-monbijou/raum`. Öffentlicher Direktlink: https://cal.com/spce-monbijou/raum
Buchungen und manuelle Blocker laufen über den Google-Unterkalender «<sp_ce>» (hello@oswaldkoenig.ch).
Bezahlung per Twint oder Rechnung im Anschluss, nicht im Buchungsflow.

## Bewusst provisorisch

- `alt`-Felder in `STRAENGE` (Claim- und Namensvarianten) sind Arbeitsnotizen und werden nicht gerendert
- Archiv der V1 «Gewebe» (2018er-Ablösung, erster Wurf) liegt lokal unter `V0.1/archiv-gewebe/`, nicht im Deploy
