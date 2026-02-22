# Ainary Demo v10 — Glashütte Kommune Dashboard

**Live:** [florianziesche.github.io/ainary-demo-v11](https://florianziesche.github.io/ainary-demo-v11/)

KI-gestütztes Verwaltungsdashboard für die Gemeinde Glashütte (Sachsen). Demonstriert, wie ein persönlicher KI-Assistent ("Mia") Bürgermeistern bei Verwaltung, Wirtschaftsförderung und Fördermittelrecherche hilft.

## Architektur

```
index.html          Übersicht (KPIs, Lesezeichen, Analysen)
analyse.html        Personalanalyse (Unit Charts, Evidence Chain)
projekte.html       6 KI-Anwendungen für Verwaltung
dokumente.html      Präsentationen, Analysen, Methodik
wirtschaft.html     167 Unternehmen, 3 Kategoriefilter

vergleich.html      22 Kommunen Digitalisierungs-Stufen
methodik.html       Confidence-Modell, E/I/J/A, Digital-Score

analyse-*.html      12 Einzelanalysen (5 Firmen, 7 Kommunen)
  ├── analyse-nomos, -muehle, -lange, -gurofa, -loeffler
  └── analyse-glashuette, -dippoldiswalde, -jena, -marburg,
      -gersheim, -badbelzig, -smartregion-auf

Shared Assets:
  mia-chat.js       Kontextbezogener KI-Assistent (20KB)
  mia-chat.css      Mia Styling
  bookmarks.js       Lesezeichen (localStorage, kein Server)
  cta-footer.js      Related Analyses + Projekt-CTA (auto-inject)
```

## Features

- **Mia KI-Assistent** — Kontextbezogene Begrüßung, Memory (letzte 5 Seitenbesuche), klickbare Bold-Keywords, seitenspezifische Chips
- **Bookmarks** — Ainary-Dot (gold/glow), localStorage, Lesezeichen-Sektion auf Übersicht
- **12 Einzelanalysen** — Report-Header mit Confidence, Beipackzettel, E/I/J/A Tags, Quellenverzeichnis
- **Digitalisierungs-Stufen** — 3-stufige Ordinalskala (Initial/Entwicklung/Etabliert), DESI/CMMI-basiert
- **Cross-Linking** — Kontextbezogene Related Analyses auf jeder Seite
- **Anschreiben-Generator** — BM→Firma Briefvorlagen mit Fördermittel-Referenzen
- **Weiterempfehlen** — Viraler Loop: BM→Nachbar-BM E-Mail-Template

## Design System

| Token | Wert | Verwendung |
|-------|------|------------|
| `--text` | `#1a1a1a` | Primärtext |
| `--accent` | `#9d7f3b` | Gold, CTAs, Ainary-Dot |
| `--surface` | `#fafafa` | Kartenhintergrund |
| `--f` | `Inter` | UI-Font |
| `--m` | `JetBrains Mono` | Daten, KPIs, Meta |

**Light/Cream für BM-Audience.** Keine Dark-Mode-Elemente.

## E/I/J/A Labeling

| Tag | Bedeutung | Regel |
|-----|-----------|-------|
| **E** | Evidence — belegt durch Quelle | > 50% pro Report |
| **I** | Inference — abgeleitet aus Daten | Herleitung angeben |
| **J** | Judgment — Einschätzung | < 20% pro Report |
| **A** | Assumption — Annahme, unbelegt | Minimieren |

## Datenschutz

- **Kein Backend.** Statisches HTML/CSS/JS auf GitHub Pages.
- **Kein Tracking.** Keine Cookies, kein Analytics.
- **localStorage** nur für Bookmarks (Seitenname) und Mia-Memory (Seitenname + Timestamp). Keine Inhalte, keine Eingaben.

## Quellen

Alle Zahlen mit Quellenangabe. Quellenverzeichnis auf jeder Analyse-Seite. Methodik dokumentiert auf `methodik.html`.

Hauptquellen: Demografieportal des Bundes (2024), DIHK Ausbildungsumfrage (2025), McKinsey GenAI Public Sector (2024), IW-Consult KI-Potenzialanalyse (2024), dbb Beamtenbund (2023), KGSt/Fraunhofer FOKUS (2024).

## Deployment

```bash
git push origin main  # GitHub Pages auto-deploys
```

## Kontakt

Florian Ziesche · [florian@ainaryventures.com](mailto:florian@ainaryventures.com) · [ainaryventures.com](https://ainaryventures.com)

---
© 2026 Ainary
