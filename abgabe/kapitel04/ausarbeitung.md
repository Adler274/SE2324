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
Allerdings kann die Benutzerfreundlichkeit des Navigierens das Risiko erhöhen, dass der Leser die Materialien überfliegt und fragmentierte Informationen erhält. Außerdem kann es, da Client und Server Daten teilen, zu "gesprächigen" APIs führen, die mehrere Interaktionen erfordern, damit der Client auf alle erforderlichen Informationen zugreifen kann. Was ist, wenn API-Endpunkte von verschiedenen Backend-Diensten (Microservices und serverlosen APIs) bereitgestellt werden? Dies kann durch die Nutzung eines API-Gateways mit Funktionen zur Aggregation und Komposition von Antworten gelöst werden.

Darüber hinaus wissen API-Nutzer oft zu Beginn nicht genau, was sie wollen, und es ist effizienter, eine Abfrage zu schreiben, um genau das zu erhalten, was sie wollen, wie es der Abfragenstil bietet.
[5] [6]

#### Query style

Der "Query Style" unterscheidet sich von den "Resource Style" und "Hypermedia Style", weil er einen einzelnen Einstiegspunkt für den Zugriff auf potenziell große Mengen von Ressourcen bereitstellt. Die Idee des Query-Stils besteht darin, dass diese Ressourcen in strukturierter Form vom API-Anbieter verwaltet werden. Diese Struktur kann abgefragt werden, und die Antwort enthält die Abfrageergebnisse. Dies ähnelt in gewisser Weise der Funktionsweise von Datenbanken, die ein zugrunde liegendes Datenmodell für die von ihnen gespeicherten Daten haben und eine Abfragesprache, die Teile dieser Daten auswählen und abrufen kann. Ein Vorteil des Query-Stils besteht darin, dass jeder Verbraucher genau das anfordern kann, was er möchte. Dies bedeutet, dass mit einer gut konstruierten Abfrage das Kombinieren von Ergebnissen, für die in Resource/Hypermedia-APIs zahlreiche Anfragen erforderlich gewesen wären, möglich ist. Beispielsweise können Sie eine einzige "Abfrage" für alles senden, was Sie benötigen, anstatt mehrere HTTP-Anfragen an verschiedene Endpunkte zu senden.

Im Query-Stil ist es wahrscheinlich fair zu sagen, dass GraphQL die beliebteste Wahl für die Entwicklung von Single-Page-Anwendungen (SPAs) ist. Es handelt sich um eine Abfragesprache für Datenbanken aus clientseitigen Anwendungen. Ein großer Vorteil von GraphQL ist, dass es in ein auf JSON basierendes Ökosystem integriert ist. Obwohl GraphQL JSON nicht für Abfragen verwendet, liefert es Ergebnisse in JSON, was die Verarbeitung in auf JSON fokussierten Umgebungen erleichtert.

Obwohl der Query-Stil gegenüber seinen Vorteilen nur geringfügige Nachteile hat, gehört die Komplexität von Abfragen dazu. API-Nutzer müssen ein gutes Verständnis des zugrunde liegenden Daten- und Abfragemodells haben, um die Abfrage-API ordnungsgemäß zu verwenden und effiziente Anfragen zu stellen, um Rekursion oder zu viele verschachtelte Ressourcen zu vermeiden. Außerdem ist es komplizierter, einen vereinfachten Cache mit GraphQL zu implementieren als im Resource-Stil, weil REST-APIs mehrere Endpunkte haben. Sie können nativen HTTP-Caching nutzen, um das erneute Abrufen von Ressourcen zu vermeiden. Ein weiteres Problem bei GraphQL ist die Begrenzung der Anfragen, bei der festgelegt wird, "nur diese Anzahl von Anfragen ist erlaubt".

[5] [6]

#### Tunnel style

Im "Tunnel-Stil" handelt es sich bei einer API um eine Sammlung von Funktionen, die remote aufgerufen werden. APIs werden zu einer einfachen Erweiterung eines lokalen Programmierungsszenarios, bei dem alle freigegebenen Verfahren als APIs verfügbar sind. Der Tunnel-Stil ist für Entwickler praktisch, da nur minimale Anstrengungen erforderlich sind, um APIs zu erstellen.

Eine gängige Technik, die in diesem Stil verwendet wird, ist die Methode des Remote Procedure Calls (RPC). RPC ist ein Anfrage-Antwort-Protokoll, bei dem ein Client eine Anfrage an einen entfernten Server sendet, um ein bestimmtes Verfahren auszuführen, und dann vom Client eine Antwort erhält. Allerdings sind RPC-APIs viel schwieriger zu warten und zu aktualisieren als REST-APIs, weshalb RPC-APIs in der modernen API-Entwicklung nicht so häufig verwendet werden.

gRPC ist eine effiziente Implementierung des Tunnel-Stils (RPC) und eignet sich gut für verteilte Systeme. Es verfügt über SDKs für viele Sprachen und Plattformen, sodass es weitreichend für die Kommunikation zwischen Plattformen und Sprachen eingesetzt werden kann. gRPC ist schnell und effizient, da es Protocol Buffers (protobufs) zur Serialisierung und Deserialisierung verwendet, den HTTP/2-Standard für optimierte binäre Übertragungen und bidirektionales Streaming zur Vermeidung von (langen) Abfragen und blockierenden HTTP-Aufrufen.

Tools können Verfahren als APIs freigeben, wobei ein Großteil der Aufgabe, "die API zu erstellen", automatisiert werden kann. Es sollte jedoch immer eine Managementebene zur Sicherung der APIs geben. Dies kann durch die Verwendung einer Komponente wie einem API-Gateway und dessen gRPC-Proxyfunktion zur Konvertierung von Payloads von einem Format in ein anderes über denselben Transport (von REST zu gRPC oder umgekehrt) adressiert werden, wenn im System verschiedene API-Protokolle verwendet werden.

[5] [6]

#### Event-based style

Im "Event-based Style" erstellt der API-Anbieter Ereignisse, die an die API-Nutzer übermittelt werden, anstatt dass die Nutzer etwas vom Anbieter anfordern. Anwendungen, die diese API nutzen, erwarten, über jede Änderung des Zustands eines bestimmten Datensatzes oder Datensätze in der API informiert zu werden. Es gibt viele Wege und technologische Optionen, die in Betracht gezogen werden können, wenn es darum geht, eine ereignisgesteuerte API zu implementieren. Mein Artikel "Wie man ereignisgesteuerte APIs mit Webhooks und API-Gateways erstellt" erforscht dieses Thema.

Eine andere Herangehensweise besteht darin, dass Ereigniskonsumenten sich mit einem Message-Broker verbinden, der sie von den Ereignisproduzenten entkoppelt. Der Message-Broker kümmert sich um das Management der Ereignisse, und Konsumenten müssen sich für bestimmte Ereignistypen anmelden, damit der Broker sicherstellen kann, dass Ereignisse dieses Typs an die Abonnenten ausgeliefert werden. In diesem Fall steht die Architektur im Mittelpunkt des Auslieferungs-Brokers, und alle Ereignisproduzenten und -konsumenten sind mit diesem verbunden. In diesem Zusammenhang ist eine geeignete Technologie Apache Kafka, das hochskalierbar und robust ist.

Einige Nachteile bei der Wahl des eventbasierten Stils sind, dass die Implementierung im Vergleich zu anderen Stilen mehr Zeit in Anspruch nehmen kann, dass bei falscher Anwendung des Stils mehrfache doppelte Nachrichten zwischen verschiedenen Diensten ausgelöst werden können und dass Fehlerbehandlung und Problembehebung ohne Hinzufügen von Tools von Drittanbietern zur effektiven Überwachung des Ereignisflusses herausfordernd sein können. Sie können jedoch ein API-Gateway vor ereignisbasierte APIs schalten, wenn Sie moderne Anwendungen beobachten, da es eine einfache integrierte Anbindung an verschiedene Überwachungsplattformen bietet.

[5] [6]


### API Implementation Standards


  API Implementation Standards sind Leitlinien und Best Practices, die bei der Entwicklung und Umsetzung von APIs (Application Programming Interfaces) befolgt werden sollten. Diese Standards dienen dazu, die Qualität, Konsistenz, Interoperabilität und Sicherheit von APIs sicherzustellen. Hier sind einige wichtige Aspekte, die in API Implementation Standards behandelt werden:

  Konsistenz in der Benennung und Dokumentation: Einheitliche Namenskonventionen für Endpunkte, Parameter und Ressourcen erleichtern es Entwicklern, die API zu verstehen und zu nutzen. Klare und umfassende Dokumentation ist ebenfalls entscheidend, um die API-Nutzer zu unterstützen.

  Versionierung: Die Möglichkeit zur Versionierung einer API ist wichtig, um Änderungen oder Aktualisierungen vorzunehmen, ohne bestehende Anwendungen zu unterbrechen. API Implementation Standards können Regeln für die Versionierung von APIs festlegen.

  Authentifizierung und Autorisierung: Standards für die sichere Authentifizierung und Autorisierung von API-Nutzern sind von entscheidender Bedeutung, um unbefugten Zugriff zu verhindern und die Datenintegrität zu gewährleisten.

  Datenschutz und Sicherheit: Die Standards können Richtlinien für den Schutz von sensiblen Daten in der API festlegen, um sicherzustellen, dass personenbezogene Informationen und andere vertrauliche Daten angemessen geschützt sind.

  HTTP-Methoden und Statuscodes: API Implementation Standards legen fest, welche HTTP-Methoden (GET, POST, PUT, DELETE usw.) in welchem Kontext verwendet werden sollten, sowie die Bedeutung von HTTP-Statuscodes (z. B. 200 OK, 404 Not Found).

  Datenformate und -modelle: Standards können definieren, welche Datenformate (z. B. JSON oder XML) verwendet werden sollten, sowie die Struktur der Datenmodelle und Schemata, die in der API verwendet werden.

  Rate Limiting und Caching: Sie können Richtlinien für die Begrenzung der Anfragen pro Zeiteinheit und für das Caching von Daten festlegen, um die Leistung der API zu verbessern und Missbrauch zu verhindern.

  Testen und Fehlerbehandlung: Die Standards können Anforderungen für das Testen der API und die Behandlung von Fehlern festlegen, um sicherzustellen, dass die API zuverlässig funktioniert.

  Monitoring und Analyse: API Implementation Standards können Empfehlungen für das Monitoring der API-Leistung und die Analyse von Nutzungsmetriken enthalten.

  HATEOAS und Hypermedia: Wenn der Hypermedia- oder HATEOAS-Ansatz verwendet wird, können Standards die Struktur der Hypermedia-Links und deren Verwendung festlegen.

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





### Bilder



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




