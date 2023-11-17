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
### Jeweils Implementierungsbeispiel






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