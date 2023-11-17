class: center, middle

## [Software Engineering](../../praesentationen.html)

#### Kapitel 7

# Softwareentwurf

Simon Fedrau, Sascha Hahn

---

# Inhalt
***

1. Softwareentwurf

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
### Vergleich von Mustern, Algorithmen und Frameworks
### Entkopplungsmuster
#### Repository-, Plugin-, Bridge-, Visitor-Pattern
##### Entwurfsproblem, das die Entwurfsmuster lösen
##### UML-Diagramme zur Visualisierung der Entwurfsmuster
##### Klassendiagramm, Sequenzdiagramm
##### Anwendungsbeispiele
##### Implementierungsbeispiel
### Weitere Entwurfsmuster, die Sie als relevant erachten
#### (Bitte keine weiteren "Gang of Four Patterns")
## Entwurf des Datenmodells
### Domain-Driven Design
#### Domain vs. Model
#### Domain-Driven Design Prozess
#### Entities, value objects, aggregates, services, factories
#### Ubiquitäre Sprache
#### Anemic Domain Model
#### Beispiel, Vorteile, Nachteile
## Entwurf der Benutzerschnittstelle
### UI Modelling
#### Wireframe vs Storyboard vs Wireflow vs Mockup vs Prototyping
### Usability vs. User experience (UX) vs. Customer experience (CX)
### Nielsen's 10 Usability Heuristic Prinzipien für das UI-Design
### Shneidermans's 8 Golden Rules
### Norman's 7 Principles

---
class: center, middle

# Fragen?

---
# Quellen
***

[1a] : https://t2informatik.de/wissen-kompakt/softwareentwurf/
[2a] : https://www.dev-insider.de/was-ist-ein-software-entwurf-a-ac9e018da98039bb8e4744beaa9a126f/
[3a] : https://esb-dev.github.io/mat/swt-entwurf-l.pdf
[4a] : https://chat.openai.com/c/e5ef4299-1f76-491e-b216-d702c8ec98ae frage: was ist was ist Orthogonalität im Entwurfsziel?
[5a] : https://www.isf.cs.tu-bs.de/cms/teaching/2012w/se1/VL5.pdf 
[6a] : https://beckassets.blob.core.windows.net/product/readingsample/23641827/23641827_leseprobe.pdf
[7a] : https://de.wikipedia.org/wiki/Abstraktion_(Informatik)
[8a] : https://de.wikipedia.org/wiki/Modularit%C3%A4t#Funktionsprinzipien
[9a] : https://de.wikipedia.org/wiki/Gesetz_von_Demeter#:~:text=Das%20Gesetz%20von%20Demeter%20(englisch,ihrer%20unmittelbaren%20Umgebung%20kommunizieren%20sollen.

[10a] : https://www.dev-insider.de/was-bedeutet-inversion-of-control-a-1110688/
[11a] : https://it-talents.de/it-wissen/was-ist-dependency-injection/
[12a] : http://www.scalingbits.com/java/javakurs1/oop/architektur
[13a] : https://t2informatik.de/wissen-kompakt/kiss-prinzip/
[14a] : Entwurfsprinzipien und Konstruktionskonzepte der Softwaretechnik : Link zum Buch : https://link.springer.com/chapter/10.1007/978-3-658-20055-8_3
[15a] : https://t2informatik.de/wissen-kompakt/yagni-prinzip/ 
[16a] : https://learn.microsoft.com/de-de/dotnet/architecture/modern-web-apps-azure/architectural-principles
[17a] : https://de.wikipedia.org/wiki/Don%E2%80%99t_repeat_yourself
[18a] : https://de.wikipedia.org/wiki/Komposition_an_Stelle_von_Vererbung
[19a] : https://www.microconsult.de/blog/2019/05/fl_solid-prinzipien/
[20a] : https://it-talents.de/it-wissen/prozedurale-vs-objektorientierte-programmierung/
[21a] : https://chat.openai.com/c/e5ef4299-1f76-491e-b216-d702c8ec98ae frage: was ist prozedural und objektorientiert Kopplung
[22a] : https://de.wikipedia.org/wiki/Komposition_an_Stelle_von_Vererbung
[23a] : https://chat.openai.com/c/d2358263-c323-47b3-a0a7-43b1be51bf85 Frage: Gib mir Beispiele zu * Abstraktion, Modularität, Law of demeter, Dependency Injection, Inversion of Control, Separation of Concerns, Keep It Stupid Simple, You Ain’t Gonna Need It, Don't repeat yourself, Composition Over Inheritance
