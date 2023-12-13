# Kapitel 10

**Autor:** Simon Fedrau, Sascha Hahn

## Lernziele
* Softwareprüfung
  * Bug vs Issue vs Flaw vs Fault vs Failure vs Error vs Defect
  * Continuous Testing vs. Shift-left-testing vs Shift-right-testing vs Testing-in-production
  * Testing Anti Patterns
  * Validierung vs formale Verifikation
  * Statischer Test von Software
  * Dynamischer Test von Software
  * Sicherheitstest Arten und Bedrohungen
* Funktionsorientierter Test (Black Box Test)
  * Definition
  * Verfahren zur Testfallermittlung
* Strukturorientierter Test (White-Box-Test)
  * Definition
  * Verfahren zur Testfallermittlung

## Softwareprüfung

Beim Softwaretest wird evaluiert und überprüft, ob ein Softwareprodukt oder eine Anwendung das tut, was sie tun soll. Gute Tests ermöglichen die Vermeidung von Fehlern, die Reduzierung der Entwicklungskosten und die Verbesserung der Leistung.


### Bug vs Issue vs Flaw vs Fault vs Failure vs Error vs Defect

* **Bug:**
  Ein Bug bezieht sich auf einen Fehler im Code oder im Design einer Software, der unerwünschtes Verhalten verursacht. Bugs können verschiedene Arten von Fehlern repräsentieren.


* **Issue:**
  Der Begriff "Issue" ist allgemeiner und kann sowohl Bugs als auch andere Probleme, wie Aufgaben, Verbesserungsvorschläge oder allgemeine Anfragen, umfassen. Es ist ein allgemeinerer Begriff, der alles, was die Entwicklung oder den Betrieb einer Software beeinflusst, beschreiben kann.


* **Flaw:**
  Ein Flaw deutet auf einen Fehler oder eine Schwäche in einem System oder Prozess hin. Es kann sich auf Designfehler, Implementierungsfehler oder andere Mängel beziehen, die die Qualität oder Leistung beeinträchtigen.


* **Fault:**
  Ein Fault ist ein Fehler in der Implementierung oder im Code, der zu einem Defekt führen kann. Ein Fault liegt vor, wenn ein Entwickler einen Fehler macht, der zu unerwünschtem Verhalten führen kann.


* **Failure:**
  Ein Failure tritt auf, wenn das System oder die Software nicht mehr wie erwartet funktioniert und die Anforderungen nicht erfüllt. Failures sind das sichtbare Ergebnis von Defekten oder Fehlern und können durch Bugs oder andere Probleme verursacht werden.

* **Error:**
  Ein Error ist ein menschliches Handeln, das zu einem Defekt führt. Dies könnte ein Schreibfehler im Code, ein Algorithmusfehler oder ein Verständnisfehler bei den Anforderungen sein.

* **Defect:**
  Ein Defect ist ein Mangel oder Fehler im Code oder Design, der zu einem unerwünschten Ergebnis führen kann. Defekte können die Ursache von Bugs, Failures oder anderen Problemen sein.

[1a] [2a]
 
### Continuous Testing vs. Shift-left-testing vs Shift-right-testing vs Testing-in-production

* **Continuous Testing:** 
  Continuous Testing ist ein Ansatz, bei dem Tests automatisiert und kontinuierlich während des gesamten Entwicklungs- und Bereitstellungsprozesses durchgeführt werden. Das Ziel besteht darin, frühzeitig Feedback über mögliche Defekte oder Probleme zu erhalten und die Qualität der Software kontinuierlich sicherzustellen. Continuous Testing ist integraler Bestandteil von Continuous Integration und Continuous Delivery (CI/CD)-Pipelines.

[4a]

* **Shift-left-testing:**
  Shift-left-testing bezieht sich auf den Trend, Softwaretests so früh wie möglich im Entwicklungsprozess zu integrieren. Statt Tests erst am Ende des Entwicklungszyklus durchzuführen, werden sie in den früheren Phasen, wie dem Schreiben von Code oder dem Entwurf, eingebettet. Das Ziel ist es, Probleme frühzeitig zu identifizieren, was zu schnelleren Feedbackschleifen und einer verbesserten Qualität führt.


* **Shift-right-testing**
  Im Gegensatz zu Shift-left-testing bezieht sich Shift-right-testing darauf, Tests und Qualitätssicherungsaktivitäten in spätere Phasen des Softwareentwicklungszyklus zu verschieben, insbesondere in die Produktionsumgebung. Das bedeutet, dass Tests nach der Bereitstellung in der Produktion weitergeführt werden, um reale Benutzererfahrungen zu überwachen, Leistungsdaten zu sammeln und unerwartete Probleme zu identifizieren. Dieser Ansatz ermöglicht eine schnellere Anpassung an die tatsächlichen Nutzungsbedingungen.


* **Testing-in-production**
  Testing-in-production bezieht sich darauf, Tests direkt in der Produktionsumgebung durchzuführen, während Benutzer auf das System zugreifen. Dies ermöglicht es, reale Nutzungsbedingungen zu simulieren und echtes Feedback zu erhalten. Dieser Ansatz kann jedoch risikoreich sein, da Fehler oder Probleme Auswirkungen auf echte Benutzer haben können. Daher erfordert Testing-in-production eine sorgfältige Planung und Strategien, um negative Auswirkungen zu minimieren.


[3a] 


### Testing Anti Patterns

Testing Anti-Patterns beziehen sich auf wiederkehrende Fehlermuster oder schlechte Praktiken im Bereich Softwaretests. Diese Muster führen oft zu ineffizienten, unzuverlässigen oder unangemessenen Testprozessen, die die Qualität der Software beeinträchtigen können. Beispiele für Anti-Patterns sind:


* Fehlende Teststrategie:

  Wenn ein Projekt keine klare Teststrategie hat, können wichtige Aspekte der Anwendung übersehen werden. Dies führt zu unvollständigen Testabdeckungen und einem erhöhten Risiko, dass kritische Fehler nicht erkannt werden.

* Später Beginn von Tests (Testing Too Late):

  Wenn Tests erst in späteren Phasen des Softwareentwicklungszyklus durchgeführt werden, steigt die Wahrscheinlichkeit, dass Fehler spät erkannt werden. Dies führt zu höheren Kosten und erschwert die Fehlerbehebung

* Unzureichende Testdaten:

  Mangelnde Vielfalt und Qualität der Testdaten können dazu führen, dass bestimmte Szenarien und Randfälle nicht ausreichend getestet werden. Dies kann dazu führen, dass wichtige Fehler unentdeckt bleiben.

* Ignorieren von Automatisierungsmöglichkeiten:

  Wenn Automatisierungsmöglichkeiten für Testsignifikante Anwendungsfälle ignoriert oder nicht ausreichend genutzt werden, kann dies zu ineffizienten Testprozessen führen. Automatisierung kann dazu beitragen, Tests schneller und zuverlässiger durchzuführen.

* Statisches Testen vernachlässigen:

  Statisches Testen, einschließlich Code-Reviews und statischer Code-Analyse, wird oft vernachlässigt. Dies führt dazu, dass Fehler im Code nicht frühzeitig erkannt werden, was zu höheren Kosten und Problemen in späteren Phasen führen kann.

[5a]

### Validierung vs formale Verifikation

Validierung und formale Verifikation sind zwei verschiedene Ansätze, um sicherzustellen, dass ein System oder eine Software die erforderlichen Anforderungen erfüllt. Hier sind die grundlegenden Unterschiede zwischen Validierung und formaler Verifikation:


* Validierung:
    Validierung bezieht sich darauf, sicherzustellen, dass das entwickelte System oder die Software den tatsächlichen Bedürfnissen und Anforderungen des Benutzers entspricht. Es ist ein dynamischer Prozess, der oft durch Tests, Reviews und Benutzerfeedback durchgeführt wird. Die Validierung überprüft, ob das System das Richtige tut und ob es im realen Einsatzumfeld funktioniert.

* Formale Verifikation (Korrektheitsbeweis):
    Formale Verifikation ist ein statischer Ansatz, der mathematische Modelle und Methoden verwendet, um sicherzustellen, dass ein System oder eine Software bestimmte Eigenschaften erfüllt. Diese Eigenschaften können formale Spezifikationen, Sicherheitseigenschaften oder andere mathematisch beschreibbare Kriterien sein. Formal Methods können mathematische Beweise oder Model Checking verwenden, um zu zeigen, dass ein System bestimmte Sicherheits- oder Funktionsanforderungen erfüllt.


![:scale 60%](media\fehler.png)

[6a] [7a]

### Statischer Test von Software

Statische Tests von Software beziehen sich auf Verfahren, bei denen der Quellcode, das Design oder andere Artefakte der Software ohne deren tatsächliche Ausführung überprüft werden. Im Gegensatz zu dynamischen Tests, die die Software während der Laufzeit ausführen, analysieren statische Tests die statischen Eigenschaften des Codes, um Fehler, Mängel oder Verbesserungsmöglichkeiten zu identifizieren. Hier sind einige gängige Formen von statischen Tests:

* Code Reviews:
    Entwickler überprüfen den Quellcode, um sicherzustellen, dass er den Coding-Standards entspricht, gut strukturiert ist und keine offensichtlichen Fehler enthält. Code Reviews können formell oder informell sein und helfen, Qualitätsprobleme frühzeitig zu identifizieren.

* Statische Code-Analyse:
    Tools werden verwendet, um den Quellcode statisch zu analysieren und Muster zu identifizieren, die auf mögliche Fehler, Sicherheitslücken oder Code-Stil-Verstöße hinweisen könnten. Diese Werkzeuge können automatisiert in den Entwicklungsprozess integriert werden.

* Dokumentenüberprüfungen:
    Statische Tests können auch Dokumente, wie Spezifikationen, Design-Dokumente oder Anforderungen, einschließen. Ziel ist es sicherzustellen, dass die Dokumentation konsistent, vollständig und verständlich ist.

* Datenflussanalyse:
    Die Überprüfung des Datenflusses im Code kann dazu beitragen, unerwartete Abhängigkeiten oder mögliche Fehlerquellen zu identifizieren.

* Software-Metriken:
    Metriken wie Code-Komplexität, Anzahl der Codezeilen oder Anzahl der Methoden können statisch analysiert werden, um Hinweise auf die Qualität und Wartbarkeit des Codes zu geben.

* Walkthrough:
  Ein Walkthrough bezieht sich auf eine informelle Überprüfung oder Inspektion von Software-Artefakten. Es handelt sich um eine Art informelles Treffen, bei dem ein Entwickler oder Tester das Softwareprodukt, den Code oder andere Entwicklungsartefakte Schritt für Schritt mit anderen Teammitgliedern oder relevanten Stakeholdern durchgeht. Ziel eines Walkthroughs ist es, mögliche Fehler, Unklarheiten oder Verbesserungsmöglichkeiten zu identifizieren und frühzeitig im Entwicklungsprozess zu adressieren.


Statische Tests sind besonders nützlich, um Probleme frühzeitig im Entwicklungsprozess zu erkennen, bevor die Software in die Test- oder Produktionsumgebung übergeht. Durch die Integration von statischen Tests können Entwicklerteams die Qualität verbessern, die Wartbarkeit erhöhen und die Kosten für die Fehlerbehebung reduzieren.

[8a] [9a] [10a]

#### Relevante Werkzeuge  

Es gibt eine Vielzahl von Werkzeugen, die für das Statische Testen von Software eingesetzt werden können. Diese Werkzeuge automatisieren oft den Prozess der Statischen Analyse und unterstützen Entwickler und Tester dabei, potenzielle Probleme im Quellcode zu identifizieren. Hier sind einige relevante Werkzeuge:

  * Statische Code-Analysewerkzeuge:
      Beispiele sind SonarQube, ESLint, PMD, Checkstyle und FindBugs. Diese Werkzeuge scannen den Quellcode nach festgelegten Regeln und identifizieren mögliche Fehler, Sicherheitslücken, Coding-Standards-Verstöße und andere Probleme.

  * Code Review-Tools:
      Plattformen wie GitHub, GitLab oder Bitbucket bieten integrierte Funktionen für Code-Reviews. Sie ermöglichen Teams, den Quellcode gemeinsam zu überprüfen, Kommentare zu hinterlassen und Diskussionen zu führen.

  * Dokumentenprüfungstools:
      Werkzeuge wie Collaborator, Atlassian Confluence oder Microsoft Teams unterstützen Teams bei der Überprüfung von Dokumentation, Anforderungsspezifikationen oder anderen schriftlichen Artefakten.

  * Statische Analysewerkzeuge für Sicherheit:
      Werkzeuge wie OWASP Dependency-Check oder Fortify SCA können Schwachstellen in externen Bibliotheken und Abhängigkeiten identifizieren, um die Sicherheit von Software zu verbessern.

  * Formale Methoden und Verifikationstools:
      Für anspruchsvollere Anwendungen, insbesondere in sicherheitskritischen Bereichen, können formale Verifikationswerkzeuge wie Alloy Analyzer oder SPIN verwendet werden, um mathematische Modelle auf Korrektheit zu prüfen.

  * Metrikanalysewerkzeuge:
      Werkzeuge wie SonarQube können nicht nur potenzielle Fehler identifizieren, sondern auch Metriken zur Codequalität bereitstellen, wie z. B. Code-Komplexität, Testabdeckung und Duplikate.

  * Abhängigkeitsanalysewerkzeuge:
      Werkzeuge wie Dependency-Check oder Snyk können Abhängigkeiten und Bibliotheken auf bekannte Schwachstellen und Sicherheitsprobleme überprüfen.

  * Code-Duplikationswerkzeuge:
      Werkzeuge wie Clone Detective for Visual Studio oder Simian für Java können Duplikate im Quellcode identifizieren, was die Wartbarkeit verbessern kann.

  * Modellprüfungstools:
      Model Checking-Tools wie SPIN oder NuSMV können dazu verwendet werden, formale Modelle auf bestimmte Eigenschaften oder Fehlerzustände zu überprüfen.

Es ist wichtig zu beachten, dass die Auswahl der Werkzeuge von den spezifischen Anforderungen des Projekts, der Art der Anwendung und den verfügbaren Ressourcen abhängt. Die Integration mehrerer Werkzeuge in den Entwicklungsprozess kann dazu beitragen, die Qualität und Sicherheit der Software zu verbessern.

[11a]

### Dynamischer Test von Software

Dynamische Tests von Software beziehen sich auf den Prozess, bei dem die Software während ihrer Ausführung überprüft wird. Im Gegensatz zu statischen Tests, die den Quellcode oder andere Artefakte ohne Ausführung analysieren, testen dynamische Tests die Software, während sie in einer Laufzeitumgebung läuft. Ziel ist es, das tatsächliche Verhalten der Software zu überprüfen, Fehler zu finden und sicherzustellen, dass sie den spezifizierten Anforderungen entspricht.




[12a]
#### Dynamische Testarten


#### Unittest

Diese Tests überprüfen einzelne Einheiten des Quellcodes, normalerweise einzelne Funktionen oder Methoden, um sicherzustellen, dass sie korrekt funktionieren. Unit Tests sind automatisierte Tests, die häufig im Entwicklungsprozess integriert werden.

#### Integrationstest

Integrationstests überprüfen, wie verschiedene Teile einer Anwendung zusammenarbeiten. Sie testen die Schnittstellen und Interaktionen zwischen verschiedenen Modulen, um sicherzustellen, dass sie ordnungsgemäß integriert sind.

#### E2E-Test

E2E-Tests simulieren typische Benutzerinteraktionen von Anfang bis Ende, um sicherzustellen, dass die gesamte Anwendung ordnungsgemäß funktioniert. Sie prüfen die Software aus Sicht des Endbenutzers.


#### Systemtest

Der Systemtest überprüft die vollständige und integrierte Software, um sicherzustellen, dass sie die festgelegten Anforderungen erfüllt. Er umfasst alle Aspekte der Anwendung, einschließlich Benutzeroberfläche, Datenbanken und externe Systeme.


#### Regressiontest

Bei Regressionstests wird die Softwareanwendung getestet, nachdem Änderungen, Fehlerbehebungen oder Aktualisierungen vorgenommen worden sind. Damit soll sichergestellt werden, dass die Änderungen an der Anwendung keine negativen Auswirkungen auf die bestehende Funktionalität haben oder neue Probleme verursachen. Regressionstests tragen dazu bei, die Softwarequalität und -zuverlässigkeit während des gesamten Entwicklungsprozesses aufrechtzuerhalten, indem sie sicherstellen, dass Änderungen oder Erweiterungen die Stabilität der Anwendung und die Benutzerfreundlichkeit nicht beeinträchtigen.


#### Loadtest

Load Testing (auch Belastungstest genannt) ist eine Art von Performance-Test, der darauf abzielt, die Reaktion und Stabilität einer Softwareanwendung unter einer bestimmten Last zu überprüfen. Dabei wird die Anwendung mit einer bestimmten Menge von Benutzern, Transaktionen oder Anfragen konfrontiert, um ihre Leistungsfähigkeit und Zuverlässigkeit unter realen oder simulierten Nutzungsbedingungen zu bewerten.


#### Performancetest

Diese Tests bewerten die Leistung der Software unter verschiedenen Bedingungen, einschließlich der Belastungstests, die die Reaktion der Software auf eine hohe Last simulieren, und der Skalierbarkeitstests, die die Fähigkeit der Software zur Bewältigung wachsender Benutzerzahlen überprüfen.


#### UI-Test

UI-Tests überprüfen die Benutzeroberfläche einer Anwendung, um sicherzustellen, dass sie korrekt funktioniert und die Benutzererfahrung den Erwartungen entspricht.

#### Mutation testing

Mutation Testing bezieht sich auf das Einführen kleiner Änderungen (Mutationen) in den Quellcode, um zu prüfen, ob die vorhandenen Tests diese Änderungen erkennen. Es dient dazu, die Robustheit der Testabdeckung zu bewerten.

#### Property based test

Property Based Tests verwenden zufällig generierte Eingaben, um sicherzustellen, dass bestimmte Eigenschaften oder Invarianten eines Systems immer erfüllt sind.


#### Alpha and Beta testing

Alpha Testing erfolgt in der Regel durch interne Teams, während Beta Testing externe Benutzer einbezieht. Beide Tests überprüfen die Software in realen Umgebungen vor der offiziellen Veröffentlichung.

#### A/B Testing

A/B Testing ist eine Methode, bei der zwei oder mehr Varianten einer Anwendung mit unterschiedlichen Funktionen oder Designs erstellt werden. Es wird verwendet, um die Leistung und Benutzerpräferenzen zu vergleichen und zu entscheiden, welche Variante beibehalten wird.

[13a] [14a] [15a] [16a] [17a] [18a]

#### Sicherheitstest
Eine besondere Art von dynamischen Tests sind Sicherheitstests, die darauf abzielen, Schwachstellen und Sicherheitslücken in der Software zu identifizieren. Sie können manuell oder automatisiert durchgeführt werden und umfassen verschiedene Arten von Tests, die im Folgenden beschrieben werden.

Sicherheitstest sind auch in dem Aspekt anders, dass sie nicht nicht den Nachweis erbringen, dass eine Software eine Funktion enthält, sondern dass sie eine Funktion nicht enthält.

[2b]

#### Sicherheitslücke (Vulnerability) vs Schwachstelle (Weakness)
Es gibt zwei verschwiedene Arten von Sicherheitsbedrohungen die in der Softwareentwicklung auftreten können. Zum einen die Schwachstelle (Weakness) und zum anderen die Sicherheitslücke (Vulnerability).

Der Unterschied ist, dass sich eine Sicherheitslücke auf eine tatsächliche Schwäche oder eine Verwundbarkeit in einem Computersystem oder einer Software bezieht, die es Angreifern ermöglicht, unbefugten Zugriff zu erhalten oder Schaden zu verursachen.
Eine Schwachstelle hingegen ist eine allgemeine Bezeichnung für eine potenzielle Unsicherheit oder Schwäche im System, die ausgenutzt werden könnte.
Sicherheitslücken sind konkrete Instanzen von Schwachstellen, die aktiv ausgenutzt werden können, während Schwachstellen potenzielle Angriffspunkte darstellen, die noch nicht ausgenutzt wurden oder bekannt sind. Es ist wichtig, Schwachstellen zu identifizieren und zu beheben, um Sicherheitslücken zu verhindern.

Ein Beispiel für eine Schwachstelle könnte eine unzureichende Passwortrichtlinie sein, die es einem Angreifer erleichtert, schwache Passwörter zu erraten. Die konkrete Sicherheitslücke wäre dann eine bestimmte Anmeldung mit einem unsicheren Passwort, die aufgrund der Schwachstelle in der Passwortrichtlinie möglich ist. In diesem Fall besteht die Schwachstelle in der generellen Unzulänglichkeit der Passwortrichtlinie, während die Sicherheitslücke die tatsächliche Nutzung dieser Schwachstelle durch einen spezifischen Angriff darstellt.

[1b,3b]

#### Penetrationstest
Bei einem Penetrationstest wird die Software einer umfassenden Prüfung unterzogen, die die Empfindlichkeit gegenüber Angriffen feststellen soll.
Dabei werden Methoden verwendet, die auch von echten Angreifern verwendet werden.
Dabei haben die Tester auch den gleichen Zugang auf das System wie ein Angreifer.

Während des kompletten Penetrationstests erfolgt eine genaue Protokollierung aller durchgeführten Maßnahmen.
In einem abschließenden Bericht werden die erkannten Schwachstellen und Lösungsansätze zur Verbesserung des IT-Sicherheitsniveaus aufgeführt.

[4b]

#### Static and Dynamic Application Security Testing (SAST and DAST)
Bei den Static und Dynamic Application Security Tests handelt es sich um den geleichen Unterschied wie bei den generellen statischen und dynamischen Tests von Software.
Bei den Statischen Tests wird die Software ohne/vor Ausführung überprüft.

SAST ist ein sogenanntes White-Box Verfahren, wobei der Quellcode Sichtbar ist und analysiert wird.
Bei dem Verfahren wird der Code auf drauf geprüft, ob es Zeilen gibt in denen sich später Mallware einschluesen könnte,
ob es Codeteile gibt die auf Datein zugreifen, was auch Mallware einschleusen könnte,
oder kann die Software dazu genutzt werden um unbemerkt mit anderen Programmen zu interagieren.

Bei dem DAST Verfahren testet ein automtisches externes Programm die Software während der Laufzeit auf Schwachstellen.
Es simuliert externe Angriffe ähnlich wie beim Penetrationstest.
Logischer Weise ist der Quellcode für die Testsoftware nicht sichtbar. Deshalb wird das DAST verfahren auch Black-Box Verfahren genannt.

[5b,6b]

### Relevante Werkzeuge
Hier einige der wichtigsten Tools zu Softwaretests zu den verschiedenen Testarten:

* Unit Testing:
    * JUnit: Für Java-Anwendungen ist JUnit eine beliebte Testing-Framework.
    * pytest: Eine Testing-Bibliothek für Python-Anwendungen.

* Integration Testing:
    * Selenium: Ein Open-Source-Tool für automatisierte Tests von Webanwendungen.
    * Postman: Ein Kollaborations-Tool für API-Entwicklung, das auch Funktionen für automatisierte Tests bietet.

* Last- und Performance-Testing:
    * Apache JMeter: Ein Open-Source-Tool für Last- und Performance-Testing von Anwendungen.
    * LoadRunner: Ein kommerzielles Tool von Micro Focus für Last- und Performance-Testing.

* Funktionstests / UI-Tests:
    * Selenium: Wird auch für funktionale Tests von Benutzeroberflächen verwendet.
    * Cypress: Ein JavaScript-End-to-End-Testframework, das für moderne Webanwendungen geeignet ist.

* Security Testing:
    * OWASP ZAP (Zed Attack Proxy): Ein Sicherheitstestwerkzeug für Webanwendungen.
    * Burp Suite: Ein integriertes Plattform-Toolkit für Sicherheitstests von Webanwendungen.

* Auch wichtige Tools um die verschiedenen Testarten zu verwalten sind:
    * Jira: Ein weit verbreitetes Tool für das Testmanagement und die Fehlerverfolgung.
    * TestRail: Eine Testmanagement-Software, die Testpläne, Testläufe und Testergebnisse verwaltet.

[7b]

#### Testautomatisierung
In dieser Testart werden Updates in bereits getesteten Umgebungen und erstellt Datensätze, ob die Software mit einer neuen Funktionalität schneller, besser, stabiler läuft oder aber sich zurück entwickelt hat (Regression). Die hierbei entstehenden, quantifizierbaren Daten benötigen jedoch eine breite Grundlage und dies macht Testautomatisierung unausweichlich.

[8b]

#### Test data generation
Bei der Test data generation werden automtisch Daten erstellt die verwendet werden um z.B Testfuntionen mit Werte zu füllen.
Wenn man z.B mit JUnit einen Test erstellt, der eine additions funktion Testet, muss dieser Test mit richtigen und falschen Testfällen befüllt werden.
Das keine eine sehr einfache mühselige Arbeit sein, die z.B ein KI Tool sehr schnell erledigen kann.

[9b]

### Flaky Tests
Flaky Test sind Test die erfolgreiche und fehlgeschlafene Ergebnisse liefern obwohl nichts am Test oder Code geändert wurde.
Anders gesagt, sind es Tests die unzuverlässig sind und immer andere Ergebnisse liefern.
Dies kann geschehen wenn z.B ein Test auf vorhergehende Tests angewiesen ist, die Testdaten nicht zwischen Durchläufen nicht resetet, Probleme mit der Zeitzone, etc.

[10b]

### Funktionsorientierter Test (Black Box Test)

#### Definition
Funktionsorientierte Tests untersuchen die externe Funktionalität einer Software, ohne Kenntnisse über die interne Implementierung zu haben.
Diese Tests basieren auf den Spezifikationen und Anforderungen der Software und überprüfen, ob die Funktionen gemäß den erwarteten Eingaben die korrekten Ergebnisse liefern.
Dabei werden verschiedene Szenarien und Randbedingungen berücksichtigt, um sicherzustellen, dass die Software in unterschiedlichen Situationen korrekt funktioniert.
Das Ziel solcher Tests ist es, die Benutzersicht auf die Software zu prüfen und sicherzustellen, dass sie die gewünschte Funktionalität bereitstellt, unabhängig von der internen Implementierung.

[1b,11b]

#### Verfahren zur Testfallermittlung
Um Testfälle zu erstellen, werden verschiedene Techniken verwendet, um die Testabdeckung zu maximieren und sicherzustellen, dass alle Anforderungen erfüllt sind.

##### Äquivalenzklassenbildung
Die Äquivalenzklassenbildung ist eine Methode im spezifikationsbasierten Testen, die darauf abzielt, eine repräsentative Auswahl von Eingabewerten für Tests auszuwählen.
Diese Methode teilt die möglichen Eingabewerte in Klassen oder Gruppen ein, wobei angenommen wird, dass sich alle Werte innerhalb einer Klasse ähnlich auf das Verhalten der Software auswirken.
Das Ziel ist es, eine effiziente Testabdeckung zu erreichen, ohne jeden einzelnen möglichen Wert testen zu müssen.

[1b,12b]

###### Beispiel
![](media\aequivalenzklassen.png)

Die Eingabewerte werden in drei Äquivalenzklassen eingeteilt.
Die Gültige Äquivalenzklasse zwischen 10 und 100 und die ungültigen Äquivalenzklassen kleiner 10 und größer 100.
[1b,12b]

##### Grenzwertanalyse
Die Grenzwertanalyse ist eine Methode im spezifikationsbasierten Testen, die darauf abzielt, die Testabdeckung durch die Prüfung von Werten an den Grenzen der Äquivlenzklassen zu verbessern. Diese Methode identifiziert und überprüft die Verhaltensweisen und Reaktionen einer Software in der Nähe von Grenzwerten, wo häufig Fehler auftreten können, wie z.B. bei Schleifen durchläufen.

[1b,12b]

###### Beispiel
![](media\grenzwerte.png)
Hier werden jeweils 4 Werte zwischen den 3 Äquivalenzklassen getestet.
z.B. 9 und 11, sowie 99 und 101.

[1b,12b]

### Strukturorientierter Test (White-Box-Test)

#### Definition
Ein White-Box-Test bezeichnet eine Methode des Software-Tests, bei der die Tests mit Kenntnissen über die innere Funktionsweise des zu testenden Systems entwickelt werden.
Im Gegensatz zum Black-Box-Test ist für diesen Test also ein Blick in den Quellcode gestattet. D.h., es wird am Code geprüft.

[13b]

#### Verfahren zur Testfallermittlung
Um Testfälle zu erstellen, werden verschiedene Techniken verwendet, um die Testabdeckung zu maximieren und sicherzustellen, dass alle Anforderungen erfüllt sind.

##### Statement Coverage
Die Statement Coverage ist eine Metrik im Bereich des Softwaretestens, die den Prozentsatz der ausgeführten Anweisungen im Quellcode während der Testausführung misst.
Sie gibt an, welche Teile des Codes durch die Testfälle erreicht und ausgeführt wurden.
Eine höhere Statement Coverage deutet darauf hin, dass mehr Codezeilen während der Tests durchlaufen wurden.
Es ist jedoch wichtig zu beachten, dass eine hohe Statement Coverage nicht zwangsläufig bedeutet, dass alle möglichen Szenarien oder Verzweigungen im Code getestet wurden, da sie lediglich die erreichten Codezeilen berücksichtigt.
Daher sollte Statement Coverage in Verbindung mit anderen Testmetriken verwendet werden, um eine umfassendere Qualitätssicherung sicherzustellen.

[1b,14b]

##### Branch Coverage
Branch Coverage ist eine Metrik im Softwaretest, die angibt, wie viele der Verzweigungen oder Entscheidungspunkte im Quellcode während der Testausführung durchlaufen wurden.
Diese Metrik misst, inwieweit die unterschiedlichen Pfade innerhalb von Bedingungen oder Schleifen durch die Testfälle abgedeckt wurden.
Eine höhere Branch Coverage deutet darauf hin, dass verschiedene Entscheidungsszenarien getestet wurden.
Es ist wichtig zu beachten, dass 100%ige Branch Coverage nicht unbedingt bedeutet, dass alle möglichen Kombinationen von Bedingungen getestet wurden, sondern nur, dass jede Entscheidungsverzweigung mindestens einmal durchlaufen wurde.

[1b,15b]

##### Path Coverage
Path Coverage ist eine Metrik im Softwaretest, die die Anzahl der durchlaufenden Pfade im Quellcode während der Testausführung misst.
Ein Pfad repräsentiert eine spezifische Abfolge von Anweisungen, die innerhalb des Programms durchlaufen werden können.
Path Coverage ist eine anspruchsvollere Metrik im Vergleich zu Statement Coverage oder Branch Coverage, da sie die Berücksichtigung aller möglichen Ausführungspfade erfordert.
Eine höhere Path Coverage zeigt an, dass eine umfassendere Testabdeckung erreicht wurde und mehr Kombinationen von Anweisungen getestet wurden.
Es ist jedoch oft schwierig, 100%ige Path Coverage zu erreichen, da die Anzahl der möglichen Pfade exponentiell mit der Anzahl der Entscheidungspunkte im Code wächst.
Daher wird Path Coverage in der Regel in Verbindung mit anderen Testmetriken verwendet, um eine umfassende Qualitätssicherung zu gewährleisten.

[1b,16b]

##### Condition Coverage
Condition Coverage ist eine Testmetrik im Bereich Softwaretesting, die angibt, wie viele Bedingungen im Quellcode während der Testausführung evaluiert wurden.
Diese Metrik betrachtet die Anzahl der untersuchten Bedingungen im Verhältnis zur Gesamtanzahl der Bedingungen im Code. Eine höhere Condition Coverage zeigt an, dass eine größere Anzahl von logischen Bedingungen während der Tests berücksichtigt wurde.

[1b,17b]

## Referenzen

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


[1b] :https://chat.openai.com/

[2b] :https://de.wikipedia.org/wiki/Sicherheitstest_(Software)

[3b] :https://www.linkedin.com/pulse/vulnerability-v-weakness-kirsty-ritchie-fcca-dip-cst

[4b] :https://www.security-insider.de/was-ist-ein-penetrationstest-a-667683/

[5b] :https://www.dev-insider.de/was-ist-sast-a-3b8ea455fc754f1f1b641b31bb026e7b/

[6b] :https://www.dev-insider.de/was-ist-dast-a-517156f0cc989cb6ce982ab2435c2150/#:~:text=Der%20Begriff%20%E2%80%9EDynamic%20Application%20Security,hat%20diverse%20Vor%2D%20und%20Nachteile.

[7b] :https://chat.openai.com/ : Was sind die wichtigsten Tools zu Softwaretests?

[8b] :https://www.dev-insider.de/was-ist-testautomation-a-d36545e8a9b683910805fa2cfb9b2035/

[9b] :https://www.k2view.com/blog/what-is-test-data-generation/

[10b] :https://www.jetbrains.com/de-de/teamcity/ci-cd-guide/concepts/flaky-tests/#:~:text=Flaky%2DTests%20sind%20definiert%20als,am%20Test%20selbst%20vorgenommen%20wurden.

[11b] :https://link.springer.com/chapter/10.1007/978-3-8274-2203-3_2

[12b] :https://www.hsbi.de/elearning/data/FH-Bielefeld/lm_data/lm_1359639/testing/testcases.html

[13b] :https://de.wikipedia.org/wiki/White-Box-Test

[14b] :https://www.zyxware.com/articles/4161/what-is-statement-coverage-in-testing

[15b] :https://linearb.io/blog/what-is-branch-coverage

[16b] :https://www.techslang.com/definition/what-is-path-coverage-testing/#:~:text=Path%20coverage%20testing%20is%20a,cases%20to%20exercise%20each%20path.

[17b] :https://www.educative.io/answers/what-is-condition-coverage-testing