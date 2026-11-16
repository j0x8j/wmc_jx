# CSS-Selektoren

Ein CSS-Selektor ist wie eine **Adresse**: Er wählt die Elemente aus, die eine
Regel formatieren soll. Mit passenden Selektoren lässt sich oft die HTML-
Struktur nutzen, statt viele zusätzliche Klassen zu vergeben.

## Beispiele aus dem Selektoren-Labor

```css
.karte p  { color: #5b6478; } /* alle Absätze innerhalb einer Karte */
.karte > p { font-weight: bold; } /* nur direkte Absatz-Kinder */
```

Das Leerzeichen wählt Nachfahren beliebiger Tiefe, `>` nur direkte Kinder.
Mit `+` wählst du das direkt folgende Geschwister, mit `~` spätere Geschwister.

Struktur-Pseudoklassen wählen Elemente nach ihrer Position. `:nth-child()`
zählt alle Geschwister, `:nth-of-type()` nur Geschwister desselben Elementtyps:

```css
tbody tr:nth-child(odd) { background: #f1f3fb; } /* Zebra-Streifen */
tbody tr:last-child { border-left: 4px solid rebeccapurple; }
```

Auch Attribute und Zustände helfen beim gezielten Auswählen: `a[href$=".pdf"]`
trifft Links zu PDF-Dateien, `input:checked + label` das Label direkt nach
einem angehakten Eingabefeld. Mit `.kasten:has(img)` wählst du einen Kasten,
der ein Bild enthält; `p::first-letter` formatiert dagegen nur den ersten
Buchstaben eines Absatzes.

Treffen mehrere CSS-Regeln auf dasselbe Element, entscheidet die **Spezifität**:
IDs wiegen stärker als Klassen, Attribute und Pseudoklassen; diese wiegen
stärker als Elementnamen. Bei gleichem Gewicht gilt normalerweise die später
notierte Regel.

**Unterrichtseinheit:** [Lektion KM3-04 – CSS-Selektoren](https://github.com/georgernstgraf/GRG-WMC/blob/main/unterricht/KM3-04-css-selektoren/lesson.html).

**Aufgabe:** [KM3-04 – CSS-Selektoren](./KM3-04-css-selektoren/aufgabe.md) –  Tabellen, Listen und andere Elemente ohne zusätzliche Klassen passend auszuwählen und zu formatieren.
