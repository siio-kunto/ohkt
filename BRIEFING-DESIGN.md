# Briefing: Projekt ohkt — persönliche Webseite von Osi (oswaldkoenig.ch)

Für Claude-Design-Sessions. Stand: 28.07.2026.

## Was das Projekt ist

Osis persönliche Webseite als Squarespace-Ersatz. Statische Site, reines
HTML/CSS, kein Framework, kein Build-Schritt. Stand: V1 "Gewebe" (Juli 2026).

## Das Repo (Single Source of Truth)

- GitHub: https://github.com/siio-kunto/ohkt (öffentlich, Branch `main`)
- Struktur: `index.html` (Start), `osi.html`, `wirken.html`,
  `zusammenarbeit.html`, `spce.html`, `en.html`, `gedanken/index.html`,
  ein gemeinsames `style.css`
- Noch kein Hosting aktiv; geplant ist GitHub Pages
  (dann https://siio-kunto.github.io/ohkt/, später Domain oswaldkoenig.ch)

## Rollenverteilung (gleiches Modell wie bei Osis anderen Projekten)

- **Claude Chat**: Konzept & Texte. Hat die V1-Dateien erstellt.
- **Claude Design (du)**: Visuelles — Layout, Typografie, Farben, Redesigns.
  Deine Stärke ist die visuelle Zusammenarbeit mit Osi auf dem Canvas.
- **Claude Code**: Einzige Instanz mit Schreibzugriff aufs Repo. Arbeitet
  auf Osis Mac mit lokalem Clone (`~/dev/ohkt`) und authentifiziertem
  Git/GitHub-CLI. Integriert, committet, pusht, verwaltet
  Deployment und Repo-Einstellungen.

## Warum diese Aufteilung (Fähigkeiten, verifiziert Juli 2026)

Claude Design kann aus GitHub-Repos **importieren/lesen**, aber nicht
committen, pushen oder deployen — kein Schreibzugriff auf Repos, keine
Shell, kein Zugriff auf Osis Rechner. Claude Code kann all das, hat aber
keinen visuellen Canvas für die gemeinsame Design-Iteration mit Osi.
Darum: Design entwirft, Code integriert und betreibt. Single-Writer-
Prinzip — nur Claude Code schreibt ins Repo, das verhindert Konflikte
und hält die Historie sauber.

## Wie du an den aktuellen Stand kommst

1. **Bevorzugt**: GitHub-Import in Claude Design — Repo `siio-kunto/ohkt`
   importieren, dann hast du die echten Dateien als Grundlage.
2. **Ohne Import** (Repo ist öffentlich): Rohdateien abrufen, z.B.
   https://raw.githubusercontent.com/siio-kunto/ohkt/main/index.html
   bzw. `.../main/style.css` usw.

Arbeite IMMER vom aktuellen `main`-Stand aus, nie von einer Erinnerung
an frühere Versionen.

## Arbeitsanweisungen

1. Du hast KEINEN Schreibzugriff aufs Repo — das ist Absicht. Du lieferst
   Entwürfe an Osi, der Weg ins Repo läuft über die Claude-Code-Session.
2. Übergabe an Claude Code: bevorzugt über die eingebaute
   Claude-Code-Übergabe von Claude Design (bzw. HTML-Export). Alternativ
   komplette Dateien oder klar bezeichnete Abschnitte mit Datei- und
   Stellenangabe, damit Claude Code sie 1:1 übernehmen kann.
3. Respektiere die bestehende Struktur: relative Links zwischen den
   Seiten, ein gemeinsames `style.css`, keine externen Abhängigkeiten
   (keine CDNs; Webfonts nur wenn mit Osi abgesprochen).
4. Benenne bei jedem Entwurf, auf welchem Stand er basiert
   (z.B. "basiert auf main, V1 Gewebe").
