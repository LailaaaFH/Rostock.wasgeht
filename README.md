# Rostock.wasgeht

Veranstaltungskalender für Rostock: Was geht heute, diese Woche und im ganzen Jahr – von der KTV über die Südstadt bis Warnemünde.

## Inhalt

- `index.html` – die Homepage als einzelne Datei (HTML, CSS und JavaScript, ohne Build-Schritt)
  - **Diese Woche**: Tagesauswahl, Suche, Filter nach Kategorie und Stadtteil, Terminliste mit Haltestelle
  - **Jahreskalender** (`index.html#jahr`): Monatsansicht mit Terminbalken oder Listenansicht, gleiche Filter
  - **Termin eintragen**: Formular (noch nicht angebunden)
- `fonts/` – lokal eingebundene Schriften (Big Shoulders Display, Instrument Sans, JetBrains Mono) als WOFF2 mit `fonts.css`; Lizenz: SIL Open Font License 1.1 (`OFL-*.txt`). Es werden keine Schriften von Google-Servern geladen.

## Ansehen

`index.html` im Browser öffnen. Für GitHub Pages: Settings → Pages → Branch `main`, Ordner `/`.

## Termine

- `events.json` – alle Termine, gepflegt vom Prüfgremium (Sammler, Prüfer, Redaktion)
- Auf der Seite erscheinen nur Termine mit `"status": "gruen"`
- Testmodus: `?test=1` an die Adresse hängen, dann werden auch gelbe Termine (wartet auf Freigabe) angezeigt
- Optionale Felder: `datum_bis`, `wochentage` (0 = So … 6 = Sa), `nur_gerade_tage`, `zusatzdaten`, `abgesagt`

Lokal ansehen: Wegen `fetch` die Seite über einen kleinen Server öffnen (z. B. `python3 -m http.server`), nicht per Doppelklick.
