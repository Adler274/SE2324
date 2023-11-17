class: center, middle

## [Software Engineering](../../praesentationen.html)

#### Kapitel 7

# Softwareentwurf

Simon Fedrau, Sascha Hahn

---

# Inhalt
***
1. Softwareentwurf
  1. Entwurfsprinzipien

  1. Jeweils Implementierungsbeispiel
1. Entwurfsmuster (Design Patterns)

1. Entwurf des Datenmodells

    1. Domain-Driven Design

1. Entwurf der Benutzerschnittstelle
    
    1. UI Modelling

    1. Usability vs. User experience (UX) vs. Customer experience (CX)

    1. Nielsen's 10 Usability Heuristic Prinzipien für das UI-Design

1. Zusammenfassung
1. Quellen

---
## Softwareentwurf
***
**Was ist ein Softwareentwurf?**
Der Softwareentwurf ist entscheidend für erfolgreiche Softwareentwicklung. 
Dabei werden Grundlagen, Schlüsselthemen, Struktur, Architektur, Benutzeroberfläche, Design-Notationen sowie Strategien und Methoden festgelegt.

**Warum ein Softwareentwurf?**
* Hilfsmittel für Programmierer: Fachspezifisches Wissen wird angewandt, um einen Grundriss für die Projektarbeit zu erstellen.

* Projektstart: Beantwortet grundlegende Fragen und vermittelt allen Beteiligten einen klaren Eindruck vom Projekt für einen reibungslosen Start.

[1a] [2a]
---
## Tätigkeiten im Softwareentwurf

**Infrastruktur:**
* Hardware, Tools, Services, Entwicklungsumgebungen, SDKs, Programmiersprachen, Bibliotheken

**Architektur:**
* Client-Server, Web, service-orientierte Architektur, Betriebssysteme, Netzwerkprotokolle,etc

**Teilsysteme und Schnittstellen:**

* Spezifikation von Schnittstellen, Komponenten, Module, Klassen und ihre Beziehungen

**Wichtige Fragen**
* Verteilung des Systems
* Hardware
* Persistenzmechanismus
* Betriebssysteme und Netzwerke

[1a] [3a]

---
## Entwurfsziele

Ausgehend von der Anforderungsanalyse und einer ersten Skizze des
zu konstruierenden Systems in der Szenarioanalyse, muss im Entwurf
festgelegt werden:

*  Technische Basis / Infrastruktur

*  Softwarearchitektur

*  Entwurf der Komponenten und Klassen

* Ziel ist es, eine Grundlage zu definieren, die leicht zu verstehen, zu ändern, zu erweitern und zu warten ist. 
* Überlegungen müssen in einer Weise notiert werden, dass sie den
Entwicklern zugänglich und verständlich sind. 

[3a] [1a]

---
### Orthogonalität

**Definition:**

Unabhängigkeit von verschiedenen Systemaspekten.

**Ziel:**

Änderungen in einer Komponente beeinflussen andere nicht.

**Prinzip:**

Entkopplung für Wartbarkeit, Erweiterbarkeit und Flexibilität.

**Beispiel:**

Trennung von Benutzeroberflächen- und Geschäftslogik.

[4a]
---
### Niedrige Kopplung

* Kopplung = Abhängigkeiten

* Niedrige Kopplung = Einzelne Struktureinheiten sollen möglichst unabhängig voneinander sein.

Bsp:

**Niedrige Kopplung:**

    Es muss möglich sein, Subsystem A
    weitgehend auszutauschen oder zu
    verändern, ohne Subsystem B zu
    verändern.
    Änderungen von Subsystem B
    sollten nur möglichst einfache
    Änderungen in Subsystem A nach
    sich ziehen.

[5a]
---
### Prozedural Kopplung

**Prozedurale Kopplung**

* Datenkopplung:

    * Module teilen Daten durch direkten Zugriff oder Datenaustausch über Parameter.

* Kontrollkopplung:
    * Modul benötigt Informationen über den Kontrollfluss eines anderen Moduls.

* Inhaltskopplung:

    * Modul greift direkt auf den internen Code eines anderen Moduls zu

[20a] [21a]
---
### Objektorientiert Kopplung

* Datenkopplung:

    * Objektorientierte Module teilen Daten durch direktes Lesen oder Schreiben von Datenattributen.

* Methoden- oder Nachrichtenkopplung:

    * Ein Objekt ruft die Methode oder Nachricht eines anderen Objekts auf.

* Vererbungskopplung:

    * Klasse erbt von einer anderen, Änderungen in der Basisklasse beeinflussen abgeleitete Klassen.


[20a] [21a]
---
### Hohe Kohäsion

* Kohäsion = "Zusammenhalt"
* Die Dinge sollen in Struktureinheiten zusammengefasst werden, die inhaltlich zusammengehören.

Bsp.

* Hohe Kohäsion:
    * Subsystem B darf keine Informationund Funktionalität enthalten, die zum
Zuständigkeitsbereich von A gehört
und umgekehrt.

[5a]

---

### Entwurfsprinzipien

**Gängige Entwurfsprinzipien:**

* Abstraktion

* Modularität
* Law of demeter

* Dependency Injection, Inversion of Control
* Separation of Concerns

* Keep It Stupid Simple
* You Ain’t Gonna Need It
* Don't repeat yourself

* Composition Over Inheritance

* Clean Code SOLID-Prinzipien

---
### Abstraktion

Abstraktion wird in der Informatik sehr häufig eingesetzt und beschreibt die Trennung zwischen Konzept und Umsetzung. Strukturen werden dabei über ihre Bedeutung definiert, während die detaillierten Informationen über die Funktionsweise verborgen bleiben. 

- **Ziel der Abstraktion**: Ableitung eines allgemeinen Schemas zur Lösung eines Problems, ohne Details der Implementierung zu berücksichtigen.
  
- **Abstraktionsebenen in Programmen**: Ein Computerprogramm kann unterschiedliche Abstraktionsebenen aufweisen, wobei auf jeder Ebene ein anderer Grad des Informationsgehaltes dem Programmierer preisgegeben wird. 
    - Niedrige Abstraktion: Details zur Hardware
    - Höhere Abstraktion: Geschäftslogik der Software

- **Anwendung der Abstraktion**: Beschäftigt sich mit dem Detailgrad eines Objektes, der im Kontext der aktuellen Perspektive benötigt wird. Kann auf Daten sowie die Steuerung eines Programmes angewendet werden.

[7a]
---
### Modularität

**Modularer Entwurf oder Modularität im Entwurf** ist ein Entwurfsprinzip, das ein System in kleinere Teile unterteilt, die als Module bezeichnet werden (z.B. modulare Prozesskufen). Diese Module können unabhängig voneinander erstellt, geändert, ersetzt oder mit anderen Modulen oder sogar zwischen verschiedenen Systemen ausgetauscht werden.

* Definition der Modularität: 
Aufteilung eines Systems in unabhängige, wiederverwendbare Module oder Komponenten.

* **Eigenschaften der Module**:
  * Unabhängigkeit: Jedes Modul kann unabhängig entwickelt, getestet und gewartet werden.
  * Wiederverwendbarkeit: Module können in verschiedenen Kontexten wiederverwendet werden.
  
- **Vorteile von Modularität**:
  * Skalierbarkeit: Einfache Integration neuer Module für die Skalierung des Systems.
  * Wartbarkeit: Leichtere Wartung durch die Isolierung von Modulen.
  
[8a]
---
### Law of demeter

Das **"Gesetz von Demeter"** ist eine Entwurfs-Richtlinie in der objektorientierten Softwareentwicklung. Es besagt, dass Objekte nur mit Objekten in ihrer unmittelbaren Umgebung kommunizieren sollten. Dies trägt dazu bei, die Kopplung in einem Softwaresystem zu verringern und somit die Wartbarkeit zu erhöhen. Das Gesetz von Demeter wird auch als „Prinzip der Verschwiegenheit“ bezeichnet.

- **Kernpunkt des Gesetzes von Demeter**:
  - Objekte sollten nur mit ihren direkten Nachbarn kommunizieren.
  
- **Ziel des Gesetzes von Demeter**:
  - Verringerung der Kopplung zwischen verschiedenen Teilen des Systems.
  - Verbesserung der Wartbarkeit, da Änderungen in einem Modul weniger wahrscheinlich Auswirkungen auf andere Module haben.


[9a]
---
 ### Inversion of Control

Inversion of Control (IoC) ist ein Programmierprinzip, das den herkömmlichen Kontrollfluss umkehrt.   IoC lenkt den Kontrollfluss dynamisch aus dem Framework auf den benutzerdefinierten Code des Entwicklers.

* Locker gekoppelte Abhängigkeiten

* Entkoppelung von Implementierung und Ausführung

* Leichtere Modularisierung

* Einfacher Wechsel zwischen verschiedenen Implementierungen, z. B. von verschiedenen Frameworks

* Einfacher Austausch von Modulen

* Verbessertes Testen

[Quelle: 10a]

---
### Dependency Injection


**Dependency Injection (DI)** entkoppelt Objekte, sodass Client-Code unverändert bleibt, wenn abhängige Objekte geändert werden. Es ist eine Form der Inversion der Kontrolle.

- **Verantwortungsübertragung an den Injektor:**
  - Der Client delegiert die Bereitstellung von Abhängigkeiten an den Injektor, ohne ihn selbst aufzurufen.

- **Trennung von Nutzung und Konstruktion:**
  - Der Client kennt nur die Schnittstellen der Services, nicht ihre Implementierungsdetails.

#### Akzeptanz von Dependency Injection:

*  **Setter-Injektion**
*  **Schnittstellen-Injektion**
*  **Konstruktorbasierte Injektion**

[11a]
---

### Separation of Concerns

- **Ziel:**
  - Trennung von Zuständigkeiten für Datenkapselung.

- **Umsetzung:**
  - Klassen implementieren spezifische Aufgabenbereiche.

- **Vorteile:**
  - Einfachere Pflege, Fehlerisolation, Unabhängigkeit.

#### Beispiel: Die Webarchitektur

- **html:** Seitenbeschreibung.
- **css:** Layout-Beschreibung (getrennt vom Inhalt).
- **http:** Übertragungsprotokoll (getrennt vom Inhalt).

Anwendungen sollten logisch erstellt werden, um diese Prinzipien zu folgen. Separation of Concerns spielt eine entscheidende Rolle in Anwendungsarchitekturen.

[16a] [12a]

---
### Keep It Stupid Simple

 **Grundprinzip:**
  - Suche stets die einfachste Lösung für ein Problem.

 **Wirkung:**
  - Vereinfacht komplexe Systeme und erhöht Stabilität.

 **Herausforderungen:**
  - Umsetzung kann schwierig sein, aber wirkungsvoll.

Vorteile von KISS:

 **Einfachere Konstruktion:**
  - Reduziert Komplexität beim Systemaufbau.

 **Leichter zu verstehen, zu bauen, zu testen, zu ändern und zu warten:**
  - Im Vergleich zu komplexen Systemen.


[14a] [13a]
---
### You Ain’t Gonna Need It


- **Akronym für "You Ain't Gonna Need It":**
  - Betont Vermeidung unnötiger Funktionen.

- **Entstehung und Kontext:**
  - Im Rahmen des Extreme Programming und Clean Code entstanden.

- **Prinzip:**
  - Implementiere nur die konkret benötigten Features.

- **Ergänzung zum KISS-Prinzip:**
  - KISS sucht nach einfacher Lösung, YAGNI hinterfragt die Notwendigkeit.

#### Verbindung zu KISS:

- **Einfachheit der Lösung:**
  - KISS sucht nach Einfachheit, YAGNI betont die Notwendigkeit.

[15a]
---
### Don't repeat yourself


- **(DRY):**
  - Betont Vermeidung oder Reduzierung von Redundanz.

- **Prinzip von Clean Code:**
  - Ziel ist die Vermeidung von wiederholtem Code.

#### Vermeidung von Redundanz:

- **Konsistenz durch Vermeidung:**
  - Redundanz führt zu Inkonsistenzen bei Änderungen.

- **Zentrale Autorität für Verhalten:**
  - Kapselung der Logik in einem Programmierungskonstrukt.

- **Verwendung in verschiedenen Teilen der Anwendung:**
  - Andere Teile greifen auf das zentrale Konstrukt zu.

[17a] [16a]
---
### Composition Over Inheritance

- **Betonung von Komposition statt Vererbung:**
  - Erhöht Flexibilität und Wartbarkeit.

- **Aufbau durch Kombination kleiner, unabhängiger Klassen:**
  - Vermeidet hierarchische Erweiterung.

- **Separate Klassen für Algorithmen:**
  - Von Schnittstellen abgeleitet.

- **Trennung von Klassen und Algorithmendetails:**
  - Änderungen an Algorithmen haben geringen Einfluss auf Klassen.

- **Unterstützung des Open-Closed-Prinzips:**
  - Vermeidung von Codeänderungen bei Entwicklungen und Änderungen.

[22a]

---
### Clean Code SOLID-Prinzipien

- **Ziele:**
  - Erleichterung der Erstellung von gutem Code.

- **Prinzipien:**
  - SOLID: Single-Responsibility, Open-Closed, Liskov Substitution, Interface Segregation, Dependency Inversion.

- **Checkliste für Entwickler:**
  - Dient als Reflexionshilfe und Fehlervermeidung.

- **Vorteile bei Einhaltung:**
  - Besserer Code, verbesserte Wartbarkeit der Software.

[19a]

---
### Single Responsibility Principle

- **Prinzip:**
  - Eine Klasse sollte nur eine Verantwortlichkeit haben.

- **Auswirkungen von Änderungen:**
  - Änderungen sollen nur wenige Klassen betreffen, um das Fehlerrisiko zu reduzieren.

- **Vermeidung von Abhängigkeiten und Vernetzung:**
  - Zu viele Aufgaben führen zu unhandlichen, vernetzten Klassen.

- **Erkennung von Verletzungen:**
  - Klasse darf nur einen Grund zur Änderung haben.

- **Organisation von Klassen:**
  - Besser viele kleine Klassen als wenige große für verbesserte Struktur.

[19a]
---
### Open-Closed Principle

- **Prinzip:**
  - Eine Klasse sollte offen für Erweiterungen, aber geschlossen für Modifikationen sein.

- **Vermeidung von Modifikationen:**
  - Bestehendes Verhalten darf nicht verändert werden.

- **Fehlervermeidung in fertigem Code:**
  - Reduziert die Gefahr von Fehlern in bereits implementierten Funktionen.

- **Umsetzung über:**
  - Vererbung oder Einsatz von Interfaces.

- **Erreichbare Erweiterbarkeit:**
  - Neue Funktionen können hinzugefügt werden, ohne bestehende Klassen zu ändern.

[19a]
---
### Liskov Substitution Principle

- **Prinzip:**
  - Abgeleitete Klassen müssen immer anstelle ihrer Basisklasse einsetzbar sein.

- **Verhalten der Subtypen:**
  - Subtypen müssen sich wie ihr Basistyp verhalten.

- **Erwartetes Verhalten bei Parametern:**
  - Kein Unterschied bei Verwendung von Basisklasse oder abgeleiteter Klasse als Parameter.

- **Sicherung des identischen Verhaltens:**
  - Verhalten in abgeleiteter Klasse muss identisch aus Sicht der Methode der Basisklasse sein.

- **Testmöglichkeiten:**
  - Unit-Tests sichern die Einhaltung des LSP.

[19a]
---
### Interface Segregation Principle

- **Prinzip:**
  - Ein Client darf nicht von Funktionen abhängig sein, die er nicht benötigt.

- **Inhalt von Interfaces:**
  - Nur Funktionen, die wirklich zusammengehören, sollen im Interface enthalten sein.

- **Problematik "fetter" Interfaces:**
  - Kopplungen zwischen unabhängigen Clients entstehen.

- **Auswirkungen von Änderungen:**
  - Änderungen an einem Aspekt des Interfaces beeinflussen alle Clients.

- **Lösung mit Adapter:**
  - Einsatz eines Adapters (Adapter-Entwurfsmuster) für nicht änderbare Interfaces.

[19a]

---
### Dependency Inversion Principle

- **Prinzip:**
  - Klassen auf höherem Abstraktionslevel sollen nicht von Klassen auf niedrigerem Abstraktionslevel abhängig sein.

- **Vermeidung von direkten Klassenabhängigkeiten:**
  - Keine direkten Abhängigkeiten zwischen Klassen auf unterschiedlichen Abstraktionsleveln.

- **Abhängigkeiten zu Interfaces:**
  - Abhängigkeiten sollen nur zu Interfaces bestehen, nicht zu konkreten Implementierungen.

- **Keine Detailsabhängigkeit von Interfaces:**
  - Interfaces sollen nicht von konkreten Details abhängig sein, sondern umgekehrt.

[19a]
---
### Implementierungsbeispiel Abstraktion

Abstraktion kann durch die Verwendung von Klassen und Methoden erreicht werden. Hier ist ein einfaches Beispiel:

```python
class Shape:
    def area(self):
        pass

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * self.radius * self.radius

class Square(Shape):
    def __init__(self, side):
        self.side = side

    def area(self):
        return self.side * self.side
```
[23a]
---
### Implementierungsbeispiel Modularität

Modularität kann durch die Aufteilung des Codes in unabhängige Module erreicht werden. Hier ist ein Beispiel mit zwei Modulen:


```python

def add(x, y):
    return x + y
```


```python
def multiply(x, y):
    return x * y
```
[23a]

```python
from module1 import add
from module2 import multiply

result_add = add(3, 4)
result_multiply = multiply(2, 5)

print("Addition result:", result_add)
print("Multiplication result:", result_multiply)
```
[23a]
---

### Law of Demeter
Das Law of Demeter kann durch Lockerung von Kopplungen erreicht werden. Hier ist ein Beispiel:


```python
class Engine:
    def start(self):
        print("Engine started")

class Car:
    def __init__(self):
        self.engine = Engine()

    def start(self):
        print("Car is starting")
        self.engine.start()

# Verwendung:
my_car = Car()
my_car.start()
```
[23a]
---
### Dependency Injection, Inversion of Control
Dependency Injection und Inversion of Control können durch die Verwendung von DI-Containern erreicht werden. Hier ist ein einfaches Beispiel ohne Container:

```python
class Engine:
    def start(self):
        print("Engine started")

class Car:
    def __init__(self, engine):
        self.engine = engine

    def start(self):
        print("Car is starting")
        self.engine.start()

# Verwendung:
my_engine = Engine()
my_car = Car(my_engine)
my_car.start()

```
[23a]
---

### Separation of Concerns
Separation of Concerns kann durch die Trennung von Geschäftslogik und Präsentation erreicht werden. Hier ist ein einfaches Beispiel:

```python
class Calculator:
    def add(self, x, y):
        return x + y

class CalculatorPresenter:
    def present_result(self, result):
        print("Result:", result)

# Verwendung:
calculator = Calculator()
presenter = CalculatorPresenter()

result = calculator.add(3, 4)
presenter.present_result(result)
```
[23a]
---

### Keep It Stupid Simple (KISS)
KISS kann durch die Verwendung einfacher und klarer Implementierungen erreicht werden. Hier ist ein einfaches Beispiel:

```python
def add(x, y):
    return x + y

result = add(3, 4)
print("Result:", result)
```

You Ain’t Gonna Need It (YAGNI)
YAGNI kann durch das Vermeiden von unnötigen Funktionen erreicht werden. Hier ist ein Beispiel:

```python
# Nicht benötigt
def unnecessary_feature():
    print("This feature is not needed")
```
[23a]
---

### Don't Repeat Yourself 
DRY kann durch die Vermeidung von redundantem Code erreicht werden. Hier ist ein Beispiel:

```python
# Redundanter Code
def calculate_area(radius):
    return 3.14 * radius * radius

def calculate_volume(radius, height):
    return 3.14 * radius * radius * height
```

Verbesserter Ansatz:

```python
# DRY
def calculate_area(radius):
    return 3.14 * radius * radius

def calculate_volume(radius, height):
    return calculate_area(radius) * height
```
[23a]
---

### Composition Over Inheritance
Composition Over Inheritance kann durch die Kombination von Klassen anstelle von Vererbung erreicht werden. Hier ist ein Beispiel:

```python
class Engine:
    def start(self):
        print("Engine started")

class Car:
    def __init__(self):
        self.engine = Engine()

    def start(self):
        print("Car is starting")
        self.engine.start()
```

[23a]

---


## Entwurfsmuster (Design Patterns)
***
Design Patterns sind bestimmte Code Strukutren, die schonmal ein grobes Muster zur Lösung eines Coding Problemes geben.
* ### **Vorteile:**<br>
    * ### Wiederverwendbarkeit von Code
    * ### Lesbarkeit
    * ### Code Qualität
    * ### Zeitersparnis

---

### Vergleich von Mustern, Algorithmen und Frameworks
***
Es gibt generell drei verschiedene Hauptkategorien von Design Patterns.

* **Strukturmuster:**<br>
    Strukturmuster sind für die Strukturierung von Beziehungen zwischen Klassene und Objekten zuständig.<br>
    Hierbei soll eine gewisse Abstraktion der Klasse geschaffen werden und mit Schnittstellen gearbeitet werden.

* **Verhaltensmuster:**<br>
    Verhaltensmuster sind für die Steuerung von bestimmten Prozessen oder Verhaltensweisen zuständig.<br>
    Sie geben eine Grundstruktur für komplexe Algorithmen und vereinfachen diese.

* **Erzeugungsmuster:**<br>
    Erzeugungsmuster sind für die Erzeugung von Objekten zuständig.<br>
    Sie vereinfachen die Erzeugung von Objekten und ermöglichen eine vereinfachte Prozessdarstellung für bestimmte Instanzen.

[1b]

---

### Entkopplungsmuster
***
Mit Entkopplungsmustern wird ein Systemm ein entkoppelte Teile gegliedert, die unabhängig voneinander funktionieren.
* einzelne Teile kommunizieren über Schnittstellen

* **Vorteil:** Änderungen an einem Teil des Systems haben keine Auswirkungen auf andere Teile des Systems

<br>
<br>
<br>

Im Folgenden werden einige dieser Entkopplungsmuster vorgestellt.

[2b]

---

#### Repository-, Plugin-, Bridge-, Visitor-Pattern
### Repository-Pattern
***
Damit viele unabhängige Teile eins Systems miteinander kommunizieren können wird eine zentralle Ablage erstellt.<br>
Hierbei werden Elemente in die zentralle Ablgage abgelegt und auch wieder von anderen herausgeholt.<br>
Beispiele für solche Ablagen sind Datenbanken Hypertextsysteme oder auch Dateisysteme.

[2b,3b,4b]

---

### Repository-Pattern
***
![:scale 100%](media/Reposity-Patter_UML.png)

[2b,3b,4b]

---

### Repository-Pattern
***

#### Bsp. Online Shop:
Mehrere Teile des Systems müssen auf eine große Menge an verscheidenen Produktdaten zugreifen.<br>
Die UI des OnlineShops braucht die Daten der Produkte die sie anzeigen soll, die bestell Software muss den Preis
und verfügbarkeit der Produkte wissen, und Mitarbeiter in der Logistik brauchen auch gewisse Daten.<br>
Damit alle Teile des Systems die gleichen und fehlerfreie Daten haben, macht es Sinn diese an einer zerntrallen Stelle zu speichern,auf die alle Zugreifen können.

[2b,3b,4b]

---

#### Repository-, Plugin-, Bridge-, Visitor-Pattern
### Plugin-Pattern
***
Bei dem Plugin-Pattern wird die Schnittstelle einer Klasse an eine andere Klasse angepasst.<br>
Zwischen diesen liegt die Plugin-Schnittstelle, die die Kommunikation ermöglicht.<br>
Vorteil hierbei ist, dass die bereits funktionierenden bestehenden Klasse sind refactored werden müssen.<br>

[2b,3b,4b]

---

### Plugin-Pattern
***
![:scale 100%](media/Adapter-Pattern_UML.png)

[2b,3b,4b]

---

### Plugin-Pattern
***
#### Bsp. Anzeige von Texten in einem Zeicheneditor:
Wir haben ein ZeichenProgramm in dem wir auch Texte einfügen wollen.<br>
Dazu brauchen wir eien Klassenbibliothek, die uns die Masse, sprites, berechnungen/formatierung, etc. zur verfügung stellt.<br>
Zum gerenellen erstellen von Visuellen Objekten haben wir die "GrafischesObjekt" Klasse.<br>
Diese vererbt bereits schon an die "Linie" Klasse.<br>
Um jetzt Text einfügen zu können brauche wir eine weitere Klasse "Text" welche die Methoden von "GrafischesObjekt" implementiert.<br>
die Klasse verwendet die Methoden der Bibliotheck aber von aussen kann man mit den gewohnten methoden arbeiten.<br>

[2b,3b,4b]

---

### Plugin-Pattern
***
![BSP](media/Adapter-Pattern_UML_Beispiel.png)

[2b,3b,4b]

---

#### Repository-, Plugin-, Bridge-, Visitor-Pattern
### Bridge-Pattern
***

Bei dem Bridge-Pattern wird die Schnittstelle(Interface) einer Klasse unabhängig von der Implementierung entwickelt.<br>
Das Problem ist dass er sehr unübersichtlich werden kann wenn man die Schnittstelle und Implementation gleichzeitig wetierentwickelt.<br>
Hierfür wird die erweiterung der Schnitsstelle durch weitere Schnitstellen die erbene ermöglicht.<br>
Die Hauptimplementation implementiert dann von der Hauptschnittstelle und weitere Klassen erben dann von dieser.<br>

[2b,3b,4b]

---
### Bridge-Pattern
***
![:scale 90%](media/Bridge-Pattern_UML.png)

[2b,3b,4b]

---

### Bridge-Pattern
***
Bsp. Implementierung verschieder Arten von Fenstern:
Wir haben eine Schnittstelle Fenster die von mehreren Fenster klassen implementiert wird.<br>
Jetzt wollen wir aber eine weitere unterkategorie an Fenstern erstellen, die auch wieder viele gemeinsame Methoden haben.<br>
Diese können wir nicht in der Schnittstelle implementieren, da sie sonst alle Arten von Fenster haben müssten.<br>

Dazu benutzen wir das Bridge Pattern um die Methoden in einer Schnittstelle zu definieren und dabei struktur zu behalten.<br>
Wir erstellen Interfaces die von Fenster erben und die verschiedenen unterkategorien an Fenster darstellen.<br>
Alle implentierungen voin Fenster können jetzt trotzdem von der Haupt Implementierung erben.<br>

[2b,3b,4b]

---

### Bridge-Pattern
***
![BSP](media/Bridge-Pattern_UML_Beispiel.png)

[2b,3b,4b]

---

#### Repository-, Plugin-, Bridge-, Visitor-Pattern
### Visitor-Pattern
***
Das Visitor Pattern wird verwendet wenn mehrere nicht verwandte Objekte gleiche Operationen/Berechnungen ausführen müssen.<br>
Hierfür wird eine Besucher Klasse bereitgestellt auf die alle unabghängig voneinander zugreifen können.<br>

[2b,3b,4b]

---
### Visitor-Pattern
***

![UML](media/Visitor-Pattern_UML.png)

[2b,3b,4b]

---

## Entwurf des Datenmodells
***
Ein Datenmodell ist ein Modell, das beschreibt wie Daten verarbeitet werden.<br>
Die Datenmodulierung dient dazu eine gewisse Struktur für große Datenmengen zu erstellen
und festzulegen wie ein System diese Daten verarbeitet/liest,schreibt.<br>

[5b]

---
### Domain-Driven Design
***
Domain-driven Design(DDD) ist eine Ansatz der Softwareentwicklung, bei dem die Probleme der Geschätsbereiche in den Vordergrund gestellt werden, um sie besser zu verstehen und zu Lösen.<br>
Dies wird umgesetzt durch die verwendung einer einheitlichen Sprache (Fachbegiffe) unter den verschiedenen Geschäftsbereichen.<br>
Mit DDD wird die Geschäftslogik klar in der Software representiert, um die Zusammenarbeit zu fördern.<br>

---

#### Domain vs. Model
***
Die Domain bezieht sich auf das Fachgebiet/Problemfeld, für die die Software da ist.<br>
Sie umfasst die Aspekte der Geschäftsprozzesse und modeliert die Geschäftsanforderungene und Prozesse dementsprechend.<br>

Bei dem Model handelt es sich um die strukturierte Darstellung der Elemente die die Domäne umfasst.<br>
Das Model ist die Representation der Domain in Code/Software form.<br>
Es Dient dazu,die komplexität der Domäne übsersichtlich darzustellen/verwalten und die Kommunikation zwischen den
Fachexperten zu schaffen.<br>

[5b,6b]

---

#### Domain-Driven Design Prozess
***
Der DDD Prozess ist ein systematischer Ansatz zur Entwicklung von Software, der sich auf die Modellierung und Lösung komplexer Probleme in einem bestimmten Fachgebiet konzentriert.<br>
Also generell die entwicklung eines DDD Models.<br>
Dazu müssen Fachexperten und Entwickler zusammen ein Modell erstellen.<br>
Die Fachexperten bringen ihr Wissen über die Domäne mit und die Entwickler sorgen dafür,
dass das Modell in Software umgesetzt wird und eine gewisse Struktur hat.<br>

[5b,6b]

---

#### Entities, value objects, aggregates, services, factories
***
* **Entities:**<br>
Entities sind Objekte die eine Identität haben und über die Zeit verändert werden können.<br>
Entitäten sind unabhängig von ihren Attributen und eine änderung der Attribute ändert nicht die Identität.<br>
z.B: Benutzer mit einer ID.<br>

* **Value Objects:**<br>
Value Objects sind objektähnliche Strukturen ohne eine eigene Identität.<br>
Sie repräsentieren eher Werte oder Konzepte.<br>
Die Gleichheiten von Value Objects werden durch ihre Attribute definiert.<br>
z.B: Koordinaten als Objekt mit den Attributen x und y.<br>

[5b,6b]

---

#### Entities, value objects, aggregates, services, factories
***

* **Aggregates:**<br>
Aggregates sind Gruppen von miteinander verbundenen Objekten, die als eine einzige Einheit betrachtet werden.<br>
Sie besitzen eine Wurzel, die der einzige zugangspunkt voin außen ist(Schnittstelle).<br>

* **Services:**<br>
Services repräsentieren Operationen oder Aufgaben, die nicht natürlich zu einem bestimmten Aggregate oder einer Entity gehören.<br>
Sie können Domäne übergreifende Operationen bereitstellen und sind unabhängig von den Aggregates, sowie zustandslos.<br>
z.B: Ein Berechnungsservice, der Steuern üfr einen Einkaufsborb berechnet.<br>

* **Factories:**<br>
Factories sind Mechanismen zur Erzeugung von komplexen Objekten oder Aggregaten(vgl. Faktory Pattern).<br>
Faktories kapseln den Erstellungsprozess und sorgen für eine gewisse konstitenz der Objekte.<br>
z.B: Eine "User-Faktory" die einen neuen User mit standard Attributen ertsellt.<br>

[5b,6b]

---

#### Ubiquitäre Sprache
***
Eine Hauptmerkmal eines DDD ist die ubiquitäre Sprache.<br>
Sie beschreibt die Fachlichen gegbenheiten der Domänen und wird überall in der Software benutzt.<br>
Zum Beispiel wird bit der ubiquitären Sprache Elemente, Prozesse oder Konzepte der Domänen beschrieben.<br>
Dadurch wird die Kommunikation zwischen den Fachexperten und Entwicklern vereinfacht, da Missverständisse und
Fehlinterpretationen vermieden werden.<br>

[5b]

---

#### Anemic Domain Model
***
Das Anemic Domain Model ist ein Anti-Patter, bei dem das Domönemodell zwar Objekte für diese enthält,
diese aber nur Datenstrukturen sind die keine geschäftslogische Funktionalität beseitzen.<br>
Die Datenstrukutren(Entitäten und Objekte) sind nur Datencontainer, sie besitzen keine funktionalität.<br>
Die eigentliche Geschäftslogik wird in externene Services ausgelagert.<br>
Die Domäne Objekte haben aber nur minimale Funktionen um ihr verhalten auszudrücken. <br>

[6b,7b]

---

#### Vorteile, Nachteile
***
**Vorteile:**<br>
* Fachexperten haben ein besseres Verständniss der verschiedenen Domänen
    * fördert Zusammenarbeit und kommunikation
* Durch einheitliche(ubiqquitäre) Sprache wird die Kommunikation besonders gefördert
* Einheitliche Struktur der Software
    * Domäne wird klar repräsentiert

---

#### Vorteile, Nachteile
***
**Nachteile:**<br>
* Einführung der DDD ist sehr Zeitintensiv
    * Fachexperten müssen sich mit der Entwicklung der Software beschäftigen
    * Fachexperten müssen sich mit anderen Domänen beschäftigen
    * Entwickler müssen sich mit der Domäne und Software beschäftigen
* Nicht immer notwendig
    * Bei kleinen Domänen ist die Kommunikation und Strukturierung nicht so komplex

---

## Entwurf der Benutzerschnittstelle
***
Eine Benutzerschnittstelle(User Interface, UI) ist die Schnittstelle zwischen einem Benutzer und einem System, welche die
einfache Benutzung eines Systems ermöglicht.<br>
Sie können in verschiedenen Formen auftreten und bieten vielfältige Möglichkeiten für die Kommunikation zwischen Benutzern und der Software.<br>

Im Folgenden werden einige Aspekte der modelierung von Benutzerschnittstellen vorgestellt.<br><br>
[8b]

---

### UI Modelling
***
UI Modelling ist der Prozess der Erstellung einer Benutzerschnittstelle.<br>
Er umfasst einige Aspekte, um eine gute zu Bediennde UI zu erstellen.<br>
Bei der Modelligierung einer UI muss man darauf achten, dass man ein ansprechendes Design hat,
die Benutzung einfach ist, die UI auch die gewünschten Funktionen hat und eine gute Dokumentation für die User vorhanden ist.<br>
Im folgenden werden einige Schritte angezeigt um diese Aspekte zu erfüllen.<br>

[6b,9b]

---

#### Wireframe vs Storyboard vs Wireflow vs Mockup vs Prototyping
***
**Wireframe:**<br>
* Grundlegede Visuelle Darstellung
* platziereung von Text, Bilderun, Buttons, etc.
* Kein Fokus auf Designästhetik
* Benutzerfreundliche Platzierung der Elemente

**Storyboard:**<br>
* Sammlung von Visuellen Darstellungen
* Darstellung von Interaktionen
* Simulation von Benutzererfahrungen
    * User-Cases

**Wireflow:**<br>
* Kombination aus Wireframe und Storyboard
* Verbindung zwischen Interaktionen und UI
* Darstellung der Struktur der "Screens" und Verbindungen zwischen diesen

[6b,9b]

---

#### Wireframe vs Storyboard vs Wireflow vs Mockup vs Prototyping
***
**Mockup:**<br>
* Visuelle Darstellung der UI
* Mehr Details und Designästhetik als Wireframe
* Erster realistischerer Eindruck der UI
    * Enthält Bilder, Farben und generelles Design

letzter Schritt bevor ersten Prototyp erstellt wird

* **Prototyping:**<br>
* Interaktive Simulation der UI
    * Noch keine funktionale Logik(Click Dummy)
* Testen der Benutzererfahrung
* Verbesserung von Aspekten wie Benutzerfreundlichkeit, Design, etc.

[6b,9b]

---

### Usability vs. User experience (UX) vs. Customer experience (CX)
***
Die Begriffe Usability, User Experience (UX) und Customer Experience (CX) sind alle eng miteinander verbunden, beziehen sich jedoch auf unterschiedliche Aspekte und Perspektiven im Kontext von Design und Kundeninteraktion. Hier sind die Unterschiede zwischen ihnen:

* **Usability:**<br>
Usability bezieht sich auf die Benutzerfreundlichkeit oder Gebrauchstauglichkeit der Software.<br>
Es misst und konzentriet sich darauf, wie effektiv, effizient und zufriedenstellend Benutzer bestimmte Aufgaben mit einem Produkt ausführen können.<br>

**z.B.:** Ein einfach zu bediendendes Formular mit klaren Anweisungen und Struktur die angibt wo was einzutragen ist.<br>

[6b,10b]

---

* **User Experience (UX):**<br>
Die User Experience umfasst alle Aspekte der Wechselwirkung eines Benutzers mit der Software, einschließlich seiner Wahrnehmungen, Emotionen und Reaktionen während und nach der Interaktion.<br>
Es bezieht sich auf die gesamte Erfahrung des Benutzers mit dem Produkt, es umfast also auch sowas wie Design und Ästhetik.<br>

**z.B.:** Wenn unser Formular zwar sehr einfach zu Bedienen ist, aber das Design ein sehr schlichtes grelles neon grün ist, wird die UX nicht so gut sein.<br>

* **Customer Experience (CX):**<br>
Die Customoer Experience geht noch einen Schritt weiter.<br>
Es umfasst nicht nur die Erfahrung mit der UI sondern auch generell die Erfahrung, die ein Kunde mit einem Unternehmen macht.<br>
Es betont die gesammte Reise/Interktion die ein Kunde mit dem Unternehmen macht, vom ersten Kontakt bis zum Kauf und darüber hinaus.<br>

**z.B** Ein Kunde hat unser Formular für eine bestellung ausgeführt, aber die Lieferung hat lange gedauert und der Kundenservice war schlecht.<br>

[6b,10b]

---

### Nielsen's 10 Usability Heuristic Prinzipien für das UI-Design
***
Nielsen's 10 Usability Heuristic Prinzipien sind 10 Prinzipien die bei der Erstellung einer UI beachtet werden sollten.<br>
1. Das System sollte User mittels Feedback darüber informieren, was gerade passiert.
1. Gemeinsamkeit zwischen dem System und der realen Welt. Die Anweundung sollte die Sprache des Benuters sprechen. Dieser kann wahrscheinlich nicht mit Programierspezifischen Begriffen umgehen.
1. User machen Fehler. Das System sollte darauf ausgelegt sein, dass Fehler passieren und die möglichkeite bieten diese rückgängig zu machen.
1. Einheitliches Design und Strutur sollte eingehalten werden.
1. Noch besser als Fehlerrückgängig machen ist die Fehler eines Users komplett zu vermieden. Das System sollte so gestaltet sein, dass Fehler nur schwer passieren können.

[11b]

---

### Nielsen's 10 Usability Heuristic Prinzipien für das UI-Design
***
6 . Einfache Anleitung und sichtbare Informationen<br>
7 . Flexibilität und Effektivität. Der User sollte die Möglichkeit haben abkürzungen zu benutzen was die UI auch für erfahrenen benutzer effektiv macht.<br>
8 . Die UI sollte minimalistisch designed sein. Es sollten nur die nötigsten Informationen angezeigt werden.<br>
9 . Die UI sollte dem User auch helfen Fehler zu erkene und zu vermeiden, um zukünfitge Fehler zu vermeiden.<br>
10 . Hilfe und Dokumentation. Die UI sollte dem User die Möglichkeit geben sich zu informieren und Hilfe zu holen.<br>

[11b]

---

class: center, middle

# Fragen?

---



# Quellen
***

[1a] : https://t2informatik.de/wissen-kompakt/softwareentwurf/

[2a] : https://www.dev-insider.de/was-ist-ein-software-entwurf-a-ac9e018da98039bb8e4744beaa9a126f/

[3a] : https://esb-dev.github.io/mat/swt-entwurf-l.pdf
[4a] : https://chat.openai.com/c/e5ef4299-1f76-491e-b216-d702c8ec98ae frage: was ist was ist 
Orthogonalität im Entwurfsziel?

[5a] : https://www.isf.cs.tu-bs.de/cms/teaching/2012w/se1/VL5.pdf 

[6a] : https://beckassets.blob.core.windows.net/product/readingsample/23641827/23641827_leseprobe.pdf
[7a] : https://de.wikipedia.org/wiki/Abstraktion_(Informatik)

[8a] : https://de.wikipedia.org/wiki/Modularit%C3%A4t#Funktionsprinzipien

[9a] : https://de.wikipedia.org/wiki/Gesetz_von_Demeter#:~:text=Das%20Gesetz%20von%20Demeter%20(englisch,ihrer%20unmittelbaren%20Umgebung%20kommunizieren%20sollen.

---

# Quellen
***
[10a] : https://www.dev-insider.de/was-bedeutet-inversion-of-control-a-1110688/

[11a] : https://it-talents.de/it-wissen/was-ist-dependency-injection/
[12a] : http://www.scalingbits.com/java/javakurs1/oop/architektur

[13a] : https://t2informatik.de/wissen-kompakt/kiss-prinzip/

[14a] : Entwurfsprinzipien und Konstruktionskonzepte der Softwaretechnik : Link zum Buch : https://link.springer.com/chapter/10.1007/978-3-658-20055-8_3

[15a] : https://t2informatik.de/wissen-kompakt/yagni-prinzip/ 

[16a] : https://learn.microsoft.com/de-de/dotnet/architecture/modern-web-apps-azure/architectural-principles

[17a] : https://de.wikipedia.org/wiki/Don%E2%80%99t_repeat_yourself

---

# Quellen
***
[18a] : https://de.wikipedia.org/wiki/Komposition_an_Stelle_von_Vererbung

[19a] : https://www.microconsult.de/blog/2019/05/fl_solid-prinzipien/
[20a] : https://it-talents.de/it-wissen/prozedurale-vs-objektorientierte-programmierung/

[21a] : https://chat.openai.com/c/e5ef4299-1f76-491e-b216-d702c8ec98ae frage: was ist prozedural und objektorientiert Kopplung
[22a] : https://de.wikipedia.org/wiki/Komposition_an_Stelle_von_Vererbung

[23a] : https://chat.openai.com/c/d2358263-c323-47b3-a0a7-43b1be51bf85 Frage: Gib mir Beispiele zu * Abstraktion, Modularität, Law of demeter, Dependency Injection, Inversion of Control, Separation of Concerns, Keep It Stupid Simple, You Ain’t Gonna Need It, Don't repeat yourself, Composition Over Inheritance

---

# Quellen
***

[1b] :https://www.ionos.de/digitalguide/websites/web-entwicklung/was-sind-design-patterns/

[2b] :https://www.inf.fu-berlin.de/lehre/WS02/SWT/slides4pdf/24_LE_23B.pdf

[3b] :https://de.wikipedia.org/wiki/Besucher_(Entwurfsmuster)#:~:text=Der%20Besucher%20(englisch%20visitor%20oder,dient%20der%20Kapselung%20von%20Operationen

[4b] : https://www.hsbi.de/elearning/data/FH-Bielefeld/lm_data/lm_1359639/pattern/visitor.html

[5b] : https://de.wikipedia.org/wiki/Datenmodell

[6b] : https://chat.openai.com/

---
# Quellen
***

[7b] : https://martinfowler.com/bliki/AnemicDomainModel.html

[8b] : https://de.wikipedia.org/wiki/Schnittstelle

[9b] : https://en.wikipedia.org/wiki/User_interface_modeling

[10b] : https://usabilitygeek.com/confuse-user-experience-customer-experience/#:~:text=UXers%20tend%20to%20be%20aware,a%20particular%20app%20or%20website.

[11b] : https://usersnap.com/de/blog/usability-nielsen/