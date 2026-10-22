# Notion-Widgets

Eigene Nachbauten der drei Widgets auf der Notion-Seite „Mein HQ“. Begonnen am 22.10.2026.

Anlass: Die Originale liefen über apption.co und indify.co. Die beiden Aktien-Embeds von apption zeigten
am 22.10.2026 „You've reached free usage limit“. Die Nachbauten brauchen keinen solchen Zwischenanbieter.

| Datei | Ersetzt | Datenquelle |
|---|---|---|
| `wetter.html` | apption.co/embeds/de697f39 | Open-Meteo (kostenlos, ohne API-Schlüssel), alle 15 Minuten neu |
| `uhr.html` | indify.co Clock-Widget | keine, läuft lokal im Browser |
| `kurs.html` | apption.co/embeds/1a07bf09 und 260ffe86 | offizielles TradingView-Widget „Mini Symbol Overview“ |

## Parameter (an die URL anhängen)

**wetter.html**
- `name` – angezeigter Ort, Standard `Lichtenstein/Sa.`
- `lat`, `lon` – Koordinaten, Standard 50.757 / 12.631 (Lichtenstein/Sachsen)
- `theme=dark` – dunkle Darstellung

**uhr.html**
- `bg` – Hintergrundfarbe, z. B. `?bg=%23ffffff` (`%23` steht für `#`)
- `theme=dark`

**kurs.html**
- `symbol` – TradingView-Symbol, Standard `GETTEX:ALV` (Allianz)
- `range` – Zeitraum: `1D` (Standard), `1M`, `3M`, `12M`, `60M`, `ALL`
- `theme=dark`

Die zwei Kurs-Widgets aus dem Original:
- Allianz: `kurs.html?symbol=GETTEX:ALV`
- Bitcoin in Euro: `kurs.html?symbol=BITSTAMP:BTCEUR`

## Warum GETTEX statt Xetra

Getestet am 22.10.2026: Mit `XETR:ALV` zeigt das kostenlose TradingView-Widget nur den Kurs, der Chart bleibt
leer („Bisher noch keine Daten“). `GETTEX:ALV` und `TRADEGATE:ALV` liefern Kurs und Tageschart (12–21 Uhr).
GETTEX passt zum Bild des alten Widgets und zeigt zwei Nachkommastellen, Tradegate drei.

## Unterschiede zum Original

- Uhr: Datum auf Deutsch („Donnerstag | 22. Oktober 2026“), das Original war englisch.
- Wetter: zusätzlich Höchst- und Tiefstwert je Tag.

## In Notion einbinden

Notion bettet nur Seiten ein, die öffentlich per HTTPS erreichbar sind. Lokale Dateien gehen nicht.
Stand 22.10.2026: noch nicht gehostet.
