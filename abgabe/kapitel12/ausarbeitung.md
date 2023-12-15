# Kapitel 11

**Autor:** Simon Fedrau, Sascha Hahn

## Lernziele

## Wartung von Software (Software Maintainance)
***

Die Wartung von Software, auch als Software Maintenance bekannt, bezieht sich auf den Prozess der Modifikation und Pflege einer Softwareanwendung nach ihrer ursprünglichen Entwicklung und Bereitstellung. Dieser Lebenszyklusaspekt ist entscheidend, um sicherzustellen, dass die Software effizient funktioniert, aktuell bleibt und den sich ändernden Anforderungen und Umgebungen gerecht wird. Die Softwarewartung umfasst verschiedene Aktivitäten, die im Allgemeinen in vier Kategorien unterteilt werden:

1. Korrigierende Wartung (Corrective Maintenance):
Ziel: Behebung von Fehlern oder Mängeln in der Software.
Aktivitäten: Identifikation, Analyse und Beseitigung von Fehlern, um die Softwarestabilität zu gewährleisten.
2. Adaptive Wartung (Adaptive Maintenance):
Ziel: Anpassung der Software an Änderungen in der Umgebung, wie Betriebssystem-Upgrades oder Hardwareänderungen.
Aktivitäten: Anpassung von Codes und Funktionen, um die Kompatibilität und Leistung sicherzustellen.
3. Perfective Wartung (Perfective Maintenance):
Ziel: Verbesserung der Softwareleistung, Funktionalität oder Benutzerfreundlichkeit.
Aktivitäten: Hinzufügen neuer Funktionen, Optimierung von Algorithmen oder Verbesserung der Benutzeroberfläche.
4. Preventive Wartung (Preventive Maintenance):
Ziel: Verhinderung zukünftiger Probleme oder Fehlfunktionen.
Aktivitäten: Überprüfung und Aktualisierung von Codes, um potenzielle Probleme zu identifizieren und zu beheben, bevor sie auftreten.

[15a] [16a]

### Definition Software-Wartung und Legacy-Code
***

**Software-Wartung** 
In der Softwaretechnik bezeichnet der Begriff Softwarewartung „die Veränderung eines Softwareprodukts nach dessen Auslieferung, um Fehler zu beheben, Performanz oder andere Attribute zu verbessern oder Anpassungen an die veränderte Umgebung vorzunehmen. In Deutschland wird darüber hinaus geregelt: „Die Aufgabe der Wartung umfasst sämtliche Maßnahmen zur Erhaltung der Funktionsfähigkeit der eingesetzten IT-Verfahren und Software. Hierzu gehören auch erforderliche fachliche und technische Anpassungen der IT-Infrastruktur.. Diese gesetzliche Regelung grenzt hierbei bewusst die Softwarepflege gegenüber der Softwarewartung durch Fokussierung auf den Erhalt der Funktionsfähigkeit ab. 

[17a]

**Legacy-Code**

Der Begriff Altsystem oder Legacy-System oder im engeren Sinne Legacy-Code bezeichnet in der Informatik eine etablierte, historisch gewachsene Anwendung im Bereich Unternehmenssoftware. Das englische Wort legacy ist in diesem Kontext ein weitgehend wertfreier Fachbegriff. Er kann aber umgangssprachlich auch negativ im Sinne einer lästigen „Hinterlassenschaft“ oder „Altlast“ im übertragenen Sinne verwendet werden. 

[18a]

### Evolution von Software
***

Software-Evolution ist ein Begriff aus der Softwaretechnik, im Speziellen aus der Softwarewartung, und beschreibt den Prozess, der folgt, nachdem ein Softwaresystem entwickelt und ausgeliefert wurde. Nach Auslieferung und Benutzung kommen neue Anforderungen dazu und alte Anforderungen verändern sich. Teile des Softwaresystems müssen möglicherweise korrigiert werden, da Fehler auftreten, die zuvor nicht bemerkt wurden. Das System muss an eine neue Plattform adaptiert werden. Die Performance muss verbessert werden und andere nichtfunktionale Anforderungen müssen überprüft werden.

[19a]

#### Ursachen für Änderungen an Software
***

  * Fehlerkorrektur (Bugfixing): Software enthält oft Fehler, die während oder nach der Entwicklung entdeckt werden. Änderungen sind erforderlich, um diese Fehler zu beheben und die Software zu stabilisieren.

  * Neue Anforderungen: Kunden oder Benutzer können neue Anforderungen oder Funktionen an die Software stellen. Entwickler müssen die Software aktualisieren, um diesen neuen Anforderungen gerecht zu werden.

  * Verbesserungen und Optimierungen: Auch wenn die Software funktioniert, können Entwickler Verbesserungen vornehmen, um die Leistung, Effizienz oder Benutzerfreundlichkeit zu steigern.

  * Sicherheitsaktualisierungen: Wenn Sicherheitslücken entdeckt werden, müssen Softwareentwickler entsprechende Aktualisierungen bereitstellen, um die Software vor möglichen Angriffen zu schützen.

  * Technologischer Fortschritt: Neue Technologien oder Plattformen können verfügbar werden, und die Software muss möglicherweise angepasst werden, um mit den neuesten Entwicklungen Schritt zu halten.

  * Gesetzliche Anforderungen: Änderungen an Software können notwendig sein, um gesetzlichen Bestimmungen oder regulatorischen Anforderungen zu entsprechen.

  * Hardwareänderungen: Wenn sich die zugrunde liegende Hardware ändert, kann es erforderlich sein, die Software anzupassen, um weiterhin kompatibel zu bleiben.

  * Benutzerfeedback: Rückmeldungen von Benutzern können dazu führen, dass Entwickler Änderungen vornehmen, um die Benutzererfahrung zu verbessern oder auf bestimmte Bedürfnisse einzugehen.

  * Lebenszyklus-Management: Software unterliegt einem Lebenszyklus, der Wartung, Unterstützung und schließlich die Ablösung durch eine neue Version oder ein neues Produkt umfassen kann.

[20a]

#### Arten von Änderungen an Software
***
Die Klassifizierung von Softwareänderungen nach ihrer Art erfolgt oft anhand von vier Haupttypen, korrektive, präventive, perfektionierende und adaptive Änderungen. 



##### Korrektive, präventive, perfektionierende, adaptive Änderungen
***

  * Korrektive Änderungen:
      Ziel: Behebung von Fehlern oder Bugs in der Software.
      Warum: Diese Änderungen werden vorgenommen, um Probleme zu lösen, die während der Entwicklung oder nach der Bereitstellung entdeckt wurden.

  * Präventive Änderungen:
      Ziel: Vermeidung potenzieller zukünftiger Probleme oder Risiken.
      Warum: Diese Änderungen werden durchgeführt, um mögliche Fehler oder Schwachstellen zu identifizieren und zu beheben, bevor sie zu ernsthaften Problemen führen.

  * Perfektionierende Änderungen:
      Ziel: Verbesserung der Leistung, Benutzerfreundlichkeit oder anderer Aspekte der Software, die nicht unbedingt mit Fehlern zusammenhängen.
      Warum: Dies kann aufgrund von Benutzerfeedback, neuen Designprinzipien oder dem Wunsch nach kontinuierlicher Verbesserung geschehen.

  * Adaptive Änderungen:
      Ziel: Anpassung der Software an veränderte Umgebungen, Plattformen oder Anforderungen.
      Warum: Änderungen sind erforderlich, um die Software mit neuen Technologien, Betriebssystemversionen oder sich ändernden Anforderungen in Einklang zu bringen.

[21a]

### Sanierung von Software
Software-Sanierung bezeichnet den Prozess der umfassenden Überarbeitung und Modernisierung von bestehender Software, um ihre Leistungsfähigkeit, Sicherheit und Wartbarkeit zu verbessern.
Dieser Prozess beinhaltet oft die Identifizierung und Behebung von Schwachstellen, die Aktualisierung veralteter Technologien und die Anpassung an aktuelle Standards.
Das Ziel der Software-Sanierung ist es, die Lebensdauer der Anwendung zu verlängern, ihre Funktionalität zu optimieren und sicherzustellen, dass sie den aktuellen Anforderungen und Best Practices entspricht.
Es ist eine strategische Maßnahme, um den langfristigen Nutzen und die Effizienz von Softwareanwendungen zu gewährleisten.

[1b,2b]

#### Bad Code Smells und Anti Patterns
**Code Smells:**
* Code Smells sind Anzeichen oder Hinweise auf mögliche Probleme oder Verbesserungsmöglichkeiten im Quellcode.
* Sie sind subtile, unspezifische Symptome, die darauf hinweisen können, dass Teile des Codes verbessert werden könnten.
* Code Smells weisen nicht direkt auf ein schwerwiegendes Problem hin, sondern signalisieren, dass eine nähere Prüfung und möglicher Refaktorings erforderlich sein könnte.
* Beispiele für Code Smells sind wiederholter Code, lange Methoden oder unklare Benennung von Variablen.

**Anti-Patterns:**
* Anti-Patterns sind wiederkehrende Muster oder Lösungen in der Softwareentwicklung, die als schlechte Praxis betrachtet werden.
* Im Gegensatz zu Code Smells handelt es sich bei Anti-Patterns um gut definierte, dokumentierte und wiedererkennbare Problemmuster.
* Sie stellen eine Warnung vor gängigen Fehlerquellen dar und bieten
Beispiele für ungewünschte Konsequenzen bestimmter Designentscheidungen.
* Beispiele für Anti-Patterns sind das "Big Ball of Mud"-Muster, bei dem der Code unstrukturiert und schwer wartbar ist, oder das "Golden Hammer"-Anti-Pattern, bei dem eine bestimmte Technologie für alle Probleme verwendet wird.

[1b,3b]

### Software System Management
Software System Management bezieht sich auf die Verwaltung und Kontrolle von Softwareanwendungen in einem IT-System.
Dies umfasst verschiedene Aspekte wie:

* Installation: Der Prozess der Einrichtung und Integration von Software in einem Computersystem.
* Konfiguration: Die Anpassung von Softwareeinstellungen, um sie an die spezifischen Anforderungen und Umgebungen anzupassen.
* Überwachung: Die kontinuierliche Beobachtung der Software, um Leistung, Verfügbarkeit und Sicherheit sicherzustellen.
* Wartung: Die Durchführung von Aktualisierungen, Patches und Fehlerbehebungen, um die Software auf dem neuesten Stand zu halten.
Aktualisierung: Die Implementierung von neuen Versionen oder Releases der Software, um Funktionen zu verbessern oder Sicherheitslücken zu beheben.

[1b,4b]

#### Logging vs Monitoring vs Observability
Logging:
Definition: Logging ist der Prozess des systematischen Aufzeichnens von Ereignissen, Zuständen oder Aktivitäten in einem System.
Zweck: Logs dienen der Protokollierung von Informationen, die für die Analyse von Fehlern, Diagnose von Problemen oder Überwachung von Aktivitäten relevant sind.
Inhalt: Logs enthalten normalerweise Zeitstempel, Benutzeraktionen, Fehlermeldungen und andere relevante Informationen.
Monitoring:

Definition: Monitoring bezieht sich auf die kontinuierliche Überwachung von Systemmetriken, Leistungsindikatoren oder Ereignissen in Echtzeit.
Zweck: Das Hauptziel des Monitorings ist es, frühzeitig auf Abweichungen oder Probleme im System hinzuweisen, um eine schnelle Reaktion zu ermöglichen.
Inhalt: Monitoring umfasst die Überwachung von Ressourcenauslastung, Systemleistung, Netzwerkaktivität und anderen messbaren Metriken.
Observability:

Definition: Observability ist ein Konzept, das darauf abzielt, die Sichtbarkeit und das Verständnis komplexer Systeme durch eine Kombination von Logging, Monitoring und Metriken zu verbessern.
Zweck: Observability ermöglicht es Entwicklern und Betreibern, tiefgreifende Einblicke in das Verhalten eines Systems zu gewinnen, insbesondere in nicht vorhersehbaren oder unerklärlichen Situationen.
Inhalt: Observability umfasst Logging für detaillierte Aufzeichnungen, Monitoring für Echtzeitüberwachung und Metriken für quantitative Messungen.

Zusammenfassend lässt sich sagen, dass Logging dazu dient, detaillierte Aufzeichnungen zu führen, Monitoring auf Echtzeitüberwachung abzielt und Observability ein umfassendes Verständnis und tiefe Einblicke in das System ermöglicht. Alle drei Konzepte sind wichtige Bestandteile des Managements und der Diagnose von Software- und Systemumgebungen.

[1b,5b]

#### Observability Konzepte

Observability-Konzepte beziehen sich auf Ansätze und Praktiken, die in Software- und Systemarchitekturen integriert werden, um eine verbesserte Sichtbarkeit, Verständnis und Diagnosefähigkeiten zu ermöglichen.

Im Folgenden werden einige wichtige Konzepte genannt.

[1b,6b]

##### Logs
Ein Log ist eine Aufzeichnung eines bestimmten Events in Textform.
Es beinhaltet immer einen Zeitstempel, also den exakten Moment des Auftreten des Events, und eine Nutzlast die Kontext liefert.
Logs tretten in verschiedenen Formaten auf. Unformatiert, Strukturiert und Binär.
Unformatierter Text ist am gängisten.
Strukturierte Logs bieten aber noch zusätzliche Daten und Metadaten und lassen sich zudem einfacher abfragen.

[6b]

##### Metrics
Eine Metrik ist ein Zahlenwert der in einem bestimmten Zeitintervall durch spzifische Attribute ermittelt wird.
Die Artibute sind z.B. Zeitstempel, Name und KPIs.
Metriken sind standardmäßg strukturiert im Gegensatz zu Logs, wodurch es einfacher macht sie abzufragen und und für die Speicherung zu optimieren, wordurch man sie länger verwahren kann.

[6b]

##### Traces
Traces zeigen den vollständigen Weg einer Anfrage durch ein verteiltes System auf.
Während sich eine Anfrage durch das Host-System bewegt, wird jede dafür durchgeführte Operation („Span“ genannt) mit wichtigen Daten kodiert, die sich auf den Microservice beziehen, der diese Operation ausführt. Anhand von Traces, die jeweils einen oder mehrere Spans enthalten, können Sie den Weg durch ein verteiltes System verfolgen und die Ursache eines Engpasses oder Ausfalls identifizieren.

[6b]

#### Werkzeuge
##### Prometheus, Grafana, Jaeger
**Prometheus:**
* Funktionalität: Prometheus ist ein leistungsstarkes Open-Source-System für das Monitoring und die Alarmierung von Softwareanwendungen. Es sammelt Metriken von verschiedenen Zielen, speichert sie zentral und ermöglicht die Abfrage und Visualisierung.

* Verwendung: Entwickler und Betreiber nutzen Prometheus, um die Leistung von Anwendungen und Infrastrukturkomponenten zu überwachen. Es unterstützt eine Vielzahl von Datenquellen und bietet flexible Abfrage- und Alarmierungsfunktionen.

**Grafana:**
* Funktionalität: Grafana ist ein Open-Source-Dashboard- und Visualisierungstool, das mit verschiedenen Datenquellen integriert werden kann, darunter Prometheus, InfluxDB und mehr. Es bietet eine benutzerfreundliche Oberfläche zur Erstellung von Dashboards und Visualisierung von Metriken.

* Verwendung: Grafana wird verwendet, um benutzerdefinierte Dashboards zu erstellen und Metriken in ansprechender Form darzustellen. Es ermöglicht eine umfassende Visualisierung von Daten, was es zu einem beliebten Werkzeug für das Monitoring und die Analyse macht.

**Jaeger:**
* Funktionalität: Jaeger ist ein Open-Source-System zur Verfolgung von Anfragen in verteilten Anwendungen. Es ermöglicht die Aufzeichnung und Analyse von Traces, um die Leistung und den Fluss von Anfragen durch verschiedene Dienste und Komponenten zu verstehen.

* Verwendung: Entwickler verwenden Jaeger, um die Transparenz in verteilten Systemen zu verbessern. Durch die Visualisierung von Traces können sie Engpässe, Latenzen und Wechselwirkungen zwischen Diensten identifizieren und optimieren.

[1b,7b]

### Technische Schulden
#### Definition
Technische Schulden in der Softwarewartung beziehen sich auf die Konsequenzen von Entscheidungen, die bewusst oder unbewusst getroffen wurden, um kurzfristige Vorteile zu erzielen, jedoch auf Kosten langfristiger Stabilität, Skalierbarkeit oder Wartbarkeit.

Es handelt sich um eine Metapher, die aufzeigt, dass technische Entscheidungen wie Schulden behandelt werden können, die zu einem späteren Zeitpunkt zurückgezahlt werden müssen.

[1b,8b]
#### Ursachen und Entstehung
Ursachen für das Entstehen von Technischen Schulden in der Softwareentwicklung können vielfältig sein und resultieren oft aus verschiedenen Herausforderungen im Entwicklungsprozess.
Ein zentraler Faktor ist häufig der Zeitdruck, der durch enge Projektfristen oder den Wunsch nach schneller Markteinführung entsteht.

Ressourcenmangel, sei es in Form von begrenzten personellen oder finanziellen Ressourcen, kann zu Kompromissen bei der technischen Qualität führen.
Unklare oder sich ändernde Anforderungen erschweren die Entwicklung, da Entscheidungen unter Unsicherheit getroffen werden müssen.

Die fehlende Expertise in bestimmten Technologien oder Domänen kann zu suboptimalen Lösungen führen, wenn Entwickler vor Herausforderungen stehen, für die sie nicht ausreichend qualifiziert sind. Organisatorische Prioritäten, die sich auf kurzfristige Ziele konzentrieren, können langfristige technische Überlegungen vernachlässigen.
Technologische Veränderungen und Fortschritte können dazu führen, dass bestehende Systeme veraltet sind, wenn keine regelmäßige Aktualisierung erfolgt.
Schließlich kann mangelnde Kommunikation zwischen den beteiligten Parteien zu Missverständnissen und fehlerhaften Designentscheidungen führen.

[1b,9b]


#### Risiken und Folgen (Warum ist das Thema wichtig?)
Risiken in der Softwareentwicklung sind potenzielle Bedrohungen oder Unsicherheiten, die den Erfolg eines Projekts gefährden können.
Sie können verschiedene Aspekte betreffen, darunter Zeit, Budget, Qualität, Sicherheit und Ressourcen.
Folgen von Risiken können erhebliche Auswirkungen auf die Projektziele und den gesamten Entwicklungsprozess haben.

**Allgemeine Risiken in der Softwareentwicklung könnten sein:**

1. Ungenügende Anforderungsdefinition: Unklare, widersprüchliche oder sich ändernde Anforderungen können zu Fehlinterpretationen und Fehlern führen.

1. Zeit- und Ressourcenmangel: Enge Zeitpläne und begrenzte Ressourcen können zu Überlastung der Teams, unvollständiger Testabdeckung und minderer Qualität führen.

1. Technologische Unsicherheit: Neue oder komplexe Technologien ohne ausreichende Expertise können die Entwicklung verlangsamen und zu Fehlern führen.

1. Personelle Risiken: Personalwechsel, unzureichende Qualifikationen oder Konflikte im Team können die Produktivität beeinträchtigen.

1. Externe Abhängigkeiten: Abhängigkeit von Drittanbietern oder externen Dienstleistern kann zu Verzögerungen und Unsicherheiten führen.

1. Sicherheitsrisiken: Unzureichende Sicherheitsmaßnahmen können zu Datenlecks, Datenschutzverletzungen oder anderen Sicherheitsproblemen führen.

**Die Folgen solcher Risiken können sein:**

1. Projektverzögerungen: Risiken können zu unvorhergesehenen Problemen führen, die die Projektzeitpläne verlängern.

1. Budgetüberschreitungen: Zusätzliche Arbeit oder unvorhergesehene Probleme können die Kosten erhöhen.

1. Qualitätsminderung: Zeitdruck und Ressourcenmangel können die Qualität der entwickelten Software beeinträchtigen.

1. Kundenzufriedenheit: Unerwartete Probleme können die Kundenzufriedenheit beeinträchtigen und das Vertrauen schädigen.

1. Reputationsschäden: Schwierigkeiten bei der Softwareentwicklung können das Image des Unternehmens beeinflussen.

[1b,9b]

#### Arten von technischen Schulden (Taxonomie)
Technische Schulden kann man in klar definierte Kategorien Teilen, die im Folgenden benannt und erklärt werden.

##### Architectural Debt
Architectural Debt (auch Architekturschulden genannt) bezieht sich auf die Konzeption und Struktur von Softwarearchitektur, die im Laufe der Zeit vernachlässigt, übersehen oder aufgrund von Zeit- und Ressourcenbeschränkungen nicht angemessen behandelt wurde.
Es handelt es sich bei der Architekturschuld um Kompromisse, die bewusst oder unbewusst eingegangen wurden, um kurzfristige Ziele zu erreichen, jedoch langfristige Konsequenzen haben können.

[1b,10b]

##### Documentation Debt
Documentaiton Debt (Dokumentations Schulden) beziehen sich auf den Abstand des Fortschritts zwischen der aktuellen Dokumentation und der Software.
Wenn Dokumentation nicht regelmäßig aktualisiert, überprüft und verbessert wird, wobei gleichzeitig die Softwareentwicklung vorankommt, nennt man es Documentation Debt.
Diese Schulden fürhren zu unvollsändiger, ungenauer und veralteter Dokumentation die Benutzer, Entwickler und Stakrholder verwirren und somit die Entwicklung verlangsamen.
Dadurch erhöht sich auch das Risoko and Buggs und Fehlern oder Sicherhetsproblemen.

[11b]

##### Implementation Debt
Implementation Debt (auch Implementierungsschulden genannt) bezieht sich auf die Kompromisse und Unzulänglichkeiten, die während der Implementierungsphase eines Softwareprojekts eingegangen wurden.

Dies kann beispielsweise unklaren oder nicht optimalen Code, fehlende Testabdeckung, Verstöße gegen Coding-Standards und andere Aspekte der Codequalität umfassen.

Implementation Debt entsteht oft durch Zeitdruck oder Ressourcenbeschränkungen, die dazu führen, dass Entwickler kurzfristige Entscheidungen treffen, um bestimmte Funktionen schnell zu implementieren.

Diese Kompromisse können langfristig zu Wartungsproblemen, erhöhtem Aufwand für Fehlerkorrekturen und einer insgesamt schlechteren Codequalität führen.

Um Implementation Debt zu reduzieren, ist es wichtig, regelmäßige Code-Reviews durchzuführen, auf bewährte Entwicklungspraktiken zu achten und kontinuierliche Verbesserungen in der Codebasis vorzunehmen.

[12b]

##### Testing Debt
Testing Debt beschreibt wenn die Software nicht genügend, fehlerhafte oder ungenaue Tests enthält.
Es stellt also den Unterschied dar zwischen wovon man ausgeht, was das System funktionieren sollte und wie das System tatsächlich funktioniert (Oder eher nicht funktioniert).
Wie bei den anderen Arten von Schulden sind auch hier wieder Zeitmangel, Recourcen knappheit und veränderung der Prioritäten die Ursachen.

[13b]

#### Technical Debt Management
##### Umgang mit technischen Schulden
**Identifikation und Priorisierung:** Beginnen Sie mit der Identifizierung und Bewertung von technischen Schulden. Priorisieren Sie sie basierend auf ihrer Dringlichkeit und Auswirkung auf die Software.

**Transparente Kommunikation:** Teilen Sie dem Team und den Stakeholdern die vorhandenen technischen Schulden mit. Transparente Kommunikation schafft Verständnis und Unterstützung für den Umgang mit diesen Schulden.

**Inkrementelle Verbesserungen:** Statt versuch, technische Schulden auf einmal zu beseitigen, setzen Sie auf inkrementelle Verbesserungen. Planen Sie regelmäßige Sprints oder Iterationen, um schrittweise Verbesserungen vorzunehmen.

**Automatisierte Tests:** Investieren Sie in automatisierte Tests, um sicherzustellen, dass die Software weiterhin stabil bleibt, während technische Schulden behoben werden. Dies erleichtert auch zukünftige Änderungen und Upgrades.

**Refaktorisierung:** Planen Sie Zeit für Refaktorisierungsarbeiten ein, um den Code zu verbessern, ohne die Funktionalität zu beeinträchtigen. Refaktorisierung hilft, Code klarer und leichter wartbar zu machen.

**Schulungen und Schulungen:** Stellen Sie sicher, dass Ihr Entwicklungsteam über die neuesten Best Practices und Technologien informiert ist. Schulungen können dazu beitragen, zukünftige technische Schulden zu vermeiden.

**Dokumentation aktualisieren:** Aktualisieren Sie die interne und externe Dokumentation, um sicherzustellen, dass sie mit den aktuellen Implementierungen übereinstimmt. Klare Dokumentation erleicht

[1b,14b]

###### operativ / konzeptionell
Operative Schulden und konzeptionelle Schulden sind zwei Arten von technischen Schulden, die sich in Softwareprojekten manifestieren können. Hier sind ihre Definitionen:

**Operative Schulden:**
Definition: Operative Schulden beziehen sich auf Kompromisse und Mängel, die während der laufenden Entwicklung und Wartung einer Software eingegangen werden.

Beispiele: Dies könnte unklaren oder nicht optimalen Code, fehlende Testabdeckung, kurzfristige Lösungen und andere Aspekte der Codequalität umfassen, die während der täglichen Entwicklungsarbeit entstehen.

**Konzeptionelle Schulden:**
Definition: Konzeptionelle Schulden beziehen sich auf Kompromisse und Mängel auf höherer, konzeptioneller Ebene, die oft bereits in der Planungs- und Designphase einer Softwareentscheidung getroffen werden.

Beispiele: Dies könnte eine nicht ausreichend durchdachte Architektur, unklare Anforderungen, eine unzureichende Modellierung der Domäne oder andere konzeptionelle Entscheidungen umfassen, die langfristige Auswirkungen auf die Softwarequalität haben.

[15b]

##### Erkennung von technischen Schulden
Technische Schulden lassen sich mit verschiedenen vorgehensweisen Messen/Erkennen.

###### Metriken
Es gibt verschiedene Metriken zur Messung von technischen Schulden.

**Code-Metriken:** Sie umfassen verschiedene Maßnahmen wie Code-Duplizierung und zyklomatische Komplexität.
Hohe Werte bedeuten hierbei auf hohe Schulden hin.

**Code-Churn:** Code-Churn ist eine Metrik die die quantiät der codeveränderungen misst.
Auch hier weißt ein hoher Wert auf Schulden hin.

**Time-to-Market:** Mit zunehmenden Schulden daurt es länger neue Features zu implementieren, da Entwickler mit kompizierteren/unverständlicherem Code Arbeiten müssen.
Eine Folge davon ist, dass sich er release der Softwarea verzögert.
Die Metrik misst diese verzögerung.

[16b]

###### SonarQube
SonarQube ist eine Plattform für Codeanalysen, die technische Qualität von Quellcode misst.
Das Tool unterstützt Entwickler die Qualität der Software zur überprüfen und zu verwalten um technische Schulden zu verringern.

[17b]

## Referenzen

[1b] :https://chat.openai.com

[2b] :https://software-sanieren.de/was-ist-software-sanierung/

[3b] :https://alokratnaparkhi8.medium.com/differences-between-code-smells-and-anti-patterns-d19351539f7f#:~:text=The%20most%20basic%20difference%20between,of%20hint%20and%20not%20patterns.

[4b] :https://www.ip-insider.de/was-ist-system-management-systems-management-a-1113687/#:~:text=Das%20Systems%20Management%20ist%20in,Drucker%2C%20Endger%C3%A4te%20und%20vieles%20mehr.

[5b] :https://rvprasad.medium.com/logging-monitoring-and-observability-219c043b5c81

[6b] :https://www.splunk.com/de_de/data-insider/what-is-observability.html

[7b] :https://chat.openai.com: Werkzeuge für software Management Prometheus, Grafana, Jaeger

[8b] :https://www.palladio-consulting.de/technische-schulden/#:~:text=Technical%20Debt%20oder%20kurz%20Tech,und%20k%C3%B6nnen%20IT%2DSystemfehler%20verursachen.

[9b] :https://www.objectbay.com/blog/technische-schulden

[10b] :https://www.google.com/search?q=software+architectural+debt+definition&sca_esv=591223588&rlz=1C1GCEA_enDE1022DE1022&sxsrf=AM9HkKnm0oqoROKTzxN84kEHDbRne4bniw%3A1702651146837&ei=CmV8ZZ3QMqTd7_UP67OrqAM&ved=0ahUKEwid_aHm1ZGDAxWk7rsIHevZCjUQ4dUDCBA&uact=5&oq=software+architectural+debt+definition&gs_lp=Egxnd3Mtd2l6LXNlcnAiJnNvZnR3YXJlIGFyY2hpdGVjdHVyYWwgZGVidCBkZWZpbml0aW9uMgUQIRigATIIECEYFhgeGB1IpAtQqgJYgQpwAXgBkAEAmAG3AaAB-QqqAQQwLjExuAEDyAEA-AEBwgIKEAAYRxjWBBiwA8ICCBAAGBYYHhgPwgIKECEYFhgeGA8YHcICBxAhGKABGAriAwQYACBBiAYBkAYC&sclient=gws-wiz-serp&safe=active&ssui=on

[11b] :https://www.linkedin.com/advice/0/how-do-you-deal-documentation-debt-legacy#was-sind-dokumentationsschulden?

[12b] ::https://chat.openai.com: Erkäre Implementation Debt

[13b] :https://testsigma.com/guides/test-debt/

[14b] :https://entwickler.de/programmierung/der-umgang-mit-technischen-schulden

[15b] :https://chat.openai.com: was sind operative und konzeptionelle Schulden?

[16b] :https://www.centron.de/tutorial/was-sind-technische-schulden/#:~:text=Messung%20der%20technischen%20Schulden&text=Hier%20sind%20einige%20M%C3%B6glichkeiten%2C%20technische,auf%20hohe%20technische%20Schulden%20hin.

[17b] :https://cloudogu.com/de/glossar/sonarqube/