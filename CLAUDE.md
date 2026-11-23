# WACHBL1CK: Arbeitsregeln

Müdigkeitserkennung per Webcam für Cem. Eine einzige Datei `wachbl1ck.html`
(HTML, CSS und JavaScript), dazu `vendor/` mit MediaPipe, Gesichtsmodell und
Schriftlizenzen. Kein Build. Veröffentlicht über GitHub Pages:
https://cembot90.github.io/wachbl1ck/ (`index.html` leitet auf die App weiter).
Abschnitt 6 der Datenschutzerklärung beschreibt GitHub als Hoster.

## Feste Regeln

- Design nach `DESIGN.md` (wie YEM1N): Navy und Gelb, Rosa als Farbwelt,
  Fredoka und Atkinson Hyperlegible eingebettet, Glas-Effekte aus, nur dunkel.
- Keine Gedankenstriche, weder im Code noch in Texten noch in Commit-Nachrichten.
- Texte auf Deutsch, einfach und ohne Fachjargon.
- Nichts von Dritten laden, außer der Erkennungsbibliothek nach Einwilligung,
  wenn `vendor/` fehlt. Keine Google Fonts, kein Tracking.
- Speichern nur nach Zustimmung. Impressum und Datenschutz mit den Angaben
  wie bei YEM1N (Cem Aras, Selters). Neue gespeicherte oder übertragene
  Daten immer auch in der Datenschutzerklärung nachtragen.
- Exporte bleiben abwärtskompatibel: neues Format bekommt eine neue
  `format`-Nummer, ältere Dateien müssen sich weiter einlesen lassen.
  Interne Schlüssel (`wachblick.*`, `wachblick-verlauf`, `app: "wachblick"`)
  nicht umbenennen.
- Kein Medizinprodukt: keine Aussagen wie „verhindert Unfälle“ oder
  „erkennt Schlafstörungen“.

## Prüfen

Es gibt keine Testsuite im Repo. Vor jeder Änderung im Browser prüfen
(Playwright mit simulierter Kamera), Demo ohne Kamera, Verlauf mit
Beispieldaten, Handybreite 390 px ohne seitliches Scrollen.

## Offen

- Teams-Anrufe automatisch erkennen: Eine Webseite sieht Teams nicht. Möglich
  wären die lokale Geräte-Schnittstelle von Teams (ws://localhost:8124,
  inoffiziell, muss in Teams unter Datenschutz > API verwalten erlaubt sein)
  oder Microsoft Graph Presence (braucht eine App-Registrierung in Entra ID).
  Stand 23.11.2026: "API verwalten" ist bei Cem gesperrt, die lokale
  Schnittstelle fällt damit weg. Graph ginge nur über die IT. Bis dahin gibt
  es die Pause per Klick (`startPause`/`resumePause`), an die eine
  Erkennung später angeschlossen werden kann.
- Grenzwerte (2 Minuten weg, 1 Minute Blick weg, Index 30) sind erste
  Annahmen und sollen nach echter Nutzung angepasst werden.
