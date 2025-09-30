---
jupytext:
  cell_metadata_filter: -all
  formats: ipynb,md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.14.5
kernelspec:
  display_name: Python 3 (ipykernel)
  language: python
  name: python3
---

# 2.2 Datentypen

```{admonition} Hinweise zur Vorlesung Objektorientierte Programmierung im WiSe 2025/26
:class: warning
Dieses Vorlesungsskript wird gerade umgebaut.
```

Mit Zahlen wird anders umgegangen, als mit Texten. Zahlen werden beispielsweise
addiert, bei Texten werden beispielsweise Kleinbuchstaben durch Großbuchstaben
ersetzt. Daher ist es nicht verwunderlich, dass Python für beide Arten von
Informationen eine andere technische Umsetzung verwendet. Das führt zu dem Thema
Datentypen und dem Speichern von Informationen in Variablen.

## Lernziele

```{admonition} Lernziele
:class: goals
* Sie wissen, was **Datentypen** sind.
* Sie kennen den Unterschied zwischen **Ganzzahlen** und **Fließkommazahlen**
  und die dazugehörigen Datentypen **Integer** und **Float**.
* Sie kennen den Datentyp **String**, der **Zeichenketten** repräsentiert.
* Sie können mit der Funktion **type()** den Datentyp einer Variable ermitteln.
```

## Datentypen in Python

Der Computer kann Informationen nur als 0 oder 1 verarbeiten. Auf dem
Speichermedium oder im Speicher selbst werden Daten daher als eine Folge von 0
und 1 gespeichert. Damit es für uns Programmiererinnen und Programmierer
einfacher wird, Daten zu speichern und zu verarbeiten, wurden Datentypen
eingeführt.  

**Datentypen** fassen gleichartige Objekte zusammen und stellen passende
Operationen zur Verfügung. Es hängt von der Programmiersprache ab, welche
Datentypen zur Verfügung stehen, wie diese im Hintergrund gespeichtert werden
und welche Operationen damit möglich sind. In diesem Kapitel beschäftigen wir
uns mit den einfachen Datentypen

* Integer
* Float
* String

### Zahlen (Integers und Floats)

In der Programmierung unterscheidet man grundsätzlich zwischen zwei Zahlenarten,
den **Ganzzahlen** und den Gleitkommazahlen, die auch **Fließkommazahlen**
genannt werden. Die Ganzzahlen werden in der Mathematik als ganze Zahlen
bezeichnet. In der Informatik wird meist der englische Begriff **Integer**
verwendet. Mit Integern können wir ganz normal rechnen, also Operationen
ausführen. Einige davon haben wir ja bereits ausprobiert, als wir Python als
Taschenrechner benutzt haben:

```{code-cell} ipython3
2 * (3 + 4)
```

Sobald wir eine Division vorliegen haben, die nicht aufgeht, verlassen wir den
Bereich der ganzen Zahlen und kommen automatisch zu den Fließkommazahlen. In der
Informatik wird eine Fließkommazahl als Float bezeichnet. Python rechnet
automatisch mit dem richtigen Datentyp, wie Sie hier sehen:

```{code-cell} ipython3
2/5
```

Beachten Sie bitte: Das Dezimaltrennzeichen ist ein Punkt, nicht ein Komma wie
im Deutschen. Aber ansonsten funktioniert alles wie erwartet:

```{code-cell} ipython3
2.3 + 4.6
```

```{code-cell} ipython3
1.4 - 5.2
```

```{code-cell} ipython3
(-3.8) * 3.1
```

```{code-cell} ipython3
2.4 / 0.3
```

```{code-cell} ipython3
2.5**10
```

Das folgende Video fasst Zahlen in Python zusammen.

```{dropdown} Video "Zahlen in Python" von Programmieren Starten
<iframe width="560" height="315" src="https://www.youtube.com/embed/VtiDkRDPA_c" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
```

### Strings

Daten sind aber sehr oft keine Zahlen. Beispielsweise könnte man sich
vorstellen, eine Einkaufsliste zu erstellen und diese im Computer oder in einer
Notiz-App auf dem Handy zu speichern. Eine solche Zeichenkette heißt in der
Informatik **String**. Mit Zeichen meint man dabei Zahlen, Buchstaben oder
andere wie beispielsweise `!"§$%&/()=?`.

Strings werden in Python durch einfache oder doppelte Anführungszeichen definiert:

```{code-cell} ipython3
"Dies ist ein String!"
```

Strings haben wir bei dem Hallo-Welt-Programm schon kennengelernt. Allerdings
haben wir zu diesem Zeitpunkt noch nicht den korrekten Fachbegriff String
verwendet, sondern sie als Texte bezeichnet.

Auf Strings und ihre Anwendungen kommen wir später noch zurück. Wenn Sie bereits
jetzt mehr erfahren wollen, können Sie sich folgendes Video ansehen.

```{dropdown} Video "Strings in Python" von Programmieren Starten
<iframe width="560" height="315" src="https://www.youtube.com/embed/sTEf4_mrLvw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
```

## Datentypen ermitteln mit type()

In den bisher betrachteten Beispielen sind die Python-Programme ein bis zwei
Zeilen lang. Unwahrscheinlich, dass dann nicht klar ist, welchen Datentyp eine
Variable hat. Wenn aber später die Programme länger werden und vielleicht auch
Benutzereingaben dazu kommen, kann man auch den Überblick darüber verlieren.
Dafür gibt es die **type()**-Funktion.

```{code-cell} ipython3
datentyp_integer = type(3)
print(datentyp_integer)

datentyp_float = type(3.1)
print(datentyp_float)

datentyp_string = type('Hallo')
print(datentyp_string)
```

## Weiteres Lernmaterial

Das folgende Video fasst die drei Datentypen Integer, Float uns String
übersichtsartig zusammen.

```{dropdown} Video "Datentypen in Python" von Programmieren Starten
<iframe width="560" height="315" src="https://www.youtube.com/embed/1WqFJ5wsA4o"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay;
clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
allowfullscreen></iframe>
```
