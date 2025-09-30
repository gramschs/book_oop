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

# 2.1 Variablen und Zuweisungen

```{admonition} Hinweise zur Vorlesung Objektorientierte Programmierung im WiSe 2025/26
:class: warning
Dieses Vorlesungsskript wird gerade umgebaut.
```

Ein Klassiker beim Erlernen einer neuen Programmiersprache ist das
Hallo-Welt-Programm. Dabei geht es darum, den Text "Hallo Welt" auf dem
Bildschirm anzeigen zu lassen. Klingt simpel, aber je nach Programmiersprache
kann auch diese einfache Aufgabe einen hohen Aufwand bedeuten. Bevor wir das
Hallo-Welt-Programm programmieren, nutzen wir erst Python als Taschenrechner, um
auch den Umgang mit dem Jupyter Notebook noch weiter zu festigen.

## Lernziele

```{admonition} Lernziele
:class: goals
* Sie wissen, was eine **Variable** ist und wie sie erzeugt und gefüllt wird.
```

## Variablen

**Variablen** sind beschriftete Schubladen. Oder anders formuliert sind
Variablen Objekte, denen man einen Namen gibt. Technisch gesehen sind diese
Schubladen ein kleiner Bereich im Arbeitsspeicher des Computers. Was in diesen
Schubladen aufbewahrt wird, kann sehr unterschiedlich sein. Beispielsweise die
Telefonnummer des ADAC-Pannendienstes, die 10. Nachkommastelle von $\pi$ oder die
aktuelle Position des Mauszeigers können in den Schubladen enthalten sein.

Wir verwenden Variablen, um bestimmte Werte oder ein bestimmtes Objekt zu
speichern. Eine Variable wird durch **Zuweisung** erzeugt. Damit meinen wir,
dass eine Schublade angelegt wird und die Schublade dann erstmalig gefüllt wird.
Das erstmalige Füllen der Schublade nennt man in der Informatik auch
**Initialisieren**.

```{code-cell} ipython3
x = 0.5
```

Sobald die Variable x in diesem Beispiel durch eine Zuweisung von 0.5 erstellt
wurde, können wir sie verwenden:

```{code-cell} ipython3
x * 3
```

```{code-cell} ipython3
x + 17.8
```

Variablen müssen initialisiert (erstmalig mit einem Wert versehen) werden, bevor
sie verwendet werden können, sonst tritt ein Fehler auf.

```{admonition} Mini-Übung
:class: miniexercise
Schreiben Sie in die nächste Code-Zelle einfach den Buchstaben `n` unter die Kommentarzeile und lassen Sie dann die Code-Zelle mit `run` vom Python-Interpreter ausführen. Was beobachten Sie? Recherchieren Sie im Internet nach der Fehlermeldung. 
```

```{code-cell} ipython3
# Geben Sie nach diesem Kommentar Ihren Code ein:

```

````{admonition} Lösung
:class: miniexercise, toggle
```python
n
```
Der Interpreter zeigt in rot eine Fehlermeldung an: "NameError: name 'n' is not defined". Damit weist der Interpreter darauf hin, dass die Variable bisher nicht mit einem Wert versehen wurde, sie ist nicht intialisiert worden. Daher kann damit auch nicht gearbeitet werden.
````

Gerne können Sie sich auch folgendes Video auf YouTube ansehen, das eine
Einführung in das Thema Variablen in Python gibt.

```{dropdown} Video "Variablen in Python" von Programmieren Starten
<iframe width="560" height="315" src="https://www.youtube.com/embed/jfOLXKPGXJ0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
```

## Richtlinien für Variablennamen

Früher war der Speicherplatz von Computern klein, daher wurden häufig nur kurze
Variablennamen wie beispielsweise i oder N verwendet. Heutzutage ist es
Standard, nur in Ausnahmefällen (z.B. in Schleifen, dazu kommen wir noch) kurze
Variablennamen zu nehmen. Stattdessen werden Namen benutzt, bei denen man
erraten kann, was die Variable für einen Einsatzzweck hat. Beispielsweise lässt
der Code

```{code-cell} ipython3
m = 0.19
n = 80
b = n + m * n
print(b)
```

nur schwer vermuten, was damit bezweckt wird. Oder können Sie erahnen, was dort passieren soll?
Dagegen erahnt man bei diesem Code schon eher, was bezweckt wird:

```{code-cell} ipython3
mehrwertsteuersatz = 19/100
nettopreis = 80
bruttopreis = nettopreis + mehrwertsteuersatz * nettopreis
print(bruttopreis)
```

Verwenden Sie für Variablennamen nur ASCII-Zeichen, also keine Umlaute wie ö, ü
oder ß. Zahlen sind erlaubt, aber nicht am Anfang des Namens. Es ist sinnvoll,
lange Variablen durch einen Unterstrich besser lesbar zu gestalten (sogenannte
Snake-Case-Formatierung). Ich empfehle für Variablennamen beispielsweise
`dateiname_alt` oder `dateiname_neu`, wenn beispielsweise eine Datei umbenannt
wird. Sie sind frei in der Gestaltung der Variablennamen, verboten sind nur die
sogannnten **Schlüsselwörter**. Schlüsselwörter sind beispielsweise eingebaute
Kommandos an den Python-Interpreter. Würden Sie diese als Variablennamen
benutzen, wüsste der Python-Interpreter nicht, ob das Kommando oder die Variable
gemeint ist.

```{admonition} Mini-Übung
:class: miniexercise
Initialisieren Sie eine Variable namens alter mit Ihrem aktuellen Alter, eine
Variable ``rentenalter`` mit dem Zahlenwert ``67`` und berechnen Sie dann, wie
viele Jahre es noch bis zum Renteneintritt dauert.
```

```{code-cell} ipython3
# Geben Sie nach diesem Kommentar Ihren Code ein:

```

````{admonition} Lösung
:class: miniexercise, toggle
```python
# Geben Sie nach diesem Kommentar Ihren Code ein:
alter = 21
rentenalter = 67
print(rentenalter - alter)
```
````

## Zuweisungsoperator

Wichtig ist, dass das `=` in der Informatik eine andere Bedeutung hat als in der
Mathematik. = meint nicht das Gleichheitszeichen, sondern den sogenannten
**Zuweisungsoperator**. Das ist in der Programmierung ein Kommando, das eine
Schublade befüllt oder technischer ausgedrückt, ein Objekt einer Variable
zuweist.

Sehr häufig findet man Code wie

```python
x = x + 1
```

Würden wir dies als Gleichung lesen, wie wir es aus der Mathematik gewohnt sind,
also $x = x+1$, könnten wir $x$ auf beiden Seiten subtrahieren und erhalten
$0=1$. Wir wissen, dass dies nicht wahr ist, also stimmt hier etwas nicht.

In Python sind "Gleichungen" keine mathematischen Gleichungen, sondern
Zuweisungen. "=" ist kein Gleichheitszeichen im mathematischen Sinne, sondern
eine Zuweisung. Die Zuweisung muss immer in der folgenden Weise zweistufig
gelesen werden:

1. Berechne den Wert auf der rechten Seite (also $x+1$).
2. Weise den Wert auf der rechten Seite dem auf der linken Seite stehenden
   Variablennamen zu.

Wir probieren eine solche Zuweisung in der folgenden Code-Zelle aus und benutzen
auch gleich die `print()`-Funktion, um den Wert der Variablen `x` ausgeben zu
lassen:

```{code-cell} ipython3
x = 4     
x = x + 1
print(x)
```

Der Zuweisungsoperator ist äußerst wichtig in der Python-Programmierung. Daher
empfehle ich Ihnen folgende Video.

```{dropdown} Video "Der Zuweisungsoperator" von Programmieren Starten
<iframe width="560" height="315" src="https://www.youtube.com/embed/XKFQ2_et5k8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
```
