class: center, middle

## [Software Engineering](../../praesentationen.html)

#### Kapitel 10

# Softwareprüfung

Simon Fedrau, Sascha Hahn

---
# Inhalt
***

1. Softwareprüfung
  * Bug vs Issue vs Flaw vs Fault vs Failure vs Error vs Defect
  * Continuous Testing vs. Shift-left-testing vs Shift-right-testing vs Testing-in-production
  * Testing Anti Patterns
  * Validierung vs formale Verifikation
  * Statischer Test von Software
  * Dynamischer Test von Software

1. Softwaremessung

1. Zusammenfassung

1. Quellen

---
### Softwareprüfung


Beim Softwaretest wird evaluiert und überprüft, ob ein Softwareprodukt oder eine Anwendung das tut, was sie tun soll. Gute Tests ermöglichen die Vermeidung von Fehlern, die Reduzierung der Entwicklungskosten und die Verbesserung der Leistung.


---
### Bug vs Issue vs Flaw vs Fault vs Failure vs Error vs Defect



| Fehler | Beschreibung |
|:------:|:----------:|
| **Bug** | Ein Bug bezieht sich auf einen Fehler im Code oder im Design einer Software, der unerwünschtes Verhalten verursacht. Bugs können verschiedene Arten von Fehlern repräsentieren |
| **Issue** | Der Begriff "Issue" ist allgemeiner und kann sowohl Bugs als auch andere Probleme, wie Aufgaben, Verbesserungsvorschläge oder allgemeine Anfragen, umfassen. Es ist ein allgemeinerer Begriff, der alles, was die Entwicklung oder den Betrieb einer Software beeinflusst, beschreiben kann.|
| **Flaw** | Ein Flaw deutet auf einen Fehler oder eine Schwäche in einem System oder Prozess hin. Es kann sich auf Designfehler, Implementierungsfehler oder andere Mängel beziehen, die die Qualität oder Leistung beeinträchtigen |

[1a] [2a]
---
### Bug vs Issue vs Flaw vs Fault vs Failure vs Error vs Defect


| Fehler | Beschreibung |
|:------:|:----------:|
| **Fault** | Ein Fault ist ein Fehler in der Implementierung oder im Code, der zu einem Defekt führen kann. Ein Fault liegt vor, wenn ein Entwickler einen Fehler macht, der zu unerwünschtem Verhalten führen kann |
| **Failure** |Ein Failure tritt auf, wenn das System oder die Software nicht mehr wie erwartet funktioniert und die Anforderungen nicht erfüllt. Failures sind das sichtbare Ergebnis von Defekten oder Fehlern und können durch Bugs oder andere Probleme verursacht werden |
| **Error** |Ein Error ist ein menschliches Handeln, das zu einem Defekt führt. Dies könnte ein Schreibfehler im Code, ein Algorithmusfehler oder ein Verständnisfehler bei den Anforderungen sein |
| **Defect** | Ein Defect ist ein Mangel oder Fehler im Code oder Design, der zu einem unerwünschten Ergebnis führen kann. Defekte können die Ursache von Bugs, Failures oder anderen Problemen sein |

[1a] [2a]

---
### Continuous Testing vs. Shift-left-testing vs Shift-right-testing vs Testing-in-production

![:scale 60%](media\shift-left-right-continuous-testing.png)

**Continuous Testing:** 

  Continuous Testing ist ein Ansatz, bei dem Tests automatisiert und kontinuierlich während des gesamten Entwicklungs- und Bereitstellungsprozesses durchgeführt werden. Das Ziel besteht darin, frühzeitig Feedback über mögliche Defekte oder Probleme zu erhalten und die Qualität der Software kontinuierlich sicherzustellen.

[4a]

---
### Continuous Testing vs. Shift-left-testing vs Shift-right-testing vs Testing-in-production

![:scale 60%](media\shift-left-right-continuous-testing.png)


**Shift-left-testing:**
  Shift-left-testing bezieht sich auf den Trend, Softwaretests so früh wie möglich im Entwicklungsprozess zu integrieren. Statt Tests erst am Ende des Entwicklungszyklus durchzuführen, werden sie in den früheren Phasen, wie dem Schreiben von Code oder dem Entwurf, eingebettet. Das Ziel ist es, Probleme frühzeitig zu identifizieren, was zu schnelleren Feedbackschleifen und einer verbesserten Qualität führt.

[3a] 
---
### Continuous Testing vs. Shift-left-testing vs Shift-right-testing vs Testing-in-production

![:scale 60%](media\shift-left-right-continuous-testing.png)

**Shift-right-testing**
  Im Gegensatz zu Shift-left-testing bezieht sich Shift-right-testing darauf, Tests und Qualitätssicherungsaktivitäten in spätere Phasen des Softwareentwicklungszyklus zu verschieben, insbesondere in die Produktionsumgebung. Das bedeutet, dass Tests nach der Bereitstellung in der Produktion weitergeführt werden, um reale Benutzererfahrungen zu überwachen, Leistungsdaten zu sammeln und unerwartete Probleme zu identifizieren. Dieser Ansatz ermöglicht eine schnellere Anpassung an die tatsächlichen Nutzungsbedingungen.

[3a] 
---
### Continuous Testing vs. Shift-left-testing vs Shift-right-testing vs Testing-in-production

**Testing-in-production**
  Testing-in-production bezieht sich darauf, Tests direkt in der Produktionsumgebung durchzuführen, während Benutzer auf das System zugreifen. Dies ermöglicht es, reale Nutzungsbedingungen zu simulieren und echtes Feedback zu erhalten. Dieser Ansatz kann jedoch risikoreich sein, da Fehler oder Probleme Auswirkungen auf echte Benutzer haben können. Daher erfordert Testing-in-production eine sorgfältige Planung und Strategien, um negative Auswirkungen zu minimieren.

[3a]
---

### Testing Anti Patterns

Testing Anti-Patterns beziehen sich auf wiederkehrende Fehlermuster oder schlechte Praktiken im Bereich Softwaretests. Diese Muster führen oft zu ineffizienten, unzuverlässigen oder unangemessenen Testprozessen, die die Qualität der Software beeinträchtigen können.

* Fehlende Teststrategie

* Später Beginn von Tests 

* Unzureichende Testdaten

* Ignorieren von Automatisierungsmöglichkeiten

* Statisches Testen vernachlässigen


[5a]
---
### Validierung vs formale Verifikation

**Validierung:**

  Validierung bezieht sich darauf, sicherzustellen, dass das entwickelte System oder die Software den tatsächlichen Bedürfnissen und Anforderungen des Benutzers entspricht. Es ist ein dynamischer Prozess, der oft durch Tests, Reviews und Benutzerfeedback durchgeführt wird. Die Validierung überprüft, ob das System das Richtige tut und ob es im realen Einsatzumfeld funktioniert.


**Formale Verifikation (Korrektheitsbeweis):**

  Formale Verifikation ist ein statischer Ansatz, der mathematische Modelle und Methoden verwendet, um sicherzustellen, dass ein System oder eine Software bestimmte Eigenschaften erfüllt. Diese Eigenschaften können formale Spezifikationen, Sicherheitseigenschaften oder andere mathematisch beschreibbare Kriterien sein. Formal Methods können mathematische Beweise oder Model Checking verwenden, um zu zeigen, dass ein System bestimmte Sicherheits- oder Funktionsanforderungen erfüllt.


![:scale 60%](media\fehler.png)


[6a] [7a]

---
### Statischer Test von Software

Statische Tests von Software beziehen sich auf Verfahren, bei denen der Quellcode, das Design oder andere Artefakte der Software ohne deren tatsächliche Ausführung überprüft werden.

* Code Reviews

* Statische Code-Analyse

* Dokumentenüberprüfungen

* Datenflussanalyse

* Software-Metriken

* Walkthrough


[8a] [9a] [10a]
---
### Relevante Werkzeuge 

Es gibt eine Vielzahl von Werkzeugen, die für das Statische Testen von Software eingesetzt werden können. Diese Werkzeuge automatisieren oft den Prozess der Statischen Analyse und unterstützen Entwickler und Tester dabei, potenzielle Probleme im Quellcode zu identifizieren. 

* Statische Code-Analysewerkzeuge

* Code Review-Tools

* Dokumentenprüfungstools

* Statische Analysewerkzeuge für Sicherheit

* Formale Methoden und Verifikationstools

* Metrikanalysewerkzeuge

* Abhängigkeitsanalysewerkzeuge

* Code-Duplikationswerkzeuge

* Modellprüfungstools

[11a]
---

### Dynamischer Test von Software

Dynamische Tests von Software beziehen sich auf den Prozess, bei dem die Software während ihrer Ausführung überprüft wird. Im Gegensatz zu statischen Tests, die den Quellcode oder andere Artefakte ohne Ausführung analysieren, testen dynamische Tests die Software, während sie in einer Laufzeitumgebung läuft. Ziel ist es, das tatsächliche Verhalten der Software zu überprüfen, Fehler zu finden und sicherzustellen, dass sie den spezifizierten Anforderungen entspricht.

[12a]

---

### Dynamische Testarten

* Unittest

* Integrationstest

* E2E-Test

* Systemtest

* Regressiontest

* Loadtest

* Performancetest

* UI-Test

* Mutation testing

* Property based test

* Alpha and Beta testing

* A/B Testing

[13a] [14a] [15a] [16a] [17a] [18a]

---

![:scale 20%](media/image.jpg)

![](media/image.jpg)


---


#### Sicherheitstest
***

---

#### Sicherheitslücke (Vulnerability) vs Schwachstelle (Weakness)
***

---

#### Penetrationstest
***

---

#### Static Application Security Testing (SAST)
***

---

#### Dynamic Application Security Testing (DAST)
***

---

#### etc.
***

---

### Relevante Werkzeuge
***

---

#### Testautomatisierung
***

---

#### Test data generation
***

---

### Flaky Tests
***

---

### Funktionsorientierter Test (Black Box Test)
***

---

#### Definition
***

---

#### Verfahren zur Testfallermittlung
***

---

##### Äquivalenzklassenbildung
***

---

##### Grenzwertanalyse
***

---

##### Beispiele
***

---

### Strukturorientierter Test (White-Box-Test)
***

---

#### Definition
***

---

#### Verfahren zur Testfallermittlung
***

---

##### Statement Coverage
***

---

##### Branch Coverage
***

---

##### Path Coverage
***

---

##### Condition Coverage
***

---

##### Beispiele
***

---


# Zusammenfassung



---
class: center, middle

# Fragen?



---
# Quellen
***

[1a]  : https://farhan-labib.medium.com/the-confusion-error-vs-fault-vs-bug-vs-defect-vs-failure-c557af04726b

[2a]  : https://www.geeksforgeeks.org/software-testing-bug-vs-defect-vs-error-vs-fault-vs-failure/

[3a]  : https://katalon.com/resources-center/blog/shift-right-testing

[4a]  : https://www.ibm.com/de-de/topics/continuous-testing 

[5a]  : https://www.testenvironmentmanagement.com/software-testing-anti-patterns/

[6a]  : https://de.wikipedia.org/wiki/Verifizierung_und_Validierung

[7a]  : https://files.ifi.uzh.ch/rerg/amadeus/teaching/courses/software_engineering_hs09/folien/Kapitel_07_V_V.pdf

[8a]  : https://istqb-glossary.page/de/statischer-test/

[9a]  : https://de.wikipedia.org/wiki/Statisches_Software-Testverfahren

[10a] : https://t2informatik.de/wissen-kompakt/walkthrough/

[11a] :https://chat.openai.com/ frage: was ist die Statische Analyse in einem  statischen Test von Software

[12a] : https://de.wikipedia.org/wiki/Dynamisches_Software-Testverfahren

[13a] : https://appmaster.io/de/blog/arten-von-softwaretests#unit-tests

[14a] : https://en.wikipedia.org/wiki/Load_testing

[15a] : https://www.zaptest.com/de/was-ist-das-testen-von-ui-software-tiefes-eintauchen-in-die-typen-verfahren-werkzeuge-und-umsetzung

[16a] : https://de.wikipedia.org/wiki/A/B-Test

[17a] : https://www.geeksforgeeks.org/difference-between-alpha-and-beta-testing/

[18a] : https://medium.com/criteo-engineering/introduction-to-property-based-testing-f5236229d237
