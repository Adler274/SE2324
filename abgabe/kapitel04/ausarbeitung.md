# Kapitel 4

**Autor:** Simon Fedrau, Sascha Hahn

# Lernziele
1. Welche Arten von Kommunikation zwischen Software Systemen gibt es
2. Wie Funktionieren Kommunikation patterns
3. Welche Protokolle gibt es
4. Wie funktioniert Serialisierung
5. Welche Typen/Dateiformate gibt es zur Serialisierung
6. Welche Data Management Patterns gibt es und wie funktionieren sie
7. Was sind Software System Interfaces und welche Arten gibt es


# Software system integration
Software Systems Integration ist der Prozess des Zusammenführens verschiedener Softwarekomponenten oder Systeme, um reibungslose Interaktion und nahtlose Kommunikation sicherzustellen. Dies ermöglicht es, Daten und Funktionen zwischen den Systemen auszutauschen und Geschäftsprozesse zu optimieren. Die Integration kann verschiedene Aspekte wie Datenintegration, Middleware-Kommunikation, Legacy-Systeme und Cloud-Services umfassen. Sie spielt eine entscheidende Rolle bei der Schaffung effizienter und kooperativer IT-Infrastrukturen in Unternehmen.
[1a,2a]

# Kommunikation
Kommunikation in Software-Systemintegration bezieht sich auf den Prozess des Informationsaustauschs und der Interaktion zwischen den verschiedenen integrierten Komponenten.
Effektive Kommunikation ist entscheidend, um sicherzustellen, dass die integrierten Systeme zusammenarbeiten. Sie umfasst die Festlegung von Schnittstellen, Protokollen und Mechanismen, die den Informationsaustausch unterstützen.
[1a,2a]

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

[1a,3a]

### Synchron (RPC) vs asynchron (Messages)

**Synchron (RPC - Remote Procedure Call):**<br>
* Bei synchroner Kommunikation wartet der aufrufende Prozess auf eine sofortige Antwort vom aufgerufenen Prozess.
* Dies erfolgt in der Regel über eine Funktion oder Methode, bei der der Aufruf blockiert, bis die Antwort zurückgegeben wird.
* Synchronität kann einfacher zu implementieren sein, ist aber anfälliger für Verzögerungen und Engpässe.

**Asynchron (Messages):**<br>
* Bei asynchroner Kommunikation erfolgt die Kommunikation ohne unmittelbare Antwort. Der aufrufende Prozess setzt seine Arbeit fort, ohne auf eine Antwort zu warten.
* Dies wird häufig über Nachrichten oder Events realisiert, bei denen der aufgerufene Prozess die Nachricht verarbeitet, wenn er dazu bereit ist.
* Asynchrone Kommunikation kann die Skalierbarkeit und die Reaktionsfähigkeit des Systems verbessern.

[1a,4a]

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

[1a,5a]

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

[1a,6a]

##### Continuous Connection
Continuous Connection bezieht sich auf eine anhaltende Kommunikationsverbindung zwischen einem Client und einem Server. Statt bei jeder Anfrage eine neue Verbindung zu öffnen und zu schließen, wird eine bestehende Verbindung aufrechterhalten, um Daten in Echtzeit auszutauschen.

###### Polling vs. Long-Polling vs. SSE
**Polling:**<br>
Beim Polling sendet der Client wiederholt Anfragen an den Server, um auf neue Daten zu prüfen. Dies kann ineffizient sein, da der Client oft leer ausgeht, wenn keine neuen Daten verfügbar sind.

**Long-Polling:**<br>
Long-Polling ist eine Weiterentwicklung des Pollings, bei dem der Server auf eine Anfrage des Clients nicht sofort antwortet, wenn keine neuen Daten verfügbar sind. Stattdessen wird die Anfrage offen gehalten (gehalten), bis neue Daten verfügbar sind. Dies reduziert die Anzahl der Anfragen, ist aber immer noch nicht die effizienteste Lösung.

**SSE (Server-Sent Events):**<br>
SSE ist ein Protokoll, das es dem Server ermöglicht, Daten proaktiv an den Client zu senden, sobald sie verfügbar sind. Dies eliminiert die Notwendigkeit für wiederholte Anfragen, und der Server kann Ereignisse an den Client senden, wenn sie auftreten. SSE ist besonders nützlich für Echtzeit-Informationen oder Benachrichtigungen in Webanwendungen.

[1a,7a]

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

[1a,7a]

#### Serialisierung
Serialisierung ist der Prozess der Umwandlung von Datenstrukturen oder Objekten in ein Format, das zur Übertragung oder Speicherung verwendet werden kann. Dieser Prozess ermöglicht es, Daten in eine sequenzielle Reihenfolge von Bytes oder Zeichen umzuwandeln, die später rekonstruiert werden können.

[1a,8a]

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

[1a,9a,10a]

# Software System Interfaces
Software System Interfaces sind Schnittstellen, die Benutzern ermöglichen, mit einer Softwareanwendung zu interagieren. Sie können in verschiedenen Formen auftreten und bieten vielfältige Möglichkeiten für die Kommunikation zwischen Benutzern und der Software.

## GUIs (Graphical User Interfaces)
GUIs sind Benutzerschnittstellen, die visuelle Elemente wie Fenster, Schaltflächen und Symbole verwenden, um die Interaktion zwischen einem Benutzer und einer Softwareanwendung zu ermöglichen. Mit einem GUI können Benutzer auf einfache und intuitive Weise mit einer Anwendung interagieren, indem sie Mauszeiger bewegen und auf Bildschirmelemente klicken. GUIs sind in den meisten Desktop-Anwendungen, Betriebssystemen und mobilen Apps weit verbreitet und bieten eine benutzerfreundliche Möglichkeit, Aufgaben auszuführen und Informationen anzuzeigen.

## Voice UIs (Voice User Interfaces)
Voice UIs ermöglichen Benutzern die Interaktion mit einer Softwareanwendung mithilfe gesprochener Sprache. Diese Schnittstellen nutzen Spracherkennungstechnologien, um Befehle und Anfragen des Benutzers zu verstehen und darauf zu reagieren. Voice UIs finden Anwendung in Sprachassistenten, intelligenten Lautsprechern und Anwendungen, die die Sprache als Eingabemethode unterstützen.

## CLIs (Command Line Interfaces)
CLIs sind textbasierte Schnittstellen, die es Benutzern ermöglichen, Befehle und Anweisungen direkt in einer Kommandozeile einzugeben. Mit CLIs können erfahrene Benutzer komplexe Aufgaben ausführen und Systeme steuern, indem sie Textbefehle eingeben. Diese Schnittstellen sind in vielen Betriebssystemen und Entwicklertools gebräuchlich und bieten eine effiziente Möglichkeit zur Interaktion mit Software auf einem niedrigeren Abstraktionsniveau.

[11a]

## APIs

**Was ist eine API?**

API ist die Abkürzung für „application programming interface“ und der gängige Fachbegriff für eine Programmierschnittstelle, auch Anwendungsschnittstelle genannt. Bieten Online-Dienste solche Schnittstellen an, wird häufig der Begriff „Webservices“ verwendet. [1b]

**Wie funktionieren APIs?**

Mithilfe von APIs können Ihre Produkte oder Services unabhängig von ihrer Implementierung untereinander kommunizieren. Auf diese Weise lässt sich die Anwendungsentwicklung optimieren, was wiederum Zeit und Geld spart. Sie sind flexibel und vereinfachen Design, Administration und Nutzung von Anwendungen – egal ob Sie neue Tools und Produkte entwickeln oder bestehende verwalten. Obendrein schaffen sie Möglichkeiten für Innovationen.

APIs selbst bieten eine einfache Möglichkeit zur Anbindung Ihrer eigenen Infrastruktur über die Entwicklung cloudnativer Anwendungen, ermöglichen aber auch die gemeinsame Verwendung Ihrer Daten mit Kunden und anderen externen Usern. Öffentliche APIs stellen einen hohen Geschäftswert dar, denn sie vereinfachen und erweitern die Verbindung zu Ihren Partnern und sorgen zudem für eine mögliche Monetarisierung Ihrer Daten (ein gängiges Beispiel ist hier die Google Maps API).
[2b]

### API vs. SDK

**Was ist eine SDK**

Ein SDK bietet eine integrierte Plattform, mit der Sie Anwendungen effizient von Grund auf neu entwickeln können. Es liefert Bausteine, die den Entwicklungsprozess verkürzen. Anstatt Code von Grund auf neu zu schreiben, können Sie ein SDK verwenden, das häufig aus Bibliotheken, Compilern, Debuggern, Codebeispielen und Dokumentation besteht. Eine integrierte Entwicklungsumgebung (IDE) ist die Softwareumgebung, die Sie verwenden, um alle im SDK enthaltenen Tools zu verbinden. 
[3b] [4b]

**Unterschied und Einsatzgebiete**

Ein Software Development Kit (SDK) ist eine Reihe von plattformspezifischen Entwicklungstools wie Debuggern, Compilern und Bibliotheken. SDKs stellen Tools und Ressourcen von Drittanbietern in Ihrer Umgebung bereit. Im Gegensatz dazu ist eine Anwendungsprogrammierschnittstelle (API) ein Mechanismus, der es zwei Softwarekomponenten ermöglicht, über vorgegebene Protokolle miteinander zu kommunizieren. Sie können APIs verwenden, um mit vorhandenen Softwarekomponenten zu kommunizieren und vorentwickelte Funktionen in Ihren Code zu integrieren. SDKs können APIs und mehrere andere Ressourcen für die von ihnen unterstützte Plattform enthalten. Ebenso können Sie SDKs verwenden, um neue APIs zu erstellen, die Sie mit anderen teilen können. Sowohl SDKs als auch APIs machen den Softwareentwicklungsprozess effizienter und kollaborativer.
[3b] [4b]


### API Styles

APIs sind ein wesentliches Gestaltungselement in jeder Softwarearchitektur. Sie verbinden Komponenten digital miteinander und ermöglichen es verschiedenen Systemen und Geräten, problemlos miteinander zu kommunizieren. Wenn Entwickler eine neue API erstellen, denken sie zunächst über das API-Design nach und darüber, wie die API mit der Außenwelt interagiert, indem sie einen Stil und eine Technologie auswählen.
[5b]
Im Folgenden werden fünf häufig genutzten APIs Architekturen vorgestellt.

#### Resource style

Der Ressourcenstil, wie der Name bereits andeutet, ist ressourcenorientiert. Viele der heutigen APIs verwenden diesen Stil, was leicht durch die Popularität von OpenAPI überprüft werden kann, der am weitesten verbreiteten Methode zur Beschreibung von ressourcenorientierten APIs. In diesem Stil liegt der Hauptfokus darauf, welche Ressourcen für Verbraucher freigegeben werden, damit sie mit diesen Ressourcen interagieren können. "Ressource" in diesem Kontext ist vergleichbar mit dem, was Sie beim Entwerfen einer Website für Ressourcen wie Webseiten haben würden. Die Idee von Ressourcen bietet eine gute Möglichkeit, die relevanten Aspekte der Funktionalität einer API freizulegen und gleichzeitig Implementierungsdetails hinter den Ressourcen zu verbergen. Ressourcen können für persistente Konzepte wie Produkte, Produktkategorien und Kundendaten existieren. Es können auch Ressourcen für prozessorientierte Konzepte existieren, wie beispielsweise das Bestellen von Produkten oder die Auswahl einer Versandoption.

[5b] [6b]

#### Hypermedia style

Der Hypermedia-Stil ermöglicht es, ähnlich wie im Web, die wichtigsten Pfade zwischen Ressourcen mithilfe von Links zwischen ihnen zu navigieren, anstatt jede Ressource individuell zu kennen und deren URI in die Adressleiste des Browsers einzugeben. Hypermedia tut dasselbe, jedoch für die Ressourcen einer API. Im Web lesen Menschen Seiten und entscheiden dann, welchem Link sie folgen möchten. Bei Hypermedia-APIs treffen Maschinen normalerweise diese Entscheidung. Das bedeutet, dass Links maschinenlesbare Bezeichnungen benötigen, damit Maschinen die verfügbaren Optionen identifizieren und eine Wahl treffen können. Diese Bezeichnungen sind konzeptionell ähnlich wie der Text eines Links, den Menschen auf Webseiten anklicken, jedoch werden die Bezeichnungen in der maschinenlesbaren Darstellung von Ressourcen dargestellt, die oft in JSON vorliegt. In einer Hypermedia-API kann man mithilfe der Links zwischen den Ressourcen "navigieren".
Allerdings kann die Benutzerfreundlichkeit des Navigierens das Risiko erhöhen, dass der Leser die Materialien überfliegt und fragmentierte Informationen erhält. Außerdem kann es, da Client und Server Daten teilen, zu "gesprächigen" APIs führen, die mehrere Interaktionen erfordern, damit der Client auf alle erforderlichen Informationen zugreifen kann.

Darüber hinaus wissen API-Nutzer oft zu Beginn nicht genau, was sie wollen, und es ist effizienter, eine Abfrage zu schreiben, um genau das zu erhalten, was sie wollen, wie es der Abfragenstil bietet.
[5b] [6b]

#### Query style

Der "Query Style" unterscheidet sich von den "Resource Style" und "Hypermedia Style", weil er einen einzelnen Einstiegspunkt für den Zugriff auf potenziell große Mengen von Ressourcen bereitstellt. Die Idee des Query-Stils besteht darin, dass diese Ressourcen in strukturierter Form vom API-Anbieter verwaltet werden. Diese Struktur kann abgefragt werden, und die Antwort enthält die Abfrageergebnisse. Dies ähnelt in gewisser Weise der Funktionsweise von Datenbanken, die ein zugrunde liegendes Datenmodell für die von ihnen gespeicherten Daten haben und eine Abfragesprache, die Teile dieser Daten auswählen und abrufen kann. Ein Vorteil des Query-Stils besteht darin, dass jeder Verbraucher genau das anfordern kann, was er möchte. Dies bedeutet, dass mit einer gut konstruierten Abfrage das Kombinieren von Ergebnissen, für die in Resource/Hypermedia-APIs zahlreiche Anfragen erforderlich gewesen wären, möglich ist. Beispielsweise können Sie eine einzige "Abfrage" für alles senden, was Sie benötigen, anstatt mehrere HTTP-Anfragen an verschiedene Endpunkte zu senden.

Obwohl der Query-Stil gegenüber seinen Vorteilen nur geringfügige Nachteile hat, gehört die Komplexität von Abfragen dazu. API-Nutzer müssen ein gutes Verständnis des zugrunde liegenden Daten- und Abfragemodells haben, um die Abfrage-API ordnungsgemäß zu verwenden und effiziente Anfragen zu stellen, um Rekursion oder zu viele verschachtelte Ressourcen zu vermeiden. Außerdem ist es komplizierter, einen vereinfachten Cache mit GraphQL zu implementieren als im Resource-Stil, weil REST-APIs mehrere Endpunkte haben. Sie können nativen HTTP-Caching nutzen, um das erneute Abrufen von Ressourcen zu vermeiden. Ein weiteres Problem bei GraphQL ist die Begrenzung der Anfragen, bei der festgelegt wird, "nur diese Anzahl von Anfragen ist erlaubt".

[5b] [6b]

#### Tunnel style

Im "Tunnel-Stil" handelt es sich bei einer API um eine Sammlung von Funktionen, die remote aufgerufen werden. APIs werden zu einer einfachen Erweiterung eines lokalen Programmierungsszenarios, bei dem alle freigegebenen Verfahren als APIs verfügbar sind. Der Tunnel-Stil ist für Entwickler praktisch, da nur minimale Anstrengungen erforderlich sind, um APIs zu erstellen.

Eine gängige Technik, die in diesem Stil verwendet wird, ist die Methode des Remote Procedure Calls (RPC). RPC ist ein Anfrage-Antwort-Protokoll, bei dem ein Client eine Anfrage an einen entfernten Server sendet, um ein bestimmtes Verfahren auszuführen, und dann vom Client eine Antwort erhält. Allerdings sind RPC-APIs viel schwieriger zu warten und zu aktualisieren als REST-APIs, weshalb RPC-APIs in der modernen API-Entwicklung nicht so häufig verwendet werden.

gRPC ist eine effiziente Implementierung des Tunnel-Stils (RPC) und eignet sich gut für verteilte Systeme. Es verfügt über SDKs für viele Sprachen und Plattformen, sodass es weitreichend für die Kommunikation zwischen Plattformen und Sprachen eingesetzt werden kann. gRPC ist schnell und effizient, da es Protocol Buffers (protobufs) zur Serialisierung und Deserialisierung verwendet, den HTTP/2-Standard für optimierte binäre Übertragungen und bidirektionales Streaming zur Vermeidung von (langen) Abfragen und blockierenden HTTP-Aufrufen.
[5b] [6b]

#### Event-based style

Im "Event-based Style" erstellt der API-Anbieter Ereignisse, die an die API-Nutzer übermittelt werden, anstatt dass die Nutzer etwas vom Anbieter anfordern. Anwendungen, die diese API nutzen, erwarten, über jede Änderung des Zustands eines bestimmten Datensatzes oder Datensätze in der API informiert zu werden. Es gibt viele Wege und technologische Optionen, die in Betracht gezogen werden können, wenn es darum geht, eine ereignisgesteuerte API zu implementieren. Mein Artikel "Wie man ereignisgesteuerte APIs mit Webhooks und API-Gateways erstellt" erforscht dieses Thema.

Eine andere Herangehensweise besteht darin, dass Ereigniskonsumenten sich mit einem Message-Broker verbinden, der sie von den Ereignisproduzenten entkoppelt. Der Message-Broker kümmert sich um das Management der Ereignisse, und Konsumenten müssen sich für bestimmte Ereignistypen anmelden, damit der Broker sicherstellen kann, dass Ereignisse dieses Typs an die Abonnenten ausgeliefert werden. In diesem Fall steht die Architektur im Mittelpunkt des Auslieferungs-Brokers, und alle Ereignisproduzenten und -konsumenten sind mit diesem verbunden.

Einige Nachteile bei der Wahl des eventbasierten Stils sind, dass die Implementierung im Vergleich zu anderen Stilen mehr Zeit in Anspruch nehmen kann, dass bei falscher Anwendung des Stils mehrfache doppelte Nachrichten zwischen verschiedenen Diensten ausgelöst werden können und dass Fehlerbehandlung und Problembehebung ohne Hinzufügen von Tools von Drittanbietern zur effektiven Überwachung des Ereignisflusses herausfordernd sein können. Sie können jedoch ein API-Gateway vor ereignisbasierte APIs schalten, wenn Sie moderne Anwendungen beobachten, da es eine einfache integrierte Anbindung an verschiedene Überwachungsplattformen bietet.

[5b] [6b]


### API Implementation Standards


  API Implementation Standards sind Leitlinien und Best Practices, die bei der Entwicklung und Umsetzung von APIs (Application Programming Interfaces) befolgt werden sollten. Diese Standards dienen dazu, die Qualität, Konsistenz, Interoperabilität und Sicherheit von APIs sicherzustellen. Hier sind einige wichtige Aspekte, die in API Implementation Standards behandelt werden:
  Die genauen Standards können je nach API-Entwicklungsteam, Unternehmen und Anwendungsfall variieren. Sie dienen jedoch dazu, eine konsistente und hochwertige API-Entwicklung zu fördern und die Interoperabilität zwischen verschiedenen Systemen sicherzustellen. Standards sind entscheidend, um API-Verwirrung und Inkompatibilität zu verhindern, insbesondere in der heutigen vernetzten Welt, in der APIs eine zentrale Rolle spielen.

#### Vergleich, Motivation, Vorteile, Nachteile

  **Vergleich mit individueller API-Entwicklung:**
   API Implementation Standards bieten einen einheitlichen Ansatz für die API-Entwicklung und gewährleisten Konsistenz. Im Vergleich zur individuellen API-Entwicklung, bei der Entwickler möglicherweise eigene Konventionen und Praktiken verwenden, führen Standards zu einer höheren Qualität und besseren Wartbarkeit der APIs.
  Vergleich verschiedener Standards: Es gibt verschiedene Standards und Spezifikationen wie REST, GraphQL, SOAP usw. Jede dieser Standards hat ihre eigenen Empfehlungen und Regeln. Ein Vergleich dieser Standards hilft dabei, den besten Ansatz für bestimmte Anwendungsfälle zu wählen.
  
  **Motivation:**
Interoperabilität: API Implementation Standards motivieren die Interoperabilität zwischen verschiedenen Systemen. Sie ermöglichen es, APIs unabhängig von der Plattform, der Programmiersprache oder dem Framework zu entwickeln und zu nutzen.
Qualitätssicherung: Standards fördern bewährte Praktiken in Bezug auf Sicherheit, Dokumentation, Wartbarkeit und Leistung, was dazu beiträgt, qualitativ hochwertige APIs zu erstellen.
Effizienz: Durch die Einhaltung von Standards können Entwickler APIs schneller entwickeln und implementieren, da sie 
auf bewährte Muster und Konventionen zurückgreifen können.

**Vorteile:**
Konsistenz: Standards sorgen für eine einheitliche Struktur und Benennung von APIs, was die Nutzung und Wartung erleichtert.
Interoperabilität: APIs, die Standards einhalten, sind leichter in andere Anwendungen und Systeme zu integrieren.
Sicherheit: Standards fördern bewährte Sicherheitspraktiken, die dazu beitragen, die APIs vor Angriffen zu schützen.
Dokumentation und Verständlichkeit: Gut dokumentierte Standards erleichtern Entwicklern das Verstehen und Nutzen von APIs.

**Nachteile:**
Einschränkung der Kreativität: Zu strikte Standards könnten die kreative Gestaltung von APIs einschränken, insbesondere in innovativen Anwendungsfällen.
Komplexität: Einige Standards können komplex sein und eine steile Lernkurve für Entwickler haben, insbesondere wenn sie neu in der API-Entwicklung sind.
Übermäßige Regulierung: Übermäßige Regulierung und zu viele Standards können die Flexibilität in der Entwicklung behindern und zu unnötiger Komplexität führen.
Insgesamt sind API Implementation Standards entscheidend, um die Qualität und Konsistenz von APIs sicherzustellen und die Interoperabilität zwischen verschiedenen Systemen zu fördern. Es ist jedoch wichtig, die spezifischen Anforderungen eines Projekts zu berücksichtigen und die Standards entsprechend anzupassen, um die besten Ergebnisse zu erzielen.
[8b]

#### RESTful

Representational State Transfer (REST) ist eine Software-Architektur, die Bedingungen zur Funktionsweise einer API festlegt. REST wurde ursprünglich als Leitfaden zur Verwaltung der Kommunikation auf einem komplexen Netzwerk wie dem Internet erstellt. Sie können REST-basierte Architektur verwenden, um leistungsstarke zuverlässige Kommunikation nach Maß zu unterstützen. Die Architektur ist leicht implementierbar und leicht modifizierbar. Dadurch wird jedem API-System Sichtbarkeit und plattformübergreifende Portierbarkeit verliehen.

API-Entwickler können APIs mit mehreren verschiedenen Architekturen entwerfen. APIs, die dem REST-Architekturstil folgen, werden als REST-APIs bezeichnet. Webservices, die diese REST-Architektur implementieren, werden als RESTful-Webservices bezeichnet. Der Begriff RESTful-API bezieht sich im Allgemeinen auf die RESTful-Web-APIs. Jedoch können die Begriffe REST-API und RESTful-API auch als Synonyme verwendet werden.

Eine RESTful-API ist eine Schnittstelle mit der zwei Computersysteme Informationen auf sichere Weise über das Internet austauschen können. Die meisten Geschäftsanwendungen müssen mit anderen internen und externen Anwendungen kommunizieren, um verschiedene Aufgaben zu erfüllen. Um beispielsweise monatliche Gehaltsabrechnungen zu erstellen, muss Ihr internes Buchhaltungssystem Daten mit dem Banksystem Ihres Kunden austauschen, um die Rechnungsstellung zu automatisieren und mit einer internen Zeiterfassungsanwendung zu kommunizieren. RESTful-APIs unterstützen diesen Informationsaustausch, da sie sicheren, zuverlässigen und effizienten Software-Kommunikationsstandards folgen.

[9b]

##### HATEOAS

HATEOAS ist ein Akronym, das für „Hypermedia as the Engine of Application State“ (dt. Hypermedia als Motor des Anwendungszustands) steht. Dieser Begriff, den Fielding im Rahmen seiner REST-Definition eingeführt hat, beschreibt eine der entscheidenden REST-Eigenschaften: Da der Architekturstil eine universelle Schnittstelle bieten soll, fordert HATEOAS nämlich, dass der REST-Client sich ausschließlich durch das Folgen von URIs (Uniform Resource Identifier) im Hypermedia-Format durch die Webanwendung bewegen kann. Wird dieses Prinzip umgesetzt, benötigt der Client abgesehen von einem grundsätzlichen Verständnis von Hypermedia keinerlei weitere Informationen, um mit der Applikation bzw. dem Server interagieren zu können.

Die Bereitstellung der einzelnen URIs erfolgt dabei beispielsweise:

in Form von href- und src-Attributen, wenn es sich um HTML-Dokumente oder -Snippets handelt
durch JSON- bzw. XML-Attribute/-Elemente, die von den jeweiligen Clients automatisch erkannt werden
Durch die Umsetzung des HATEOAS-Prinzips lässt sich die Schnittstelle eines REST-Services jederzeit anpassen, was ein wichtiger Vorteil dieser Architektur gegenüber anderen Applikationsstrukturen ist – beispielsweise gegenüber solchen, die auf Grundlage von SOAP (Simple Object Access Protocol) funktionieren.

[10b] [11b]

###### Best Practices für RESTful


###### Naming REST API Endpoints

Die Benennung von REST-API-Endpunkten ist ein entscheidender Aspekt bei der Gestaltung einer klaren, verständlichen und konsistenten API. Hier sind bewährte Praktiken und Empfehlungen für die Benennung von REST-API-Endpunkten:

* Verwendung von Substantiven: Verwenden Sie Substantive, um Ihre Ressourcen in den Endpunkten zu bezeichnen. Vermeiden Sie Verben in den Endpunkt-URLs, da die HTTP-Methoden (GET, POST, PUT, DELETE) bereits die Aktionen beschreiben.

* Klare und beschreibende Namen: Wählen Sie Namen, die die Ressource oder den Zweck des Endpunkts klar beschreiben. Vermeiden Sie abgekürzte oder kryptische Bezeichnungen, die für API-Benutzer unverständlich sein könnten.

* Plurale Form für Sammlungen: Verwenden Sie die Pluralform von Substantiven, um Sammlungen von Ressourcen zu bezeichnen. Dies macht die API konsistenter und leichter verständlich.

* Hierarchische Struktur: Wenn Ihre Ressourcen hierarchisch verschachtelt sind, spiegeln Sie dies in der URL wider. Dies hilft, die Beziehungen zwischen Ressourcen klar darzustellen.

* Verwendung von Bindestrichen: Verwenden Sie Bindestriche, um Worte in URL-Namen zu trennen. Vermeiden Sie Leerzeichen, Unterstriche oder Sonderzeichen.

* Versionierung: Wenn Sie Versionen Ihrer API erstellen, fügen Sie die Version in den Endpunkt-URLs hinzu, um Abwärtskompatibilität sicherzustellen.

* Klare Hierarchie: Strukturieren Sie Ihre Endpunkte so, dass sie eine klare Hierarchie widerspiegeln und den Benutzern ermöglichen, Ressourcen intuitiv zu navigieren.

[12b] [13b] [14b]


##### Error Handling 

Der erste Schritt im Umgang mit Fehlern besteht darin, dem Client einen angemessenen Statuscode bereitzustellen. Zusätzlich kann es erforderlich sein, weitere Informationen im Antworttext bereitzustellen.

* Grundlegende Antworten
* Die einfachste Möglichkeit, Fehler zu behandeln, besteht darin, mit einem entsprechenden Statuscode zu antworten. Hier sind einige häufige Statuscodes:
  * 400 Bad Request: Der Client hat eine ungültige Anfrage gesendet, z. B. fehlende Anfragekörper oder Parameter.
  * 401 Unauthorized: Der Client konnte sich nicht beim Server authentifizieren.
  * 403 Forbidden: Der Client ist authentifiziert, hat jedoch keine Berechtigung für den Zugriff auf die angeforderte Ressource.
  * 404 Not Found: Die angeforderte Ressource existiert nicht.
  * 412 Precondition Failed: Eine oder mehrere Bedingungen in den Anfrage-Headern waren falsch.
  * 500 Internal Server Error: Ein allgemeiner Fehler ist auf dem Server aufgetreten.
  * 503 Service Unavailable: Der angeforderte Dienst steht nicht zur Verfügung.

* Standardmäßige Spring-Fehlerantworten

  * Diese Grundsätze sind so weit verbreitet, dass Spring sie in seinem standardmäßigen Fehlerbehandlungsmechanismus kodiert hat. Spring gibt automatisch den HTTP-Statuscode 500 zurück, wenn eine Ausnahme wie "BookNotFoundException" ausgelöst wird. Es wird empfohlen, den spezifischsten Fehlercode zu verwenden, wenn dies möglich ist.

* Detaillierte Antworten

Manchmal reicht ein Statuscode nicht aus, um die Spezifikationen des Fehlers anzuzeigen. In solchen Fällen kann der Antworttext dem Client zusätzliche Informationen bereitstellen, einschließlich:

* Error: Eine eindeutige Kennung für den Fehler.
* Message: Eine kurze, für Menschen lesbare Nachricht.
* Detail: Eine ausführlichere Erklärung des Fehlers.
* Help: Eine URL, die den Client zu weiteren Informationen führt.
Normalerweise sollte das "Error"-Feld nicht mit dem Statuscode übereinstimmen, sondern eine eindeutige Anwendungsfehlerkennung sein. Die "Message" sollte für die Benutzeroberfläche geeignet sein, während die "Detail"-Information für Entwickler bestimmt ist.

* Standardisierte Antworttexte

In einem Versuch, die Fehlerbehandlung von RESTful APIs zu standardisieren, hat das IETF RFC 7807 entwickelt, das ein generalisiertes Fehlerbehandlungsschema erstellt. Dieses Schema besteht aus fünf Teilen: "type", "title", "status", "detail" und "instance". Es soll die einheitliche Fehlerbehandlung erleichtern.

Die Verwendung von RFC 7807 ermöglicht es, anstelle von benutzerdefinierten Fehlerantworten einen einheitlichen Fehlerantwortkörper zu verwenden. Dies erleichtert Bibliotheken und Frameworks die einheitliche Behandlung von Fehlern.
[15b]

##### Best Practices Security

Um Missbrauch der API durch schädliche oder unachtsame Benutzer zu verhindern, ist eine Zugriffsrichtlinie erforderlich. Dies definiert, wer Daten auf Ihrem Server anzeigen oder ändern kann. Dieser Prozess wird als "Autorisierung" bezeichnet.

* Es wird dringend empfohlen, immer TLS (Transport Layer Security) zu verwenden, um die Daten zu schützen, die über Ihre API gesendet werden.

* OAuth2 ist eine gute Methode für Single Sign-On (SSO) und ermöglicht es Benutzern, sich mit vertrauenswürdigen Drittanbietern zu authentifizieren, um auf Ressourcen zuzugreifen.

* Die Verwendung von API-Schlüsseln ist eine einfache Methode, um vorhandenen Benutzern programmatischen Zugriff zu gewähren. Diese Schlüssel sollten sorgfältig behandelt werden, um die Sicherheit zu gewährleisten.

* Die Konfiguration verschiedener Berechtigungen für verschiedene API-Schlüssel kann nützlich sein, um den Zugriff auf verschiedene Teile Ihrer API zu steuern.

* Komplexe Autorisierungslogik sollte in der Anwendungslogik und nicht in der Middleware umgesetzt werden. Tools wie Oso können bei der Vereinfachung von Autorisierungsrichtlinien helfen.

Zusammenfassend wird empfohlen, auf bewährte Bibliotheken und Tools zurückzugreifen, um die Autorisierung zu erleichtern und Fehler zu minimieren. Die Sicherheit und die ordnungsgemäße Umsetzung von Autorisierung sind entscheidend für die Gestaltung nützlicher und sicherer API-Endpunkte.


#### GraphQL

GraphQL ist eine Abfragesprache und serverseitige Runtime für APIs, die den Kunden nur diejenigen Daten zur Verfügung stellt, die sie wirklich brauchen.

GraphQL macht APIs schneller, flexibler und entwicklerfreundlicher. Es kann sogar innerhalb einer IDE namens GraphiQL bereitgestellt werden. Mit dieser Alternative zu REST können Entwickler Anfragen strukturieren, die mit einem einzigen API-Aufruf Daten aus mehreren Quellen gleichzeitig abrufen.

Außerdem können API-Maintainer mit GraphQL flexibel Felder hinzufügen oder entfernen, ohne dass dies bestehende Abfragen beeinträchtigt. Entwickler können APIs mit ihrer bevorzugten Methode erstellen, und die GraphQL-Spezifikation stellt sicher, dass die API für den Kunden auf vorhersehbare Weise funktioniert.

#### Schema

Das Schema ist die Grundlage jeder GraphQL-API. Es definiert, welche Daten abgerufen werden können und wie diese Daten strukturiert sind.
Es besteht aus zwei Hauptteilen: dem Query-Typ und dem Mutation-Typ.
Der Query-Typ enthält die Abfragen (Queries), die verwendet werden, um Daten abzurufen.
Der Mutation-Typ enthält die Mutationen, die verwendet werden, um Daten zu ändern oder zu erstellen.
Das Schema wird normalerweise in einer speziellen Abfragesprache definiert, die oft als "Schema Definition Language" (SDL) bezeichnet wird.

* API-Entwickler erstellen mit GraphQL Schemata für alle möglichen Daten, die ein Kunde über diesen Service abfragen kann.

* Ein GraphQL-Schema definiert, welche Objekttypen Sie anfordern können und welche Felder enthalten sein sollen.

* GraphQL gleicht die eingehenden Abfragen mit dem Schema ab und führt die validierten Abfragen aus.

Ein GraphQL-Schema besteht aus zwei Hauptteilen:

Query-Typ: Dieser definiert die Lesedatenoperationen (Abfragen), die Client-Anwendungen durchführen können. Jede Abfrage beginnt mit einem Feld auf dem Query-Typ.

Mutation-Typ: Dieser definiert die Schreib- und Änderungsoperationen (Mutations), die Client-Anwendungen ausführen können. Mutations werden verwendet, um Daten zu erstellen, zu aktualisieren oder zu löschen.

* Zusätzlich zu diesen Hauptteilen kann ein GraphQL-Schema auch benutzerdefinierte Typen definieren. Diese benutzerdefinierten Typen können Objekttypen, Skalar- oder Enumerationstypen sein. Objekttypen beschreiben die Datenstruktur und die Beziehungen zwischen verschiedenen Entitäten in Ihrer Anwendung. Skalar- und Enumerationstypen definieren, welche Arten von Werten für bestimmte Felder erlaubt sind.

[16b] [17b]

##### Query:

Eine Query in GraphQL ist eine Operation, mit der Daten aus der API abgerufen werden.
Sie ermöglicht es dem Client, genau anzugeben, welche Daten und Felder benötigt werden.
Die Struktur einer Query folgt der Struktur des Schemas und spiegelt oft die gewünschte Datenstruktur wider.
Ein Beispiel für eine Query könnte sein: "Gib mir den Namen und das Alter eines Benutzers sowie die Titel seiner Beiträge."


###### Resolver:

Resolver sind Funktionen, die die eigentliche Arbeit in einer GraphQL-API ausführen. Sie bestimmen, wie die Daten für die verschiedenen Felder im Schema abgerufen oder verarbeitet werden.
Jedes Feld im Schema ist einem Resolver zugeordnet. Wenn eine Query ausgeführt wird, ruft GraphQL die entsprechenden Resolver auf, um die angeforderten Daten zu erhalten.
Resolver können Daten aus einer Datenbank abrufen, APIs aufrufen, Berechnungen durchführen oder auf andere Weise die Daten bereitstellen, die in der Query angefordert werden.
Ein einfaches Beispiel für einen Resolver könnte sein: "Wenn nach dem Namen eines Benutzers gefragt wird, greife auf die Datenbank zu und gib den Namen des Benutzers zurück."

###### Mutation:

Mutationen sind Operationen in GraphQL, mit denen Daten geändert oder erstellt werden können.
Im Gegensatz zu Queries, die nur lesend sind, erlauben Mutationen das Schreiben von Daten auf den Server.
Mutationen sind oft in der Art einer Anfrage aufgebaut, die beschreibt, welche Daten geändert oder hinzugefügt werden sollen.
Ein Beispiel für eine Mutation könnte sein: "Erstelle einen neuen Benutzer mit dem Namen und der E-Mail-Adresse."

[16b] [17b]

###### Backend For Frontend

Das Backends for Frontends Pattern (BFF-Muster) ist ein Designmuster für die Architektur von Mikroservices. Dieses Muster konzentriert sich auf die Trennung von API-Gateways entsprechend den spezifischen Frontend-Anwendungen. Anstatt nur ein allgemeines API-Backend zu haben, werden mehrere Backend-Services für Frontend-Anwendungen bereitgestellt, und dazwischen wird ein API-Gateway zur Handhabung von Routing und Aggregationsvorgängen platziert.

* Die Verwendung dieses Musters hilft, den sogenannten Single Point of Failure zu vermeiden. Anstatt ein komplexes API-Gateway zu haben, das ein Risiko darstellen und zum Flaschenhals in der Architektur werden könnte, werden mehrere API-Gateways erstellt, die die Client-Anwendungen entsprechend ihrer Anwendungsgrenzen gruppieren.

* Durch die Anwendung des BFF-Musters können unterschiedliche Anforderungen der Frontend-Anwendungen erfüllt werden, ohne die anderen Frontend-Anwendungen zu beeinträchtigen. Das Muster ermöglicht die Implementierung mehrerer Gateways, wodurch eine flexible Anpassung an die Bedürfnisse der Benutzeroberfläche erfolgt.

* In der Praxis bedeutet dies, dass für verschiedene Arten von Client-Anwendungen, wie mobile, Web- und Desktop-Anwendungen, separate API-Gateways erstellt werden. Jedes dieser Gateways bietet maßgeschneiderte APIs, um den spezifischen Anforderungen der jeweiligen Client-Anwendung gerecht zu werden. Zum Beispiel kann ein mobiles Frontend unterschiedliche API-Anforderungen haben, die in speziellen API-Gateway-Services implementiert werden können.

* Die Anwendung des Backends for Frontends Pattern ist besonders hilfreich in Szenarien, in denen eine Anpassung eines einzigen Backends für verschiedene Benutzeroberflächen vermieden werden soll.

Insgesamt ermöglicht das BFF-Muster eine effiziente und flexible Gestaltung von APIs, die auf die Bedürfnisse der Frontend-Umgebungen zugeschnitten sind. Es bietet eine klare Richtlinie für die Implementierung mehrerer Gateways, um den Anforderungen verschiedener Client-Anwendungen gerecht zu werden.

[18b]


#### API Design

API-Design bezieht sich auf die Gestaltung von Schnittstellen, über die Softwarekomponenten miteinander kommunizieren. Eine gut gestaltete API sollte benutzerfreundlich, konsistent, effizient, sicher, und gut dokumentiert sein. Sie sollte auch flexibel, testbar und gut überwachbar sein. Ein gutes API-Design ist entscheidend, um die Nutzung und Integration von Software zu erleichtern.

###### Code First vs Design First

* Es gibt zwei Hauptansätze zur Entwicklung von APIs: 
Der Code-First-Ansatz, bei dem der Code nach Festlegung der Geschäftsanforderungen entwickelt wird, und die Dokumentation aus dem Code generiert wird. 
Der Design-First-Ansatz hingegen legt den Fokus darauf, den API-Vertrag zuerst zu entwerfen, bevor der Code geschrieben wird. Dieser Ansatz verwendet häufig das OpenAPI-Format, um menschen- und maschinenlesbare Verträge zu erstellen, bevor die eigentliche Entwicklung beginnt.
[19b]



* Design First
Beim Design-First-Ansatz wird die API zuerst geplant und spezifiziert, bevor der eigentliche Programmcode geschrieben wird. Dies bedeutet, dass zuerst die Struktur, das Verhalten und die Dokumentation der API festgelegt werden, oft mit Hilfe von Design-Tools wie Swagger. Erst danach beginnt die eigentliche Entwicklung des Codes, basierend auf diesem Design. Dieser Ansatz legt den Fokus auf eine klare und sorgfältige Gestaltung der API, bevor die Umsetzung beginnt.

* Code First 
Der Code-First-Ansatz ist eine Methode zur Entwicklung von APIs, bei der die Implementierung des API-Codes zuerst geschrieben wird, bevor die API-Spezifikation entworfen wird. Dies bedeutet, dass die API auf Grundlage des vorhandenen Codebasis gestaltet wird.

Die Vorteile dieses Ansatzes sind ein besseres Verständnis der Funktionalität und des Verhaltens der API sowie eine effizientere Entwicklung. Entwickler können direkt mit der tatsächlichen Implementierung arbeiten und Anpassungen in Echtzeit vornehmen. Dies ist besonders nützlich für kleinere oder einfachere Projekte und in Fällen, in denen Anforderungen nicht gut definiert sind oder häufig ändern.

Nachteile des Code-First-Ansatzes :Der Code-First-Ansatz kann zu mangelnder Dokumentation und Standardisierung führen, da es keine klare API-Spezifikation gibt. Das kann zu Verwirrung und Ineffizienz führen.

Vorteile des Code-First-Ansatzes :Der Code-First-Ansatz kann zu schnellere Entwicklung, einfache Iteration, direkte Kontrolle über die Implementierung und nahtlose Integration mit vorhandenem Code. Nachteile sind mangelnde Dokumentation, erhöhte Abhängigkeit vom Codebasis und begrenzte Designflexibilität.

#### API Versioning

API-Versionierung ist ein Konzept in der Softwareentwicklung, das bei der Veröffentlichung von APIs verwendet wird. Es bezieht sich auf die Verwaltung und Aktualisierung von APIs über die Zeit, um sicherzustellen, dass bestehende Anwendungen, die die API verwenden, weiterhin korrekt funktionieren, während gleichzeitig neue Funktionen hinzugefügt oder bestehende verbessert werden.

Es gibt verschiedene Ansätze zur API-Versionierung:

* URI-Versionierung: Hier wird die Versionsnummer in der URL der API angegeben, z.B. https://api.example.com/v1/resource. Dies ermöglicht es, verschiedene Versionen der API parallel zu betreiben.

* Header-Versionierung: Die Version wird im HTTP-Header der Anfrage oder Antwort angegeben, um die Version der API zu identifizieren. Dies kann nützlich sein, wenn die Versionsnummer nicht in der URL erscheinen soll.

* Media-Type-Versionierung: Die Version wird im Media Type (z.B., application/vnd.example.v1+json) angegeben, um die Darstellung der API-Ressource zu kennzeichnen.

* Accept-Version Header: Dies ist eine Erweiterung von Header-Versionierung, bei der der Client mit dem Accept-Version-Header angibt, welche Version der API er verwenden möchte.

API-Versionierung ist wichtig, um die Abwärtskompatibilität zu wahren, bestehende Benutzer nicht zu beeinträchtigen und gleichzeitig Raum für Weiterentwicklung zu schaffen. Die Wahl des Versionierungsansatzes hängt von den Anforderungen des Projekts und den Präferenzen des Entwicklungsteams ab.

[20b] [21b]

#### API Testing
Mit einem API-Test können Entwickler bestimmen, ob APIs die Anforderungen in Sachen Funktionalität, Leistung, Zuverlässigkeit und Sicherheit erfüllen. Ziel ist es, Fehler und andere unerwartete Verhaltensweisen zu finden, damit Ihre Benutzer kein mangelhaftes oder unsicheres Produkt erhalten. Sie müssen sicherstellen, dass Sie APIs veröffentlichen, die effizient und effektiv funktionieren, sonst werden sie nicht eingesetzt.

Arten von API-Tests und ihre Bedeutung:

 API-Tests umfassen:
oft **Validierungs-, Funktion-, Last-, Zuverlässigkeits-, Sicherheits- und Penetrationstests**. 
* Validierungstests beurteilen die Qualität des Produkts und dessen Effizienz. 
* Funktionstests gewährleisten die korrekte Funktionsweise der API, während Lasttests prüfen, wie gut sie hohe Belastungen bewältigen kann. 
* Zuverlässigkeitstests stellen sicher, dass die API konsistente Ergebnisse liefert, und Sicherheitstests schützen vor Sicherheitslücken.
* Penetrationstests testen die API gegen Angriffe von außen.

Warum sind API-Tests wichtig?

API-Tests erfüllen den selben Zweck wie auch andere Softwaretests, sie helfen Entwicklern, Fehler frühzeitig zu erkennen, bevor sie zu größeren Problemen werden. Sie ermöglichen den Zugriff auf die App ohne Benutzeroberfläche und sparen Zeit und Kosten. API-Tests sind technologieunabhängig und können mit GUI-Tests integriert werden.

Vor- und Nachteile von API-Tests:

Die Vorteile von API-Tests sind die Effizienz, der frühzeitige Fehlerhinweis, die Unabhängigkeit von Technologien und die Integration mit GUI-Tests. Die Nachteile sind die Validierung von Parametern, die Kombination von Parametern und die Aufrufreihenfolge, insbesondere bei Multithreading-Anwendungen.
[22b]

###### Spezifikation / Dokumentation

#### OpenAPI

OpenAPI ist ein Standard zur Beschreibung von APIs. Die OpenAPI-Spezifikation definiert ein offenes und herstellerneutrales Beschreibungsformat für API-Dienste. Insbesondere lassen sich mithilfe von OpenAPI REST-konforme APIs beschreiben, entwickeln, testen und dokumentieren.

Im Gegensatz zu JSON Schema handelt es sich bei einem OpenAPI-Dokument um eine Definition für eine komplette API und nicht nur um Datenmodelle. Vor der Einführung von OpenAPI wurden viele APIs entworfen, ohne die Möglichkeit, wie sie funktionieren sollten, oder die Möglichkeit zur Überprüfung, ob sie wie erwartet arbeiten. Mit dieser maschinenlesbaren Beschreibung können auch nützliche Tools für Menschen generiert werden, wie beispielsweise Dokumentation und Mock-Server.

Man kann das JSON Schema verwenden, um Datenobjekte für Anfragen und Antworten zu beschreiben. OpenAPI geht jedoch über die Formatierung dieser Anfragen und Antworten hinaus und beinhaltet auch, wie sie strukturiert sein sollten. Ähnlich kannst du API-Antworten mit JSON Schema nachahmen, aber du benötigst etwas wie OpenAPI, um einen vollständigen Mock-Server zu generieren.

OpenAPI ist also ein leistungsstarkes Werkzeug, um APIs umfassend zu beschreiben, von ihren Endpunkten über Datenmodelle bis hin zur Formatierung von Anfragen und Antworten. Dies erleichtert nicht nur die Entwicklung von APIs, sondern ermöglicht auch die Generierung von Dokumentation und Mock-Servern, die bei der Entwicklung und dem Test von APIs äußerst hilfreich sind.

[23b] [24b]

###### JSON Schema

JSON Schema ist ein Werkzeug zur Beschreibung von JSON-Dokumenten und deren Struktur. Es handelt sich nicht um eine Datenbank oder ein JSON-Dokument selbst, sondern um eine Vorlage oder eine Schablone für die Struktur von JSON-Daten.

Ein Schema dient dazu, wie Daten strukturiert sein sollten. Es bietet den Vorteil, dass Teams die Struktur ihrer Daten planen und überarbeiten können, bevor sie diese tatsächlich erstellen. Durch die Festlegung von Formaten können Teams effizienter zusammenarbeiten und Fehler vermeiden. Zum Beispiel können Client- und Server-Teams Feedback austauschen und Anwendungsfälle testen, ohne eine vollständige API mit Live-Daten zu benötigen.

JSON Schema wird häufig in Verbindung mit APIs verwendet, aber es kann auch in anderen Kontexten nützlich sein. Es beschreibt ausschließlich die Struktur der Daten in einem JSON-Dokument. JSON Schema kann auch dazu verwendet werden, Datenbanken in wiederverwendbare Blöcke zu strukturieren, um die Effizienz und Handhabbarkeit zu steigern. Überall dort, wo JSON-Daten auf Übereinstimmung mit einem festgelegten Muster geprüft werden müssen, kann JSON Schema hilfreich sein.

JSON Schema ermöglicht also die Definition von Regeln und Mustern, nach denen JSON-Daten validiert werden können. Dies ist besonders nützlich in der Entwicklung von APIs und anderen Anwendungen, bei denen die Struktur von JSON-Daten von großer Bedeutung ist.
[24]

# Referenzen

[1a] :https://chat.openai.com/
[2a] :https://www.snaplogic.com/de/blog/system-integration-types-and-approaches
[3a] :https://kwahome.medium.com/microservice-interactions-query-command-event-d7e01d8cd63c#:~:text=The%20difference%20between%20queries%2C%20commands,completed%20(in%20the%20past).
[4a] :https://de.wikipedia.org/wiki/Remote_Procedure_Call
[5a] :https://de.wikibrief.org/wiki/Message_passing
[6a] :https://de.wikipedia.org/wiki/Internetprotokollfamilie
[7a] :https://medium.com/dailyjs/a-comparison-between-websockets-server-sent-events-and-polling-7a27c98cb1e3
[8a] :https://de.wikipedia.org/wiki/Serialisierung
[9a] :https://learn.microsoft.com/en-us/azure/architecture/patterns/category/data-management
[10a] :https://www.oreilly.com/library/view/design-patterns-for/9781492090700/ch04.html
[11a] :https://de.wikipedia.org/wiki/Schnittstelle
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
[16b] : https://www.redhat.com/de/topics/api/what-is-graphql
[17b] : https://chat.openai.com/ frage: erkläre mir was was Schema, Query, Resolver, Mutation in Graphql sind
[18b] : https://waytoeasylearn.com/learn/backends-for-frontends-pattern/
[19b] : https://www.visual-paradigm.com/guide/development/code-first-vs-design-first/
[20b] : https://chat.openai.com/ frage : was ist API Versioning
[21b] : https://www.torocloud.com/blog/api-versioning-url-vs-header-vs-media-type-versioning#:~:text=Header%20versioning%20is%20another%20approach,sent%20along%20with%20the%20request.
[22b] : https://www.lucidchart.com/blog/de/api-tests-grundlagen-und-best-prectices#:~:text=Was%20sind%20API%2DTests%3F,mangelhaftes%20oder%20unsicheres%20Produkt%20erhalten.
[23b] : https://www.ionos.de/digitalguide/websites/web-entwicklung/was-ist-openapi/
[24b] : https://blog.stoplight.io/openapi-json-schema#:~:text=Both%20are%20description%20formats%20for,API%2C%20not%20just%20data%20models.