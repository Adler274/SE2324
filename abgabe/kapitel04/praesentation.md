class: center, middle

## [Software Engineering](../../praesentationen.html)

#### Kapitel 4


Simon Fedrau, Sascha Hahn

---
# Inhalt
***
1. Software system integration

1. Software system interfaces

1. APIs

1. Quellen

---
## APIs

**Was ist eine API?**
***
API ist die Abkürzung für „application programming interface“ und der gängige Fachbegriff für eine Programmierschnittstelle, auch Anwendungsschnittstelle genannt. Bieten Online-Dienste solche Schnittstellen an, wird häufig der Begriff „Webservices“ verwendet.
[1]

**Wie funktionieren APIs?**

APIs ermöglichen die nahtlose Kommunikation zwischen Produkten und Diensten, verbessern die Anwendungsentwicklung, sparen Zeit und Geld, fördern Flexibilität und Innovation. Sie erleichtern die Integration Ihrer Infrastruktur, den Datenaustausch mit Kunden und bieten Geschäftschancen, einschließlich Monetarisierung.
---
### API vs. SDK
***
**Was ist eine SDK?**

Ein SDK (Software Development Kit) bietet eine integrierte Plattform, um Anwendungen effizient von Grund auf neu zu entwickeln. Es enthält Bausteine, die den Entwicklungsprozess verkürzen. Statt Code von Grund auf neu zu schreiben, können Sie auf Bibliotheken, Compiler, Debugger, Codebeispiele und Dokumentation im SDK zurückgreifen. Die integrierte Entwicklungsumgebung verbindet alle im SDK enthaltenen Tools.

---

**Unterschied und Einsatzgebiete**
***
* **API**

  * Mechanismus für die Kommunikation zwischen Softwarekomponenten
  * Ermöglicht die Interaktion mit bestehenden Softwarekomponenten
  * Integration vorentwickelter Funktionen in Ihren Code
  * Einsatzgebiete:
    * Datenaustausch zwischen Anwendungen
    * Integration von Diensten von Drittanbietern (z. B. Zahlungsabwicklung)
    * Erstellung von benutzerdefinierten Erweiterungen für Plattformen
  
* **SDK**

  * Plattformspezifische Entwicklungstools wie Debugger, Compiler und Bibliotheken
  * Enthält Bausteine zur Beschleunigung des Entwicklungsprozesses
  * Bereitstellung von Tools und Ressourcen von Drittanbietern
  * Einsatzgebiete:
    * Entwicklung von Anwendungen für eine bestimmte Plattform
    * Verwendung von vorgefertigten Bausteinen, um die Entwicklungszeit zu verkürzen
    * Schaffung konsistenter Entwicklungsprozesse
---

### API Styles
***
  API Styles sind grundlegende Ansätze und Methoden, die bei der Gestaltung von APIs verwendet werden, um die Art und Weise zu definieren, wie API-Endpunkte, Anfragen, und Antworten strukturiert werden. Sie beeinflussen, wie Entwickler mit der API interagieren und welche Konventionen bei der Kommunikation befolgt werden sollten. 

---

### Resource style
***

**Was ist der Resource Style?**

  Ein ressourcenorientierter API-Designstil
  Betont die Freigabe von Ressourcen für Verbraucher

  **Beispiele für Ressourcen:**

Vergleichbar mit Webseiten beim Entwurf einer Website
Ressourcen können persistente Konzepte wie Produkte und Kundendaten oder prozessorientierte Konzepte wie Bestellungen und Versandoptionen darstellen.

**Popularität des Resource Styles:**

Häufig verwendet, bestätigt durch die Popularität von OpenAPI
Fokus auf die Offenlegung der API-Funktionalität durch Ressourcen
Vorteile des Resource Styles:

Abstrahiert Implementierungsdetails hinter den Ressourcen
Bietet eine klare und konsistente Struktur für die API

---
### Hypermedia-Style
***
**Was ist der Hypermedia-Style?**
  * Ähnlich zum Navigieren im Web
  * Verknüpft Ressourcen mithilfe von Links
  * Maschinen entscheiden normalerweise über die Navigation
  * Links benötigen maschinenlesbare Bezeichnungen

**Bezeichnungen in Hypermedia-APIs:**
  * Konzeptuell ähnlich wie Textlinks auf Webseiten
  * In maschinenlesbarer Darstellung, oft in JSON
  * Ermöglichen das Navigieren zwischen Ressourcen
**Herausforderungen:**
  * Benutzerfreundliches Navigieren kann zu fragmentierten Informationen führen
  * "Gesprächige" APIs, die mehrere Interaktionen erfordern
  * API-Nutzer sind oft unsicher über ihre Anforderungen

**Effizienz und Anwendungsfall:**
* Geeignet für Szenarien, in denen Navigieren und Entdecken wichtig sind
* Nicht ideal, wenn Benutzer präzise Ergebnisse benötigen

---
### Query style
***
**Was ist der Query Style?**
* Ein einzelner Einstiegspunkt für den Zugriff auf Ressourcen
* API-Anbieter verwaltet strukturierte Ressourcen
* Abfrageergebnisse ähnlich der Arbeitsweise von Datenbankabfragen

**Vorteile des Query Styles:**
* Individuelle Anforderungen können abgefragt werden
* Kombinieren von Ergebnissen in einer einzigen Abfrage
* Effizienzsteigerung durch Reduzierung von HTTP-Anfragen

**Herausforderungen:**
* Abfragekomplexität erfordert Verständnis des Daten- und Abfragemodells
* Cache-Implementierung kann komplexer sein
* Begrenzung von Anfragen in einigen Implementierungen

**Anwendungsgebiete:**
* Geeignet für flexible und individuelle Datenabfragen
* Ideal für Szenarien, in denen viele verschachtelte Ressourcen benötigt werden

---

### Tunnel Style 
***
**Was ist der Tunnel Style?**
* API als Sammlung von remote aufrufbaren Funktionen
* APIs erweitern lokale Programmierungsszenarien

**Haupttechnik: Remote Procedure Calls (RPC)**
* Client sendet Anfragen an entfernten Server für bestimmte Verfahren
* Antwort wird vom Server an den Client gesendet
* Einfach und praktisch, aber weniger häufig in moderner API-Entwicklung

**Effiziente Implementierung: gRPC**
* SDKs für verschiedene Sprachen und Plattformen
* Verwendet Protocol Buffers für Serialisierung und Deserialisierung
* Nutzt HTTP/2 für optimierte binäre Übertragungen und bidirektionales Streaming

---

### Event-based style
***
- Was ist der Event-based Style?
  - API-Anbieter erzeugt Ereignisse und informiert API-Nutzer darüber
  - Nutzer erwarten Benachrichtigungen bei Zustandsänderungen in der API

- Message-Broker-Konzept:
  - Broker verwaltet und leitet Ereignisse
  - Konsumenten abonnieren spezifische Ereignistypen
  - Schwerpunkt auf der Architektur des Auslieferungs-Brokers

- Herausforderungen und Lösungen:
  - Implementierungsaufwand kann höher sein
  - Potenzielle Probleme wie doppelte Nachrichten
  - Fehlerbehebung und Überwachung erfordern spezielle Tools

---
### API Implementation Standards
***
API Implementation Standards sind Leitlinien und Best Practices, die bei der Entwicklung und Umsetzung von APIs (Application Programming Interfaces) befolgt werden sollten. Diese Standards dienen dazu, die Qualität, Konsistenz, Interoperabilität und Sicherheit von APIs sicherzustellen.

**Wichtige Aspekte der API Implementation Standards:**

- Konsistenz in Bezug auf Endpunktbenennung und URI-Struktur
- Datensicherheit und Authentifizierungsmethoden
- Dokumentation und Beschreibung von API-Ressourcen
- Versionierung und Änderungsverwaltung
- Fehlerbehandlung und Statuscodes
- Performanzoptimierung und Lastverteilung
- Compliance mit branchenspezifischen Vorschriften (z. B. GDPR)

---

### Vergleich, Motivation, Vorteile, Nachteile
***

**Vergleich:**
* Einheitlicher Ansatz:
   * Standards vs. individuelle Entwicklung.
   * Qualität und Wartbarkeit.

* Verschiedene Standards:
  * REST, GraphQL, SOAP usw.
  * Anwendungsfall-basierte Wahl.

**Motivation:**
* Interoperabilität:
  * Plattformunabhängige API-Entwicklung.
  * Qualitativ hochwertige APIs.

* Effizienz:
  * Schnellere Entwicklung durch Standards.

---
### Vergleich, Motivation, Vorteile, Nachteile
***

**Vorteile:**

* Konsistenz und Interoperabilität:

  * Einheitliche Struktur, Integration.

  * Sicherheit und Dokumentation.

**Nachteile:**

* Kreativitätseinschränkung:

  * Strikte Standards in innovativen Fällen.
  * Steile Lernkurven bei einigen Standards.
 
  * Regulierung:

  * Übermäßige Standards können Flexibilität behindern.

---
### RESTful
***

- **Representational State Transfer (REST):**
  - Software-Architektur für API-Design.
  - Leitfaden für effiziente Kommunikation.
  
- **RESTful-APIs:**
  - Schnittstellen für sicheren Informationsaustausch.
  - Verbindung von Computersystemen.
  
- **Wichtige Merkmale:**
  - Leicht implementierbar und modifizierbar.
  - Sichtbarkeit und Portierbarkeit.
  
- **Anwendungsbeispiele:**
  * Monatliche Gehaltsabrechnungen.
  * Kommunikation zwischen Systemen.

---
### HATEOAS
***

- **HATEOAS-Prinzip:**
  - "Hypermedia as the Engine of Application State."
  - Teil der REST-Architektur, von Fielding definiert.
  - REST-Client navigiert durch Hypermedia-URIs.

- **URIs im Hypermedia-Format:**
  - Bereitstellung von URIs durch die Anwendung.
  - HTML-Dokumente, JSON, oder XML-Attribute/Elemente.

- **Anpassbare Schnittstelle:**
  - Einzigartiger Vorteil von HATEOAS.
  - Flexibilität zur Anpassung der API.

- **Vergleich mit SOAP:**
  - Gegenüber SOAP-basierten Strukturen.

[10] [11]

---


### Naming REST API Endpoints
***
- **Entscheidende Aspekte:**
  - Klare, verständliche und konsistente API-Gestaltung.

- **Bewährte Praktiken und Empfehlungen:**
  - Verwendung von Substantiven: Beschreibung der Ressourcen, Vermeidung von Verben.

  - Klare und beschreibende Namen: Verständliche Benennungen, keine Abkürzungen.

  - Plurale Form für Sammlungen: Konsistenz und Verständlichkeit.

  - Hierarchische Struktur: Darstellung von Beziehungen.

  - Verwendung von Bindestrichen: Trennung von Worten.

  - Versionierung: Hinzufügen der Version für Abwärtskompatibilität.

  - Klare Hierarchie: Intuitive Navigation für Benutzer.

[12] [13] [14]

---
### Error Handling
***
- **Grundlegende Antworten:**
  - Verwendung von Statuscodes, um Fehler zu identifizieren.
  - Beispiele für häufige Statuscodes: 400, 401, 403, 404, 412, 500, 503.

- **Standardmäßige Spring-Fehlerantworten:**
  - Spring enthält standardmäßige Fehlerbehandlung für gängige Ausnahmen.
  - Verwendung des spezifischsten Fehlercodes wird empfohlen.

- **Detaillierte Antworten:**
  - Manchmal sind Statuscodes allein nicht ausreichend.
  - Error, Message, Detail und Help bieten zusätzliche Informationen.
  - Fehlerkennung, Nachricht für Benutzer und detaillierte Erklärung.
  
- **Standardisierte Antworttexte:**
  - RFC 7807 bietet ein generalisiertes Fehlerbehandlungsschema.
  - Enthält "type", "title", "status", "detail" und "instance".
  - Fördert einheitliche Fehlerbehandlung in RESTful APIs.
[15]
---
### Best Practices Security
***

- Zugriffsrichtlinie und Autorisierung: 
Definieren, wer auf Ihre API-Ressourcen zugreifen darf.

- **TLS verwenden:** Schützen Sie Daten während der Übertragung mit Transport Layer Security (TLS).

- **OAuth2 für SSO:** Nutzen Sie OAuth2 für sicheres Single Sign-On (SSO).

- **API-Schlüssel:** Gewähren Sie programmatischen Zugriff, behandeln Sie API-Schlüssel sorgfältig.

- **Differenzierte Berechtigungen:** Konfigurieren Sie Berechtigungen für verschiedene API-Schlüssel zur Zugriffssteuerung.

- **Komplexe Autorisierungslogik:** Implementieren Sie komplexe Autorisierungslogik in der Anwendungslogik, nicht in der Middleware.

- **Bewährte Tools nutzen:** Vertrauen Sie bewährten Bibliotheken und Tools zur Fehlerminimierung und Vereinfachung der Autorisierung.

- **Sicherheit hat Priorität:** Sicherheit und korrekte Autorisierung sind entscheidend für sichere und nützliche API-Endpunkte.

---

### GraphQL
***

- GraphQL ist eine Abfragesprache und serverseitige Runtime für APIs.

- Es bietet nur die benötigten Daten für Clients an, wodurch APIs schneller und flexibler werden.

- GraphQL ermöglicht das gleichzeitige Abrufen von Daten aus verschiedenen Quellen mit einer einzigen Anfrage.

- API-Maintainer können Felder hinzufügen oder entfernen, ohne bestehende Abfragen zu beeinträchtigen.

- Entwickler können APIs auf ihre bevorzugte Weise erstellen, und GraphQL stellt sicher, dass sie auf vorhersehbare Weise funktionieren.
[16]
---

### Schema in GraphQL
***

- Das Schema bildet die Grundlage jeder GraphQL-API.

- Es definiert, welche Daten abgerufen werden können und wie sie strukturiert sind.

- Das Schema besteht aus zwei Hauptteilen:

  - **Query-Typ:** Enthält Abfragen (Queries) zum Abrufen von Daten.

  - **Mutation-Typ:** Enthält Mutationen zum Ändern oder Erstellen von Daten.

- In der Regel wird das Schema in einer speziellen Abfragesprache definiert, die oft als "Schema Definition Language" (SDL) bezeichnet wird.
[16] [17]
---

### Query in GraphQL
***
- Eine Query in GraphQL ist eine Abfrageoperation, mit der Daten aus der API abgerufen werden.

- Sie ermöglicht dem Client, präzise anzugeben, welche Daten und Felder benötigt werden.

- Die Struktur einer Query folgt dem Schema und spiegelt oft die gewünschte Datenstruktur wider.

- Beispiel einer Query: "Gib mir den Namen und das Alter eines Benutzers sowie die Titel seiner Beiträge."

[17] [18]
---

### Resolver in GraphQL

- Resolver sind Funktionen, die die eigentliche Arbeit in einer GraphQL-API ausführen.

- Jedes Feld im Schema ist einem Resolver zugeordnet.

- Wenn eine Query ausgeführt wird, ruft GraphQL die entsprechenden Resolver auf, um die angeforderten Daten zu erhalten.

- Resolver können Daten aus einer Datenbank abrufen, APIs aufrufen, Berechnungen durchführen oder auf andere Weise die Daten bereitstellen, die in der Query angefordert werden.

- Beispiel für einen Resolver: "Wenn nach dem Namen eines Benutzers gefragt wird, greife auf die Datenbank zu und gib den Namen des Benutzers zurück."

[17] [18]

---

### Mutation in GraphQL
***

- Mutationen sind Operationen in GraphQL, mit denen Daten geändert oder erstellt werden können.

- Im Gegensatz zu Queries, die nur lesend sind, erlauben Mutationen das Schreiben von Daten auf den Server.

- Mutationen sind oft in der Art einer Anfrage aufgebaut, die beschreibt, welche Daten geändert oder hinzugefügt werden sollen.

- Beispiel für eine Mutation: "Erstelle einen neuen Benutzer mit dem Namen und der E-Mail-Adresse."

[17] [18]

---

### Backend For Frontend (BFF-Muster)
***

- Das Backends for Frontends Pattern  ist ein Designmuster für die Architektur von Mikroservices.
- Dieses Muster konzentriert sich auf die Trennung von API-Gateways entsprechend den spezifischen Frontend-Anwendungen.
- Anstatt nur ein allgemeines API-Backend zu haben, werden mehrere Backend-Services für Frontend-Anwendungen bereitgestellt, und dazwischen wird ein API-Gateway zur Handhabung von Routing und Aggregationsvorgängen platziert.
- hilft den sogenannten Single Point of Failure zu vermeiden, da mehrere API-Gateways für verschiedene Frontend-Anwendungen geschaffen werden.
- Es können unterschiedliche Anforderungen der Frontend-Anwendungen erfüllt werden, ohne die anderen Frontend-Anwendungen zu beeinträchtigen.
- Das BFF-Muster ist besonders hilfreich, wenn eine Anpassung eines einzigen Backends für verschiedene Benutzeroberflächen vermieden werden soll.[18]


---
### API Design
***
- API-Design bezieht sich auf die Gestaltung von Schnittstellen, über die Softwarekomponenten miteinander kommunizieren.

- Eine gut gestaltete API sollte folgende Eigenschaften aufweisen:
  - Benutzerfreundlichkeit: Einfache und intuitive Nutzung für Entwickler.
  - Konsistenz: Einheitliche Struktur und Namenskonventionen.
  - Effizienz: Schnelle und ressourceneffiziente Datenübertragung.
  - Sicherheit: Schutz vor unautorisiertem Zugriff und Datenlecks.
  - Dokumentation: Klare und umfassende Anleitungen für Entwickler.
  - Flexibilität: Anpassbar an verschiedene Anwendungsfälle.
  - Testbarkeit: Einfache Prüfung und Fehlerbehebung.
  - Überwachbarkeit: Ermöglicht die Überwachung und Analyse der API-Nutzung.

- Ein gutes API-Design ist entscheidend, um die Nutzung und Integration von Software zu erleichtern.
[19]

---

### Code First vs. Design First
***
- Code-First-Ansatz:
  - Beginnt mit dem Schreiben des API-Codes.
  - Schnellere Entwicklung und direkte Kontrolle.
  - Mangel an klarer Spezifikation und umfassender Dokumentation.
  - Kann zu Problemen führen.

- Design-First-Ansatz:
  - Legt die API-Spezifikation zuerst fest.
  - Bessere Benutzerfreundlichkeit.
  - Kürzere Entwicklungszeit.
  - Verbesserte Dokumentation.
  - Kann die Flexibilität einschränken.
  - Erfordert spezialisierte Designwerkzeuge.

---
### API Versioning
***

- Bedeutung: Wichtig bei API-Veröffentlichungen.
- Ziel: Bestehende Anwendungen sollen korrekt funktionieren, während neue Funktionen hinzugefügt oder verbessert werden.

* Ansätze:

1. **URI-Versionierung:** Versionsnummer in der URL, z.B. https://api.example.com/v1/resource.
2. **Header-Versionierung:** Version im HTTP-Header der Anfrage oder Antwort.
3. **Media-Type-Versionierung:** Version im Media Type, z.B., `application/vnd.example.v1+json`.
4. **Accept-Version Header:** Der Client gibt mit dem Accept-Version-Header an, welche API-Version er verwenden möchte.

*  Wichtige Aspekte:

- Bewahrung der Abwärtskompatibilität.
- Keine Beeinträchtigung bestehender Benutzer.
- Raum für Weiterentwicklung.
- Der Ansatz hängt von den Projektanforderungen ab.
[20] [21]
---

### API Testing

- **Zweck:** Überprüfung von APIs auf Funktionalität, Leistung, Zuverlässigkeit und Sicherheit.

- **Wichtigkeit:** Verhindert Fehler, sichert Zuverlässigkeit und fördert effiziente Nutzung.

- **Testarten:** Funktionale, Leistungs-, Sicherheits- und Zuverlässigkeitstests.

- **Werkzeuge:** Postman, Newman, JUnit und spezialisierte API-Testtools.

- **Automatisierung:** Automatisierung für effiziente und wiederholbare Tests.

- **Testabdeckung:** Deckt verschiedene Szenarien ab.

API-Tests sind entscheidend für eine zuverlässige und fehlerfreie API-Nutzung.

[22]
---
### OpenAPI
***
- **Was ist OpenAPI?** Ein Standard zur API-Beschreibung.
- **Zweck:** Beschreibung, Entwicklung, Test und Dokumentation von REST-APIs.
- **Unterschied zu JSON Schema:** OpenAPI beschreibt die gesamte API, inklusive Endpunkten und Formatierung von Anfragen und Antworten.
- **Warum ist OpenAPI nützlich?** Ermöglicht die Generierung von Dokumentation und Mock-Servern.
- **Vereinfacht:** Die Entwicklung und das Testen von APIs.

[23] [24]


---

### JSON Schema
***
## JSON Schema

- **Was ist JSON Schema?** Eine Vorlage zur Beschreibung der Struktur von JSON-Daten.
- **Verwendung:** Zur Planung und Validierung von JSON-Datenstrukturen.
- **Vorteile:** Effizientere Zusammenarbeit und Fehlervermeidung durch strukturierte Datenplanung.
- **Anwendungen:** Häufig in API-Entwicklung und anderen Bereichen, wo Datenstrukturen eine wichtige Rolle spielen.
[24]
---

---
class: center, middle

# Fragen?
***
* Was sind APIs
* Wie schreibt man gute APIs
* Welche Styles gibt es und wie wähle ich die richtige
* Was ist RESTful
* Wie geht gutes Error Handling
* Warum ist GraphQL so wichtig


---
# Quellen
***
[1] : https://it-service.network/it-lexikon/api
[2] : https://www.redhat.com/de/topics/api/what-are-application-programming-interfaces
[3] : https://aws.amazon.com/de/compare/the-difference-between-sdk-and-api/
[4] : https://geekflare.com/de/sdk-and-api-comparison/
[5] : https://www.redhat.com/architect/api-styles
[6] : https://www.deepl.com/de/translator
[7] : https://chat.openai.com/c/d8c075bc-13b9-4124-aca4-4fd590244a2a frage : was sind API Implementation Standards
[8] : https://chat.openai.com/c/d8c075bc-13b9-4124-aca4-4fd590244a2a frage : Was wären in dem Kontext  Vergleich, Motivation, Vorteile, Nachteile
[9] : https://aws.amazon.com/de/what-is/restful-api/
[10] : https://www.ionos.de/digitalguide/websites/web-entwicklung/hateoas-alle-informationen-zu-der-rest-eigenschaft/
[11] : https://de.wikipedia.org/wiki/HATEOAS
[12] : https://stackoverflow.blog/2020/03/02/best-practices-for-rest-api-design/
[13] : https://www.freecodecamp.org/news/rest-api-best-practices-rest-endpoint-design-examples/
[14] : https://www.makeuseof.com/api-endpoints-naming-best-practices/
[15] : https://www.baeldung.com/rest-api-error-handling-best-practices
[16] : https://www.redhat.com/de/topics/api/what-is-graphql
[17] : https://chat.openai.com/ frage: erkläre mir was was Schema, Query, Resolver, Mutation in Graphql sind
[18] : https://waytoeasylearn.com/learn/backends-for-frontends-pattern/
[19] : https://www.visual-paradigm.com/guide/development/code-first-vs-design-first/
[20] : https://chat.openai.com/ frage : was ist API Versioning
[21] : https://www.torocloud.com/blog/api-versioning-url-vs-header-vs-media-type-versioning#:~:text=Header%20versioning%20is%20another%20approach,sent%20along%20with%20the%20request.
[22] : https://www.lucidchart.com/blog/de/api-tests-grundlagen-und-best-prectices#:~:text=Was%20sind%20API%2DTests%3F,mangelhaftes%20oder%20unsicheres%20Produkt%20erhalten.
[23] : https://www.ionos.de/digitalguide/websites/web-entwicklung/was-ist-openapi/
[24] : https://blog.stoplight.io/openapi-json-schema#:~:text=Both%20are%20description%20formats%20for,API%2C%20not%20just%20data%20models.

-