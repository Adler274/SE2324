class: center, middle

## [Software Engineering](../../praesentationen.html)

#### Kapitel 10

## Wartung von Software (Software Maintainance)


Simon Fedrau, Sascha Hahn

---

# Inhalt
***
1. 

1.

1. Zusammenfassung

1. Quellen

---

### Fragen
***

---

## Wartung von Software (Software Maintainance)
***


---

### Definition Software-Wartung und Legacy-Code
***


---

### Evolution von Software
***


---

#### Ursachen für Änderungen an Software
***


---

#### Arten von Änderungen an Software
***


---

##### Korrektive, präventive, perfektionierende, adaptive Änderungen
***


---

### Sanierung von Software
***
Software-Sanierung bezeichnet den Prozess der umfassenden Überarbeitung und Modernisierung von bestehender Software, um ihre Leistungsfähigkeit, Sicherheit und Wartbarkeit zu verbessern.

Dieser Prozess beinhaltet oft die Identifizierung und Behebung von Schwachstellen, die Aktualisierung veralteter Technologien und die Anpassung an aktuelle Standards.

Das Ziel der Software-Sanierung ist es, die Lebensdauer der Anwendung zu verlängern, ihre Funktionalität zu optimieren und sicherzustellen, dass sie den aktuellen Anforderungen und Best Practices entspricht.

Es ist eine strategische Maßnahme, um den langfristigen Nutzen und die Effizienz von Softwareanwendungen zu gewährleisten.

[1b,2b]

---

#### Bad Code Smells und Anti Patterns
***
**Code Smells:**
* Anzeichen oder Hinweise auf mögliche Probleme oder Verbesserungsmöglichkeiten im Quellcode.

* subtile, unspezifische Symptome, die darauf hinweisen können, dass Teile des Codes verbessert werden könnten.

* weisen nicht direkt auf ein schwerwiegendes Problem hin
    * signalisieren, dass eine nähere Prüfung und möglicher Refaktorings erforderlich sein könnte.

* **Beispiele** für Code Smells sind wiederholter Code, lange Methoden oder unklare Benennung von Variablen.

[1b,3b]

---

#### Bad Code Smells und Anti Patterns
***
**Anti-Patterns:**
* wiederkehrende Muster oder Lösungen in der Softwareentwicklung, die als schlechte Praxis betrachtet werden.

* Im Gegensatz zu Code Smells handelt es sich bei Anti-Patterns um gut definierte, dokumentierte und wiedererkennbare Problemmuster.

* stellen eine Warnung vor gängigen Fehlerquellen dar
* bieten Beispiele für ungewünschte Konsequenzen bestimmter Designentscheidungen.

* **Beispiele** für Anti-Patterns sind das "Big Ball of Mud"-Muster, bei dem der Code unstrukturiert und schwer wartbar ist, oder das "Golden Hammer"-Anti-Pattern, bei dem eine bestimmte Technologie für alle Probleme verwendet wird.

[1b,3b]

---

### Software System Management
***
Software System Management bezieht sich auf die Verwaltung und Kontrolle von Softwareanwendungen in einem IT-System.
Aspekte:

* **Installation:** Der Prozess der Einrichtung und Integration von Software in einem Computersystem.

* **Konfiguration:** Die Anpassung von Softwareeinstellungen, um sie an die spezifischen Anforderungen und Umgebungen anzupassen.

* **Überwachung:** Die kontinuierliche Beobachtung der Software, um Leistung, Verfügbarkeit und Sicherheit sicherzustellen.

* **Wartung:** Die Durchführung von Aktualisierungen, Patches und Fehlerbehebungen, um die Software auf dem neuesten Stand zu halten.
Aktualisierung: Die Implementierung von neuen Versionen oder Releases der Software, um Funktionen zu verbessern oder Sicherheitslücken zu beheben.

[1b,4b]

---

#### Logging vs Monitoring vs Observability
***
**Logging:**
* **Definition:** Logging ist der Prozess des systematischen Aufzeichnens von Ereignissen, Zuständen oder Aktivitäten in einem System.

* **Zweck:** Logs dienen der Protokollierung von Informationen, die für die Analyse von Fehlern, Diagnose von Problemen oder Überwachung von Aktivitäten relevant sind.

* **Inhalt:** Logs enthalten normalerweise Zeitstempel, Benutzeraktionen, Fehlermeldungen und andere relevante Informationen.

[1b,5b]

---

#### Logging vs Monitoring vs Observability
***
**Monitoring:**
* **Definition:** Monitoring bezieht sich auf die kontinuierliche Überwachung von Systemmetriken, Leistungsindikatoren oder Ereignissen in Echtzeit.

* **Zweck:** Das Hauptziel des Monitorings ist es, frühzeitig auf Abweichungen oder Probleme im System hinzuweisen, um eine schnelle Reaktion zu ermöglichen.

* **Inhalt:** Monitoring umfasst die Überwachung von Ressourcenauslastung, Systemleistung, Netzwerkaktivität und anderen messbaren Metriken.

[1b,5b]

---

#### Logging vs Monitoring vs Observability
***
**Observability:**
* **Definition:** Observability ist ein Konzept, das darauf abzielt, die Sichtbarkeit und das Verständnis komplexer Systeme durch eine Kombination von Logging, Monitoring und Metriken zu verbessern.

* **Zweck:** Observability ermöglicht es Entwicklern und Betreibern, tiefgreifende Einblicke in das Verhalten eines Systems zu gewinnen, insbesondere in nicht vorhersehbaren oder unerklärlichen Situationen.

* **Inhalt:** Observability umfasst Logging für detaillierte Aufzeichnungen, Monitoring für Echtzeitüberwachung und Metriken für quantitative Messungen.
***
Zusammenfassend lässt sich sagen, dass Logging dazu dient, detaillierte Aufzeichnungen zu führen, Monitoring auf Echtzeitüberwachung abzielt und Observability ein umfassendes Verständnis und tiefe Einblicke in das System ermöglicht.
Alle drei Konzepte sind wichtige Bestandteile des Managements und der Diagnose von Software- und Systemumgebungen.

[1b,5b]

---

#### Observability Konzepte
***
Observability-Konzepte beziehen sich auf Ansätze und Praktiken, die in Software- und Systemarchitekturen integriert werden, um eine verbesserte Sichtbarkeit, Verständnis und Diagnosefähigkeiten zu ermöglichen.

**Im Folgenden werden einige wichtige Konzepte genannt.**

[1b,6b]

---

##### Logs
***
* Aufzeichnung eines bestimmten Events in Textform

* beinhaltet immer einen Zeitstempel
    * also den exakten Moment des Auftreten des Events, und eine Nutzlast die Kontext liefert

* tretten in verschiedenen Formaten auf
    * Unformatiert, Strukturiert und Binär.
    * Unformatierter Text ist am gängisten.
    * Strukturierte Logs bieten aber noch zusätzliche Daten und Metadaten und lassen sich zudem einfacher abfragen.

[6b]

---

##### Metrics
***
* Zahlenwert der in einem bestimmten Zeitintervall durch spzifische Attribute ermittelt wird

* Artibute sind z.B. Zeitstempel, Name und KPIs.

* Metriken sind standardmäßg strukturiert im Gegensatz zu Logs, wodurch es einfacher macht sie abzufragen und und für die Speicherung zu optimieren
    * macht längere verwahrung möglich

[6b]

---

##### Traces
***
* zeigen den vollständigen Weg einer Anfrage durch ein verteiltes System auf

* Während sich eine Anfrage durch das Host-System bewegt, wird jede dafür durchgeführte Operation („Span“ genannt) mit wichtigen Daten kodiert, die sich auf den Microservice beziehen, der diese Operation ausführt

* Anhand von Traces, die jeweils einen oder mehrere Spans enthalten, können Sie den Weg durch ein verteiltes System verfolgen und die Ursache eines Engpasses oder Ausfalls identifizieren.

[6b]

---

#### Werkzeuge
##### Prometheus, Grafana, Jaeger
***
**Prometheus:**
* **Funktionalität:**

Prometheus ist ein leistungsstarkes Open-Source-System für das Monitoring und die Alarmierung von Softwareanwendungen.

Es sammelt Metriken von verschiedenen Zielen, speichert sie zentral und ermöglicht die Abfrage und Visualisierung.

* **Verwendung:**

Entwickler und Betreiber nutzen Prometheus, um die Leistung von Anwendungen und Infrastrukturkomponenten zu überwachen.

Es unterstützt eine Vielzahl von Datenquellen und bietet flexible Abfrage- und Alarmierungsfunktionen.

[1b,7b]

---

#### Werkzeuge
##### Prometheus, Grafana, Jaeger
***
**Grafana:**
* **Funktionalität:**

Grafana ist ein Open-Source-Dashboard- und Visualisierungstool, das mit verschiedenen Datenquellen integriert werden kann, darunter Prometheus, InfluxDB und mehr.

Es bietet eine benutzerfreundliche Oberfläche zur Erstellung von Dashboards und Visualisierung von Metriken.

* **Verwendung:**

Grafana wird verwendet, um benutzerdefinierte Dashboards zu erstellen und Metriken in ansprechender Form darzustellen.

Es ermöglicht eine umfassende Visualisierung von Daten, was es zu einem beliebten Werkzeug für das Monitoring und die Analyse macht.

[1b,7b]

---

#### Werkzeuge
##### Prometheus, Grafana, Jaeger
***
**Jaeger:**
* **Funktionalität:**

Jaeger ist ein Open-Source-System zur Verfolgung von Anfragen in verteilten Anwendungen.

Es ermöglicht die Aufzeichnung und Analyse von Traces, um die Leistung und den Fluss von Anfragen durch verschiedene Dienste und Komponenten zu verstehen.

* **Verwendung:**

Entwickler verwenden Jaeger, um die Transparenz in verteilten Systemen zu verbessern. 

Durch die Visualisierung von Traces können sie Engpässe, Latenzen und Wechselwirkungen zwischen Diensten identifizieren und optimieren.

[1b,7b]

---

### Technische Schulden
#### Definition
***
Technische Schulden in der Softwarewartung beziehen sich auf die Konsequenzen von Entscheidungen, die bewusst oder unbewusst getroffen wurden, um kurzfristige Vorteile zu erzielen, jedoch auf Kosten langfristiger Stabilität, Skalierbarkeit oder Wartbarkeit.

Im folgenden werden Ursachen, Risiken, Folgen und Arten erkäutert.

[1b,8b]

---

#### Ursachen und Entstehung
***
Ursachen für das Entstehen von Technischen Schulden in der Softwareentwicklung können vielfältig sein und resultieren oft aus verschiedenen Herausforderungen im Entwicklungsprozess.

* Zeitdruck, der durch enge Projektfristen oder den Wunsch nach schneller Markteinführung entsteht

* Ressourcenmangel, sei es in Form von begrenzten personellen oder finanziellen Ressourcen, kann zu Kompromissen bei der technischen Qualität führen.

* Unklare oder sich ändernde Anforderungen erschweren die Entwicklung
    * Entscheidungen müssen unter Unsicherheit getroffen werden

* Fehlende Expertise in bestimmten Technologien oder Domänen kann zu suboptimalen Lösungen führen, wenn Entwickler vor Herausforderungen stehen, für die sie nicht ausreichend qualifiziert sind

[1b,9b]

---

#### Ursachen und Entstehung
***
* Organisatorische Prioritäten, die sich auf kurzfristige Ziele konzentrieren
    * können langfristige technische Überlegungen vernachlässigen.

* Technologische Veränderungen und Fortschritte können dazu führen, dass bestehende Systeme veraltet sind, wenn keine regelmäßige Aktualisierung erfolgt.

* Schließlich kann mangelnde Kommunikation zwischen den beteiligten Parteien zu Missverständnissen und fehlerhaften Designentscheidungen führen.

[1b,9b]

---

#### Risiken und Folgen (Warum ist das Thema wichtig?)
***
Risiken in der Softwareentwicklung sind potenzielle Bedrohungen oder Unsicherheiten, die den Erfolg eines Projekts gefährden können.

Sie können verschiedene Aspekte betreffen, darunter Zeit, Budget, Qualität, Sicherheit und Ressourcen.

[1b,9b]

---

#### Risiken und Folgen (Warum ist das Thema wichtig?)
***
**Allgemeine Risiken in der Softwareentwicklung könnten sein:**

1. Ungenügende Anforderungsdefinition: Unklare, widersprüchliche oder sich ändernde Anforderungen können zu Fehlinterpretationen und Fehlern führen.

1. Zeit- und Ressourcenmangel: Enge Zeitpläne und begrenzte Ressourcen können zu Überlastung der Teams, unvollständiger Testabdeckung und minderer Qualität führen.

1. Technologische Unsicherheit: Neue oder komplexe Technologien ohne ausreichende Expertise können die Entwicklung verlangsamen und zu Fehlern führen.

1. Personelle Risiken: Personalwechsel, unzureichende Qualifikationen oder Konflikte im Team können die Produktivität beeinträchtigen.

1. Externe Abhängigkeiten: Abhängigkeit von Drittanbietern oder externen Dienstleistern kann zu Verzögerungen und Unsicherheiten führen.

1. Sicherheitsrisiken: Unzureichende Sicherheitsmaßnahmen können zu Datenlecks, Datenschutzverletzungen oder anderen Sicherheitsproblemen führen.

[1b,9b]

---

#### Risiken und Folgen (Warum ist das Thema wichtig?)
***
**Die Folgen solcher Risiken können sein:**

1. Projektverzögerungen: Risiken können zu unvorhergesehenen Problemen führen, die die Projektzeitpläne verlängern.

1. Budgetüberschreitungen: Zusätzliche Arbeit oder unvorhergesehene Probleme können die Kosten erhöhen.

1. Qualitätsminderung: Zeitdruck und Ressourcenmangel können die Qualität der entwickelten Software beeinträchtigen.

1. Kundenzufriedenheit: Unerwartete Probleme können die Kundenzufriedenheit beeinträchtigen und das Vertrauen schädigen.

1. Reputationsschäden: Schwierigkeiten bei der Softwareentwicklung können das Image des Unternehmens beeinflussen.

[1b,9b]

---

#### Arten von technischen Schulden (Taxonomie)
***


---

##### Architectural Debt
***


---

##### Documentation Debt
***


---

##### Implementation Debt
***


---

##### Testing Debt
***


---

##### etc.
***


---

#### Technical Debt Management
***


---

##### Umgang mit technischen Schulden
***


---

###### operativ / konzeptionell
***


---

##### Erkennung von technischen Schulden
***


---

###### Metriken 
***


---

###### Werkzeuge
***


---

###### SonarQube
***


---

class: center, middle

# Fragen?

---

# Quellen
***