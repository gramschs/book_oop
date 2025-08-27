---
jupytext:
  formats: ipynb,md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.13.8
kernelspec:
  display_name: Python 3 (ipykernel)
  language: python
  name: python3
---

# 8.3 OOP in der Praxis

```{admonition} Hinweise zur Vorlesung Objektorientierte Programmierung im WiSe 2025/26
:class: warning
Dieses Vorlesungsskript wird gerade umgebaut.
```

Mit Klassen, Objekten und Methoden haben wir die Grundlagen der objektorientierten Programmierung kennengelernt. In diesem Kapitel schauen wir uns an, wie wir diese Konzepte in der Praxis anwenden: Wir verwalten mehrere Objekte in Listen und sorgen dafür, dass unsere Objekte sich schön ausgeben lassen.

## Lernziele

```{admonition} Lernziele
:class: goals
* Sie können Objekte in Listen speichern und verwalten.
* Sie können Listen von Objekten durchlaufen und durchsuchen.
* Sie verstehen die `__str__`-Methode und können sie implementieren.
* Sie können ein vollständiges objektorientiertes Programm zur Datenverwaltung erstellen.
* Sie verstehen, wie OOP bei der Lösung praktischer Probleme hilft.
```

## Konzept

TODO: Einleitungstext über die Bedeutung von Listen von Objekten in der Praxis. Beispiel aus dem Alltag (Kursverwaltung an der Hochschule). Überleitung zu den drei Hauptthemen des Kapitels.

```{dropdown} Video zu "Listen von Objekten" von Programmieren lernen
TODO: Passendes Video suchen oder eigenes erstellen
```

## Listen von Objekten verwalten

TODO: Erklärender Text über die Notwendigkeit, mehrere Objekte zu verwalten. Vergleich zu bisherigen Ansätzen (viele einzelne Variablen vs. Listen von Objekten).

### Objekte in Listen speichern

TODO: Grundlegendes Beispiel - mehrere Student-Objekte in einer Liste erstellen.

```{code-cell} ipython3
# TODO: Code-Beispiel für das Erstellen einer Liste mit mehreren Student-Objekten
class Student:
    def __init__(self, nachname, vorname, studiengang, semester, matrikelnummer):
        self.nachname = nachname
        self.vorname = vorname
        self.studiengang = studiengang
        self.semester = semester
        self.matrikelnummer = matrikelnummer

# Liste mit mehreren Studierenden erstellen
studierende = [
    Student("Abendrot", "Anna", "Maschinenbau", 3, "12345678"),
    Student("Berliner", "Bob", "Maschinenbau", 5, "87654321"),
    Student("Colorado", "Charlie", "Elektrotechnik", 2, "11223344")
]

print(f"Anzahl Studierende: {len(studierende)}")
```

### Listen von Objekten durchlaufen

TODO: Erklärung, wie man mit for-Schleifen über Listen von Objekten iteriert.

```{code-cell} ipython3
# TODO: Code-Beispiel für das Durchlaufen einer Liste von Objekten mit for-Schleife
```

### Objekte in Listen suchen und filtern

TODO: Praktische Beispiele für das Suchen nach bestimmten Objekten in Listen.

```{code-cell} ipython3
# TODO: Code-Beispiele für:
# - Suche nach Student mit bestimmtem Namen
# - Filtern nach Studiengang
# - Filtern nach Semester
```

```{admonition} Mini-Übung
:class: miniexercise
TODO: Übung zum Filtern von Objektlisten - z.B. "Finden Sie alle Studierenden im 1. Semester"
```

```{code-cell} ipython3
# Geben Sie nach diesem Kommentar Ihren Code ein:

```

````{admonition} Lösung
:class: miniexercise, toggle
```python
# TODO: Musterlösung für die Mini-Übung
```
TODO: Erklärung der Lösung
````

## Die __str__-Methode für schöne Ausgabe

TODO: Problemstellung - was passiert, wenn wir `print(objekt)` ohne `__str__`
aufrufen? Kryptische Ausgabe zeigen.

### Das Problem: Kryptische Objektausgabe

```{code-cell} ipython3
# TODO: Beispiel zeigen, wie Objekte ohne __str__ ausgegeben werden
```

### Die Lösung: Die __str__-Methode implementieren

TODO: Erklärung, was `__str__` ist und warum Python diese Methode automatisch aufruft.

```{code-cell} ipython3
# TODO: Student-Klasse um __str__-Methode erweitern
```

### Vergleich: mit und ohne __str__

TODO: Direkter Vergleich der Ausgabe mit und ohne `__str__`-Methode.

```{code-cell} ipython3
# TODO: Code-Beispiel, das den Unterschied deutlich macht
```

### Best Practices für benutzerfreundliche Ausgabe

TODO: Richtlinien für gute `__str__`-Implementierungen (kurz, informativ, lesbar).

```{admonition} Mini-Übung
:class: miniexercise
TODO: Übung zur Implementierung einer `__str__`-Methode
```

```{code-cell} ipython3
# Geben Sie nach diesem Kommentar Ihren Code ein:

```

````{admonition} Lösung
:class: miniexercise, toggle
```python
# TODO: Musterlösung
```
TODO: Erklärung
````

## Ein vollständiges Beispiel: Kursverwaltung

TODO: Zusammenführung aller gelernten Konzepte in einem praktischen Beispiel.

### Die vollständige Student-Klasse

```{code-cell} ipython3
# TODO: Komplette Student-Klasse mit allen bisher gelernten Methoden und __str__
```

### Kursverwaltung implementieren

TODO: Praktische Funktionen für eine einfache Kursverwaltung.

```{code-cell} ipython3
# TODO: Code für:
# - Studierende hinzufügen
# - Studierende anzeigen
# - Nach Studiengang filtern
# - Statistiken erstellen (Anzahl pro Semester, etc.)
```

### Praktische Operationen

TODO: Beispiele für typische Verwaltungsaufgaben.

```{code-cell} ipython3
# TODO: Beispiele für:
# - Alle Studierenden eines Studiengangs anzeigen
# - Durchschnittliches Semester berechnen
# - Studierende nach Namen sortieren
```

## Zusammenfassung und Ausblick

TODO

* Listen von Objekten sind ein mächtiges Werkzeug zur Datenverwaltung
* Die `__str__`-Methode macht Objekte benutzerfreundlich
* OOP hilft dabei, komplexe Datenstrukturen übersichtlich zu verwalten
* Diese Konzepte sind die Grundlage für viele Data Science-Werkzeuge

```{dropdown} Video zu "Klassen und Objekte" von Programmieren lernen
<iframe width="560" height="315" src="https://www.youtube.com/embed/XxCZrT7Z3G4" 
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; 
clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen>
</iframe>
```

```{dropdown} Video zu "Der self Parameter" von Programmieren lernen
<iframe width="560" height="315" src="https://www.youtube.com/embed/CLoK-_qNTnU" 
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; 
clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen>
</iframe>
```

```{dropdown} Video zu "Methoden in Klassen" von Programmieren lernen
<iframe width="560" height="315" src="https://www.youtube.com/embed/58IjjwHs_4A" 
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; 
clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen>
</iframe>
```
