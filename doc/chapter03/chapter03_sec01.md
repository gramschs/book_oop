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

# 3.1 Wahrheitswerte und Vergleiche

```{admonition} Hinweise zur Vorlesung Objektorientierte Programmierung im WiSe 2025/26
:class: warning
Dieses Vorlesungsskript wird gerade umgebaut.
```

Viele Möglichkeiten unserer Gesellschaft stehen nur Volljährigen offen und sind
damit an eine Altersangabe gebunden. Wenn jetzt ein Computersystem vorab prüfen
soll, ob Volljährigkeit vorliegt oder nicht, dann brauchen wir einen einfachen
Vergleich. Daher beschäftigen wir uns in diesem Kapitel mit Vergleichen und dem
Datentyp Bool.

## Lernziele

```{admonition} Lernziele
:class: goals
* Sie kennen den Datentyp **Bool** mit seinen beiden Werten `True` und `False`.
* Sie kennen die wichtigsten **Vergleichsoperatoren** für Zahlen und Strings.
```

## Der Datentyp Bool

Zurück zu dem Beispiel mit der Überprüfung der Volljährigkeit. Angenommen, wir
speichern das Alter der Benutzers oder der Benutzerin in der Variable `alter`.
Damit wäre ein simples Beispiel für eine einfache Bedingung der mathematische
Ausdruck `alter < 18`. Der Wert der Variablen `alter` wird also mit der Zahl 18
verglichen. Dieser Vergleich ist entweder **wahr (True)** oder **falsch
(False)**. Oder anders formuliert, diese Bedingung ist entweder erfüllt oder
nicht erfüllt.

Um den Wahrheitswert einer Bedingung zu speichern, hat Python einen eigenen
Datentyp, einen sogenannten booleschen Datentyp. Nach dem englischen Wort wird
dieser Datentyp in der Informatik üblicherweise **Bool** oder **Boolean**
genannt. Das besondere an diesem Datentyp ist, dass eine Variable diesen
Datentyps nur zwei verschiedene Werte annehmen kann, nämlich

* True: Wahrheitswert ist wahr oder
* False: Wahrheitswert ist falsch.

Aber wie kann man dann überprüfen, welcher Datentyp in einer Variablen
gespeichert ist? Dazu gibt es das Kommando `type`. Führen Sie die nächste
Code-Zelle aus.

```{code-cell} ipython3
a = False
type(a)
```

## Vergleiche mit Zahlen

Nachdem wir jetzt den Datentyp kennengelernt haben, mit dem Python das Ergebnis
eines Vergleichs speichert, kommen wir nun zu dem Vergleich selbst.

Zunächst beschäftigen wir uns mit mathematischen Vergleichen. In der Mathematik
ist ein Vergleich ein Ausdruck mit zwei Argumenten und einem Vergleichsoperator
in der Mitte. Die beiden Argumente können auch unterschiedliche Datentypen
haben, dann muss der Vergleichsoperator aber sinnvoll für diese Datentypen
definiert sein. Zum Beispiel darf man einen Integer mit einem Float vergleichen

`3 < 17.2`

aber

`3 < 'vier'`

ist nicht sinnvoll und undefiniert. Es gibt die folgenden Vergleichsoperatoren
in Python:

* `<`   kleiner
* `<=`  kleiner oder gleich
* `>`   größer
* `>=`  größer oder gleich
* `==`  gleich
* `!=` ungleich

Im interaktiven Modus von Python können wir leicht den Wahrheitsgehalt von
Vergleichen überprüfen. Wir setzen eine Variable auf den Wert 7:

```{code-cell} ipython3
x = 7
```

Jetzt probieren wir in den nachfolgenden Code-Zellen verschiedene
Vergleichsoperatoren aus.

Ist x genau gleich 15?

```{code-cell} ipython3
x == 15    
```

Ist x kleiner als 42?

```{code-cell} ipython3
x < 42
```

Ist x genau 30?

```{code-cell} ipython3
x == 30
```

Ist x ungleich 42?

```{code-cell} ipython3
x != 42 
```

Ist x größer als 30?

```{code-cell} ipython3
x > 30
```

Ist x größer gleich 30?

```{code-cell} ipython3
x >= 30
```

```{admonition} Mini-Übung
:class: miniexercise
Wählen Sie sich eine Zahl. Testen Sie anschließend:
* Ist Ihre Zahl kleiner gleich 5?
* Ist Ihre Zahl genau 17?
* Ist Ihre Zahl nicht gleich 17?
* Ist Ihre Zahl positiv?
* Ist Ihre Zahl kleiner als -17.7?
```

```{code-cell} ipython3
# Geben Sie nach diesem Kommentar Ihren Code ein:

```

````{admonition} Lösung
:class: miniexercise, toggle
```python
# Eingabe: Wahl meiner Zahl
x = 33

# kleiner gleich 5?
x <= 5

# genau gleich 17?
x == 17

# nicht gleich 17?
x != 17

# positiv?
x > 0

# kleiner als -17.7?
x < -17.7
```
````

```{dropdown} Video "Vergleiche in Python" von Programmieren Starten
<iframe width="560" height="315" src="https://www.youtube.com/embed/ucsv_Nhhxmk"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write;
encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

## Vergleiche mit Strings

Als nächstes werden wir uns mit der Verwendung von Strings in Vergleichen
beschäftigen. Strings werden häufig in Vergleichen verwendet, um festzustellen,
ob zwei Strings gleich sind oder ob ein String in einem anderen enthalten ist.

Um festzustellen, ob zwei Strings in Python gleich sind, können wir den
Gleichheitsoperator `==` verwenden. Der Gleichheitsoperator gibt `True` zurück,
wenn die beiden Strings exakt übereinstimmen, und `False`, wenn sie sich
unterscheiden.

```{code-cell} ipython3
string01 = 'Hallo'
string02 = 'Welt'
string03 = 'Hallo'
string04 = 'hallo'

print(string01 == string02)  # Ausgabe: False
print(string01 == string03)  # Ausgabe: True
print(string01 == string04)  # Ausgabe: False
```

In diesem Beispiel sind die Strings `string01` und `string03` gleich. Der String
`string02` ist jedoch unterschiedlich von `string01`, daher ist das Ergebnis
`False`. Beachten Sie auch, dass der String `string04` nicht gleich `string01`
ist, obwohl er den gleichen Wert hat, da Groß- und Kleinschreibung in Python bei
der Vergleichsoperation berücksichtigt werden.

Um zu überprüfen, ob ein String in einem anderen enthalten ist, können wir den
Operator `in` verwenden. Der Operator `in` gibt `True` zurück, wenn der String
in dem anderen String enthalten ist, und `False`, wenn nicht.

```{code-cell} ipython3
string01 = 'Hallo Welt'
string02 = 'Welt'
string03 = 'Python'

print(string02 in string01)  # Ausgabe: True
print(string03 in string01)  # Ausgabe: False
```

In diesem Beispiel ist der String `string02` in dem String `string01` enthalten,
daher ist das Ergebnis `True`. Der String `string03` ist jedoch nicht in
`string01` enthalten, daher ist das Ergebnis `False`.

Beachten Sie, dass bei der Überprüfung die Groß- und Kleinschreibung in Python
beachtet werden muss. Wenn wir also nach dem String `'welt'` suchen, erhalten wir
`False`, da der String `'Welt'` großgeschrieben ist.

Wir können auch andere Vergleichsoperationen wie <, >, <=, >= mit Strings
verwenden. Diese Operationen vergleichen die Strings nach ihrem
lexikographischen Wert, d.h. sie vergleichen die Zeichen eines Strings in der
Reihenfolge, in der sie auftreten.

```{code-cell} ipython3
a = "Apfel"
b = "Banane"

print(a < b)  # Ausgabe: True
print(a > b)  # Ausgabe: False
print(a <= b)  # Ausgabe: True
print(a >= b)  # Ausgabe: False
```

In diesem Beispiel ist `'Apfel'` kleiner als `'Banane'`, da "A" im Alphabet vor
"B" steht, daher ist das Ergebnis des `<`-Operators `True`. Der `>`-Operator
gibt `False` zurück, da `'Apfel'` nicht größer als `'Banane'` ist. Der
`<=`-Operator gibt `True` zurück, da `'Apfel'` kleiner oder gleich `'Banane'`
ist. Der `>=`-Operator gibt `False` zurück, da `'Apfel'` nicht größer oder
gleich `'Banane'` ist.

````{admonition} Mini-Übung
:class: miniexercise
Gegeben sind die folgenden Strings:
```python
material1 = "Stahl"
material2 = "Aluminium"
material3 = "Stahllegierung"
material4 = "aluminium"
```
Überprüfen Sie folgende Vergleiche und notieren Sie, ob das Ergebnis `True` oder
`False` ist:

1. Ist `material1` lexikographisch größer als `material2`?
2. Enthält `material3` den String `material1`?
3. Sind `material2` und `material4` identisch?
4. Überprüfen Sie mit dem `in-`Operator, ob die Zeichenfolge "leg" in
   `material3` vorkommt.
5. Ist `material4` lexikographisch kleiner als `material1`?
````

```{code-cell} ipython3
# Geben Sie nach diesem Kommentar Ihren Code ein:

```

````{admonition} Lösung
:class: miniexercise, toggle
```python
material1 = "Stahl"
material2 = "Aluminium"
material3 = "Stahllegierung"
material4 = "aluminium"

# 1. Ist material1 lexikographisch größer als material2?
print(material1 > material2)  # True, da 'S' im Alphabet nach 'A' kommt

# 2. Enthält material3 den String material1?
print(material1 in material3)  # True, da "Stahl" in "Stahllegierung" enthalten ist

# 3. Sind material2 und material4 identisch?
print(material2 == material4)  # False, da Groß-/Kleinschreibung unterschiedlich ist

# 4. Überprüfen Sie mit dem in-Operator, ob die Zeichenfolge "leg" in material3 vorkommt.
print("leg" in material3)  # True, da "leg" in "Stahllegierung" enthalten ist

# 5. Ist material4 lexikographisch kleiner als material1?
print(material4 < material1)  # False, da Großbuchstaben im ASCII-Code vor Kleinbuchstaben kommen
```
````

## Zusammenfassung und Ausblick

In diesem Kapitel haben wir den booleschen Datentyp Bool mit seinen Werten True
und False kennengelernt. Wir haben Vergleichsoperatoren (<, >, ==, !=, <=, >=)
für Zahlen und Strings untersucht und gesehen, wie String-Vergleiche auf
lexikographischer Ordnung basieren. Außerdem haben wir den 'in'-Operator zur
Überprüfung von Teil-Strings kennengelernt.

## Lernziele 2

```{admonition} Lernziele
:class: goals
* Sie kennen die logischen Operatoren und können diese in Python einsetzen:
    * logisches UND: `and`
    * logisches ODER: `or`
    * logisches NICHT: `not`
* Sie verstehen die Priorität der logischen Operatoren und können komplexe
  Bedingungen korrekt formulieren.
```

## Das logische UND

Beim logischen UND müssen beide Bedingungen erfüllt sein, damit insgesamt die
kombinierte Bedingung erfüllt ist. Vergleichbar ist dies mit einer
Reihenschaltung in der Elektrotechnik: Nur wenn beide Schalter eingeschaltet
sind, kann der Strom fließen.

Hier finden Sie ein erläuterndes Video (ca. 3:14 min) zur UND-Schaltung:

<https://www.youtube.com/watch?v=79WVEr2BVZI>

Die Ergebnisse der UND-Verknüpfung lassen sich in einer Wahrheitstabelle
darstellen:

Bedingung 1 | Bedingung 2 | Ergebnis mit ```and```
------------|-------------|--------------------------
True | True | True
False | True | False
True | False | False
False | False | False

Beispiel aus der Industrie: Ein automatisches Werkzeug darf nur dann betätigt
werden, wenn das Werkstück korrekt eingespannt ist UND der Sicherheitsbereich
frei ist:

```{code-cell} ipython3
werkstueck_eingespannt = True
sicherheitsbereich_frei = True

if werkstueck_eingespannt and sicherheitsbereich_frei:
    print('Werkzeug kann betätigt werden.')
else:
    print('Sicherheitsvoraussetzungen nicht erfüllt.')
```

Bei komplexeren Bedingungen kann die Verwendung von Klammern die Lesbarkeit
verbessern, auch wenn dies syntaktisch nicht immer erforderlich ist:

```{code-cell} ipython3
temperatur = 75
druck = 3.5

if (temperatur < 80) and (druck < 4.0):
    print('System arbeitet im normalen Betriebszustand.')
else:
    print('System außerhalb der normalen Parameter.')
```

```{admonition} Mini-Übung
:class: miniexercise
Schreiben Sie ein Programm für die Steuerung einer Hydraulikpresse. Die Presse
darf nur betätigt werden, wenn

1. die Betriebstemperatur zwischen 60°C und 85°C liegt und
2. der Druck zwischen 2.5 und 5.0 bar beträgt.

Lassen Sie die Werte vom Benutzer eingeben und geben Sie eine entsprechende
Meldung aus.
```

```{code-cell} ipython3
# Hier Ihr Code
```

````{admonition} Lösung
:class: miniexercise, toggle
```python
# Eingabe
temperatur = float(input('Aktuelle Betriebstemperatur (°C): '))
druck = float(input('Aktueller Druck (bar): '))

# Verarbeitung und Ausgabe
if (60 <= temperatur <= 85) and (2.5 <= druck <= 5.0):
    print('Hydraulikpresse kann betätigt werden.')
else:
    print('Betriebsparameter außerhalb des sicheren Bereichs!')
```
````

## Das logische ODER

Beim logischen ODER muss nur eine der Bedingungen erfüllt sein, damit insgesamt
die kombinierte Bedingung erfüllt ist. Die Bedingung ist auch erfüllt, wenn
beide Teilbedingungen wahr sind. Vergleichbar ist dies mit einer
Parallelschaltung in der Elektrotechnik: Es reicht, wenn einer der beiden
Schalter eingeschaltet ist, damit der Strom fließen kann.

Hier finden Sie ein erläuterndes Video (ca. 2:42 min) zur ODER-Schaltung:

<https://www.youtube.com/watch?v=UNkXbvSN9w8>

Die Wahrheitstabelle für das logische ODER:

Bedingung 1 | Bedingung 2 | Ergebnis mit ```or```
------------|-------------|--------------------------
True | True | True
False | True | True
True | False | True
False | False | False

Beispiel aus der Produktion: Ein Notaus-System muss aktiviert werden, wenn
entweder der Temperaturwert zu hoch ist ODER der Druckwert einen kritischen Wert
überschreitet:

```{code-cell} ipython3
temperatur = 95  # in Grad Celsius
druck = 4.8      # in bar

if (temperatur > 90) or (druck > 5.0):
    print('WARNUNG: Notabschaltung wird eingeleitet!')
else:
    print('System arbeitet im normalen Betriebsbereich.')
```

Python verwendet eine sogenannte **Kurzschlussauswertung** für logische
Operatoren. Dies bedeutet:

* Bei einem `and`-Ausdruck: Wenn der erste Teil `False` ist, wird der zweite
  Teil nicht mehr ausgewertet.
* Bei einem `or`-Ausdruck: Wenn der erste Teil `True` ist, wird der zweite Teil
  nicht mehr ausgewertet.

Dies kann man sich zur Verbesserung der Performance zunutze machen, indem man
bei `and`-Verknüpfungen die Bedingung mit der höheren Wahrscheinlichkeit für
`False` zuerst platziert.

```{admonition} Mini-Übung
:class: miniexercise
Schreiben Sie ein Programm für ein Alarmsystem einer CNC-Fräse. Das System soll
einen Alarm auslösen, wenn:

1. Die Drehzahl unter 500 U/min fällt oder über 2000 U/min steigt
2. Die Kühlmitteltemperatur über 60°C steigt

Lassen Sie die Werte vom Benutzer eingeben und geben Sie eine entsprechende
Meldung aus.
```

```{code-cell} ipython3
# Hier Ihr Code
```

````{admonition} Lösung
:class: miniexercise, toggle
```python
# Eingabe
drehzahl = float(input('Aktuelle Drehzahl (U/min): '))
kuehlmitteltemperatur = float(input('Aktuelle Kühlmitteltemperatur (°C): '))

# Verarbeitung und Ausgabe
if (drehzahl < 500) or (drehzahl > 2000) or (kuehlmitteltemperatur > 60):
    print('ALARM: Betriebsparameter außerhalb des sicheren Bereichs!')
else:
    print('System arbeitet im normalen Betriebsbereich.')
```
````

## Das logische NICHT

Das logische NICHT kehrt eine Aussage um. Wenn eine Bedingung wahr ist, wird sie
falsch und umgekehrt. In Python verwenden wir den Operator `not` für diese
Umkehrung.

Die Wahrheitstabelle für das logische NICHT:

Bedingung | Ergebnis mit ```not```
----------|--------------------------
True | False
False | True

Beispiel aus dem Maschinenbau: Eine Maschine darf nicht gestartet werden, wenn
der Wartungsmodus aktiviert ist:

```{code-cell} ipython3
wartungsmodus_aktiv = True

if not wartungsmodus_aktiv:
    print('Maschine kann gestartet werden.')
else:
    print('Maschine im Wartungsmodus: Start nicht möglich.')
```

Die Verwendung von `not` kann oft komplexe Bedingungen vereinfachen. Statt zu
prüfen, ob ein Wert außerhalb eines Bereichs liegt, kann man prüfen, ob er nicht
innerhalb des Bereichs liegt:

```{code-cell} ipython3
temperatur = 78

# Diese beiden Bedingungen sind äquivalent
if (temperatur < 60) or (temperatur > 85):
    print('Temperatur außerhalb des Betriebsbereichs.')
    
if not (60 <= temperatur <= 85):
    print('Temperatur außerhalb des Betriebsbereichs.')
```

## Priorität der logischen Operatoren

Bei mehreren logischen Operatoren in einem Ausdruck ist die Reihenfolge der
Auswertung wichtig. In Python gilt folgende Priorität:

1. Klammern `()`
2. Nicht `not`
3. Und `and`
4. Oder `or`

Zur Verdeutlichung einige Beispiele:

```{code-cell} ipython3
# Priorität der logischen Operatoren
a = True
b = False
c = True

# not hat Vorrang vor and
ergebnis1 = not a and b  # entspricht (not a) and b
print(f"not a and b = {ergebnis1}")

# and hat Vorrang vor or
ergebnis2 = a and b or c  # entspricht (a and b) or c
print(f"a and b or c = {ergebnis2}")

# Klammern ändern die Priorität
ergebnis3 = a and (b or c)  # erst b or c, dann and
print(f"a and (b or c) = {ergebnis3}")
```

Um Missverständnisse zu vermeiden, ist es oft ratsam, Klammern zu setzen, auch
wenn sie aufgrund der Prioritätsregeln nicht unbedingt nötig wären. Dies
verbessert die Lesbarkeit des Codes.

```{admonition} Mini-Übung
:class: miniexercise
Überlegen Sie zunächst, was das Ergebnis der folgenden logischen Verknüpfungen
ist (wahr oder falsch):

1. True and True
2. True or False
3. not True
4. False or True
5. True or (not False)
6. (not True) and False
7. not (True or False)
8. (not False) or (False and False)

Prüfen Sie Ihre Antworten anschließend im Python-Interpreter.
```

```{code-cell} ipython3
# Hier Ihr Code
```

````{admonition} Lösung
:class: miniexercise, toggle
```python
# 1. True and True
print("True and True =", True and True)  # True

# 2. True or False
print("True or False =", True or False)  # True

# 3. not True
print("not True =", not True)  # False

# 4. False or True
print("False or True =", False or True)  # True

# 5. True or (not False)
print("True or (not False) =", True or (not False))  # True

# 6. (not True) and False
print("(not True) and False =", (not True) and False)  # False

# 7. not (True or False)
print("not (True or False) =", not (True or False))  # False

# 8. (not False) or (False and False)
print("(not False) or (False and False) =", (not False) or (False and False))  # True
```
````

```{dropdown} Video zu "Logische Operatoren" von Programmieren Starten
<iframe width="560" height="315" src="https://www.youtube.com/embed/075l6R42tkQ"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write;
encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

## Zusammenfassung und Ausblick 2

Die booleschen Operatoren `and`, `or` und `not` sind fundamentale Werkzeuge für
die Programmierung von Bedingungen in Python. Sie ermöglichen die Formulierung
komplexer Entscheidungslogik und sind besonders für Steuerungs- und
Regelungsanwendungen von großer Bedeutung. Im nächsten Kapitel beschäftigen wir
uns mit Schleifen.
