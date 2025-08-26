# Quiz-Fragen: Klassen und Objekte (OOP)

## Multiple Choice Fragen

### Frage 1: Grundkonzept
**Was ist eine Klasse in der objektorientierten Programmierung?**

a) Eine Variable, die Daten speichert  
b) Ein Bauplan oder Formular, das die Struktur von Objekten festlegt ✓  
c) Eine Funktion, die Berechnungen durchführt  
d) Eine Liste mit zusammengehörigen Daten  

**Erklärung:** Eine Klasse funktioniert wie ein Bauplan oder Formular - sie definiert, welche Attribute und Methoden Objekte dieser Klasse haben sollen.

### Frage 2: Syntax
**Wie erstellt man ein Objekt der Klasse `Student`?**

a) `Student.create("Müller", "Anna", ...)`  
b) `new Student("Müller", "Anna", ...)`  
c) `Student("Müller", "Anna", ...)` ✓  
d) `create Student("Müller", "Anna", ...)`  

**Erklärung:** In Python erstellt man Objekte durch Aufruf des Klassennamens mit den entsprechenden Parametern.

### Frage 3: Attributzugriff
**Wie greift man auf das Attribut `nachname` des Objekts `student1` zu?**

a) `student1->nachname`  
b) `student1.nachname` ✓  
c) `student1["nachname"]`  
d) `get_nachname(student1)`  

**Erklärung:** In Python verwendet man die Punkt-Notation: `objektname.attributname`

### Frage 4: Begriffe unterscheiden
**Was ist der Unterschied zwischen einer Klasse und einem Objekt?**

a) Es gibt keinen Unterschied  
b) Eine Klasse ist der Bauplan, ein Objekt die konkrete Ausprägung ✓  
c) Eine Klasse speichert Daten, ein Objekt führt Funktionen aus  
d) Eine Klasse ist größer als ein Objekt  

**Erklärung:** Die Klasse definiert die Struktur (wie ein Formular), das Objekt enthält die konkreten Daten (wie ein ausgefülltes Formular).

## True/False Fragen

### Frage 5: Objektunabhängigkeit
**Wenn ich `student1.semester = 5` schreibe, ändert sich auch das Semester von `student2`.**

- [ ] Wahr  
- [x] Falsch ✓  

**Erklärung:** Jedes Objekt hat seine eigenen Attribute. Änderungen an einem Objekt beeinflussen andere Objekte nicht.

### Frage 6: Attributzugriff
**Man kann Attribute sowohl lesen als auch schreiben.**

- [x] Wahr ✓  
- [ ] Falsch  

**Erklärung:** Mit der Punkt-Notation kann man sowohl den Wert eines Attributs abfragen (`print(student.name)`) als auch ändern (`student.name = "Neuer Name"`).

### Frage 7: Klassen-Definition
**Eine Klasse kann nur einmal verwendet werden, um ein Objekt zu erstellen.**

- [ ] Wahr  
- [x] Falsch ✓  

**Erklärung:** Von einer Klasse können beliebig viele Objekte erstellt werden, genau wie von einem Formular beliebig viele Kopien ausgefüllt werden können.

## Fill in the Blanks (Lückentext)

### Frage 8: Syntax vervollständigen
**Vervollständigen Sie den Code:**

```python
class Student:
    def _______(self, nachname, vorname):
        self.nachname = _______
        self.vorname = vorname
```

**Antworten:** 
- Lücke 1: `__init__`
- Lücke 2: `nachname`

**Erklärung:** `__init__` ist der Konstruktor, der beim Erstellen eines Objekts aufgerufen wird. `self.nachname = nachname` weist den übergebenen Wert dem Attribut zu.

### Frage 9: Objekterstellung
**Vervollständigen Sie den Code zum Erstellen eines Objekts:**

```python
student1 = _______("Müller", "Anna", "Maschinenbau", 3, "12345")
```

**Antwort:** `Student`

**Erklärung:** Der Klassenname wird wie eine Funktion aufgerufen, um ein neues Objekt zu erstellen.

## Drag and Drop / Zuordnung

### Frage 10: Begriffe zuordnen
**Ordnen Sie die Begriffe den richtigen Beschreibungen zu:**

**Begriffe:**
- Klasse
- Objekt  
- Attribut
- __init__

**Beschreibungen:**
- Bauplan für Objekte → **Klasse**
- Konkrete Ausprägung einer Klasse → **Objekt**
- Gespeicherte Daten in einem Objekt → **Attribut**
- Spezielle Methode zum Initialisieren → **__init__**

## Code-Analyse Fragen

### Frage 11: Code verstehen
**Was gibt dieser Code aus?**

```python
class Student:
    def __init__(self, name):
        self.name = name

student1 = Student("Anna")
student2 = Student("Bob")
print(student1.name)
print(student2.name)
```

a) Anna, Anna  
b) Bob, Bob  
c) Anna, Bob ✓  
d) Fehler  

**Erklärung:** Jedes Objekt hat seinen eigenen Namen-Wert: student1 hat "Anna", student2 hat "Bob".

### Frage 12: Attribut ändern
**Was ist nach diesem Code der Wert von `student1.semester`?**

```python
student1 = Student("Müller", "Anna", "MB", 3, "123")
student1.semester = 4
student1.semester = student1.semester + 1
```

a) 3  
b) 4  
c) 5 ✓  
d) Fehler  

**Erklärung:** Startwert ist 3, wird auf 4 gesetzt, dann um 1 erhöht → 5.

## Anwendungsfrage

### Frage 13: Praktische Anwendung
**Sie wollen eine Klasse für Bücher in einer Bibliothek erstellen. Welche Attribute wären sinnvoll?**

- [x] Titel ✓
- [x] Autor ✓  
- [x] ISBN ✓
- [ ] Temperatur
- [x] Erscheinungsjahr ✓
- [ ] Klausurnote

**Erklärung:** Titel, Autor, ISBN und Erscheinungsjahr sind typische Eigenschaften von Büchern. Temperatur und Klausurnote gehören nicht zu einem Buch.