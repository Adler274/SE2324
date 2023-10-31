
**Autor:** Simon Fedrau, Jannis Wilmsmeier, Sascha Hahn

# Verteilte Softwaresysteme

**Def.:** Ein verteiltes SoftwareSystem, ist ein ComputerSystem
bei welchem die Software Komponenten über mehrere Rechner/Server 
verteilt sind. Dem Anwender erscheint dies als ein einziges System.

## Eigenschaften, Vorteile, Nachteile
Verteilte Systeme ermöglichen es die Leistungsfähigkeit eines Systems zu erhöhen, indem die Aufgaben auf mehrere Rechner verteilt werden. Die Rechner sind über Netzwerke und dem Internet miteinander verbunden und kommunizieren über bestimmte protokolle miteinander.
Im Nachfolgenden sind einige Vor- und Nachteile aufgelistet.
[1,2]


| Vorteile|Nachteile|
|:-------|:-------|
|**Skalierbarkeit:** <br> Bei steigenden Anforderungen ist das erweitern von hardware Komponenten einfacher umzusetzen|**Komplexität:**<br>Kommunikation aufwändig mit speziellen Protokolen und Techniken<br>Koordinierung von Aktivitäten:Mechanismen zur Synchronisation und Koordininierung<br>|
|**AusfallSicherheit:** <br> Bei Ausfall einzelner Komponenten ist das System nicht zwingengt komplett beeinträchtigt sondern nur Teilweise.Außerderm kann das System so gebaut werden dass mehrere Komponenten die gleiche Aufgabe erfüllen und bei Ausfällen entprächend ein anderes Gerät übernimmt|==>**Ausfallerkennung - Leslie Lamport:**<br>A distributed system is one in which the failure of a computer which you didn't even know existd can render your own computer unusable.<br> **1.** Es existsieren trotzdem abhängigkeiten, die einen stark beeinträchtigen können<br> **2.** Bei sehr großen System kann sich die suche nach dem Fehler über eine große Anzahl von Rechner als sehr zeit- und kostspielig herausstellen.|
|**Transparenz**:<br> Entwickler und Benutzer müssen nicht wissen wie bestimmte Eigenschafte auf die einzelnen Rchner verteilt sind.(Ortstransparenz, Zugriffsttransparenz, Replikationstransparenz, Namenstransparenz)|**Datensicherheit:**Daten müssen massiver gegen Angriffe geschnützt werden, da es mehrere Angriffspunkte gibt.|
|**Heterogenität:**<br>das System kann aus verschiedenen Hardware- und Softwarekomponenten besteht, was mehr möglichkeiten bietet.|
[1,2]


## Motivation (Warum man Verteilung braucht)
Wie schon bei den Vor- und Nachteilen zu sehen bieten verteilte Systeme viele möglichkeiten zur Systemverbesserung, wie z.B. die Skalierbarkeit, Ausfallsicherheit, Transparenz und Heterognetität. Diese Eigenschaften sind in der heutigen Zeit sehr wichtig, da die Anforderungen an die Systeme immer weiter steigen. Verteilte Systeme sind zwar deutlich komplexer und aufwändiger zu entwickeln, bieten aber die Möglichkeiten große Systeme anforderungsgerecht aufzubauen.
[1,2]

## Distributed vs decentralized
Wie wir schon wissen beziehen sich Distributed(Verteilte) Systeme auf die Verteilung der Software auf physisch getrennte Geräte.
Jetzt stellt sich die Frage was mit einem dezentrallene System gemeint ist. Ein dezentrallenes System ist ein System, bei dem die *Entscheidungen* nicht von einer zentralen Instanz getroffen werden, sondern von mehreren/verteilten Instanzen.
Beispiele hierfür sind z.B. Cryptowährungen oder allgemein die Blockchain-Technologie. Hierbei werden die Entscheidungen von mehreren Instanzen getroffen, die sich gegenseitig überprüfen und somit die Sicherheit des Systems gewährleisten.
[3]

## Concurrent vs parallel
Die beiden Begriffe Beziehen sich darauf wie mehrere Aufgaben in der Informatik gleichzeit ausgeführt werden.
Bei der Konkurrenz werden die Aufgaben nicht gleichzeitig bearbeitet, sondern schnell hintereinander/abwechelnd.
Bei der Parallelität werden die Aufgaben auch tatsächlich gleichzeit bearbeitet.
Beides wird genutzt um Resourcen effizient zu nutzen und Aufagaen schneller zu bearbeiten.
[17]


# Systemarchitektur verteilter Softwaresysteme

* Die Systemarchitektur in verteilten Softwaresystemen beschreibt die strukturelle Organisation und Interaktion von Komponenten an verschiedenen Standorten. Sie definiert Aufgabenverteilung, Kommunikation, Datenflüsse und die Verteilung von Software über Netzwerke. Diese Architektur beeinflusst Funktion, Skalierbarkeit und Verhalten des Systems, um Leistungs- und Zuverlässigkeitsanforderungen zu erfüllen. Sie dient als Leitfaden für Entwicklung und Wartung, inklusive Skalierung, Leistungsoptimierung und Sicherheitsmaßnahmen. Eine klare Dokumentation ist entscheidend, um die Architektur zu verstehen und effektiv zu arbeiten.
 
 [1-2,17]

## Visualisierung von Systemarchitekturen

*  hIER MUSS NOCH WAS HIN `#### Irgendwelche Bilder oder so`

## Systemarchitekturmuster

* Systemarchitekturmuster, auch bekannt als Architekturmuster oder Entwurfsmuster, sind erprobte Lösungsansätze für wiederkehrende Herausforderungen im Softwarearchitekturdesign. Diese Muster fungieren als Leitfaden und Vorlage für die Gestaltung von Softwareprojekten, fördern bewährte Vorgehensweisen und tragen zur Effizienz und Wartbarkeit der Softwareentwicklung bei. Nachfolgend sind einige häufig verwendete Systemarchitekturmuster aufgeführt 

### Client Server

* Dieses Muster strukturiert das System in zwei Hauptkomponenten: den Client, der Benutzeranfragen verarbeitet, und den Server, der Daten und Dienste bereitstellt. Diese Aufteilung erleichtert die Skalierbarkeit und optimale Ressourcennutzung.
#### Anwendungsbespiel

* E-Mail-Clients wie Outlook oder Thunderbird kommunizieren mit E-Mail-Servern, um E-Mails abzurufen, zu senden und zu speichern. Der Server verwaltet die E-Mail
Datenbanken und stellt E-Mail-Clients die erforderlichen Informationen zur Verfügung.
[3,17]
#### Web Architekturen

* Einfach ausgedrückt, ist die Architektur einer Webanwendung eine Übersicht darüber, wie die verschiedenen Komponenten deiner Webanwendung miteinander interagieren.

##### PWA vs SPA vs MPA

### PWA (Progressive Web App): 
PWAs sind webbasierte Anwendungen, die eine App-ähnliche Erfahrung bieten. Sie zeichnen sich durch Ressourceneffizienz, Offline-Fähigkeiten, Push-Benachrichtigungen und schnelle Ladezeiten aus. PWAs sind auf verschiedenen Geräten und Betriebssystemen nutzbar.
### SPA (Single Page Application): 
SPAs sind Webanwendungen, bei denen der gesamte Inhalt auf einer einzigen HTML-Seite geladen wird. Sie erlauben dynamische Aktualisierungen ohne Seitenneuladung und bieten nahtlose Benutzererlebnisse mit schnellen Ansichtswechseln.
### MPA (Multi-Page Application): 
MPAs sind traditionelle Webanwendungen, bei denen jede Seite separat vom Server geladen wird. Seitenwechsel erfordern komplette Serveranfragen. MPAs sind einfach zu entwickeln und SEO-freundlich, können jedoch in der Benutzerinteraktion langsamer sein als SPAs.
### Gemeinsamkeiten:
#### Benutzerfreundlichkeit: 
Sie legen Wert auf eine gute Benutzererfahrung und bieten reaktionsschnelle Oberflächen.
Responsivität: Alle können auf verschiedenen Geräten und Bildschirmgrößen funktionieren.
Interaktivität: Sie ermöglichen die Interaktion mit Benutzern und reagieren auf Benutzeraktionen.

#### Unterschiede:
##### Ladeverhalten: 
PWAs zeichnen sich durch schnelles und flüssiges Laden aus, während SPAs einmalig geladen werden und danach nur den Inhalt dynamisch nachladen. MPAs haben im Vergleich längere Ladezeiten.
Seitennavigation: PWAs können sowohl dynamische als auch mehrseitige Navigation verwenden, während SPAs auf dynamische Navigation auf einer einzigen HTML-Seite setzen und MPAs separate HTML-Seiten für die Navigation verwenden.
##### SEO-Freundlichkeit: 
PWAs und MPAs können SEO-freundlich sein, während SPAs möglicherweise zusätzliche Maßnahmen benötigen. MPAs sind von Natur aus SEO-freundlich.
##### Komplexität:
PWAs und SPAs sind in der Regel komplexer, da sie Technologien und Frameworks nutzen, während MPAs einfacher in Entwicklung und Wartung sind.
##### Offline-Fähigkeit:
PWAs sind auf die Offline-Nutzung ausgerichtet, während SPAs und MPAs möglicherweise zusätzlichen Aufwand erfordern.
[4-5,17]

### Peer to peer

 Das Peer-to-Peer (P2P)-Systemarchitekturmuster ist eine Art von Architektur, bei der Computer oder Knoten (Peers) gleichberechtigt miteinander kommunizieren, um Ressourcen, Dienste oder Informationen gemeinsam zu nutzen, ohne die Notwendigkeit eines zentralen Servers oder einer zentralen Autorität. In einem P2P-System kann jeder Peer Anfragen stellen und Dienste bereitstellen, was zu einem dezentralen und selbstorganisierten Netzwerk führt. 

### Merkmale des P2P-Systemarchitekturmusters:
Gleichberechtigung: Alle Peers sind gleichberechtigt und können Ressourcen teilen oder anfordern.
Dezentralisierung: Kein zentraler Server kontrolliert den Datenverkehr, was zu einer dezentralisierten Struktur führt.
#### Selbstorganisation: 
Peers organisieren sich selbst, ohne zentrale Koordination.
Ressourcenteilung: Peers teilen verschiedene Ressourcen, darunter Dateien, Rechenleistung und Bandbreite.
#### Skalierbarkeit: 
Das System kann leicht skaliert werden, indem neue Peers hinzugefügt werden.
#### Robustheit: 
P2P-Systeme sind widerstandsfähig gegenüber Ausfällen.
#### Sicherheit und Datenschutz:
Sicherheit und Datenschutz sind von besonderer Bedeutung, da Peers direkt miteinander kommunizieren.


#### Anwendungsbeispiel

* P2P-Systeme sind besonders bekannt für ihre Verwendung in Filesharing-Netzwerken. Beispiele sind BitTorrent, eDonkey, und das ursprüngliche Napster. In diesen Netzwerken teilen Benutzer Dateien direkt miteinander, ohne einen zentralen Server.
* #### Internet of Things (IoT):
In einigen IoT-Anwendungen kommunizieren IoT-Geräte direkt miteinander über P2P-Netzwerke, um Daten auszutauschen und Aufgaben zu automatisieren.
[2,5,17]
### Event Driven Architecture

* #### Event-Driven Architecture (EDA):
 ist ein architektonisches Muster, bei dem die Kommunikation und Informationsverarbeitung zwischen Systemkomponenten durch das Senden und Empfangen von Ereignissen strukturiert ist. In einer EDA sendet eine Komponente, der sogenannte Ereignisproduzent, ein Ereignis aus. Andere Komponenten, die Ereignisverbraucher, können auf diese Ereignisse reagieren und entsprechende Aktionen auslösen. Ereignisse fungieren als Vermittler zur Kommunikation und Koordination zwischen den verschiedenen Teilen des Systems. 
EDA wird in verschiedenen Anwendungen und Systemen eingesetzt, einschließlich Microservices-Architekturen, IoT-Anwendungen, Streaming-Datenverarbeitung und Benutzeroberflächenereignissen in Anwendungen. Es ist ein effektiver Ansatz, um die Interaktion und Koordination zwischen den Komponenten eines Systems zu erleichtern und gleichzeitig die Flexibilität und Skalierbarkeit zu erhöhen.
[6,17]
### Event Types

In einer ereignisgesteuerten Architektur (Event-Driven Architecture, EDA) repräsentieren Event-Typen verschiedene Kategorien oder Klassifikationen von Ereignissen, die in einem System auftreten können. Diese Event-Typen organisieren, beschreiben und klassifizieren Ereignisse, um sicherzustellen, dass die entsprechenden Systemkomponenten oder Verbraucher sie verstehen und darauf reagieren können. Die Auswahl der Event-Typen hängt von den spezifischen Anforderungen der Anwendung ab. 
Hier sind einige Beispiele für Event-Typen in ereignisgesteuerten 

### Architekturen: 
Systemereignisse: Systemereignisse sind Ereignisse, die durch den Betriebssystem oder niedrigeren Ebenen des Systems ausgelöst werden. Dies können Ereignisse wie Hardwarefehler, Geräteverbindungen, Systemwartungen oder Änderungen des Systemzustands sein.
Fehler- und Ausnahmeereignisse: Diese Event-Typen repräsentieren Fehler, Ausnahmen oder unerwartete Bedingungen im System. Sie umfassen etwa Fehlerprotokolle, Absturzmeldungen und Fehlerbenachrichtigungen.


### Message Broker

* Ein Message Broker in einer EDA ist eine spezialisierte Softwarekomponente oder ein Dienst, der die Vermittlung und Verteilung von Ereignissen oder Nachrichten zwischen verschiedenen Komponenten, Anwendungen oder Diensten im System ermöglicht. Der Message Broker übernimmt die Aufgabe eines Vermittlers, indem er Nachrichten empfängt, weiterleitet und an die entsprechenden Empfänger weitergibt. Dies erleichtert die Umsetzung einer lose gekoppelten Kommunikation zwischen den verschiedenen Komponenten im System und trägt zur einfacheren Entwicklung und Skalierung von ereignisgesteuerten Systemen bei.

#### Bsp:
Nachrichtenvermittlung: Der Message Broker fungiert als Zwischenschicht, um die Kommunikation zwischen verschiedenen Komponenten zu ermöglichen. Er nimmt Nachrichten von Produzenten Ereignisproduzenten entgegen und leitet sie an die entsprechenden Konsumenten Ereignisverbraucher weiter.

### ESB vs Message Queue

* Ein Enterprise Service Bus (ESB) und eine Message Queue (Nachrichtenwarteschlange) sind zwei unterschiedliche Technologien, die in EDAs verwendet werden, um die Kommunikation und Koordination zwischen Anwendungen und Systemkomponenten zu ermöglichen. Sie erfüllen spezifische Funktionen und haben unterschiedliche Einsatzzwecke. Im Folgenden sind die wichtigsten Unterschiede zwischen ESB und Message Queue. 
#### Funktionalität:
ESB ist eine umfassende Integrationsplattform, die verschiedene Anwendungen miteinander verknüpft und Nachrichtenvermittlung, Routing und umfangreiche Nachrichtenverarbeitungsfunktionen bietet.
Message Queues sind Mechanismen zur Nachrichtenvermittlung und Fokussieren sich darauf, Nachrichten temporär zu speichern und zu übertragen, um eine zuverlässige Kommunikation zwischen Anwendungen zu ermöglichen.

Die Unterschiede zwischen ESB und Message Queues sind entscheidend, um die jeweilige Verwendung und Funktionalität zu verstehen. ESB bietet umfassende Integrationsmöglichkeiten, Routing- und Transformationsfunktionen sowie Protokollübersetzung für komplexe Integrationsszenarien. Auf der anderen Seite sind Message Queues auf die zuverlässige Nachrichtenübermittlung und die Bewahrung der Entkopplung zwischen Anwendungen ausgerichtet, wobei sie weniger komplexe Routing- und Transformationsmöglichkeiten bieten.

Trotz dieser Unterschiede weisen beide Technologien einige Gemeinsamkeiten auf, darunter die Entkopplung, Nachrichtenvermittlung, Skalierbarkeit und Fehlertoleranz. Diese Merkmale sind für viele ereignisgesteuerte Architekturen von großer Bedeutung.

Die Wahl zwischen ESB und Message Queues hängt von den spezifischen Anforderungen und Zielen Ihres Projekts ab. In einigen Fällen kann es sogar sinnvoll sein, beide Technologien zu kombinieren, um die Vorteile beider Ansätze zu nutzen und eine effiziente Kommunikation und Integration in Ihrem System zu gewährleisten.

### Anwendungsbeispiel Event Type

#### Ereignistyp: "Benutzerregistrierung" 
Dieser Ereignistyp wird ausgelöst, wenn ein neuer Benutzer sich in einer Webanwendung registriert.
#### Beispielereignis: 
Ein Benutzer mit dem Namen "Max" hat sich erfolgreich registriert.

### Anwendungsbeispiel Message Broker:

#### Sender: 
Eine Webanwendung, die Benutzerregistrierungen verarbeitet.
#### Empfänger: 
Ein Benachrichtigungsdienst, der E-Mails an Administratoren sendet.
#### Ablauf:
Die Webanwendung sendet eine Benutzerregistrierungsanfrage an den Message Broker "EventHub".
Der EventHub leitet das Ereignis an den Benachrichtigungsdienst weiter.
Der Benachrichtigungsdienst sendet eine E-Mail an die Administratoren über die neue Benutzerregistrierung. 

### Anwendungsbeispiel ESB (Enterprise Service Bus)

#### Anwendung A: 
Eine E-Commerce-Plattform für Bestellungen.
#### Anwendung B:
 Ein Lagerverwaltungssystem für die Bestandsverwaltung.
#### Ablauf:
Ein Kunde tätigt eine Bestellung auf der E-Commerce-Plattform (Anwendung A).

Die E-Commerce-Plattform sendet die Bestellnachricht an den ESB.
Der ESB wandelt die Nachricht in ein für das Lagerverwaltungssystem (Anwendung B) verständliches Format um und leitet sie dorthin weiter.
Das Lagerverwaltungssystem aktualisiert den Lagerbestand und sendet eine Bestätigungsnachricht an den ESB.
Der ESB leitet die Bestätigungsnachricht zurück an die E-Commerce-Plattform.

### Anwendungsbeispiele Message Queue (Nachrichtenwarteschlange)

#### Anwendung A: Ein Flugbuchungssystem.
#### Anwendung B: 
Ein Sitzplatzbestätigungsdienst.
#### Ablauf:
Ein Kunde bucht einen Flug über das Flugbuchungssystem (Anwendung A).
Die Buchungsanfrage wird in die Message Queue gestellt.
Der Sitzplatzbestätigungsdienst (Anwendung B) überwacht die Message Queue und empfängt die Buchungsanfrage.
Der Sitzplatzbestätigungsdienst bestätigt den Sitzplatz und legt die Buchungsbestätigung in die Message Queue.
Die Buchungsbestätigung wird an das Flugbuchungssystem zurückgegeben, und der Kunde erhält eine Bestätigung
[7,17]

## Modulare Architekturen

* Modulare Architekturen in verteilten Softwaresystemen beziehen sich auf eine Designmethode, bei der das Gesamtsystem in separate, unabhängige Module oder Komponenten aufgeteilt wird. Jedes Modul erfüllt eine spezifische Funktion und ist so gestaltet, dass es eigenständig agieren kann. Diese Module sind in der Lage, miteinander zu kommunizieren und zusammenzuarbeiten, um die gewünschte Gesamtfunktionalität des verteilten Systems bereitzustellen.
#### Bsp:
Modulare Anwendungsplattformen: Einige Plattformen und Frameworks, wie das Spring Framework für Java oder die .NET-Plattform von Microsoft, verwenden modulare Architekturen. Entwickler können Module hinzufügen oder entfernen, um die Funktionalität der Plattform anzupassen. Zum Beispiel kann ein Entwickler spezifische Module für Datenbankzugriff, Sicherheit oder Webentwicklung in eine Anwendungsplattform integrieren. 

### Service oriented architecture (SOA)

* Service-Oriented Architecture (SOA) ist ein Softwareentwurfsansatz, bei dem Softwarefunktionen als eigenständige Dienste organisiert sind. Diese Dienste bieten klare Schnittstellen für den Aufruf und sind wiederverwendbar. SOA fördert die lose Kopplung zwischen Diensten, verbessert die Interoperabilität und ermöglicht die Orchestrierung von Diensten zur Erstellung komplexer Geschäftsprozesse. Zum Beispiel kann ein E-Commerce-System separate Dienste für Benutzerverwaltung, Produktkatalog, Bestellverarbeitung und Zahlungsabwicklung verwenden. Dies steigert die Flexibilität und Wiederverwendbarkeit von Softwarekomponenten in verteilten Systemen.
#### und was ist dann Service Discovery in dem Kontext? 
Service Discovery (Diensteerkennung) ist von großer Bedeutung in einer Service-Oriented Architecture (SOA) und anderen verteilten Systemen. Dieser Prozess bezieht sich darauf, wie Dienste in einem verteilten Netzwerk automatisch identifiziert und aufgefunden werden. In SOA ist Service Discovery entscheidend, um Dienste zu entdecken, auf sie zuzugreifen und sie in Anwendungen zu verwenden.
Bsp:
Ihre Anwendungen, z. B. die Bestellverwaltungsanwendung, müssen auf den Produktkatalog-Service zugreifen.
Die Anwendung kann das Service Discovery-System abfragen und nach Diensten suchen, die den Namen "ProductService" anbieten.
Das Service Discovery-System liefert die IP-Adresse "192.168.1.100" zurück, unter der der Produktkatalog-Service erreichbar ist.
[9,17]
### Microservices

* Microservices sind spezielle Module in modularen Architekturen, die häufig in einer Service-Oriented Architecture (SOA) oder einer verteilten Systemarchitektur zum Einsatz kommen. Diese Module repräsentieren eigenständige, in sich geschlossene Dienste, die spezifische Geschäftsfunktionen oder Aufgaben in einer Anwendung bereitstellen. Der Hauptfokus von Microservices liegt auf einer stark entkoppelten, dezentralen und skalierbaren Architektur.

#### Monolith vs. Distributed Monolith vs. Microservice

* Monolith: Eine einzige, zusammenhängende Anwendungseinheit.
* Distributed Monolith: Ein Monolith, bei dem Teile auf mehrere Server verteilt sind, aber die Struktur eines Monolithen beibehalten wird.
* Microservices: Eine Sammlung kleiner, unabhängiger Dienste.

##### Kommunikation

* Monolith
 Interne Kommunikation erfolgt direkt innerhalb der Anwendung, normalerweise über Funktionen oder Methodenaufrufe.
* Distributed Monolith: 
 Interne Kommunikation erfolgt in der Regel über das Netzwerk, aber die Struktur ähnelt einem Monolithen.
* Microservices: Dienste kommunizieren über definierte APIs, oft über  HTTP-REST oder Messaging-Protokolle.


##### Skalierbarkeit

* Monolith: In der Regel schwieriger zu skalieren, da die gesamte Anwendung zusammenhängt.
* Distributed Monolith: Skalierung kann auf einzelne Teile des Monolithen beschränkt sein.
* Microservices: Dienste sind unabhängig skalierbar, was eine fein abgestimmte Skalierung ermöglicht.


##### Vorteile

* Monolith
 Einfachheit: Monolithen sind oft einfacher in der Entwicklung und anfänglichen Implementierung.

* Distributed Monolith
 Ermöglicht eine begrenzte Skalierbarkeit, indem Teile des Monolithen auf verschiedene Server verteilt werden.
Erweiterbarkeit: Ermöglicht die Erweiterung eines Monolithen auf mehrere Server.

* Microservices:
 Skalierbarkeit: Bietet flexible und unabhängige Skalierbarkeit für einzelne Dienste, was in großen, stark frequentierten Anwendungen von Vorteil ist.
 Entwicklungsunabhängigkeit: Ermöglicht es verschiedenen Teams, verschiedene Dienste unabhängig voneinander zu entwickeln und bereitzustellen.
 Wiederverwendbarkeit: Dienste können in verschiedenen Anwendungen wiederverwendet werden.
 Technologische Vielfalt: Ermöglicht die Verwendung verschiedener Technologien und Frameworks für verschiedene Dienste.

[10,17]
#### Choreography Pattern vs Orchestration Pattern

Das "Choreography Pattern" und das "Orchestration Pattern" sind zwei unterschiedliche Ansätze zur Koordination von Diensten oder Komponenten in einer verteilten Softwarearchitektur

* ##### Choreography Pattern
  Das Choreography Pattern konzentriert sich auf die Interaktion und Kommunikation zwischen verschiedenen Diensten oder Komponenten in einem verteilten System. Im Rahmen dieses Musters handeln die Dienste autonom und reagieren auf Ereignisse oder Nachrichten, die von anderen Diensten gesendet werden. Die Koordination erfolgt dezentral, ohne eine zentrale Steuerungseinheit. Die Dienste sind so konzipiert, dass sie wissen, wie sie auf bestimmte Ereignisse reagieren sollen, und sie initiieren Aktionen aufgrund der empfangenen Nachrichten. Dieses Muster findet oft Anwendung in Microservices-Architekturen, in denen die Dienste eigenständig agieren und sich aufgrund von Systemereignissen anpassen.

* ##### Orchestration Pattern
 Das Orchestration Pattern konzentriert sich auf die zentrale Steuerung und Koordination von Diensten oder Komponenten in einem verteilten System. Dieses Muster beinhaltet eine zentrale Entität, die oft als Orchestrator bezeichnet wird. Der Orchestrator legt den Ablauf und die Reihenfolge der auszuführenden Aufgaben oder Dienste fest. Er definiert, wie die verschiedenen Dienste miteinander interagieren sollen und initiiert die Ausführung von Aufgaben basierend auf einem vordefinierten Workflow.

* Das Orchestration Pattern findet Anwendung in BPM (Business Process Management) und Workflow-Systemen, ebenso wie in Service-Oriented Architecture (SOA). Es wird verwendet, um komplexe Geschäftsprozesse zu steuern und zu automatisieren, wobei der Orchestrator die zentrale Figur ist, die die verschiedenen Aktivitäten koordiniert und den Prozessablauf definiert.

##### Fazit

Zusammenfassend lassen sich die Unterschiede zwischen dem Choreography Pattern und dem Orchestration Pattern wie folgt festhalten:
Das Choreography Pattern legt den Fokus auf dezentrale Interaktion und die Autonomie der Dienste.
Das Orchestration Pattern betont eine zentrale Steuerung und Koordination durch einen Orchestrator.
Trotz dieser Unterschiede haben beide Muster gemeinsame Ziele
Die Organisation und Steuerung der Zusammenarbeit und Interaktion zwischen Diensten oder Komponenten in verteilten Systemen.
Ihre Anwendbarkeit in verschiedenen Architekturkontexten, einschließlich Microservices und Service-Oriented Architecture (SOA).
Die Wahl zwischen Choreography und Orchestration hängt von den spezifischen Anforderungen eines Systems und der gewünschten Art der Steuerung ab. Choreography bietet Autonomie und Flexibilität für Dienste, während Orchestration eine genauere Kontrolle über den Ablauf von Aufgaben ermöglicht. In vielen Fällen können sie auch miteinander kombiniert werden, um komplexe Systeme zu erstellen, die sowohl die Autonomie der Dienste als auch eine zentrale Steuerung nutzen.

[11,17]
#### Service Mesh 

 Ein Service Mesh ist eine spezielle Komponente in Microservices-Architekturen. Es besteht aus einer Gruppe von Proxies, die zwischen den einzelnen Mikrodiensten in einer verteilten Anwendung platziert sind. Diese Proxies übernehmen die Verwaltung verschiedener Netzwerkaufgaben und -dienste, um die Kommunikation, Sicherheit, Zuverlässigkeit und Überwachung der Dienste in einem Microservices-System zu gewährleisten.
 Stellen Sie sich vor, Sie betreiben ein E-Commerce-System, das auf einer Microservices-Architektur basiert. In diesem System gibt es verschiedene Dienste, wie den Benutzerservice, den Produktservice und den Bestellungsservice, die miteinander interagieren müssen. Ein Service Mesh unterstützt Sie bei der Verwaltung dieser Interaktionen.
[12,17]
# Systemdesign

 Systemdesign beinhaltet architektonische Entscheidungen darüber, wie verschiedene Komponenten eines Systems interagieren und funktionieren sollten. In diesem Zusammenhang sind API-Gateway, Proxy, Reverse Proxy und Lastenausgleicher Komponenten, die unterschiedliche Zwecke in einem System erfüllen

## API Gateway vs Proxy vs Reverse Proxy vs Load Balancer

* API-Gateway 
 Verwaltet APIs, einschließlich Routen, Sicherheit und Analyse. Bietet Funktionen wie  API-Dokumentation und Versionierung. Schwerpunkt auf API-Verwaltung.

* Proxy
 Leitet Client-Anfragen an Backend-Server weiter. Kann Lastenausgleich, Caching und Sicherheit bieten, ist vielseitig einsetzbar.

* Reverse Proxy
 Verarbeitet Client-Anfragen, um sie an die richtigen Backend-Server weiterzuleiten. Fokussiert auf Sicherheit und Leistungsverbesserung.

* Lastenausgleicher
 Verteilt Datenverkehr auf Server zur Leistungssteigerung und Ausfallsicherheit. Spezialisiert auf gleichmäßige Lastenverteilung und Serverüberwachung.

Insgesamt sind diese Komponenten nicht ausschließlich voneinander getrennt und können in Kombination verwendet werden, um die Anforderungen eines bestimmten Systems zu erfüllen. Die Wahl zwischen ihnen hängt von den spezifischen Anforderungen und Zielen Ihres Projekts ab. 


## Skalierungsmuster

Ein Skaliermuster bezieht sich auf bewährte Praktiken und Techniken, die verwendet werden, um die Skalierbarkeit eines Systems zu ermöglichen oder zu verbessern. Die Skalierbarkeit eines Systems bezieht sich auf seine Fähigkeit, eine wachsende Anzahl von Benutzern, Daten oder Lasten zu bewältigen, ohne dass die Leistung erheblich beeinträchtigt wird. Skaliermuster dienen dazu, die Struktur und die Komponenten eines Systems so zu gestalten, dass es in der Lage ist, mit steigender.

### Horizontale Skalierung vs vertikale Skalierung

* Horizontale Skalierung
 Bei diesem Muster werden zusätzliche Ressourcen hinzugefügt, indem mehr Server oder Instanzen eines Dienstes bereitgestellt werden. Dies erhöht die Kapazität des Systems, indem die Last auf mehrere Ressourcen verteilt wird. Es ist besonders nützlich für Systeme, die viele parallele Anfragen verarbeiten müssen.

* Vertikale Skalierung 
 Hierbei wird die Leistungsfähigkeit einer vorhandenen Ressource durch Hinzufügen von CPU, RAM oder anderen Ressourcen erhöht. Dies ist effektiv, wenn ein einzelner Server oder eine einzelne Instanz mehr Last bewältigen muss.

Sowohl horizontale als auch vertikale Skalierung sind Skalierungsstrategien, die darauf abzielen, die Leistungsfähigkeit und Kapazität eines Systems zu erhöhen, um mehr Benutzer, Daten oder Lasten zu bewältigen.

### Replication

Replikation bedeutet das Erstellen und Pflegen von Kopien von Daten an verschiedenen Standorten oder Servern. Das Hauptziel ist, Leistung, Verfügbarkeit und Ausfallsicherheit zu verbessern. Daten werden redundant gespeichert, um Ausfallsicherheit zu erhöhen und Lasten zu verteilen. Replikation kann auch zur Reduzierung der Latenz für Benutzer in verschiedenen Regionen verwendet werden und ist entscheidend für die Skalierung und Zuverlässigkeit von Systemen.

### Partitioning und Sharding

Der Begriff "Partitioning" und "Sharding" werden oft synonym verwendet, da beide Konzepte auf die Aufteilung großer Datenmengen in kleinere Teile abzielen, um die Leistung und Skalierbarkeit zu verbessern. Der Hauptunterschied besteht im Kontext, in dem sie verwendet werden, und in den damit verbundenen Konzepten.

* Partitioning
 Partitioning bezieht sich auf das Teilen von Daten oder Ressourcen in überschaubare Teile oder Partitionen. Partitionierung kann auf der Ebene von Dateien, Datenbanktabellen oder beliebigen Ressourcen erfolgen


* Sharding
 Sharding ist ein spezifischer Begriff im Kontext von Datenbanken. Sharding bezieht sich auf die Aufteilung von Datenbankdatensätzen in separate Server oder Datenbankinstanzen (Shards) basierend auf einem Schlüsselwert, wie z. B. Benutzername oder Region. In Sharding-Szenarien müssen Mechanismen zur Synchronisation und Aufrechterhaltung der Konsistenz zwischen den Shards implementiert werden.
[14,17]

### Load Balancing

Load Balancing (Lastenausgleich) ist eine Technik im Systemdesign und in der Netzwerkarchitektur. Sie verteilt eingehenden Netzwerkverkehr oder Anfragen auf verschiedene Server oder Ressourcen, um die Last gleichmäßig zu verteilen und die Leistung, Zuverlässigkeit und Verfügbarkeit des Systems zu steigern. Der Hauptzweck des Lastenausgleichs besteht darin, sicherzustellen, dass keine einzelne Serverinstanz oder Ressource überlastet wird, während andere unterausgelastet sind. 

#### Round Robin und andere Algorithmen
 
* Round Robin
   Dieser Algorithmus verteilt den Datenverkehr gleichmäßig auf eine Liste von Servern oder Ressourcen. Jede Anfrage wird nacheinander an den nächsten Server in der Liste weitergeleitet. Nachdem der letzte Server erreicht ist, beginnt der Zyklus von vorne. Round Robin ist eine einfache und effektive Methode, berücksichtigt jedoch nicht die aktuelle Auslastung der Server. 

* Least Connections
   Bei diesem Algorithmus werden Anfragen an den Server mit der geringsten Anzahl aktiver Verbindungen weitergeleitet. Dies gewährleistet, dass weniger ausgelastete Server priorisiert werden und ist hilfreich, wenn die Server unterschiedliche Lasten aufweisen.

* IP-Hash
  Bei diesem Ansatz wird die IP-Adresse des Clients zur Ermittlung des Zielservers verwendet. Dies sorgt dafür, dass ein bestimmter Client bei wiederholten Anfragen immer zum gleichen Server weitergeleitet wird. Dies kann wichtig sein, wenn Sitzungsinformationen oder zustandsbezogene Daten auf dem Server gespeichert sind.

* Random 
 Es wird zufällig verteilt.
[15,17]
### Caching
 Caching im Kontext von Skalierungsmustern bedeutet, häufig verwendete Daten vorübergehend zu speichern, um den Zugriff zu beschleunigen und die Belastung der ursprünglichen Datenquelle zu verringern. Dies verbessert die Leistung und Skalierbarkeit von Systemen, indem wiederholte Anfragen schneller bedient werden. Caching wird häufig in Webanwendungen, Datenbanken und anderen Systemen eingesetzt, um Antwortzeiten zu optimieren und Ressourcen effizient zu nutzen.
 Es gibt verschiedene Arten von Caching, wie "lokales Caching", "CDN" und "Hierarchisches Caching" usw. Diese Ansätze beschreiben, wie das Caching im System organisiert ist

* ### Application Server Cache
  Der Application Server Cache ist ein Speicher, der in einer Webanwendung in Verbindung mit dem Anwendungsserver verwendet wird. Er speichert oft angefragte Daten im Arbeitsspeicher, um die Antwortzeiten zu beschleunigen. Bei wiederholten Anfragen werden die Daten aus dem Cache zurückgegeben. Wenn neue Anfragen auftreten, werden die Daten von der Festplatte geladen und dann in den Cache gelegt. Dies hilft, die Leistung zu verbessern.

* ### Lokales Caching
  Lokales Zwischenspeichern von Daten ist eine Technik, die verwendet wird, um den Netzwerkzugriff auf Datendateien zu beschleunigen. Dabei werden Daten, wenn möglich, auf den Client-Geräten zwischengespeichert, anstatt auf den Servern. Die Auswirkung des lokalen Zwischenspeicherns besteht darin, dass es ermöglicht, mehrere Schreibvorgänge auf demselben Bereich einer Datei zu einem einzelnen Schreibvorgang über das Netzwerk zusammenzufassen.

* ### Globales Caching 
  Wie der Name bereits sagt, handelt es sich um einen einzigen gemeinsam genutzten Cache, den alle Anwendungsknoten verwenden. Wenn die angeforderten Daten nicht im globalen Cache gefunden werden, liegt es in der Verantwortung des Caches, das fehlende Datenstück aus dem zugrunde liegenden Datenspeicher zu ermitteln.

* ### Distributed Caching
  Beim Distributed Caching wird der Cache über mehrere Server oder Knoten im Netzwerk verteilt.

* ### Hierarchisches Caching
  Hierarchical Caching beinhaltet eine Kombination aus Local und Distributed Caching in einem hierarchischen Aufbau.

* ### Content Delivery Networks
  Ein Content Delivery Network ist eine spezialisierte Form des verteilten Cachings, das auf die Bereitstellung von Inhalten, wie Bilder, Videos und Webseiten, spezialisiert ist. 

[17,18]

### Skalierungswürfel

Der Skalierungswürfel (Scale Cube) ist ein Konzept im Systemdesign von Martin Fowler, einem renommierten Softwarearchitekten. Er dient dazu, die verschiedenen Dimensionen der Skalierung zu verstehen und zu planen. Der Würfel unterteilt die Skalierung in drei Hauptdimensionen:

#### X-Achse (Horizontale Skalierung):
 Zusätzliche Instanzen oder Server werden hinzugefügt, um die Last zu verteilen, was in Cloud-Umgebungen zur Bewältigung von Lastspitzen und zur Steigerung der Ausfallsicherheit verwendet wird.
#### Y-Achse (Funktionale Aufteilung):
 Die Anwendung wird in separate Funktionen oder Dienste aufgeteilt, um die Skalierbarkeit und Wartbarkeit zu verbessern. Jeder Dienst kann unabhängig skaliert und gewartet werden.
#### Z-Achse (Datenpartitionierung):
 Daten werden in separate Partitionen aufgeteilt, um die Leistung und Skalierbarkeit der Datenverarbeitung zu steigern. Dies kann durch Sharding oder Replikation erfolgen, um große Datenmengen zu bewältigen.### Bilder
[17,19]

---

## Referenzen

[1] :https://de.wikipedia.org/wiki/IT-Architektur  

[2] :https://www.heise.de/blog/Was-ist-Architektur-4931898.html

[3] :https://www.fonial.de/wissen/begriff/client-server-modell/

[4] :https://www.linkedin.com/pulse/mpa-spa-pwa-whats-difference-how-does-work-together-marek-kubacak 

[5] :https://kinsta.com/de/blog/web-anwendungs-architektur/

[6] :https://innowise-group.com/de/blog/best-software-architecture-patterns/

[7] :https://en.wikipedia.org/wiki/Event-driven_architecture 

[8] :https://nordicapis.com/whats-the-difference-between-event-brokers-and-message-queues/

[9] :https://www.redhat.com/de/topics/integration/what-is-event-driven-architecture

[10] :https://www.sciencedirect.com/science/article/abs/pii/S0306437920300028

[11] :https://scoutapm.com/blog/distributed-monoliths-vs-microservices

[12] :https://camunda.com/blog/2023/02/orchestration-vs-choreography/

[13] :https://www.redhat.com/de/topics/microservices/what-is-a-service-mesh

[14] :https://www.designgurus.io/blog/Load-Balancer-Reverse-Proxy-API-Gateway

[15] :https://www.singlestore.com/blog/database-sharding-vs-partitioning-whats-the-difference/

[16] :https://www.enjoyalgorithms.com/blog/types-of-load-balancing-algorithms

[17] :https://chat.openai.com/

[18] :https://www.geeksforgeeks.org/caching-system-design-concept-for-beginners/

[19] :https://www.geeksforgeeks.org/the-scale-cube/

[20] :https://www.youtube.com/watch?v=MYjQWiDDdVQ&list=PLcVYkCRLcLtGHzfmkfYjdN8Ai9tkHaHvi&index=2

[21] :https://www.youtube.com/watch?v=RR_iiLYTdDM

[22] :https://www.hivenet.com/post/decentralized-or-distributed-whats-the-big-difference#:~:text=In%20a%20decentralized%20system%2C%20control,sharing%20of%20resources%20and%20workloads.