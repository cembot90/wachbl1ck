# Design-Schema für die Apps von Cem Aras

Gilt für YEM1N, Wachbl1ck und alle weiteren Apps. Vorbild ist YEM1N
(`YEM1N/Design.swift` für iOS, `docs/vorstellung.html` für das Web).
Damit sehen alle Apps aus wie aus einer Hand, auch wenn sie später unter
einem Gewerbe veröffentlicht werden.

## Farben

Zwei Farbwelten. Blau ist Standard, Rosa wählt man in den Einstellungen.
Im Web hängt die Farbwelt an `<html data-farbwelt="rosa">`.

| Rolle | Blau | Rosa | Wofür |
|---|---|---|---|
| tief | `#061230` | `#1d041d` | Seitenhintergrund, Kamerabühne |
| navy | `#0a1d48` | `#4a0f40` | Flächen, Dialoge, Schrift auf Gelb |
| karte | `#10295f` | `#5a1650` | Karten und Kacheln |
| karte-hoch | `#163473` | `#6b1d60` | Eingabefelder, aktive Flächen |
| linie | `rgba(214,226,255,.14)` | `rgba(255,214,240,.16)` | Rahmen, Trennlinien |
| text | `#f2f5ff` | `#fff3fa` | Haupttext |
| sanft | `#a7b4d6` | `#dcb6cf` | Nebentext |
| gelb (Akzent) | `#ffe100` | `#ff73bd` | Knöpfe, Hervorhebungen, Marke |
| glanz | `#2966d9` | `#eb4da8` | Lichtschein im Hintergrund |
| himmel | `#6cc4ff` | `#ccadff` | Links, Fokusrahmen, Datenreihe in Diagrammen |
| mint | `#5fe0b5` | gleich | Zustand gut |
| amber | `#ffb54d` | gleich | Zustand Achtung |
| koralle | `#ff6b6b` | gleich | Zustand Alarm |

Regeln:
- Gelb (bzw. Rosa) ist Akzent, nie Datenfarbe. Diagramme zeichnen in Himmel
  (bzw. Lavendel), damit sie sich klar von Amber und Koralle abheben.
  Geprüft mit dem Farbprüfer: Abstand bei Farbsehschwäche mindestens 11,7,
  bei normaler Sicht mindestens 18, Kontrast überall mindestens 3:1.
- Mint, Amber und Koralle sind Zustandsfarben und stehen immer mit Text
  oder Beschriftung, nie allein.
- Schrift auf Gelb, Mint, Amber oder Koralle ist Navy.
- Nur dunkel. Es gibt keinen hellen Modus.
- Glas-Effekte sind standardmäßig aus. Karten sind flach mit feiner Linie.

## Schriften

- Überschriften und große Zahlen: **Fredoka** 600 und 700
- Text: **Atkinson Hyperlegible** 400 und 700
- Beide sind eingebettet (woff2 als data-URI), damit nichts bei Google
  geladen wird. Lizenz: SIL Open Font License 1.1, Texte in `vendor/fonts`.
- Oberzeilen: Fredoka 600, Großbuchstaben, Sperrung 0,12em, in Gelb.

## Formen und Bausteine

- Rundungen: Karten 22 px, Felder 14 px, Knöpfe und Chips als Pille.
- Hauptknopf: gelbe Pille, Navy-Schrift, leichter gelber Schein.
- Nebenknopf: Pille in Kartenfarbe mit feiner Linie.
- Marke: Wortmarke in Großbuchstaben auf gelber Kachel
  (`.marke-kachel`, Radius 9 px), zum Beispiel `YEM1N`, `WACHBL1CK`.
- Kopfleiste: klebt oben, Tief mit 88 % Deckkraft und leichter Unschärfe.
- Startbereich (Held): Oberzeile, große Fredoka-Überschrift mit einem
  gelben Wort, kurzer Leittext, darunter Kennzahlen.
- Kennzahl: gelber Strich oben (3 px), große Fredoka-Zahl, Nebentext.
- Umschalter: Pillenleiste, gewählte Option gelb mit Navy-Schrift.
- Schritte und Aufzählungen: gelbe Nummernkachel bzw. gelber Punkt.
- Fokusrahmen: 3 px in Himmel.

## Texte

- Deutsch, einfache Sätze, keine Fachsprache.
- Keine Gedankenstriche. Minus ist ein normaler Bindestrich,
  Mal ist `·`, Geteilt ist `:`, Spannen mit „bis“.
- Knöpfe sagen genau, was passiert („Thema setzen“, „Verlauf löschen“).

## Datenschutz als Teil des Designs

- Nichts von Dritten laden (keine Schriften, kein Tracking).
- Speichern nur nach Zustimmung, Ablehnen gleich prominent wie Zustimmen.
- Impressum und Datenschutzerklärung in jeder App, Angaben wie bei YEM1N.
