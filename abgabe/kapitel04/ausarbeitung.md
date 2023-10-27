# Kapitel 4

**Autor:** Simon Fedrau

# Lernziele

## APIs

**Was ist eine API?**

API ist die Abkürzung für „application programming interface“ und der gängige Fachbegriff für eine Programmierschnittstelle, auch Anwendungsschnittstelle genannt. Bieten Online-Dienste solche Schnittstellen an, wird häufig der Begriff „Webservices“ verwendet. [1]

**Wie funktionieren APIs?**

Mithilfe von APIs können Ihre Produkte oder Services unabhängig von ihrer Implementierung untereinander kommunizieren. Auf diese Weise lässt sich die Anwendungsentwicklung optimieren, was wiederum Zeit und Geld spart. Sie sind flexibel und vereinfachen Design, Administration und Nutzung von Anwendungen – egal ob Sie neue Tools und Produkte entwickeln oder bestehende verwalten. Obendrein schaffen sie Möglichkeiten für Innovationen.

APIs selbst bieten eine einfache Möglichkeit zur Anbindung Ihrer eigenen Infrastruktur über die Entwicklung cloudnativer Anwendungen, ermöglichen aber auch die gemeinsame Verwendung Ihrer Daten mit Kunden und anderen externen Usern. Öffentliche APIs stellen einen hohen Geschäftswert dar, denn sie vereinfachen und erweitern die Verbindung zu Ihren Partnern und sorgen zudem für eine mögliche Monetarisierung Ihrer Daten (ein gängiges Beispiel ist hier die Google Maps API).
[2]

### API vs. SDK

**Was ist eine SDK**

Ein SDK bietet eine integrierte Plattform, mit der Sie Anwendungen effizient von Grund auf neu entwickeln können. Es liefert Bausteine, die den Entwicklungsprozess verkürzen. Anstatt Code von Grund auf neu zu schreiben, können Sie ein SDK verwenden, das häufig aus Bibliotheken, Compilern, Debuggern, Codebeispielen und Dokumentation besteht. Eine integrierte Entwicklungsumgebung (IDE) ist die Softwareumgebung, die Sie verwenden, um alle im SDK enthaltenen Tools zu verbinden. 
[3] [4]

**Unterschied und Einsatzgebiete**

Ein Software Development Kit (SDK) ist eine Reihe von plattformspezifischen Entwicklungstools wie Debuggern, Compilern und Bibliotheken. SDKs stellen Tools und Ressourcen von Drittanbietern in Ihrer Umgebung bereit. Im Gegensatz dazu ist eine Anwendungsprogrammierschnittstelle (API) ein Mechanismus, der es zwei Softwarekomponenten ermöglicht, über vorgegebene Protokolle miteinander zu kommunizieren. Sie können APIs verwenden, um mit vorhandenen Softwarekomponenten zu kommunizieren und vorentwickelte Funktionen in Ihren Code zu integrieren. SDKs können APIs und mehrere andere Ressourcen für die von ihnen unterstützte Plattform enthalten. Ebenso können Sie SDKs verwenden, um neue APIs zu erstellen, die Sie mit anderen teilen können. Sowohl SDKs als auch APIs machen den Softwareentwicklungsprozess effizienter und kollaborativer.
[3] [4]


### API Styles

Anwendungsprogrammierschnittstellen (APIs) sind ein wesentliches Gestaltungselement in jeder Softwarearchitektur. Sie verbinden Komponenten digital miteinander und ermöglichen es verschiedenen Systemen und Geräten, problemlos miteinander zu kommunizieren. Wenn Entwickler eine neue API erstellen, denken sie zunächst über das API-Design nach und darüber, wie die API mit der Außenwelt interagiert, indem sie einen Stil und eine Technologie auswählen.
[5]
Im Folgenden werden fünf häufig genutzten APIs Architekturen vorgestellt.

#### Resource style

Der Ressourcenstil, wie der Name bereits andeutet, ist ressourcenorientiert. Viele der heutigen APIs verwenden diesen Stil, was leicht durch die Popularität von OpenAPI überprüft werden kann, der am weitesten verbreiteten Methode zur Beschreibung von ressourcenorientierten APIs. In diesem Stil liegt der Hauptfokus darauf, welche Ressourcen für Verbraucher freigegeben werden, damit sie mit diesen Ressourcen interagieren können. "Ressource" in diesem Kontext ist vergleichbar mit dem, was Sie beim Entwerfen einer Website für Ressourcen wie Webseiten haben würden. Die Idee von Ressourcen bietet eine gute Möglichkeit, die relevanten Aspekte der Funktionalität einer API freizulegen und gleichzeitig Implementierungsdetails hinter den Ressourcen zu verbergen. Ressourcen können für persistente Konzepte wie Produkte, Produktkategorien und Kundendaten existieren. Es können auch Ressourcen für prozessorientierte Konzepte existieren, wie beispielsweise das Bestellen von Produkten oder die Auswahl einer Versandoption.

[5] [6]

#### Hypermedia style

Der Hypermedia-Stil ermöglicht es, ähnlich wie im Web, die wichtigsten Pfade zwischen Ressourcen mithilfe von Links zwischen ihnen zu navigieren, anstatt jede Ressource individuell zu kennen und deren URI in die Adressleiste des Browsers einzugeben. Hypermedia tut dasselbe, jedoch für die Ressourcen einer API. Im Web lesen Menschen Seiten und entscheiden dann, welchem Link sie folgen möchten. Bei Hypermedia-APIs treffen Maschinen normalerweise diese Entscheidung. Das bedeutet, dass Links maschinenlesbare Bezeichnungen benötigen, damit Maschinen die verfügbaren Optionen identifizieren und eine Wahl treffen können. Diese Bezeichnungen sind konzeptionell ähnlich wie der Text eines Links, den Menschen auf Webseiten anklicken, jedoch werden die Bezeichnungen in der maschinenlesbaren Darstellung von Ressourcen dargestellt, die oft in JSON vorliegt. In einer Hypermedia-API kann man mithilfe der Links zwischen den Ressourcen "navigieren".
Allerdings kann die Benutzerfreundlichkeit des Navigierens das Risiko erhöhen, dass der Leser die Materialien überfliegt und fragmentierte Informationen erhält. Außerdem kann es, da Client und Server Daten teilen, zu "gesprächigen" APIs führen, die mehrere Interaktionen erfordern, damit der Client auf alle erforderlichen Informationen zugreifen kann.

Darüber hinaus wissen API-Nutzer oft zu Beginn nicht genau, was sie wollen, und es ist effizienter, eine Abfrage zu schreiben, um genau das zu erhalten, was sie wollen, wie es der Abfragenstil bietet.
[5] [6]

#### Query style

Der "Query Style" unterscheidet sich von den "Resource Style" und "Hypermedia Style", weil er einen einzelnen Einstiegspunkt für den Zugriff auf potenziell große Mengen von Ressourcen bereitstellt. Die Idee des Query-Stils besteht darin, dass diese Ressourcen in strukturierter Form vom API-Anbieter verwaltet werden. Diese Struktur kann abgefragt werden, und die Antwort enthält die Abfrageergebnisse. Dies ähnelt in gewisser Weise der Funktionsweise von Datenbanken, die ein zugrunde liegendes Datenmodell für die von ihnen gespeicherten Daten haben und eine Abfragesprache, die Teile dieser Daten auswählen und abrufen kann. Ein Vorteil des Query-Stils besteht darin, dass jeder Verbraucher genau das anfordern kann, was er möchte. Dies bedeutet, dass mit einer gut konstruierten Abfrage das Kombinieren von Ergebnissen, für die in Resource/Hypermedia-APIs zahlreiche Anfragen erforderlich gewesen wären, möglich ist. Beispielsweise können Sie eine einzige "Abfrage" für alles senden, was Sie benötigen, anstatt mehrere HTTP-Anfragen an verschiedene Endpunkte zu senden.

Obwohl der Query-Stil gegenüber seinen Vorteilen nur geringfügige Nachteile hat, gehört die Komplexität von Abfragen dazu. API-Nutzer müssen ein gutes Verständnis des zugrunde liegenden Daten- und Abfragemodells haben, um die Abfrage-API ordnungsgemäß zu verwenden und effiziente Anfragen zu stellen, um Rekursion oder zu viele verschachtelte Ressourcen zu vermeiden. Außerdem ist es komplizierter, einen vereinfachten Cache mit GraphQL zu implementieren als im Resource-Stil, weil REST-APIs mehrere Endpunkte haben. Sie können nativen HTTP-Caching nutzen, um das erneute Abrufen von Ressourcen zu vermeiden. Ein weiteres Problem bei GraphQL ist die Begrenzung der Anfragen, bei der festgelegt wird, "nur diese Anzahl von Anfragen ist erlaubt".

[5] [6]

#### Tunnel style

Im "Tunnel-Stil" handelt es sich bei einer API um eine Sammlung von Funktionen, die remote aufgerufen werden. APIs werden zu einer einfachen Erweiterung eines lokalen Programmierungsszenarios, bei dem alle freigegebenen Verfahren als APIs verfügbar sind. Der Tunnel-Stil ist für Entwickler praktisch, da nur minimale Anstrengungen erforderlich sind, um APIs zu erstellen.

Eine gängige Technik, die in diesem Stil verwendet wird, ist die Methode des Remote Procedure Calls (RPC). RPC ist ein Anfrage-Antwort-Protokoll, bei dem ein Client eine Anfrage an einen entfernten Server sendet, um ein bestimmtes Verfahren auszuführen, und dann vom Client eine Antwort erhält. Allerdings sind RPC-APIs viel schwieriger zu warten und zu aktualisieren als REST-APIs, weshalb RPC-APIs in der modernen API-Entwicklung nicht so häufig verwendet werden.

gRPC ist eine effiziente Implementierung des Tunnel-Stils (RPC) und eignet sich gut für verteilte Systeme. Es verfügt über SDKs für viele Sprachen und Plattformen, sodass es weitreichend für die Kommunikation zwischen Plattformen und Sprachen eingesetzt werden kann. gRPC ist schnell und effizient, da es Protocol Buffers (protobufs) zur Serialisierung und Deserialisierung verwendet, den HTTP/2-Standard für optimierte binäre Übertragungen und bidirektionales Streaming zur Vermeidung von (langen) Abfragen und blockierenden HTTP-Aufrufen.
[5] [6]

#### Event-based style

Im "Event-based Style" erstellt der API-Anbieter Ereignisse, die an die API-Nutzer übermittelt werden, anstatt dass die Nutzer etwas vom Anbieter anfordern. Anwendungen, die diese API nutzen, erwarten, über jede Änderung des Zustands eines bestimmten Datensatzes oder Datensätze in der API informiert zu werden. Es gibt viele Wege und technologische Optionen, die in Betracht gezogen werden können, wenn es darum geht, eine ereignisgesteuerte API zu implementieren. Mein Artikel "Wie man ereignisgesteuerte APIs mit Webhooks und API-Gateways erstellt" erforscht dieses Thema.

Eine andere Herangehensweise besteht darin, dass Ereigniskonsumenten sich mit einem Message-Broker verbinden, der sie von den Ereignisproduzenten entkoppelt. Der Message-Broker kümmert sich um das Management der Ereignisse, und Konsumenten müssen sich für bestimmte Ereignistypen anmelden, damit der Broker sicherstellen kann, dass Ereignisse dieses Typs an die Abonnenten ausgeliefert werden. In diesem Fall steht die Architektur im Mittelpunkt des Auslieferungs-Brokers, und alle Ereignisproduzenten und -konsumenten sind mit diesem verbunden.

Einige Nachteile bei der Wahl des eventbasierten Stils sind, dass die Implementierung im Vergleich zu anderen Stilen mehr Zeit in Anspruch nehmen kann, dass bei falscher Anwendung des Stils mehrfache doppelte Nachrichten zwischen verschiedenen Diensten ausgelöst werden können und dass Fehlerbehandlung und Problembehebung ohne Hinzufügen von Tools von Drittanbietern zur effektiven Überwachung des Ereignisflusses herausfordernd sein können. Sie können jedoch ein API-Gateway vor ereignisbasierte APIs schalten, wenn Sie moderne Anwendungen beobachten, da es eine einfache integrierte Anbindung an verschiedene Überwachungsplattformen bietet.

[5] [6]


### API Implementation Standards


  API Implementation Standards sind Leitlinien und Best Practices, die bei der Entwicklung und Umsetzung von APIs (Application Programming Interfaces) befolgt werden sollten. Diese Standards dienen dazu, die Qualität, Konsistenz, Interoperabilität und Sicherheit von APIs sicherzustellen. Hier sind einige wichtige Aspekte, die in API Implementation Standards behandelt werden:

  Konsistenz in der Benennung und Dokumentation: Einheitliche Namenskonventionen für Endpunkte, Parameter und Ressourcen erleichtern es Entwicklern, die API zu verstehen und zu nutzen. Klare und umfassende Dokumentation ist ebenfalls entscheidend, um die API-Nutzer zu unterstützen.

  Authentifizierung und Autorisierung: Standards für die sichere Authentifizierung und Autorisierung von API-Nutzern sind von entscheidender Bedeutung, um unbefugten Zugriff zu verhindern und die Datenintegrität zu gewährleisten.

  Datenschutz und Sicherheit: Die Standards können Richtlinien für den Schutz von sensiblen Daten in der API festlegen, um sicherzustellen, dass personenbezogene Informationen und andere vertrauliche Daten angemessen geschützt sind.

  HTTP-Methoden und Statuscodes: API Implementation Standards legen fest, welche HTTP-Methoden (GET, POST, PUT, DELETE usw.) in welchem Kontext verwendet werden sollten, sowie die Bedeutung von HTTP-Statuscodes (z. B. 200 OK, 404 Not Found).

  Datenformate und -modelle: Standards können definieren, welche Datenformate (z. B. JSON oder XML) verwendet werden sollten, sowie die Struktur der Datenmodelle und Schemata, die in der API verwendet werden.

  Rate Limiting und Caching: Sie können Richtlinien für die Begrenzung der Anfragen pro Zeiteinheit und für das Caching von Daten festlegen, um die Leistung der API zu verbessern und Missbrauch zu verhindern.

  Monitoring und Analyse: API Implementation Standards können Empfehlungen für das Monitoring der API-Leistung und die Analyse von Nutzungsmetriken enthalten.

  Die genauen Standards können je nach API-Entwicklungsteam, Unternehmen und Anwendungsfall variieren. Sie dienen jedoch dazu, eine konsistente und hochwertige API-Entwicklung zu fördern und die Interoperabilität zwischen verschiedenen Systemen sicherzustellen. Standards sind entscheidend, um API-Verwirrung und Inkompatibilität zu verhindern, insbesondere in der heutigen vernetzten Welt, in der APIs eine zentrale Rolle spielen.

#### Vergleich, Motivation, Vorteile, Nachteile

**Vergleich:**

  Vergleich mit individueller API-Entwicklung: API Implementation Standards bieten einen einheitlichen Ansatz für die API-Entwicklung und gewährleisten Konsistenz. Im Vergleich zur individuellen API-Entwicklung, bei der Entwickler möglicherweise eigene Konventionen und Praktiken verwenden, führen Standards zu einer höheren Qualität und besseren Wartbarkeit der APIs.
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
[8]

#### RESTful

Representational State Transfer (REST) ist eine Software-Architektur, die Bedingungen zur Funktionsweise einer API festlegt. REST wurde ursprünglich als Leitfaden zur Verwaltung der Kommunikation auf einem komplexen Netzwerk wie dem Internet erstellt. Sie können REST-basierte Architektur verwenden, um leistungsstarke zuverlässige Kommunikation nach Maß zu unterstützen. Die Architektur ist leicht implementierbar und leicht modifizierbar. Dadurch wird jedem API-System Sichtbarkeit und plattformübergreifende Portierbarkeit verliehen.

API-Entwickler können APIs mit mehreren verschiedenen Architekturen entwerfen. APIs, die dem REST-Architekturstil folgen, werden als REST-APIs bezeichnet. Webservices, die diese REST-Architektur implementieren, werden als RESTful-Webservices bezeichnet. Der Begriff RESTful-API bezieht sich im Allgemeinen auf die RESTful-Web-APIs. Jedoch können die Begriffe REST-API und RESTful-API auch als Synonyme verwendet werden.

Eine RESTful-API ist eine Schnittstelle mit der zwei Computersysteme Informationen auf sichere Weise über das Internet austauschen können. Die meisten Geschäftsanwendungen müssen mit anderen internen und externen Anwendungen kommunizieren, um verschiedene Aufgaben zu erfüllen. Um beispielsweise monatliche Gehaltsabrechnungen zu erstellen, muss Ihr internes Buchhaltungssystem Daten mit dem Banksystem Ihres Kunden austauschen, um die Rechnungsstellung zu automatisieren und mit einer internen Zeiterfassungsanwendung zu kommunizieren. RESTful-APIs unterstützen diesen Informationsaustausch, da sie sicheren, zuverlässigen und effizienten Software-Kommunikationsstandards folgen.

[9]

##### HATEOAS

HATEOAS ist ein Akronym, das für „Hypermedia as the Engine of Application State“ (dt. Hypermedia als Motor des Anwendungszustands) steht. Dieser Begriff, den Fielding im Rahmen seiner REST-Definition eingeführt hat, beschreibt eine der entscheidenden REST-Eigenschaften: Da der Architekturstil eine universelle Schnittstelle bieten soll, fordert HATEOAS nämlich, dass der REST-Client sich ausschließlich durch das Folgen von URIs (Uniform Resource Identifier) im Hypermedia-Format durch die Webanwendung bewegen kann. Wird dieses Prinzip umgesetzt, benötigt der Client abgesehen von einem grundsätzlichen Verständnis von Hypermedia keinerlei weitere Informationen, um mit der Applikation bzw. dem Server interagieren zu können.

Die Bereitstellung der einzelnen URIs erfolgt dabei beispielsweise:

in Form von href- und src-Attributen, wenn es sich um HTML-Dokumente oder -Snippets handelt
durch JSON- bzw. XML-Attribute/-Elemente, die von den jeweiligen Clients automatisch erkannt werden
Durch die Umsetzung des HATEOAS-Prinzips lässt sich die Schnittstelle eines REST-Services jederzeit anpassen, was ein wichtiger Vorteil dieser Architektur gegenüber anderen Applikationsstrukturen ist – beispielsweise gegenüber solchen, die auf Grundlage von SOAP (Simple Object Access Protocol) funktionieren.

[10] [11]

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

[12] [13] [14]


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
[15]

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

[16] [17]

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

[16] [17]

###### Backend For Frontend

Das Backends for Frontends Pattern (BFF-Muster) ist ein Designmuster für die Architektur von Mikroservices. Dieses Muster konzentriert sich auf die Trennung von API-Gateways entsprechend den spezifischen Frontend-Anwendungen. Anstatt nur ein allgemeines API-Backend zu haben, werden mehrere Backend-Services für Frontend-Anwendungen bereitgestellt, und dazwischen wird ein API-Gateway zur Handhabung von Routing und Aggregationsvorgängen platziert.

* Die Verwendung dieses Musters hilft, den sogenannten Single Point of Failure zu vermeiden. Anstatt ein komplexes API-Gateway zu haben, das ein Risiko darstellen und zum Flaschenhals in der Architektur werden könnte, werden mehrere API-Gateways erstellt, die die Client-Anwendungen entsprechend ihrer Anwendungsgrenzen gruppieren.

* Durch die Anwendung des BFF-Musters können unterschiedliche Anforderungen der Frontend-Anwendungen erfüllt werden, ohne die anderen Frontend-Anwendungen zu beeinträchtigen. Das Muster ermöglicht die Implementierung mehrerer Gateways, wodurch eine flexible Anpassung an die Bedürfnisse der Benutzeroberfläche erfolgt.

* In der Praxis bedeutet dies, dass für verschiedene Arten von Client-Anwendungen, wie mobile, Web- und Desktop-Anwendungen, separate API-Gateways erstellt werden. Jedes dieser Gateways bietet maßgeschneiderte APIs, um den spezifischen Anforderungen der jeweiligen Client-Anwendung gerecht zu werden. Zum Beispiel kann ein mobiles Frontend unterschiedliche API-Anforderungen haben, die in speziellen API-Gateway-Services implementiert werden können.

* Die Anwendung des Backends for Frontends Pattern ist besonders hilfreich in Szenarien, in denen eine Anpassung eines einzigen Backends für verschiedene Benutzeroberflächen vermieden werden soll.

Insgesamt ermöglicht das BFF-Muster eine effiziente und flexible Gestaltung von APIs, die auf die Bedürfnisse der Frontend-Umgebungen zugeschnitten sind. Es bietet eine klare Richtlinie für die Implementierung mehrerer Gateways, um den Anforderungen verschiedener Client-Anwendungen gerecht zu werden.

[18]


#### API Design

API-Design bezieht sich auf die Gestaltung von Schnittstellen, über die Softwarekomponenten miteinander kommunizieren. Eine gut gestaltete API sollte benutzerfreundlich, konsistent, effizient, sicher, und gut dokumentiert sein. Sie sollte auch flexibel, testbar und gut überwachbar sein. Ein gutes API-Design ist entscheidend, um die Nutzung und Integration von Software zu erleichtern.

###### Code First vs Design First

* Es gibt zwei Hauptansätze zur Entwicklung von APIs: 
Der Code-First-Ansatz, bei dem der Code nach Festlegung der Geschäftsanforderungen entwickelt wird, und die Dokumentation aus dem Code generiert wird. 
Der Design-First-Ansatz hingegen legt den Fokus darauf, den API-Vertrag zuerst zu entwerfen, bevor der Code geschrieben wird. Dieser Ansatz verwendet häufig das OpenAPI-Format, um menschen- und maschinenlesbare Verträge zu erstellen, bevor die eigentliche Entwicklung beginnt.
[19]


**Dieses Thema muss überrarbeiet werden** 

* Design First
Beim Design-First-Ansatz wird die API zuerst geplant und spezifiziert, bevor der eigentliche Programmcode geschrieben wird. Dies bedeutet, dass zuerst die Struktur, das Verhalten und die Dokumentation der API festgelegt werden, oft mit Hilfe von Design-Tools wie Swagger. Erst danach beginnt die eigentliche Entwicklung des Codes, basierend auf diesem Design. Dieser Ansatz legt den Fokus auf eine klare und sorgfältige Gestaltung der API, bevor die Umsetzung beginnt.

* Code First 
Der Code-First-Ansatz ist eine Methode zur Entwicklung von APIs, bei der die Implementierung des API-Codes zuerst geschrieben wird, bevor die API-Spezifikation entworfen wird. Dies bedeutet, dass die API auf Grundlage des vorhandenen Codebasis gestaltet wird.

Die Vorteile dieses Ansatzes sind ein besseres Verständnis der Funktionalität und des Verhaltens der API sowie eine effizientere Entwicklung. Entwickler können direkt mit der tatsächlichen Implementierung arbeiten und Anpassungen in Echtzeit vornehmen. Dies ist besonders nützlich für kleinere oder einfachere Projekte und in Fällen, in denen Anforderungen nicht gut definiert sind oder häufig ändern.

Nachteile des Code-First-Ansatzes :Der Code-First-Ansatz kann zu mangelnder Dokumentation und Standardisierung führen, da es keine klare API-Spezifikation gibt. Das kann zu Verwirrung und Ineffizienz führen.

Vorteile des Code-First-Ansatzes :Der Code-First-Ansatz kann zu schnellere Entwicklung, einfache Iteration, direkte Kontrolle über die Implementierung und nahtlose Integration mit vorhandenem Code. Nachteile sind mangelnde Dokumentation, erhöhte Abhängigkeit vom Codebasis und begrenzte Designflexibilität.

* Code First vs Design First

Der Code-First-Ansatz beginnt mit dem Schreiben des API-Codes und bietet schnellere Entwicklung und direkte Kontrolle. Allerdings fehlt eine klare Spezifikation und umfassende Dokumentation, was zu Problemen führen kann.

Der Design-First-Ansatz legt die API-Spezifikation zuerst fest, was zu besserer Benutzerfreundlichkeit, kürzerer Entwicklungszeit und verbesserter Dokumentation führt. Allerdings kann er die Flexibilität einschränken und erfordert spezialisierte Designwerkzeuge.


#### API Versioning

API-Versionierung ist ein Konzept in der Softwareentwicklung, das bei der Veröffentlichung von APIs verwendet wird. Es bezieht sich auf die Verwaltung und Aktualisierung von APIs über die Zeit, um sicherzustellen, dass bestehende Anwendungen, die die API verwenden, weiterhin korrekt funktionieren, während gleichzeitig neue Funktionen hinzugefügt oder bestehende verbessert werden.

Es gibt verschiedene Ansätze zur API-Versionierung:

* URI-Versionierung: Hier wird die Versionsnummer in der URL der API angegeben, z.B. https://api.example.com/v1/resource. Dies ermöglicht es, verschiedene Versionen der API parallel zu betreiben.

* Header-Versionierung: Die Version wird im HTTP-Header der Anfrage oder Antwort angegeben, um die Version der API zu identifizieren. Dies kann nützlich sein, wenn die Versionsnummer nicht in der URL erscheinen soll.

* Media-Type-Versionierung: Die Version wird im Media Type (z.B., application/vnd.example.v1+json) angegeben, um die Darstellung der API-Ressource zu kennzeichnen.

* Accept-Version Header: Dies ist eine Erweiterung von Header-Versionierung, bei der der Client mit dem Accept-Version-Header angibt, welche Version der API er verwenden möchte.

API-Versionierung ist wichtig, um die Abwärtskompatibilität zu wahren, bestehende Benutzer nicht zu beeinträchtigen und gleichzeitig Raum für Weiterentwicklung zu schaffen. Die Wahl des Versionierungsansatzes hängt von den Anforderungen des Projekts und den Präferenzen des Entwicklungsteams ab.

[20] [21]

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
[22]

###### Spezifikation / Dokumentation

#### OpenAPI

OpenAPI ist ein Standard zur Beschreibung von APIs. Die OpenAPI-Spezifikation definiert ein offenes und herstellerneutrales Beschreibungsformat für API-Dienste. Insbesondere lassen sich mithilfe von OpenAPI REST-konforme APIs beschreiben, entwickeln, testen und dokumentieren.

Im Gegensatz zu JSON Schema handelt es sich bei einem OpenAPI-Dokument um eine Definition für eine komplette API und nicht nur um Datenmodelle. Vor der Einführung von OpenAPI wurden viele APIs entworfen, ohne die Möglichkeit, wie sie funktionieren sollten, oder die Möglichkeit zur Überprüfung, ob sie wie erwartet arbeiten. Mit dieser maschinenlesbaren Beschreibung können auch nützliche Tools für Menschen generiert werden, wie beispielsweise Dokumentation und Mock-Server.

Man kann das JSON Schema verwenden, um Datenobjekte für Anfragen und Antworten zu beschreiben. OpenAPI geht jedoch über die Formatierung dieser Anfragen und Antworten hinaus und beinhaltet auch, wie sie strukturiert sein sollten. Ähnlich kannst du API-Antworten mit JSON Schema nachahmen, aber du benötigst etwas wie OpenAPI, um einen vollständigen Mock-Server zu generieren.

OpenAPI ist also ein leistungsstarkes Werkzeug, um APIs umfassend zu beschreiben, von ihren Endpunkten über Datenmodelle bis hin zur Formatierung von Anfragen und Antworten. Dies erleichtert nicht nur die Entwicklung von APIs, sondern ermöglicht auch die Generierung von Dokumentation und Mock-Servern, die bei der Entwicklung und dem Test von APIs äußerst hilfreich sind.

[23] [24]

###### JSON Schema

JSON Schema ist ein Werkzeug zur Beschreibung von JSON-Dokumenten und deren Struktur. Es handelt sich nicht um eine Datenbank oder ein JSON-Dokument selbst, sondern um eine Vorlage oder eine Schablone für die Struktur von JSON-Daten.

Ein Schema dient dazu, wie Daten strukturiert sein sollten. Es bietet den Vorteil, dass Teams die Struktur ihrer Daten planen und überarbeiten können, bevor sie diese tatsächlich erstellen. Durch die Festlegung von Formaten können Teams effizienter zusammenarbeiten und Fehler vermeiden. Zum Beispiel können Client- und Server-Teams Feedback austauschen und Anwendungsfälle testen, ohne eine vollständige API mit Live-Daten zu benötigen.

JSON Schema wird häufig in Verbindung mit APIs verwendet, aber es kann auch in anderen Kontexten nützlich sein. Es beschreibt ausschließlich die Struktur der Daten in einem JSON-Dokument. JSON Schema kann auch dazu verwendet werden, Datenbanken in wiederverwendbare Blöcke zu strukturieren, um die Effizienz und Handhabbarkeit zu steigern. Überall dort, wo JSON-Daten auf Übereinstimmung mit einem festgelegten Muster geprüft werden müssen, kann JSON Schema hilfreich sein.

JSON Schema ermöglicht also die Definition von Regeln und Mustern, nach denen JSON-Daten validiert werden können. Dies ist besonders nützlich in der Entwicklung von APIs und anderen Anwendungen, bei denen die Struktur von JSON-Daten von großer Bedeutung ist.
[24]

## Referenzen

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


