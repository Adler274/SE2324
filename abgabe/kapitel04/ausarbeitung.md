# Kpitel 4

# Software system integration
Software Systems Integration ist der Prozess des Zusammenführens verschiedener Softwarekomponenten oder Systeme, um reibungslose Interaktion und nahtlose Kommunikation sicherzustellen. Dies ermöglicht es, Daten und Funktionen zwischen den Systemen auszutauschen und Geschäftsprozesse zu optimieren. Die Integration kann verschiedene Aspekte wie Datenintegration, Middleware-Kommunikation, Legacy-Systeme und Cloud-Services umfassen. Sie spielt eine entscheidende Rolle bei der Schaffung effizienter und kooperativer IT-Infrastrukturen in Unternehmen.

# Kommunikation
Kommunikation in Software-Systemintegration bezieht sich auf den Prozess des Informationsaustauschs und der Interaktion zwischen den verschiedenen integrierten Komponenten.
Effektive Kommunikation ist entscheidend, um sicherzustellen, dass die integrierten Systeme zusammenarbeiten. Sie umfasst die Festlegung von Schnittstellen, Protokollen und Mechanismen, die den Informationsaustausch unterstützen.

### Command vs Query vs Event
**Command (Befehl):**<br>
* Ein Command ist eine Anweisung, um eine Aktion auszuführen oder eine Veränderung im System vorzunehmen.
* Commands sind in der Regel zustandsverändernd und haben Auswirkungen auf das System, wie das Speichern von Daten oder das Auslösen einer Aktion.
* Beispiel: "Erstelle einen neuen Benutzer."

**Query (Abfrage):**<br>
* Eine Query ist eine Anfrage nach Informationen oder Daten, die keine Veränderung im System verursacht.
* Queries sind in der Regel schreibgeschützt und liefern Informationen, ohne den Systemzustand zu verändern.
* Beispiel: "Gib alle Benutzer in der Datenbank zurück."

**Event (Ereignis):**<br>
* Ein Event ist eine Meldung über etwas, das im System geschehen ist.
* Events sind in der Regel nachrichtenbasiert und werden verwendet, um über Änderungen oder Ereignisse zu informieren.
* Beispiel: "Benutzer hat sich angemeldet."


### Synchron (RPC) vs asynchron (Messages)

**Synchron (RPC - Remote Procedure Call):**<br>
* Bei synchroner Kommunikation wartet der aufrufende Prozess auf eine sofortige Antwort vom aufgerufenen Prozess.
* Dies erfolgt in der Regel über eine Funktion oder Methode, bei der der Aufruf blockiert, bis die Antwort zurückgegeben wird.
* Synchronität kann einfacher zu implementieren sein, ist aber anfälliger für Verzögerungen und Engpässe.

**Asynchron (Messages):**<br>
* Bei asynchroner Kommunikation erfolgt die Kommunikation ohne unmittelbare Antwort. Der aufrufende Prozess setzt seine Arbeit fort, ohne auf eine Antwort zu warten.
* Dies wird häufig über Nachrichten oder Events realisiert, bei denen der aufgerufene Prozess die Nachricht verarbeitet, wenn er dazu bereit ist.
* Asynchrone Kommunikation kann die Skalierbarkeit und die Reaktionsfähigkeit des Systems verbessern.

### Patterns
Patterns in der Softwareentwicklung sind bewährte Lösungsansätze für wiederkehrende Probleme. Sie helfen Entwicklern, effizienten und wartbaren Code zu schreiben, indem sie strukturierte Herangehensweisen für typische Aufgaben bieten. Diese Muster sind wie Bausteine, die in vielen Projekten wiederverwendet werden können, um Zeit zu sparen und die Qualität der Software zu erhöhen. Sie umfassen Beispiele wie Singleton für eine einzige Instanz einer Klasse, Factory zur Objekterzeugung und Observer für die Verfolgung von Änderungen im System. Patterns sind ein wertvolles Werkzeug, um Entwicklungsprozesse zu optimieren.

**Publish-Subscribe:**<br>
* Publish-Subscribe ist ein Muster, bei dem Sender (Publisher) Nachrichten an ein oder mehrere Empfänger (Subscriber) senden, ohne zu wissen, welche Empfänger die Nachrichten erhalten.
* Dies fördert die Lockerheit der Kopplung zwischen Komponenten, da Publisher und Subscriber unabhängig voneinander agieren können.
* Dieses Muster ist nützlich für ereignisgesteuerte Systeme, bei denen Komponenten auf Ereignisse oder Zustandsänderungen reagieren müssen.

**Message Queueing:**<br>

* Message Queueing ist ein Muster, bei dem Nachrichten in einer Warteschlange zwischengespeichert werden, bevor sie von den Empfängern verarbeitet werden.
* Dies ermöglicht die Entkopplung von Sender und Empfänger, da Nachrichten in der Warteschlange auf Empfänger warten, um sie abzurufen.
* Dieses Muster ist nützlich, um die Skalierbarkeit und Zuverlässigkeit in verteilten Systemen zu verbessern.

**Request-Response Model:**<br>

* Das Request-Response-Modell ist ein Kommunikationsmuster, bei dem ein Sender (Client) eine Anfrage an einen Empfänger (Server) sendet und auf eine direkte Antwort wartet.
* Dieses Muster ist in Webanwendungen weit verbreitet, wo Benutzeranfragen an Webserver gesendet werden, die dann eine entsprechende Antwort generieren.

**Push- und Pull-Model:**<br>

* Das Push- und Pull-Modell sind zwei Ansätze zur Aktualisierung von Daten oder zur Kommunikation zwischen Systemen.
* Im Push-Modell sendet der Sender aktiv Daten an Empfänger, ohne dass diese darum bitten.
* Im Pull-Modell fordern Empfänger aktiv Daten vom Sender an.
* Die Wahl zwischen Push und Pull hängt von den Anforderungen und dem Kontext des Systems ab.

**Webhooks:**<br>

* Webhooks sind ein Muster, bei dem ein System oder eine Anwendung Benachrichtigungen an andere Systeme sendet, wenn bestimmte Ereignisse auftreten.
* Die empfangenden Systeme sind in der Regel von den auslösenden Ereignissen entkoppelt und können auf Benachrichtigungen reagieren.
* Webhooks sind nützlich, um Echtzeitinformationen in verteilten Systemen zu übertragen.

### Protokolle
In der Softwareentwicklung sind Regelsätze und Vereinbarungen, die den Kommunikationsaustausch zwischen verschiedenen Systemen oder Komponenten ermöglichen. Sie dienen dazu, wie Daten gesendet, empfangen und interpretiert werden, festzulegen.

#### gRPC
* **Beschreibung:**
gRPC ist ein Remote Procedure Call (RPC)-Framework, das von Google entwickelt wurde. Es ermöglicht die Kommunikation zwischen verschiedenen Diensten und Systemen, wobei RPC-Aufrufe verwendet werden, um Methoden auf entfernten Servern aufzurufen.

* **Merkmale:**
gRPC bietet Effizienz, hohe Interoperabilität, Unterstützung für verschiedene Programmiersprachen und automatische Codegenerierung aus Protobuf-Dateien.

#### HTTP/s
HTTP/s (Hypertext Transfer Protocol Secure) ist ein Kommunikationsprotokoll, das für den Austausch von Informationen und Daten im World Wide Web verwendet wird. Die "s" steht für "sicher", da es die Verschlüsselung von Daten ermöglicht.

**HTTP:**<br>
* Unverschlüsselte Datenübertragung: Bei HTTP werden Daten unverschlüsselt übertragen, was bedeutet, dass sie während der Übertragung abgefangen und gelesen werden können.
* Standardport: HTTP verwendet in der Regel Port 80 für die Kommunikation.

**HTTPS:**<br>
* Verschlüsselte Datenübertragung: Bei HTTPS werden die Daten verschlüsselt, sodass sie während der Übertragung geschützt sind und nicht ohne weiteres von Dritten gelesen werden können.
* Verwendung von SSL/TLS: HTTPS basiert auf dem Einsatz von SSL (Secure Sockets Layer) oder TLS (Transport Layer Security) zur Verschlüsselung und Authentifizierung.
* Standardport: HTTPS verwendet in der Regel Port 443 für die Kommunikation.

##### Continuous Connection
Continuous Connection bezieht sich auf eine anhaltende Kommunikationsverbindung zwischen einem Client und einem Server. Statt bei jeder Anfrage eine neue Verbindung zu öffnen und zu schließen, wird eine bestehende Verbindung aufrechterhalten, um Daten in Echtzeit auszutauschen.

###### Polling vs. Long-Polling vs. SSE
**Polling:**<br>
Beim Polling sendet der Client wiederholt Anfragen an den Server, um auf neue Daten zu prüfen. Dies kann ineffizient sein, da der Client oft leer ausgeht, wenn keine neuen Daten verfügbar sind.

**Long-Polling:**<br>
Long-Polling ist eine Weiterentwicklung des Pollings, bei dem der Server auf eine Anfrage des Clients nicht sofort antwortet, wenn keine neuen Daten verfügbar sind. Stattdessen wird die Anfrage offen gehalten (gehalten), bis neue Daten verfügbar sind. Dies reduziert die Anzahl der Anfragen, ist aber immer noch nicht die effizienteste Lösung.

**SSE (Server-Sent Events):**<br>
SSE ist ein Protokoll, das es dem Server ermöglicht, Daten proaktiv an den Client zu senden, sobald sie verfügbar sind. Dies eliminiert die Notwendigkeit für wiederholte Anfragen, und der Server kann Ereignisse an den Client senden, wenn sie auftreten. SSE ist besonders nützlich für Echtzeit-Informationen oder Benachrichtigungen in Webanwendungen.

##### WebSockets
Websockets sind ein Kommunikationsprotokoll, das eine bidirektionale, interaktive und kontinuierliche Kommunikation zwischen einem Client und einem Server ermöglicht. Im Gegensatz zum traditionellen HTTP, das auf anfragebasierten Kommunikation beruht, bleibt die Websocket-Verbindung geöffnet, sodass sowohl der Client als auch der Server Nachrichten in Echtzeit senden und empfangen können.

* **Echtzeitkommunikation:**<br>
Websockets ermöglichen Echtzeitkommunikation zwischen Client und Server, was ideal für Anwendungen ist, die auf schnelle Aktualisierungen und Benachrichtigungen angewiesen sind.

* **Bidirektional:**<br>
Die Verbindung ermöglicht das Senden von Daten in beide Richtungen, wodurch sowohl der Client als auch der Server aktive Teilnehmer im Kommunikationsprozess sind.

* **Geringer Overhead:**<br>
Im Vergleich zu HTTP-Anfragen, bei denen jedes Mal Headerinformationen gesendet werden müssen, haben Websockets geringeren Overhead und sind effizienter für kontinuierliche Kommunikation.

* **Unterstützung in Webbrowsern:**<br>
Moderne Webbrowser unterstützen Websockets, was sie zu einer geeigneten Wahl für webbasierte Anwendungen macht.

Websockets werden in einer Vielzahl von Anwendungen eingesetzt, darunter Online-Chats, Multiplayer-Spiele, Aktienhandelssysteme und Echtzeit-Dashboards.

#### Serialisierung
Serialisierung ist der Prozess der Umwandlung von Datenstrukturen oder Objekten in ein Format, das zur Übertragung oder Speicherung verwendet werden kann. Dieser Prozess ermöglicht es, Daten in eine sequenzielle Reihenfolge von Bytes oder Zeichen umzuwandeln, die später rekonstruiert werden können.

##### JSON, XML, Protocol Buffers
JSON (JavaScript Object Notation), XML (eXtensible Markup Language) und Protocol Buffers (Protobuf) sind verschiedene Datenformate, die in der Serialisierung verwendet werden. Diese Formate dienen dazu, Daten zu strukturieren und für den Datenaustausch zu speichern. Sie sind unabhängig von der zugrunde liegenden Programmiersprache oder Plattform und ermöglichen so eine erhöhte Interoperabilität. Dies bedeutet, dass sie in verschiedenen Umgebungen und auf verschiedenen Geräten verwendet werden können.

### Data Management Patterns
Data Management Patterns (Muster für die Datenverwaltung) sind bewährte Ansätze und Methoden zur Organisation und Verwaltung von Daten in einer Softwareanwendung. Diese Muster helfen Entwicklern, Daten effizient zu speichern, abzurufen und zu aktualisieren, um die Anforderungen einer Anwendung zu erfüllen. Hier sind zwei gängige Data Management Patterns:

#### CRUD (Create, Read, Update, Delete)

CRUD ist ein grundlegendes Datenverwaltungsmuster, das vier grundlegende Operationen beschreibt: Erstellen (Create), Lesen (Read), Aktualisieren (Update) und Löschen (Delete) von Daten.

 * **Create:**<br>
 Diese Phase beinhaltet das Anlegen neuer Datensätze oder Objekte. Entwickler haben die Möglichkeit, neue Einträge in einer Datenbank oder Datenstruktur zu erstellen, sei es ein neuer Benutzeraccount, ein Produkt oder andere Informationen.

* **Read:**<br>
Die Leseoperation ermöglicht das Abfragen und Abrufen von Daten aus der Datenquelle. Dies beinhaltet das Suchen nach bestimmten Datensätzen, das Anzeigen von Informationen und das Lesen von Daten für verschiedene Zwecke.

* **Update:**<br>
Während dieser Phase können vorhandene Datensätze geändert oder aktualisiert werden. Benutzer können beispielsweise ihre Profilinformationen ändern oder Entwickler können Daten aktualisieren, um sie auf dem neuesten Stand zu halten.

* **Delete:**<br>
Die Löschoperation erlaubt das Entfernen von Datensätzen oder Objekten aus der Datenquelle. Dies kann beispielsweise bei der Deaktivierung eines Benutzerkontos oder dem Entfernen von nicht mehr benötigten Informationen erfolgen.

#### CQRS (Command Query Responsibility Segregation)
CQRS ist ein erweitertes Datenmanagementmuster, das die Trennung von Lese- (Query) und Schreiboperationen (Command) betont. Es schlägt vor, separate Modelle für Lese- und Schreibzugriffe zu verwenden.
CQRS wird in komplexen Anwendungen eingesetzt, in denen die Anforderungen an die Lese- und Schreibvorgänge stark voneinander abweichen. Es ermöglicht die Optimierung und Skalierung von Lese- und Schreibzugriffen unabhängig voneinander.

# Software System Interfaces
Software System Interfaces sind Schnittstellen, die Benutzern ermöglichen, mit einer Softwareanwendung zu interagieren. Sie können in verschiedenen Formen auftreten und bieten vielfältige Möglichkeiten für die Kommunikation zwischen Benutzern und der Software.

## GUIs (Graphical User Interfaces)
GUIs sind Benutzerschnittstellen, die visuelle Elemente wie Fenster, Schaltflächen und Symbole verwenden, um die Interaktion zwischen einem Benutzer und einer Softwareanwendung zu ermöglichen. Mit einem GUI können Benutzer auf einfache und intuitive Weise mit einer Anwendung interagieren, indem sie Mauszeiger bewegen und auf Bildschirmelemente klicken. GUIs sind in den meisten Desktop-Anwendungen, Betriebssystemen und mobilen Apps weit verbreitet und bieten eine benutzerfreundliche Möglichkeit, Aufgaben auszuführen und Informationen anzuzeigen.

## Voice UIs (Voice User Interfaces)
Voice UIs ermöglichen Benutzern die Interaktion mit einer Softwareanwendung mithilfe gesprochener Sprache. Diese Schnittstellen nutzen Spracherkennungstechnologien, um Befehle und Anfragen des Benutzers zu verstehen und darauf zu reagieren. Voice UIs finden Anwendung in Sprachassistenten, intelligenten Lautsprechern und Anwendungen, die die Sprache als Eingabemethode unterstützen.

## CLIs (Command Line Interfaces)
CLIs sind textbasierte Schnittstellen, die es Benutzern ermöglichen, Befehle und Anweisungen direkt in einer Kommandozeile einzugeben. Mit CLIs können erfahrene Benutzer komplexe Aufgaben ausführen und Systeme steuern, indem sie Textbefehle eingeben. Diese Schnittstellen sind in vielen Betriebssystemen und Entwicklertools gebräuchlich und bieten eine effiziente Möglichkeit zur Interaktion mit Software auf einem niedrigeren Abstraktionsniveau.

# Referenzen

[1] :https://chat.openai.com/
[2] :