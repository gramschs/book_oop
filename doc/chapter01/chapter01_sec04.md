---
jupytext:
  cell_metadata_filter: -all
  formats: ipynb,md:myst
  main_language: python
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

# Übungen

```{admonition} Übung 1.1
:class: miniexercise
Installieren Sie Anaconda auf Ihrem System. Starten Sie JupyterLab und erstellen
Sie ein neues Notebook. Bei Problemen konsultieren Sie die
Installationsanleitung im nächsten Kapitel.
```

```{admonition} Übung 1.2
:class: miniexercise 
Benutzen Sie Python als Taschenrechner. Fügen Sie dazu diesem Jupyter Notebook
eine Code-Zelle hinzu und lassen Sie die folgenden Ausdrücke berechnen:
* 2 + 3
* 2 - 3
* 4 * 5
* 16 / 4
* 16 / 3
* 5**2
```

```{admonition} Übung 1.3
:class: miniexercise
In der vorhergehenden Aufgabe haben Sie den Ausdruck `5**2` berechnen lassen.
Fügen Sie jetzt eine Markdown-Zelle ein. Schreiben Sie auf, was Ihrer Vermutung
nach der `**`-Operator für eine Bedeutung hat. Recherchieren Sie anschließend im
Internet, nach seiner Bedeutung und vergleichen Sie Ihre Antwort mit der Recherche.
Fügen Sie die Internetseite als URL in die Markdown-Zelle ein.
```

```{admonition} Übung 1.4
:class: miniexercise
Speichern Sie das bearbeitete Jupyter Notebook unter einem anderen Namen ab.
```

```{admonition} Übung 1.5
:class: miniexercise
Probieren Sie bewusst falsche Python-Anweisungen aus und beobachten Sie die
Fehlermeldungen:
* Geben Sie `print(Hallo Welt)` ein (ohne Anführungszeichen)
* Versuchen Sie `2 +* 3` (falsche Operatorenkombination)
* Schreiben Sie `Print(5)` (großes P) Notieren Sie in einer Markdown-Zelle,
welche Fehlermeldungen erscheinen und was sie bedeuten könnten.
```

````{admonition} Übung 1.6
:class: miniexercise
Erstellen Sie eine Code-Zelle mit folgendem Inhalt:
```python
# Das ist ein Kommentar
print(7 + 3)  # Hier wird 7 + 3 berechnet
# print(5 * 2)
print(8 - 2)
```
Führen Sie die Zelle aus. Erklären Sie in einer Markdown-Zelle, warum manche
Zeilen ausgeführt werden und andere nicht.
````

```{admonition} Übung 1.7
:class: miniexercise
Berechnen Sie folgende Ausdrücke und vergleichen Sie die Ergebnisse:
* `2 + 3 * 4`
* `(2 + 3) * 4`
* `2**3*4`
* `2**(3*4)`
Schreiben Sie in eine Markdown-Zelle, welche Regeln Python für die Reihenfolge
der Operationen befolgt.
```

```{admonition} Übung 1.8
:class: miniexercise
Experimentieren Sie mit der print()-Funktion:

* `print("Mein Name ist", "Max")`
* `print("Das Ergebnis ist:", 5*6)`
* `print(2, 4, 6, 8)`
Was beobachten Sie, wenn print() mehrere Argumente erhält?
```

```{admonition} Übung 1.9
:class: miniexercise
Berechnen Sie mit Python typische Ingenieursaufgaben:

* Den Umfang eines Kreises mit Radius 5 cm ($U = 2\pi r$, verwenden Sie $\pi \approx 3.14159$)
* Die Fläche eines Rechtecks mit Länge 12 m und Breite 8 m
* Die Geschwindigkeit bei gleichförmiger Bewegung: Weg 150 km in Zeit 2.5 h

Verwenden Sie `print()` um die Ergebnisse mit beschreibendem Text auszugeben.
```
