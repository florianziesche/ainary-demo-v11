# Changelog

Alle Änderungen am Ainary Demo v10 Dashboard.

## [2026-02-22] Session 3 — Mia Intelligence + UX Polish

### Added
- **Mia Memory** — Merkt sich letzte 5 Seitenbesuche (nur page+timestamp). Begrüßung referenziert letzten Besuch mit kontextbezogenem Follow-up. Kein Inhalt gespeichert, kein DSGVO-Risiko.
- **Bookmarks** — Ainary-Dot (leerer Kreis → goldener Dot mit Glow). localStorage-basiert. Lesezeichen-Sektion auf Übersicht.
- **Verfügbare Analysen Karten** — 6 Karten auf Analyse-Seite mit Meta, Confidence, Aufwand.
- **CTA-Footer (shared)** — `cta-footer.js` auf allen Seiten. 3 kontextbezogene Related Analyses + dezenter Projekt-CTA.
- **Kontextbezogene Mia-Texte** — Intro-Message + Chips passen sich pro Seite an (Wirtschaft/Analyse/Projekte/Dokumente/Vergleich).
- **Klickbare Bold-Keywords** — `<strong>` in Mia-Nachrichten werden gold + dotted underline + Klick → sendChip().
- **"Analyse anfordern" Flow** — Alle CTA-Request-Links öffnen Mia. Mia fragt nach Firmenname, bestätigt 2 Werktage.

### Changed
- **Digital-Score → Digitalisierungs-Stufe** — 3 Stufen (Initial/Entwicklung/Etabliert) statt Zahlen. Vorreiter entfernt. Score-Balken aus Tabelle entfernt. Ordinalskala statt Pseudo-Intervallskala.
- **Dokumente aufgeräumt** — 6 echte Dokumente aktiv, 3 ausgegraut ("In Vorbereitung"). go-digital entfernt (Programm eingestellt).

### Removed
- Statische Mia-Duplikate auf projekte.html + dokumente.html
- Analyse-Gates (Blur/Paywall) auf allen 4 Analyse-Seiten
- Credit-System Referenzen (bereits in vorheriger Session)

### Fixed
- Mia nur noch 1x pro Seite (war 2x auf projekte + dokumente)

## [2026-02-22] Session 2 — Kommunalanalysen + Vergleich + Context-Aware Mia

### Added
- 5 Firmenanalysen (Nomos, Mühle, Lange, Gurofa, Löffler)
- 7 Kommunalanalysen (Glashütte, Dippoldiswalde, Jena, Marburg, Gersheim, Bad Belzig, Smart Region AUF)
- vergleich.html — 22 Kommunen Digitalisierungsvergleich
- Mia kontextbezogen auf 12 Seiten (Greeting, Info, Anschreiben, Weiterempfehlen)
- Report-Header mit Confidence, Beipackzettel, E/I/J/A, Quellenverzeichnis
- CTA-Split: "Analyse einsehen" (accent) vs "Analyse anfordern" (muted)
- methodik.html — Digital-Score Methodik dokumentiert

### Fixed
- Nichtbesetzungsquote: 49%/14 → 31%/9 (Demografieportal)
- 5 broken links (foerderdatenbank, alange-soehne, glashuhrg, smartcountry, smarte-regionen)
- UTF-8 encoding (perl zerstörte Umlaute, Python-Fix)
- Alle Quellenangaben vervollständigt (Titel + Organisation + Jahr + Link)

## [2026-02-21] Session 1 — v10 Initial

### Added
- Snapshot von v9 als v10 Baseline
- Wirtschaft page mit 3 Kategoriefiltern
- Gewerbe-Tabelle (18 Betriebe)
- Shared mia-chat.js + mia-chat.css
