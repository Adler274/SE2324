class: center, middle

## [Software Engineering](../../praesentationen.html)

#### Kapitel 10

## Software Development Lifecycle (SDLC) & Wartung von Software (Software Maintainance)


Simon Fedrau, Sascha Hahn

---
# Inhalt
***

1. Software Development Lifecycle (SDLC)

1. Wartung von Software (Software Maintainance)

1. Zusammenfassung

1. Quellen

---


### Fragen
***
* Welche Klassische (sequenzielle) Vorgehensmodelle gibt es und wofür sind sie da?

* Welche Agile Vorgehensmodelle gibt es?

* Welche Evolutionäre Vorgehensmodelle gibt es?

* In welchen Situationen setzt man welches Vorgehensmodelle ein?

* Welche Arten der Software Wartung gibt es, und was ist in dem Kontext Legacy-Code 

* Was sind Ursachen für eine Software Änderung


---
### Software Development Lifecycle (SDLC)
***

Der Softwareentwicklungszyklus ist der kosteneffektive und zeitsparende Prozess, den Entwicklungsteams verwenden, um hochwertige Software zu entwerfen und zu entwickeln. Das Ziel des SDLC ist es, die Projektrisiken durch vorausschauende Planung zu minimieren, damit die Software die Erwartungen der Kunden während der Produktion und darüber hinaus erfüllt. Diese Methodik umreißt eine Reihe von Schritten, die den Softwareentwicklungsprozess in Aufgaben unterteilen, die Sie zuweisen, abschließen und messen können.

[1a]
---
### Phasen im Software-Lebenszyklus
***

* Anforderungsanalyse und -spezifikation
* Entwurf
* Implementierung 
* Test
* Bereitstellung 
* Wartung und Aktualisierung

![:scale 50%](media\Softwarelebenszyklus.png)


[1a]
---
### Klassische (sequenzielle) Vorgehensmodelle
***

Ein Vorgehensmodell ist eine abstrakte Darstellung eines Softwareprozesses. Der Prozess wird hierbei immer nur aus einer bestimmten Perspektive dargestellt. Daher beinhaltet ein Vorgehensmodell immer nur einen Teil der Informationen über den Prozess. Dies hat allerdings den Vorteil, dass die den einzelnen Softwareprozessen zugrunde liegenden Prinzipien übersichtlich und verständlich dargestellt werden können. 

[2a]

---
### Wasserfallmodell
***

Der Name Wasserfall kommt von der häufig gewählten grafischen Darstellung der als Kaskade angeordneten Projektphasen. In der betrieblichen Praxis ist es traditionell ein weitverbreitetes Vorgehensmodell, von dem es viele Varianten gibt. 


![:scale 60%](media\Waterfall_model.png)

[3a]
---
### V-Modell
***
* Entwicklungsphasen:
    * Diese Phasen entsprechen im Wesentlichen den Schritten im Wasserfallmodell.

* Testphasen:
    * Jede Entwicklungsphase ist mit einer entsprechenden Testphase verknüpft. Während der Entwicklungsphasen werden die zugehörigen Tests vorbereitet, und die eigentlichen Tests werden während der Testphasen durchgeführt.

![:scale 60%](media\v-modell.jpg)

[4a]
---
### Agile Vorgehensmodelle
***

Der eindeutige Mehrwert der agilen Vorgehensmodelle besteht darin, dass sich durch ihre iterative Entwicklung, das kurzfristige Feedback der Kunden und die intensive Kommunikation der gesamte Entwicklungsprozess sehr schlank und flexibel gestaltet.

![:scale 50%](media\Vorgehensmodelle.JPG)

[5a] [6a]
---
### PDCA-Zyklus
***
* Plan (Planen): Festlegung von Zielen und Entwickeln eines Umsetzungsplans.

* Do (Umsetzen): Ausführung des Plans, um gewünschte Verbesserungen zu erzielen.

* Check (Überprüfen): Messen und Bewerten der Ergebnisse im Vergleich zu den Zielen.

* Act (Handeln): Auf Grundlage der Überprüfung werden Entscheidungen getroffen, und der Plan wird angepasst, um den Prozess weiter zu verbessern.

![:scale 40%](media\PDCA_Zirkel.png)

[7a] [8a]

---
### OODA loop
***


* Fortschrittsüberwachung, Feedbacksammeln und Probleme/Chancen identifizieren.


* Analyse der gesammelten Informationen, Identifikation von Mustern und Bewertung der Situation.


* Basierend auf der Analyse werden Anpassungen am Projektplan, Änderungen in den Anforderungen oder strategische Entscheidungen getroffen.


* Umsetzung der Entscheidungen durch konkrete Maßnahmen wie Codeaktualisierung, Aufgabenneuplanung oder Implementierung neuer Funktionen.

![:scale 20%](media\ooda-loop.png)

[9a]

---
### Stacey-Matrix
***




![:scale 80%](media\stacey_Matrix.png)

[10a]

---
### 4 Werte und 12 Prinzipien
***

* Individuen und Interaktionen mehr als Prozesse und Werkzeuge

* Funktionierende Software mehr als umfassende Dokumentation

* Zusammenarbeit mit dem Kunden mehr als Vertragsverhandlung

* Reagieren auf Veränderung mehr als das Befolgen eines Plans

[24a]
---
### 4 Werte und 12 Prinzipien
***

![:scale 80%](media\Agile-Prinzipien.jpg)

[24a]
---
#### Anti patterns
***

* Planungsverweigerung

* Alles für den Kunden

* Konkurrierende Kräfte

* Sprechender Code ist genügend Dokumentation

* Allzeit änderungsbereit

* Unzuverlässigkeitsformel: Spontanität = Agilität

* I believe in Miracles

* Der „agile Ad-hoc-Prozess“


![:scale 40%](media\antipattern.jpg)


[22a]

---
### XP, Scrum, Kanban (jeweils kurze Darstellung)
***

* Extreme Programming (XP):
    - Agile Softwareentwicklungsmethode
    - Betont kontinuierliches Feedback, gemeinsame Verantwortung und Flexibilität
    - Schlüsselpraktiken: Paarprogrammierung, TDD, kontinuierliche Integration

* Scrum:
    - Agiles Rahmenwerk für Produktentwicklung und -management
    - Organisiert Arbeit in Sprints (zwei bis vier Wochen)
    - Definiert klare Rollen (Product Owner, Scrum Master, Entwicklungsteam) und Artefakte

* Kanban:
    - Agiler Ansatz basierend auf visueller Darstellung von Arbeit
    - Aufgaben werden auf einem Kanban-Board in Spalten organisiert
    - Ziel: Workflow visualisieren, Engpässe identifizieren, kontinuierliche Verbesserung fördern

[11a]

---
### Evolutionäre Vorgehensmodelle
***


Evolutionäres Design ist ein Entwurfsansatz in der Softwareentwicklung und kommt überwiegend im Kontext des Extreme Programming zum Einsatz. Im Gegensatz zu geplantem Design propagieren die Befürworter des evolutionären Ansatzes die Entwicklung eines Softwaresystems in kleinen Schritten.

[12a]
---
### Prototyping (Prototype Model)
***

Beim evolutionären Prototyping wird die Anwendung nach und nach erweitert. Dabei werden vor allem die Rückmeldungen der zukünftigen Nutzer bzw. des Auftraggebers genutzt. Der Prototyp wird dabei stets lauffähig gehalten und bis zur Produktreife weiterentwickelt. 



Ziel: Anhand der Grundfunktionalitäten die Akzeptanz beim Nutzer und die Notwendigkeit ergänzender Funktionen zu überprüfen
  Wichtigstes Ergebnis: Ein Programm mit den Grundfunktionalitäten


[13a]
---
### Vor und Nachteile der Vorgehensmodelle
***

**Agile Vorgehensmodelle:**

| Vorteile                        | Nachteile                                |
|---------------------------------|------------------------------------------|
| Hohe Flexibilität und Anpassung | Mögliche Komplexität in großen Projekten |
| Enge Kundenbeteiligung          | Hohe Anforderungen an Teammitglieder     |
| Kontinuierliche Lieferung       | Möglicher Mangel an umfassender Dokumentation |
| Fokus auf Wert durch funktionierende Software |                                        |
| Schnelle Markteinführung        |        |                       |


[14a]
---
### Vor und Nachteile der Vorgehensmodelle
***


**Evolutionäre Vorgehensmodelle:**

| Vorteile                        | Nachteile                                |
|---------------------------------|------------------------------------------|
| Schrittweise Verbesserungen     | Zeit- und Ressourcenaufwand              |
| Flexibilität                    | Mögliche Dokumentationsherausforderungen |
| Frühzeitiges Kundenfeedback     | Eventuell begrenzte Kundenbeteiligung    |
| Fokussiert auf Prototyping      |  |         |        

[14a]

---
### Vor und Nachteile der Vorgehensmodelle
***


**Klassische (Sequenzielle) Vorgehensmodelle:**

| Vorteile                        | Nachteile                                |
|---------------------------------|------------------------------------------|
|  Klare Struktur und Planung    |   Geringe Anpassungsfähigkeit an Änderungen           |
|  Umfassende Dokumentation                  | Lange Entwicklungszyklen |
|  Gut geeignet für stabile Anforderungen    |  Geringe Kundenbeteiligung während der Entwicklung   |
         
[14a]

---
### Empfehlungen, unter welchen Bedingungen welches Vorgehensmodell sinnvoll ist
***

 **Klassisches (sequenzielle) Vorgehensmodell:**

* Stabile Anforderungen: Wenn die Anforderungen gut verstanden und stabil sind, eignet sich ein sequenzielles Modell.


   * Geringe oder keine Änderungserwartung: Wenn nicht erwartet wird, dass sich die Anforderungen während des Entwicklungsprozesses erheblich ändern.

[23a]
---
### Empfehlungen, unter welchen Bedingungen welches Vorgehensmodell sinnvoll ist
***

**Agiles Vorgehensmodell:** 

* Dynamische Anforderungen: Wenn die Anforderungen sich ändern oder nicht vollständig vor Projektbeginn bekannt sind.

* Kundeninteraktion und -beteiligung: Wenn eine enge Zusammenarbeit mit dem Kunden und schnelle Anpassungen wichtig sind.
Inkrementelle Entwicklung: Wenn die schrittweise Bereitstellung von Funktionen bevorzugt wird.


[23a]
---
### Empfehlungen, unter welchen Bedingungen welches Vorgehensmodell sinnvoll ist
***
**Evolutionäres Vorgehensmodell:**

    
* Komplexe Projekte: Bei komplexen Projekten mit unsicheren Anforderungen, bei denen eine schrittweise Entwicklung bevorzugt wird.

* Forschung und Entwicklung: In Fällen, in denen die Entwicklung als Forschungsprozess betrachtet wird und iterative Prototypen wichtig sind.

[23a]
---
### Wartung von Software (Software Maintainance)
***
Die Wartung von Software, auch als Software Maintenance bekannt, bezieht sich auf den Prozess der Modifikation und Pflege einer Softwareanwendung nach ihrer Bereitstellung.

1. Korrigierende Wartung (Corrective Maintenance):
    * Ziel: Behebung von Fehlern oder Mängeln in der Software.

2. Adaptive Wartung (Adaptive Maintenance):
    * Ziel: Anpassung der Software an Änderungen in der Umgebung, wie Betriebssystem-Upgrades.
3. Perfective Wartung (Perfective Maintenance):
    * Ziel: Verbesserung der Softwareleistung, Funktionalität.

4. Preventive Wartung (Preventive Maintenance):
    * Ziel: Verhinderung zukünftiger Probleme oder Fehlfunktionen.

[15a] [16a]

---
### Definition Software-Wartung und Legacy-Code
***

In der Softwaretechnik bezeichnet der Begriff Softwarewartung „die Veränderung eines Softwareprodukts nach dessen Auslieferung, um Fehler zu beheben, Performanz oder andere Attribute zu verbessern oder Anpassungen an die veränderte Umgebung vorzunehmen.


**Legacy-Code**

Der Begriff Altsystem oder Legacy-System oder im engeren Sinne Legacy-Code bezeichnet in der Informatik eine etablierte, historisch gewachsene Anwendung im Bereich Unternehmenssoftware


[17a]
---
### Evolution von Software
***

Software-Evolution ist ein Begriff aus der Softwaretechnik, im Speziellen aus der Softwarewartung, und beschreibt den Prozess, der folgt, nachdem ein Softwaresystem entwickelt und ausgeliefert wurde. Nach Auslieferung und Benutzung kommen neue Anforderungen dazu und alte Anforderungen verändern sich. Teile des Softwaresystems müssen möglicherweise korrigiert werden, da Fehler auftreten, die zuvor nicht bemerkt wurden. Das System muss an eine neue Plattform adaptiert werden. Die Performance muss verbessert werden und andere nichtfunktionale Anforderungen müssen überprüft werden.

[19a]

---
### Ursachen für Änderungen an Software
***

* Fehlerkorrektur (Bugfixing)

* Neue Anforderungen

* Verbesserungen und Optimierungen

* Sicherheitsaktualisierungen
* Technologischer Fortschritt

* Gesetzliche Anforderungen
* Hardwareänderungen

* Benutzerfeedback
* Lebenszyklus-Management

[20a]
---
#### Arten von Änderungen an Software
***
Die Klassifizierung von Softwareänderungen nach ihrer Art erfolgt oft anhand von vier Haupttypen, korrektive, präventive, perfektionierende und adaptive Änderungen. 

---
### Korrektive, präventive, perfektionierende, adaptive Änderungen
***
* Korrektive Änderungen:
    Ziel: Behebung von Fehlern oder Bugs in der Software.

* Präventive Änderungen:
    Ziel: Vermeidung potenzieller zukünftiger Probleme oder Risiken.

* Perfektionierende Änderungen:
    Ziel: Verbesserung der Leistung, Benutzerfreundlichkeit oder anderer Aspekte der Software, die nicht unbedingt mit Fehlern zusammenhängen.

* Adaptive Änderungen:
    Ziel: Anpassung der Software an veränderte Umgebungen, Plattformen oder Anforderungen.

[21a]

---

class: center, middle

# Fragen?

---

# Quellen
***
[1a]  : https://aws.amazon.com/de/what-is/sdlc/

[2a]  : https://de.wikipedia.org/wiki/Vorgehensmodell_zur_Softwareentwicklung

[3a]  : https://de.wikipedia.org/wiki/Wasserfallmodell

[4a]  : https://de.wikipedia.org/wiki/V-Modell

[5a]  : https://fh-bielefeld-mif-sw-engineerin.gitbooks.io/klausurthemen/content/continuous-software-engineering/Agile-Vorgehensmodelle.html#:~:text=Agile%20Vorgehensmodelle%20sind%20eine%20Methode,%2DAufwand%20verbunden%20sind%2C%20abl%C3%B6sen.

[6a]  : https://www.rewion.com/agiles-it-projektmanagement-vorgehensmodelle/

[7a]  : https://de.wikipedia.org/wiki/Demingkreis

[8a]  : https://karrierebibel.de/pdca-zyklus/

---

# Quellen
***

[9a]  : https://waydev.co/ooda-agile-data-driven/

[10a] : https://digitaleneuordnung.de/blog/stacey-matrix/

[11a] : https://www.heise.de/blog/Extreme-Programming-Scrum-Kanban-was-fuer-wen-4951363.html

[12a] : https://de.wikipedia.org/wiki/Evolution%C3%A4res_Design

[13a] : https://de.wikipedia.org/wiki/Prototyping_(Softwareentwicklung)

[14a] : https://chat.openai.com/ frage: Schreib mir einen Vergleich zwischen den Agilen Vorgehensmodellen  und den Evolutionären Vorgehensmodellen 

[15a] : https://cpl.thalesgroup.com/de/software-monetization/four-types-of-software-maintenance

[16a] : https://www.geeksforgeeks.org/software-engineering-software-maintenance/

[17a] : https://de.wikipedia.org/wiki/Softwarewartung


---

# Quellen
***

[18a] : https://de.wikipedia.org/wiki/Altsystem

[19a] : https://de.wikipedia.org/wiki/Software-Evolution#:~:text=Software%2DEvolution%20ist%20ein%20Begriff,und%20alte%20Anforderungen%20ver%C3%A4ndern%20sich.

[20a] :  https://chat.openai.com/  frage: was sind Ursachen für Änderungen an Software?

[21a] : https://cpl.thalesgroup.com/de/software-monetization/four-types-of-software-maintenance

[22a] : https://entwickler.de/agile/agile-anti-patterns-001

[23a] : https://www.rewion.com/klassisches-it-projektmanagement/

---


