class: center, middle

## [Software Engineering](../../praesentationen.html)

#### Kapitel 4


Simon Fedrau, Sascha Hahn

---

# Software system integration
***
Software Systems Integration ist der Prozess des Zusammenführens verschiedener Softwarekomponenten oder Systeme, um reibungslose Interaktion und nahtlose Kommunikation sicherzustellen. Dies ermöglicht es, Daten und Funktionen zwischen den Systemen auszutauschen und Geschäftsprozesse zu optimieren. Die Integration kann verschiedene Aspekte wie Datenintegration, Middleware-Kommunikation, Legacy-Systeme und Cloud-Services umfassen. Sie spielt eine entscheidende Rolle bei der Schaffung effizienter und kooperativer IT-Infrastrukturen in Unternehmen.

[1a,2a]

---

# Kommunikation
***
Kommunikation in Software-Systemintegration bezieht sich auf den Prozess des Informationsaustauschs und der Interaktion zwischen den verschiedenen integrierten Komponenten.
Effektive Kommunikation ist entscheidend, um sicherzustellen, dass die integrierten Systeme zusammenarbeiten. Sie umfasst die Festlegung von Schnittstellen, Protokollen und Mechanismen, die den Informationsaustausch unterstützen.

[1a,2a]

---

### Command vs Query vs Event
***
**Command (Befehl):**<br>
* Ein Command ist eine Anweisung, um eine Aktion auszuführen oder eine Veränderung im System vorzunehmen.
* Commands sind in der Regel zustandsverändernd und haben Auswirkungen auf das System, wie das Speichern von Daten oder das Auslösen einer Aktion.
* Beispiel: "Erstelle einen neuen Benutzer."

**Query (Abfrage):**<br>
* Eine Query ist eine Anfrage nach Informationen oder Daten, die keine Veränderung im System verursacht.
* Queries sind in der Regel schreibgeschützt und liefern Informationen, ohne den Systemzustand zu verändern.
* Beispiel: "Gib alle Benutzer in der Datenbank zurück."

[1a,3a]
---

### Command vs Query vs Event
***
**Event (Ereignis):**<br>
* Ein Event ist eine Meldung über etwas, das im System geschehen ist.
* Events sind in der Regel nachrichtenbasiert und werden verwendet, um über Änderungen oder Ereignisse zu informieren.
* Beispiel: "Benutzer hat sich angemeldet."

[1a,3a]

---

### Synchron (RPC) vs asynchron (Messages)
***
**Synchron (RPC - Remote Procedure Call):**<br>
* Bei synchroner Kommunikation wartet der aufrufende Prozess auf eine sofortige Antwort vom aufgerufenen Prozess.
* Dies erfolgt in der Regel über eine Funktion oder Methode, bei der der Aufruf blockiert, bis die Antwort zurückgegeben wird.
* Synchronität kann einfacher zu implementieren sein, ist aber anfälliger für Verzögerungen und Engpässe.

**Asynchron (Messages):**<br>
* Bei asynchroner Kommunikation erfolgt die Kommunikation ohne unmittelbare Antwort. Der aufrufende Prozess setzt seine Arbeit fort, ohne auf eine Antwort zu warten.
* Dies wird häufig über Nachrichten oder Events realisiert, bei denen der aufgerufene Prozess die Nachricht verarbeitet, wenn er dazu bereit ist.
* Asynchrone Kommunikation kann die Skalierbarkeit und die Reaktionsfähigkeit des Systems verbessern.

[1a,4a]

---

### Patterns
***
Patterns in der Softwareentwicklung sind bewährte Lösungsansätze für wiederkehrende Probleme. Sie helfen Entwicklern, effizienten und wartbaren Code zu schreiben, indem sie strukturierte Herangehensweisen für typische Aufgaben bieten. Diese Muster sind wie Bausteine, die in vielen Projekten wiederverwendet werden können, um Zeit zu sparen und die Qualität der Software zu erhöhen. Sie umfassen Beispiele wie Singleton für eine einzige Instanz einer Klasse, Factory zur Objekterzeugung und Observer für die Verfolgung von Änderungen im System. Patterns sind ein wertvolles Werkzeug, um Entwicklungsprozesse zu optimieren.

[1a,5a]
---

### Patterns
***
**Publish-Subscribe:**<br>
* Publish-Subscribe ist ein Muster, bei dem Sender (Publisher) Nachrichten an ein oder mehrere Empfänger (Subscriber) senden, ohne zu wissen, welche Empfänger die Nachrichten erhalten.
* Dies fördert die Lockerheit der Kopplung zwischen Komponenten, da Publisher und Subscriber unabhängig voneinander agieren können.
* Dieses Muster ist nützlich für ereignisgesteuerte Systeme, bei denen Komponenten auf Ereignisse oder Zustandsänderungen reagieren müssen.


**Message Queueing:**<br>

* Message Queueing ist ein Muster, bei dem Nachrichten in einer Warteschlange zwischengespeichert werden, bevor sie von den Empfängern verarbeitet werden.
* Dies ermöglicht die Entkopplung von Sender und Empfänger, da Nachrichten in der Warteschlange auf Empfänger warten, um sie abzurufen.
* Dieses Muster ist nützlich, um die Skalierbarkeit und Zuverlässigkeit in verteilten Systemen zu verbessern.

[1a,5a]
---

### Patterns
***
**Request-Response Model:**<br>

* Das Request-Response-Modell ist ein Kommunikationsmuster, bei dem ein Sender (Client) eine Anfrage an einen Empfänger (Server) sendet und auf eine direkte Antwort wartet.
* Dieses Muster ist in Webanwendungen weit verbreitet, wo Benutzeranfragen an Webserver gesendet werden, die dann eine entsprechende Antwort generieren.

**Push- und Pull-Model:**<br>

* Das Push- und Pull-Modell sind zwei Ansätze zur Aktualisierung von Daten oder zur Kommunikation zwischen Systemen.
* Im Push-Modell sendet der Sender aktiv Daten an Empfänger, ohne dass diese darum bitten.
* Im Pull-Modell fordern Empfänger aktiv Daten vom Sender an.
* Die Wahl zwischen Push und Pull hängt von den Anforderungen und dem Kontext des Systems ab.

[1a,5a]
---

### Patterns
***
**Webhooks:**<br>

* Webhooks sind ein Muster, bei dem ein System oder eine Anwendung Benachrichtigungen an andere Systeme sendet, wenn bestimmte Ereignisse auftreten.
* Die empfangenden Systeme sind in der Regel von den auslösenden Ereignissen entkoppelt und können auf Benachrichtigungen reagieren.
* Webhooks sind nützlich, um Echtzeitinformationen in verteilten Systemen zu übertragen.

[1a,5a]

---

### Protokolle
***
In der Softwareentwicklung sind Regelsätze und Vereinbarungen, die den Kommunikationsaustausch zwischen verschiedenen Systemen oder Komponenten ermöglichen. Sie dienen dazu, wie Daten gesendet, empfangen und interpretiert werden, festzulegen.

#### gRPC
* **Beschreibung:**
gRPC ist ein Remote Procedure Call (RPC)-Framework, das von Google entwickelt wurde. Es ermöglicht die Kommunikation zwischen verschiedenen Diensten und Systemen, wobei RPC-Aufrufe verwendet werden, um Methoden auf entfernten Servern aufzurufen.

* **Merkmale:**
gRPC bietet Effizienz, hohe Interoperabilität, Unterstützung für verschiedene Programmiersprachen und automatische Codegenerierung aus Protobuf-Dateien.

[1a,6a]
---

### Protokolle
***
#### HTTP/s
HTTP/s (Hypertext Transfer Protocol Secure) ist ein Kommunikationsprotokoll, das für den Austausch von Informationen und Daten im World Wide Web verwendet wird. Die "s" steht für "sicher", da es die Verschlüsselung von Daten ermöglicht.

**HTTP:**<br>
* Unverschlüsselte Datenübertragung: Bei HTTP werden Daten unverschlüsselt übertragen, was bedeutet, dass sie während der Übertragung abgefangen und gelesen werden können.
* Standardport: HTTP verwendet in der Regel Port 80 für die Kommunikation.

[1a,6a]
---

### Protokolle
***
**HTTPS:**<br>
* Verschlüsselte Datenübertragung: Bei HTTPS werden die Daten verschlüsselt, sodass sie während der Übertragung geschützt sind und nicht ohne weiteres von Dritten gelesen werden können.
* Verwendung von SSL/TLS: HTTPS basiert auf dem Einsatz von SSL (Secure Sockets Layer) oder TLS (Transport Layer Security) zur Verschlüsselung und Authentifizierung.
* Standardport: HTTPS verwendet in der Regel Port 443 für die Kommunikation.

[1a,6a]

---

##### Continuous Connection
***
Continuous Connection bezieht sich auf eine anhaltende Kommunikationsverbindung zwischen einem Client und einem Server. Statt bei jeder Anfrage eine neue Verbindung zu öffnen und zu schließen, wird eine bestehende Verbindung aufrechterhalten, um Daten in Echtzeit auszutauschen.

###### Polling vs. Long-Polling vs. SSE
**Polling:**<br>
Beim Polling sendet der Client wiederholt Anfragen an den Server, um auf neue Daten zu prüfen. Dies kann ineffizient sein, da der Client oft leer ausgeht, wenn keine neuen Daten verfügbar sind.

**Long-Polling:**<br>
Long-Polling ist eine Weiterentwicklung des Pollings, bei dem der Server auf eine Anfrage des Clients nicht sofort antwortet, wenn keine neuen Daten verfügbar sind. Stattdessen wird die Anfrage offen gehalten (gehalten), bis neue Daten verfügbar sind. Dies reduziert die Anzahl der Anfragen, ist aber immer noch nicht die effizienteste Lösung.

[1a,7a]
---

##### Continuous Connection
***
**SSE (Server-Sent Events):**<br>
SSE ist ein Protokoll, das es dem Server ermöglicht, Daten proaktiv an den Client zu senden, sobald sie verfügbar sind. Dies eliminiert die Notwendigkeit für wiederholte Anfragen, und der Server kann Ereignisse an den Client senden, wenn sie auftreten. SSE ist besonders nützlich für Echtzeit-Informationen oder Benachrichtigungen in Webanwendungen.

[1a,7a]

---

##### WebSockets
***
Websockets sind ein Kommunikationsprotokoll, das eine bidirektionale, interaktive und kontinuierliche Kommunikation zwischen einem Client und einem Server ermöglicht. Im Gegensatz zum traditionellen HTTP, das auf anfragebasierten Kommunikation beruht, bleibt die Websocket-Verbindung geöffnet, sodass sowohl der Client als auch der Server Nachrichten in Echtzeit senden und empfangen können.

* **Echtzeitkommunikation:**<br>
Websockets ermöglichen Echtzeitkommunikation zwischen Client und Server, was ideal für Anwendungen ist, die auf schnelle Aktualisierungen und Benachrichtigungen angewiesen sind.

* **Bidirektional:**<br>
Die Verbindung ermöglicht das Senden von Daten in beide Richtungen, wodurch sowohl der Client als auch der Server aktive Teilnehmer im Kommunikationsprozess sind.

* **Geringer Overhead:**<br>
Im Vergleich zu HTTP-Anfragen, bei denen jedes Mal Headerinformationen gesendet werden müssen, haben Websockets geringeren Overhead und sind effizienter für kontinuierliche Kommunikation.

[1a,7a]
---

##### WebSockets
***
* **Unterstützung in Webbrowsern:**<br>
Moderne Webbrowser unterstützen Websockets, was sie zu einer geeigneten Wahl für webbasierte Anwendungen macht.

Websockets werden in einer Vielzahl von Anwendungen eingesetzt, darunter Online-Chats, Multiplayer-Spiele, Aktienhandelssysteme und Echtzeit-Dashboards.

[1a,7a]

---

#### Serialisierung
***
Serialisierung ist der Prozess der Umwandlung von Datenstrukturen oder Objekten in ein Format, das zur Übertragung oder Speicherung verwendet werden kann. Dieser Prozess ermöglicht es, Daten in eine sequenzielle Reihenfolge von Bytes oder Zeichen umzuwandeln, die später rekonstruiert werden können.

##### JSON, XML, Protocol Buffers
JSON (JavaScript Object Notation), XML (eXtensible Markup Language) und Protocol Buffers (Protobuf) sind verschiedene Datenformate, die in der Serialisierung verwendet werden. Diese Formate dienen dazu, Daten zu strukturieren und für den Datenaustausch zu speichern. Sie sind unabhängig von der zugrunde liegenden Programmiersprache oder Plattform und ermöglichen so eine erhöhte Interoperabilität. Dies bedeutet, dass sie in verschiedenen Umgebungen und auf verschiedenen Geräten verwendet werden können.

[1a,8a]
---

### Data Management Patterns
***
Data Management Patterns (Muster für die Datenverwaltung) sind bewährte Ansätze und Methoden zur Organisation und Verwaltung von Daten in einer Softwareanwendung. Diese Muster helfen Entwicklern, Daten effizient zu speichern, abzurufen und zu aktualisieren, um die Anforderungen einer Anwendung zu erfüllen. Hier sind zwei gängige Data Management Patterns:

[1a,9a,10a]
---

#### CRUD (Create, Read, Update, Delete)
***
CRUD ist ein grundlegendes Datenverwaltungsmuster, das vier grundlegende Operationen beschreibt: Erstellen (Create), Lesen (Read), Aktualisieren (Update) und Löschen (Delete) von Daten.

 * **Create:**<br>
 Diese Phase beinhaltet das Anlegen neuer Datensätze oder Objekte. Entwickler haben die Möglichkeit, neue Einträge in einer Datenbank oder Datenstruktur zu erstellen, sei es ein neuer Benutzeraccount, ein Produkt oder andere Informationen.

* **Read:**<br>
Die Leseoperation ermöglicht das Abfragen und Abrufen von Daten aus der Datenquelle. Dies beinhaltet das Suchen nach bestimmten Datensätzen, das Anzeigen von Informationen und das Lesen von Daten für verschiedene Zwecke.

[1a,9a,10a]
---

#### CRUD (Create, Read, Update, Delete)
***
* **Update:**<br>
Während dieser Phase können vorhandene Datensätze geändert oder aktualisiert werden. Benutzer können beispielsweise ihre Profilinformationen ändern oder Entwickler können Daten aktualisieren, um sie auf dem neuesten Stand zu halten.

* **Delete:**<br>
Die Löschoperation erlaubt das Entfernen von Datensätzen oder Objekten aus der Datenquelle. Dies kann beispielsweise bei der Deaktivierung eines Benutzerkontos oder dem Entfernen von nicht mehr benötigten Informationen erfolgen.

[1a,9a,10a]
---

#### CQRS (Command Query Responsibility Segregation)
***
CQRS ist ein erweitertes Datenmanagementmuster, das die Trennung von Lese- (Query) und Schreiboperationen (Command) betont. Es schlägt vor, separate Modelle für Lese- und Schreibzugriffe zu verwenden.
CQRS wird in komplexen Anwendungen eingesetzt, in denen die Anforderungen an die Lese- und Schreibvorgänge stark voneinander abweichen. Es ermöglicht die Optimierung und Skalierung von Lese- und Schreibzugriffen unabhängig voneinander.

[1a,9a,10a]

---

# Software System Interfaces
***
Software System Interfaces sind Schnittstellen, die Benutzern ermöglichen, mit einer Softwareanwendung zu interagieren. Sie können in verschiedenen Formen auftreten und bieten vielfältige Möglichkeiten für die Kommunikation zwischen Benutzern und der Software.

[11a]
---

### GUIs (Graphical User Interfaces)
***
GUIs sind Benutzerschnittstellen, die visuelle Elemente wie Fenster, Schaltflächen und Symbole verwenden, um die Interaktion zwischen einem Benutzer und einer Softwareanwendung zu ermöglichen. Mit einem GUI können Benutzer auf einfache und intuitive Weise mit einer Anwendung interagieren, indem sie Mauszeiger bewegen und auf Bildschirmelemente klicken. GUIs sind in den meisten Desktop-Anwendungen, Betriebssystemen und mobilen Apps weit verbreitet und bieten eine benutzerfreundliche Möglichkeit, Aufgaben auszuführen und Informationen anzuzeigen.

[11a]
---

### Voice UIs (Voice User Interfaces)
***
Voice UIs ermöglichen Benutzern die Interaktion mit einer Softwareanwendung mithilfe gesprochener Sprache. Diese Schnittstellen nutzen Spracherkennungstechnologien, um Befehle und Anfragen des Benutzers zu verstehen und darauf zu reagieren. Voice UIs finden Anwendung in Sprachassistenten, intelligenten Lautsprechern und Anwendungen, die die Sprache als Eingabemethode unterstützen.

### CLIs (Command Line Interfaces)
***
CLIs sind textbasierte Schnittstellen, die es Benutzern ermöglichen, Befehle und Anweisungen direkt in einer Kommandozeile einzugeben. Mit CLIs können erfahrene Benutzer komplexe Aufgaben ausführen und Systeme steuern, indem sie Textbefehle eingeben. Diese Schnittstellen sind in vielen Betriebssystemen und Entwicklertools gebräuchlich und bieten eine effiziente Möglichkeit zur Interaktion mit Software auf einem niedrigeren Abstraktionsniveau.

[11a]

---
## APIs

**Was ist eine API?**
***
API ist die Abkürzung für „application programming interface“ und der gängige Fachbegriff für eine Programmierschnittstelle, auch Anwendungsschnittstelle genannt. Bieten Online-Dienste solche Schnittstellen an, wird häufig der Begriff „Webservices“ verwendet.
[1b]

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

[10b] [11b]

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

[12b] [13b] [14b]

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
[15b]
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
[16b]
---

### Schema in GraphQL
***

- Das Schema bildet die Grundlage jeder GraphQL-API.

- Es definiert, welche Daten abgerufen werden können und wie sie strukturiert sind.

- Das Schema besteht aus zwei Hauptteilen:

  - **Query-Typ:** Enthält Abfragen (Queries) zum Abrufen von Daten.

  - **Mutation-Typ:** Enthält Mutationen zum Ändern oder Erstellen von Daten.

- In der Regel wird das Schema in einer speziellen Abfragesprache definiert, die oft als "Schema Definition Language" (SDL) bezeichnet wird.
[16b] [17b]
---

### Query in GraphQL
***
- Eine Query in GraphQL ist eine Abfrageoperation, mit der Daten aus der API abgerufen werden.

- Sie ermöglicht dem Client, präzise anzugeben, welche Daten und Felder benötigt werden.

- Die Struktur einer Query folgt dem Schema und spiegelt oft die gewünschte Datenstruktur wider.

- Beispiel einer Query: "Gib mir den Namen und das Alter eines Benutzers sowie die Titel seiner Beiträge."

[17b] [18b]
---

### Resolver in GraphQL

- Resolver sind Funktionen, die die eigentliche Arbeit in einer GraphQL-API ausführen.

- Jedes Feld im Schema ist einem Resolver zugeordnet.

- Wenn eine Query ausgeführt wird, ruft GraphQL die entsprechenden Resolver auf, um die angeforderten Daten zu erhalten.

- Resolver können Daten aus einer Datenbank abrufen, APIs aufrufen, Berechnungen durchführen oder auf andere Weise die Daten bereitstellen, die in der Query angefordert werden.

- Beispiel für einen Resolver: "Wenn nach dem Namen eines Benutzers gefragt wird, greife auf die Datenbank zu und gib den Namen des Benutzers zurück."

[17b] [18b]

---

### Mutation in GraphQL
***

- Mutationen sind Operationen in GraphQL, mit denen Daten geändert oder erstellt werden können.

- Im Gegensatz zu Queries, die nur lesend sind, erlauben Mutationen das Schreiben von Daten auf den Server.

- Mutationen sind oft in der Art einer Anfrage aufgebaut, die beschreibt, welche Daten geändert oder hinzugefügt werden sollen.

- Beispiel für eine Mutation: "Erstelle einen neuen Benutzer mit dem Namen und der E-Mail-Adresse."

[17b] [18b]

---

### Backend For Frontend (BFF-Muster)
***

- Das Backends for Frontends Pattern  ist ein Designmuster für die Architektur von Mikroservices.
- Dieses Muster konzentriert sich auf die Trennung von API-Gateways entsprechend den spezifischen Frontend-Anwendungen.
- Anstatt nur ein allgemeines API-Backend zu haben, werden mehrere Backend-Services für Frontend-Anwendungen bereitgestellt, und dazwischen wird ein API-Gateway zur Handhabung von Routing und Aggregationsvorgängen platziert.
- hilft den sogenannten Single Point of Failure zu vermeiden, da mehrere API-Gateways für verschiedene Frontend-Anwendungen geschaffen werden.
- Es können unterschiedliche Anforderungen der Frontend-Anwendungen erfüllt werden, ohne die anderen Frontend-Anwendungen zu beeinträchtigen.
- Das BFF-Muster ist besonders hilfreich, wenn eine Anpassung eines einzigen Backends für verschiedene Benutzeroberflächen vermieden werden soll.[18b]


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
[19b]

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
[20b] [21b]
---

### API Testing

- **Zweck:** Überprüfung von APIs auf Funktionalität, Leistung, Zuverlässigkeit und Sicherheit.

- **Wichtigkeit:** Verhindert Fehler, sichert Zuverlässigkeit und fördert effiziente Nutzung.

- **Testarten:** Funktionale, Leistungs-, Sicherheits- und Zuverlässigkeitstests.

- **Werkzeuge:** Postman, Newman, JUnit und spezialisierte API-Testtools.

- **Automatisierung:** Automatisierung für effiziente und wiederholbare Tests.

- **Testabdeckung:** Deckt verschiedene Szenarien ab.

API-Tests sind entscheidend für eine zuverlässige und fehlerfreie API-Nutzung.

[22b]
---
### OpenAPI
***
- **Was ist OpenAPI?** Ein Standard zur API-Beschreibung.
- **Zweck:** Beschreibung, Entwicklung, Test und Dokumentation von REST-APIs.
- **Unterschied zu JSON Schema:** OpenAPI beschreibt die gesamte API, inklusive Endpunkten und Formatierung von Anfragen und Antworten.
- **Warum ist OpenAPI nützlich?** Ermöglicht die Generierung von Dokumentation und Mock-Servern.
- **Vereinfacht:** Die Entwicklung und das Testen von APIs.

[23b] [24b]


---

### JSON Schema
***
## JSON Schema

- **Was ist JSON Schema?** Eine Vorlage zur Beschreibung der Struktur von JSON-Daten.
- **Verwendung:** Zur Planung und Validierung von JSON-Datenstrukturen.
- **Vorteile:** Effizientere Zusammenarbeit und Fehlervermeidung durch strukturierte Datenplanung.
- **Anwendungen:** Häufig in API-Entwicklung und anderen Bereichen, wo Datenstrukturen eine wichtige Rolle spielen.
[24b]
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

[1b] : https://it-service.network/it-lexikon/api
[2b] : https://www.redhat.com/de/topics/api/what-are-application-programming-interfaces
[3b] : https://aws.amazon.com/de/compare/the-difference-between-sdk-and-api/
[4b] : https://geekflare.com/de/sdk-and-api-comparison/
[5b] : https://www.redhat.com/architect/api-styles
[6b] : https://www.deepl.com/de/translator
[7b] : https://chat.openai.com/c/d8c075bc-13b9-4124-aca4-4fd590244a2a frage : was sind API Implementation Standards
[8b] : https://chat.openai.com/c/d8c075bc-13b9-4124-aca4-4fd590244a2a frage : Was wären in dem Kontext  Vergleich, Motivation, Vorteile, Nachteile
[9b] : https://aws.amazon.com/de/what-is/restful-api/
[10b] : https://www.ionos.de/digitalguide/websites/web-entwicklung/hateoas-alle-informationen-zu-der-rest-eigenschaft/
[11b] : https://de.wikipedia.org/wiki/HATEOAS
[12b] : https://stackoverflow.blog/2020/03/02/best-practices-for-rest-api-design/
[13b] : https://www.freecodecamp.org/news/rest-api-best-practices-rest-endpoint-design-examples/
[14b] : https://www.makeuseof.com/api-endpoints-naming-best-practices/
[15b] : https://www.baeldung.com/rest-api-error-handling-best-practices

---

# Quellen
***
[16b] : https://www.redhat.com/de/topics/api/what-is-graphql
[17b] : https://chat.openai.com/ frage: erkläre mir was was Schema, Query, Resolver, Mutation in Graphql sind
[18b] : https://waytoeasylearn.com/learn/backends-for-frontends-pattern/
[19b] : https://www.visual-paradigm.com/guide/development/code-first-vs-design-first/
[20b] : https://chat.openai.com/ frage : was ist API Versioning
[21b] : https://www.torocloud.com/blog/api-versioning-url-vs-header-vs-media-type-versioning#:~:text=Header%20versioning%20is%20another%20approach,sent%20along%20with%20the%20request.
[22b] : https://www.lucidchart.com/blog/de/api-tests-grundlagen-und-best-prectices#:~:text=Was%20sind%20API%2DTests%3F,mangelhaftes%20oder%20unsicheres%20Produkt%20erhalten.
[23b] : https://www.ionos.de/digitalguide/websites/web-entwicklung/was-ist-openapi/
[24b] : https://blog.stoplight.io/openapi-json-schema#:~:text=Both%20are%20description%20formats%20for,API%2C%20not%20just%20data%20models.

---

# Quellen
***
[1a] https://chat.openai.com/
[2] :https://www.snaplogic.com/de/blog/system-integration-types-and-approaches
[3a] :https://kwahome.medium.com/microservice-interactions-query-command-event-d7e01d8cd63c#:~:text=The%20difference%20between%20queries%2C%20commands,completed%20(in%20the%20past).
[4a] :https://de.wikipedia.org/wiki/Remote_Procedure_Call
[5a] :https://de.wikibrief.org/wiki/Message_passing
[6a] :https://de.wikipedia.org/wiki/Internetprotokollfamilie
[7a] :https://medium.com/dailyjs/a-comparison-between-websockets-server-sent-events-and-polling-7a27c98cb1e3
[8a] :https://de.wikipedia.org/wiki/Serialisierung
[9a] :https://learn.microsoft.com/en-us/azure/architecture/patterns/category/data-management
[10a] :https://www.oreilly.com/library/view/design-patterns-for/9781492090700/ch04.html
[11a] :https://de.wikipedia.org/wiki/Schnittstelle