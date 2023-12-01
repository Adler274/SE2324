# Kapitel 9

**Autor:** Simon Fedrau, Sascha Hahn

## Lernziele
* Softwaresysteme
  * Systeme
  * Systemeigenschaften
  * Systemstrukturen
  * Systems-Thinking (Systemdenken)
  * Softwaresysteme
  * Qualitätsmerkmale von Softwaresystemen
  * Metriken zur Messung von Softwarequalität
  * Modelierung/Visualisierung von Softwaresystemen
  * UML und Arten von Diagrammen und deren Anwendung


## Softwaresysteme

Ein Softwaresystem ist eine Verbindung von miteinander kommunizierenden Komponenten (Bausteinen) auf Softwarebasis, die das Zusammenwirken von Teilen eines Computersystems (eine Kombination aus Hardware und Software) ermöglichen.

Es besteht aus einer Reihe von separaten Hauptprogrammen, Unterprogrammen und Konfigurationsdateien (Module) die zur Einrichtung von Programmen (welche die Struktur des Systems ermöglichen) sowie einer Anwender-Dokumentation (die erklärt wie das System zu benutzen ist) notwendig sind. Während ein Computerprogramm eine Vielzahl von Anweisungen (Quellen- oder Objektcodes) beinhaltet, verfügt ein Softwaresystem über weitere Komponenten wie zum Beispiel Spezifikationen, Testergebnisse, Endbenutzer-Dokumentationen und Instandhaltung. 

[1a]


### Systeme

Ein "System“ ist eine integrierte Lösung für ein organisatorisches Problem. Daher können Sie die Software, Anwendung oder das Tool nicht als System bezeichnen. Beispielsweise ist ein System ein Satz miteinander verbundener Komponenten (Module, Subsysteme usw.), die zusammenarbeiten, um ein zusammenhängendes Ganzes zu bilden. Besonders wenn das Ergebnis der Operation oder Funktionen des Ganzen mehr ist als die Summe der Teile, nennen wir es ein System. Wenn sie zum Erreichen des gewünschten Ergebnisses benötigt werden, sind auch Mitarbeiter, Handbücher und Geschäftsprozesse Teil des Systems. Ein System impliziert oft ein viel größeres Ganzes und bezieht sich oft auf die Hardware und die Software als Ganzes. Separat spricht man oft von einem Hardwaresystem oder einem Softwaresystem.

[3a]

#### Sozioökonomische Systeme

In der heutigen vernetzten Welt erfolgt nahezu alles online, von der Informationsbeschaffung über den Handel bis hin zu Dienstleistungen, basierend auf entsprechenden Informatiksystemen. Diese digitalen Plattformen bringen jedoch faszinierende Herausforderungen mit sich, die das Zusammentreffen von Angebot und Nachfrage in der virtuellen Sphäre aufwerfen. Fragen wie die Funktionsweise elektronischer Märkte, die Balance zwischen Informationen von Anbietern und Nutzern, die Gestaltung effizienter Online-Auktionen sowie die Verhinderung von Manipulationen und einseitigen Informationsnachteilen stehen im Mittelpunkt dieser Entwicklungen.

[2a]

#### Technische Systeme

Ein technisches System ist ein System, das schlicht und einfach technisch ist. Es ist von Menschen auf technische Weise geschaffen. Ein technisches System ist also eine spezielle Art von System. Zudem kann ein technisches System Teil eines weiteren technischen oder nicht-technischen Systems sein. Das technische System Motor ist Teil des technischen Systems Auto. Und das Auto ist Teil des nur teilweise technischen Verkehrssystems.

„Technische Systeme lassen sich ohne Softwaresysteme nicht nutzen.“ Ein Fahrrad ist ein technisches System. Software braucht es aber nicht. Umgekehrt kann man aber ein Softwaresystem nur nutzen, wenn aus auf einer Hardwareplattform läuft. Diese Hardwareplattform ist ein technisches System. Wie das Softwaresystem im Übrigen auch.

[4a]

#### Natürliche Systeme

Natürliche Systeme, das sind Systeme aus der Natur, stellen einerseits eine potentielle Quelle für neuartige Algorithmen bzw. Anwendungen in der Technik dar, andererseits ist ein Erforschen dieser Systeme notwendig, um die Folgen von Eingriffen abschätzen zu können. Für das Erforschen werden Simulationssysteme, die auf Multi-Agenten-Technik bzw. Methoden der Verteilten Künstlichen Intelligenz basieren, verwendet, um die Zugangsschwelle zu senken und somit einen erweiterten Anwenderkreis zu erreichen. Verfügbare Simulationssysteme können hinsichtlich des Simulationsmodells verbessert werden, so dass diese früh im Kontext schulischer Anwendung zur Förderung des systemischen Denkens anwendbar wären.

[5a]


### Systemeigenschaften

Unter den Systemeigenschaften versteht man einen Satz von Eigenschaften, die für ein System charakteristisch sind. Sie ergeben sich zum einen aus den Eigenschaften der Elemente des Systems und zum anderen aus der Systemstruktur, also ihren Beziehungen untereinander

[6a]

#### Komplizierte vs. komplexe Systeme

  * **Komplizierte Systeme**
    * In einem komplizierten System gibt es eindeutig definierte Verbindungen der einzelnen Elemente. Es mag ein sehr großes System sein, das unser Können und unsere Kenntnisse übersteigt, zum Beispiel ein ICE mit all seinen Drähten und Bauteilen. Doch alle Zusammenhänge darin sind kausal; Ursache-Wirkung – und können vorhergesagt werden. 

  [7a]

  * **Komplexe Systeme**

    * In einem komplexen System sieht das anders aus. Es ist lebendig und seine Ursache-Wirkungszusammenhänge sind unüberschaubar. Komplexe Organisationen nehmen durch Offenheit zu ihrem Umfeld Informationen auf und entwickeln sich daran angelehnt autonom weiter. Das heißt nicht unbedingt, dass für uns komplexe Systeme immer anspruchsvoller sein müssen. Aber dass wir lernen müssen, in unserer digitalisierten VUCA-Welt durch das Nicht-Lineare, Ergebnisoffene und Unvohersehbare zu navigieren.

  [7a]

#### Adaptive Systeme

Adaptive System passen sich den Veränderungen ihrer Umgebung an. Sie ermöglichen es aus Daten und Fakten der Vergangenheit Informationen zu destillieren, Muster zu erkennen und Schlüsse für die Zukunft zu ziehen. Sie bedienen sich hierzu Algorithmen der Künstlichen Intelligenz (KI) und bilden Wahrnehmungsfolgen auf mögliche, sinnvolle Aktionen ab. 

[8a]

#### Lernende Systeme

Ein lernendes System ist ein System, welches sich auf Einflüsse der Außenwelt einstellen kann und sich anpasst. Ein System ist dabei die Gesamtheit von einzelnen Elementen, die aufeinander bezogen sind und miteinander wechselwirken.

Ein lernendes System ist ein offenes System, das seine Eigenschaften aufgrund seiner Interaktion mit der Außenwelt selbstständig modifizieren kann.

[9a]

#### Dynamische Systeme

Ein dynamisches System ist eine abgegrenzte zeitabhängige Funktionseinheit, die durch ihre Signaleingänge und Signalausgänge in einer Wechselwirkung mit der Umwelt steht. Das System kann beispielsweise ein mechanisches Gebilde, ein elektrisches Netzwerk, aber auch ein biologischer Vorgang oder ein Bestandteil der Volkswirtschaft sein.

Das System hat mindestens einen Signaleingang und einen Signalausgang und reagiert zu einem bestimmten Zeitpunkt auf ein beliebiges Eingangssignal mit einer bestimmten zeitlichen Reaktion auf das Ausgangssignal. Die in dem System enthaltenen Energiespeicher als Ursache des Zeitverhaltens können je nach Beobachtungszeitpunkt gewollt oder ungewollt einen Systemzustand ≠ 0 im Zustandsraum einnehmen, bei dem sich die Wirkung des Eingangssignals mit dem Systemverhalten und dem Systemzustand auf das Systemausgangssignal überlagert. 

[10a]

#### Selektive Systeme

Selektivität ist ein Maß, das in der Informatik bei Datenbankabfragen auf Datenbanktabellen in relationalen Datenbankensystemen gebraucht wird; sie bestimmt den Anteil der Datensätze, die bei einer Abfrage nicht durch eine Selektionsbedingung aus der Ergebnismenge ausgefiltert werden, relativ zur Gesamtzahl der Datensätze des Datenbestandes, welcher der Abfrage zugrunde liegt. Bei der am weitesten verbreiteten Abfragesprache für relationale Datenbanken, SQL, werden Selektionsbedingungen in der WHERE-Klausel der Abfrage spezifiziert. 


[11a]

### Systemstrukturen

Unter der Struktur versteht man in der Systemtheorie die Gesamtheit der Elemente eines Systems sowie ihre Funktion(en) und Wechselbeziehungen auf der Mikroebene, Makroebene und Mesoebene. Systemstruktur, Systemverhalten und Systementwicklung bedingen sich gegenseitig

[12a]


#### System, Subsystem, Supersystem, Kontext, Umgebung, Grenze, Eingabe, Ausgabe



* **System**




* **Subsystem und Supersystem:**
  * Ein System kann Teilsysteme (Subsysteme) enthalten und selbst Teil eines umfassenderen Systems (Supersystem) sein.

[13a]


* **Supersystem**

Ein Supersystem ist ein System, das andere Systeme umfasst oder enthält, und es steht in einer hierarchischen Beziehung zu diesen Unter- oder Teilsystemen. Die Struktur und Hierarchie von Systemen können auf verschiedene Weisen dargestellt werden, darunter Subsysteme, Komponenten und eben auch Supersysteme.


* **Kontext**

Der "Kontext" in einer Systemstruktur bezieht sich auf die Umgebung oder den Rahmen, in dem ein bestimmtes System existiert, funktioniert oder betrachtet wird. Es bezieht sich darauf, wie das System mit seiner äußeren Umgebung interagiert, welche Einflüsse es erhält und welche Auswirkungen es auf seine Umgebung hat. Der Kontext ist entscheidend, um das Verständnis für die Funktionsweise und Bedeutung eines Systems zu vertiefen.

* **Umgebung**

In der Kontextualisierung von Systemen ist die "Umgebung" der äußere Bereich oder das äußere System, das das betrachtete System beeinflusst und von diesem beeinflusst wird. Die Umgebung enthält alle externen Elemente, die für das Verständnis des Systems und seiner Funktionsweise relevant sind. Das Verständnis der Umgebung ist entscheidend, um die Interaktionen und Beziehungen zwischen dem betrachteten System und seiner äußeren Welt zu verstehen.


* **Grenze**

In einer Systemstruktur bezieht sich die "Grenze" auf die definierende Linie zwischen dem betrachteten System und seiner Umgebung. Es ist die Trennlinie, die angibt, was zum System gehört und was nicht. Die Festlegung der Grenzen eines Systems ist entscheidend, um den Fokus auf die relevanten Aspekte zu legen und die Interaktionen mit der Umgebung zu verstehen.


* **Eingabe**

Eingabe bezieht sich auf alle Informationen, Daten oder Signale, die vom System oder von externen Quellen in das System hineingehen. Diese Eingaben können verschiedene Formen annehmen, darunter Benutzereingaben, Sensorinformationen, Daten von anderen Systemen oder externe Ereignisse.



* **Ausgabe**

Ausgabe bezieht sich auf alle Informationen, Daten oder Signale, die vom System an seine Umgebung oder an andere Systeme weitergegeben werden. Dies können Berechnungsergebnisse, Statusberichte, Benachrichtigungen, Steuersignale oder andere Arten von Informationen sein.



#### Systems-Thinking (Systemdenken)

Systemdenken (engl. Systems Thinking)  ist ein ganzheitlicher Analyseansatz, um das Verhalten dynamischer und komplexer Systeme zu erklären und zu optimieren. Dabei erklärt Systemdenken , wie Bestandteile eines Systems miteinander in Beziehung stehen und bildet darauf aufbauend Hypothesen über die Funktionsweisen des Systems.

[14a]


Systemdenken bedeutet, eine weitgehend beliebige Art von Phänomen zu untersuchen und gegebenenfalls zu erklären, indem der Versuch unternommen wird, das besagte Phänomen in einem Systemmodell zu erfassen: Ein komplexes Set von Wechselwirkungen wird – oft unter Einbeziehung von Subsystemen, alle innerhalb eines Systems – modelliert (oder als Subsystem im Modell angedacht, jedoch wegen Irrelevanz reduziert). Voraussetzung dafür ist, dass das besagte Phänomen überhaupt modellierbar ist. Andererseits ist es aber auch möglich, mit dem fertigen Modell eines Phänomens zu beginnen oder auch nur ein Teilmodell zu erarbeiten und darauf Systemdenken anzuwenden. In besonderen Szenarien kann Systemdenken das Erfordernis beinhalten, logische, mathematische, technische oder philosophische Paradigmen und Rahmen zu entwickeln, in denen physikalische, technologische, biologische, soziale, kognitive oder metaphysische Phänomene systemisch analysiert und ihr Systemverhalten zu deuten und zu erklären versucht wird (insbesondere dann, wenn Modellwissen dafür noch nicht ausgearbeitet zur Verfügung steht). 

[15a]

####  Vernetzung, Synthese, Emergenz, Feedbackschleifen, Kausalität und Systemabbildung

* **Vernetzung**
  Das Grundprinzip des Umdenkens, das mit Systems Thinking einher geht, ist das alles miteinander verbunden ist und wir dadurch viele Schnittstellen zwischen den Elementen innerhalb und außerhalb unseres Systems haben. 

  Bedeutet: statt alles losgelöst voneinander zu betrachten, trete einen Schritt zurück und betrachte wie sich die Aktionen gegenseitig beeinflussen und wie alles zusammenhängt. 

  Die „Vogelperspektive“ kann einen spannenden Effekt haben.  

* **Synthese**
  Im Grunde bezieht sich die Synthese auf die Kombination von zwei oder mehr Dingen, um innerhalb einer bewusst gewählten Systemgrenze etwas Neues zu schaffen. 

  Eine Analyse der Einzelteile allein reicht nicht aus, um Systeme zu verstehen. Es braucht einen ganzheitlichen Ansatz, um sowohl die Teile als auch das Ganze zu betrachten. Dazu benötigen wir die Synthese. 

  Im Wesentlichen schafft Synthese erst die Möglichkeit die Zusammenhänge des Systems zu erkennen.



* **Emergenz:**
  Von Emergenz spricht man, wenn Teile zusammenwirken und dadurch Eigenschaften auf ein ganzes System zuzuschreiben sind statt nur auf einzelne Teile des Systems. 

  Dahinter liegt das Konzept, dass im Zusammenspiel mehr erreicht werden kann als durch eine isolierte Vorgehensweise in Silos. 

  Betrachtet man die Emergenz in der Systemdefinition, kann man feststellen, dass ein System mehr ist, als nur die Summe seiner Teile.  

  Schaffen wir es innerhalb einer Struktur Synergien zwischen einzelnen Elementen zu nutzen ist das Ergebnis Emergenz. 


* **Feedbackschleifen:**
  Da alles miteinander verbunden ist, gibt es ständige Feedbackschleifen des Systems und zwischen den Elementen des Systems. Bei der Zirkularität des Systems ist es wichtig die Lebenszyklusphasen eines betrachtenden Systems mit zu betrachten – eine Darstellung davon ist in dem Artikel „System Lifecycle“ zu finden. 

  Sobald wir die Art und Dynamik von Feedbackschleifen kennen, können wir sie verstehen und steuern. Die Hauptarten sind dabei sich verstärkende und ausgleichende Feedbackschleifen. Dabei können verstärkende Schleifen einen negativen Einfluss haben, wenn dadurch ein ungewünschtes exponentielles Wachstum entsteht, wie bspw. Das Bevölkerungswachstum oder das Wachstum von Algen in einem Teich. 

  Bei einer ausgleichenden Feedbackschleife hingegen balancieren sich die Elemente innerhalb eines Systems aus.  


* **Kausalität**
  Um Feedbackschleifen zu verstehen, muss die Perspektive der Kausalität eingenommen werden. Kausalität beschreibt dabei den Zusammenhang von Ursache und Wirkung: wie eine Sache zur nächsten führt und zu einem dynamischen, sich ständig weiterentwickelnden System führt. 

  Bei der Kausalität als Konzept des Systemdenkens geht es darum, die Art und Weise zu entschlüsseln, wie sich die Dinge in einem System gegenseitig beeinflussen. Das Verständnis von Kausalität führt zu einer tieferen Sichtweise auf Handlungsfähigkeit, Feedbackschleifen sowie Verbindungen und Beziehungen, die alle grundlegende Bestandteile der Systemabbildung sind. 

* **Systemabbildung**
  Die Systemabbildung ist eines der wichtigsten Werkzeuge des Systemdenkers. Die Möglichkeiten der Umsetzung sind vielfältig, mithilfe von Modellen können Verhalten, Strukturen, Abhängigkeiten und Systemkonzepte dargestellt werden. Dabei geht es darum Elemente zu kategorisieren und das System als Ganzes in verschiedenen Sichten abzubilden. 

  Von dieser Darstellung aus können einzigartige Einsichten und Entdeckungen gemacht werden um diese als Entscheidungsgrundlage für Veränderungen zu nutzen.

  Betrachtet man nun ein System aus der Metaebene – von einem Blickwinkel außerhalb der Systemgrenzen – hat man die Möglichkeit eine Perspektive auf das System einzunehmen, die es ermöglicht neue Zusammenhänge zu erkennen. 

[16a]




#### Eingebettet, intelligent, Informationssysteme, etc.

* **Eingebettet:**

  Ein eingebettetes System (auch englisch „embedded system“) ist ein Computer, der in einen technischen Kontext eingebunden (eingebettet) ist. Dabei übernimmt der Rechner entweder Überwachungs-, Steuerungs- oder Regelfunktionen oder ist für eine Form der Daten- bzw. Signalverarbeitung zuständig, beispielsweise beim Ver- bzw. Entschlüsseln, Codieren bzw. Decodieren oder Filtern.

  Eingebettete Systeme verrichten – weitestgehend unsichtbar für den Benutzer – ihren Dienst in einer Vielzahl von Anwendungsbereichen und Geräten, beispielsweise in Geräten der Medizintechnik, Waschmaschinen, Flugzeugen, Kraftfahrzeugen, Kühlschränken, Fernsehern, DVD-Playern, Set-Top-Boxen, Routern, Mobiltelefonen oder allgemein in Geräten der Unterhaltungselektronik. Im Fall von komplexen Gesamtsystemen handelt es sich dabei meist um eine Vernetzung einer Vielzahl von ansonsten autonomen eingebetteten Systemen (so im Fahrzeug oder Flugzeug). 

* **intelligent**

  Intelligente Softwaresysteme sind Computerprogramme oder Softwareanwendungen, die in der Lage sind, Aufgaben auszuführen, die normalerweise menschliche Intelligenz erfordern. Diese Systeme nutzen fortschrittliche Technologien wie maschinelles Lernen, künstliche Intelligenz (KI), Datenanalyse und andere intelligente Algorithmen, um Probleme zu lösen, Muster zu erkennen, Entscheidungen zu treffen und sich im Laufe der Zeit zu verbessern.

  Hier sind einige Merkmale und Eigenschaften intelligenter Softwaresysteme:

    Maschinelles Lernen (ML): Intelligente Systeme können Muster in Daten erkennen und durch wiederholte Anpassung an neue Informationen lernen. Das maschinelle Lernen ist eine Schlüsselkomponente für viele intelligente Softwaresysteme.

    Künstliche Intelligenz (KI): KI bezieht sich auf die Fähigkeit von Computern, Aufgaben auszuführen, die normalerweise menschliche Intelligenz erfordern, wie zum Beispiel Spracherkennung, Bildverarbeitung, Entscheidungsfindung und Problemlösung.

    Datenanalyse: Intelligente Softwaresysteme nutzen umfangreiche Datenmengen, um Muster zu identifizieren, Vorhersagen zu treffen und fundierte Entscheidungen zu treffen. Big-Data-Technologien können ebenfalls in diese Systeme integriert sein.

    Autonome Entscheidungsfindung: Einige intelligente Softwaresysteme sind in der Lage, autonom Entscheidungen zu treffen, ohne auf menschliche Eingriffe angewiesen zu sein. Dies ist insbesondere bei selbstlernenden Systemen der Fall.
 
  [17a]

* **Informationssysteme**

  Ein Informationssystem (kurz IS, auch Informations- und Kommunikationssystem, kurz IuK-System) ist ein soziotechnisches System, das die Deckung von Informationsnachfrage zur Aufgabe hat. Es handelt sich um ein Mensch-/Aufgabe-/Technik-System, das Daten (bzw. Informationen) produziert, beschafft, verteilt und verarbeitet. Angrenzende Themenfelder sind die Informationsinfrastruktur und die Informationsfunktion.

  Daneben bezeichnet Informationssystem im allgemeineren Sinne ein „System von Informationen“, die in einem wechselseitigen Zusammenhang stehen und auf eine bestimmte Art organisiert sind. Insbesondere Wissen ist ein solches System aus Informationen.

  Die Begriffe Informationssystem und Anwendungssystem werden häufig synonym verwendet. Dabei wird Informationssystem im engeren Sinne („und so wird es i. d. R. verstanden“) als computergestütztes Anwendungssystem verstanden. Es ist jedoch wichtig zu verstehen, dass ein Anwendungssystem mit Anwendungssoftware und Datenbanken nur Teil eines Informationssystems ist.

[18a]


### Softwaresystembausteine

* **System:**
  * Ein umfassendes Softwareprodukt oder -projekt, das verschiedene Komponenten und Module umfassen kann. Ein System kann aus mehreren Subsystemen bestehen.

* **Subsystem:**
  * Ein Teil eines größeren Systems, der spezifische Funktionen oder Dienste bereitstellt. Subsysteme sind eigenständige Module innerhalb eines Systems.

* **Modul:**
  * Eine abgegrenzte und wiederverwendbare Einheit von Code, die eine oder mehrere eng verwandte Funktionen ausführt. Module sind oft Bausteine innerhalb von Subsystemen.

* **Paket:**
  * Eine Gruppierung von Modulen oder Klassen, die gemeinsam verwendet werden, um eine bestimmte Funktionalität bereitzustellen. Pakete helfen bei der Organisation von Code und der Wiederverwendbarkeit.

* **Komponente**
  * Eine eigenständige und austauschbare Softwareeinheit, die bestimmte Funktionen bereitstellt. Komponenten können unabhängig entwickelt und getestet werden und sind oft wiederverwendbar.

* **Klasse:**
  * In objektorientierten Programmiersprachen wie Java oder Python ist eine Klasse eine Vorlage für die Erstellung von Objekten. Sie definiert die Eigenschaften und Methoden, die Objekte einer bestimmten Klasse haben können.

* **Interface:**
  * Eine Schnittstelle definiert, wie verschiedene Softwarekomponenten miteinander kommunizieren können. Sie spezifiziert die Methoden oder Funktionen, die verfügbar sind, aber nicht deren Implementierung.

* **Funktion:**
  * Eine in sich geschlossene Einheit von Code, die eine bestimmte Aufgabe erfüllt. Funktionen können Teil von Modulen, Klassen oder Komponenten sein.

[19a]

### Qualitätsmerkmale von Softwaresystemen



#### Perspektiven auf Softwarequalität

  Die Softwarequalität kann aus verschiedenen Perspektiven betrachtet werden, um sicherzustellen, dass sie den Anforderungen und Erwartungen entspricht. 

Zum einen kann man Qualität von Software aus zwei Perspektiven betrachten: von außen (nutzerseitig) und von innen (entwicklerseitig). Des Weiteren muss bei der Qualitätssicherung nach den Arten von Software unterschieden werden, die jeweils eigene Anforderungen haben.

[20a]

#### Innere und äußere Qualität (Kunde, Anwender, Softwareentwickler, etc.)

**Innere Qualität:**

  * Softwareentwicklerperspektive:

    Für Entwickler bezieht sich die innere Qualität auf die strukturelle Integrität des Codes. Dies umfasst Aspekte wie Modularität, Lesbarkeit, Wartbarkeit und die Einhaltung von Coding-Standards. Entwickler legen Wert auf gut organisierten, effizienten Code, der leicht zu verstehen und zu erweitern ist.

  * Managementperspektive:

    Das Management interessiert sich ebenfalls für die innere Qualität, da dies Auswirkungen auf die Wartbarkeit, die Entwicklungsgeschwindigkeit und die langfristigen Kosten haben kann. Eine gute innere Qualität erleichtert auch die Zusammenarbeit im Entwicklerteam.

* **Äußere Qualität:**

  * Kundenperspektive:

    Kunden bewerten die Software oft nach ihrer äußeren Qualität, die direkt mit der Erfüllung der funktionalen und nicht-funktionalen Anforderungen verbunden ist. Benutzerfreundlichkeit, Leistung, Zuverlässigkeit und Sicherheit sind Beispiele für Kriterien, die Kunden als Teile der äußeren Qualität betrachten.

  * Anwenderperspektive:

    Anwender legen Wert darauf, dass die Software ihre Bedürfnisse erfüllt und eine positive Benutzererfahrung bietet. Eine intuitive Benutzeroberfläche, schnelle Reaktionszeiten und zuverlässige Funktionen sind für Anwender wichtige Aspekte der äußeren Qualität.

[20a]


### Qualitätsdreieck und Teufelsquadrat

* **Qualitätsdreieck oder auch Das Magische Dreieck**

Das magische Dreieck beschäftigt sich mit den drei Zielgrößen Kosten, Zeit und Leistung, die untereinander ausbalanciert werden müssen.

Die Grundidee des Modells besagt, dass sich die Zielgrößen untereinander beeinflussen und sich jedes Projekt in einem Spannungsfeld befindet. Oft ist es nicht möglich, alle drei Zielgrößen gleichermaßen zu optimieren.

![:scale 50%](media\magisches-dreieck-projektmanagement.jpg)

[21a]

* **Teufelsquadrat**

Harry Sneed geht einen ähnlichen Weg, jedoch wird die Zielgröße „Leistung“ aufgespalten in Inhalt und Qualität dieser Leistung. Daraus ergeben sich nun vier Zielgrößen:

Wird eine der Zielgrößen geändert, so wirkt sich das auf die anderen Zielgrößen aus.

Das Teufelsquadrat stellt schön dar, dass Eingriffe ins Projekt Auswirkungen auf andere Zielgrößen haben. Anders ausgedrückt: Wird eine Zielgröße verändert, muss auch mit Anpassungen von einer oder mehrerer anderer Zielgrößen gerechnet werden.


![:scale 50%](media\teufelsquadrat-projektmanagement.jpg)

![:scale 80%](media\teufelsquadrat-auswirkungen.jpg)

Das Teufelsquadrat kann gut für folgende Zwecke eingesetzt werden:

  * Grobe Zieldefinition und Visualisierung zum Projektstart: Alle Beteiligten sehen auf einen Blick die wichtigsten Zielgrößen. „Was wollen im wir im Projekt erreichen?“

  * Darstellung von Schwachstellen: Die grafische Darstellung hilft dabei, Widersprüche und Konkurrenzen zwischen den wichtigsten Zielgrößen früh zu erkennen.

  * Aufzeigen von Änderungen von Rahmenbedingungen: Eingriffe ins Projekt können visualisiert werden. Wie wirken sich Änderungen auf unsere Projektziele aus?

[21a]


### Qualitätsmodelle

Der Begriff der Softwarequalität selbst ist nicht operabel, d. h. in der Praxis nicht direkt anwendbar. Deshalb existieren Qualitätsmodelle, die den Begriff konkretisieren und durch eine weitere Detaillierung operationalisieren. Dadurch entsteht ein Baum (oder ein Netz) von Begriffen und Unterbegriffen. 

[24a]

#### Qualitätsziele

Qualitätsziele in Qualitätsmodellen sind messbare und spezifische Ziele, die dazu dienen, die Qualität von Softwareprodukten oder -prozessen zu verbessern. Diese Ziele sind ein wesentlicher Bestandteil von Qualitätsmodellen, da sie dazu beitragen, die Erfüllung von Qualitätsanforderungen zu überwachen und sicherzustellen. Hier sind einige allgemeine Qualitätsziele, die in verschiedenen Software-Qualitätsmodellen verfolgt werden können:

* Funktionalität

* Zuverlässigkeit

* Effizienz

* Benutzbarkeit

* Wartbarkeit

* Sicherheit

* Übertragbarkeit

#### FCM- Modelle

Die Qualitätsmerkmale tragen im Englischen die Bezeichnung factor, ein Qualitätsteilmerkmal heißt criterion und die Qualitätsindikatoren metrics. Deswegen erscheinen derartige Qualitätsmodelle in der Literatur auch als „FCM-Modelle

[24a]


#### ISO 25010


Die ISO/IEC 25010 ist eine Norm, die Qualitätsanforderungen und Evaluationskriterien für Softwareprodukte und -systeme festlegt. Diese Norm wurde entwickelt, um einen Rahmen für die Definition, Messung und Bewertung von Qualitätsmerkmalen von Software bereitzustellen. Die vollständige Bezeichnung lautet "ISO/IEC 25010:2011 Systems and software engineering -- Systems and software Quality Requirements and Evaluation (SQuaRE) -- System and software quality models."

Die Norm ISO/IEC 25010 basiert auf dem SQuaRE (Systems and Software Quality Requirements and Evaluation) Framework, das von der International Organization for Standardization (ISO) und der International Electrotechnical Commission (IEC) entwickelt wurde.

[23a]


#### FURPS

FURPS ist ein Akronym aus dem Bereich der Softwarequalität. Es entstammt dem Englischen und fasst Qualitätsmerkmale von Software zusammen. 

Die Buchstaben von FURPS bedeuten im Einzelnen folgendes:

* Functionality (Funktionalität)
* Usability (Benutzbarkeit)
* Reliability (Zuverlässigkeit)
* Performance (Effizienz)
* Supportability (Änderbarkeit), sinngemäße Übersetzung Wartbarkeit

Die Übersetzungen in Klammern sind die Begriffe, wie sie auch in der ISO/IEC 25000 zu finden sind.
Das P kann auch für Portability (Übertragbarkeit) stehen. 


![:scale 80%](media\FURPS.jpg)

[23a]


### Relevante Qualitätsmerkmale im Detail


#### Inhärente (essential) Komplexität

Die "inhärente Komplexität" auch als "essentielle Komplexität" bezeichnet, bezieht sich auf die Komplexität, die intrinsisch mit der Natur des zu lösenden Problems oder der zu entwickelnden Software verbunden ist. Anders ausgedrückt, es handelt sich um die Komplexität, die aufgrund der inhärenten Schwierigkeiten und Anforderungen des Problems selbst entsteht und nicht leicht vermieden oder reduziert werden kann.

* Algorithmenkomplexität

* Natur von Datenstrukturen

* Geschäftsregeln und Logik

* Probleminteraktionen

[26a] [27a]

#### Unbeabsichtigte (accidential) Komplexität

Die "unbeabsichtigte Komplexität" in einem Softwaresystem bezieht sich auf die Komplexität, die durch Faktoren entsteht, die nicht direkt mit den eigentlichen Anforderungen oder der Lösung des Problems zusammenhängen. Diese Art von Komplexität entsteht eher aus technischen Entscheidungen, Werkzeugen, Prozessen oder anderen äußeren Einflüssen. 

* Komplexität durch Technologiewechsel

* Werkzeugkomplexität

* Prozesskomplexität

* Abhängigkeitskomplexität

* Over-Engineering

* Legacy-Systeme und Altlasten

[26a] [27a]

#### Cynefin-Framework

Das Cynefin-Framework ist ein Wissensmanagement-Modell mit der Aufgabe Probleme, Situationen und Systeme zu beschreiben. Das Modell liefert eine Typologie von Kontexten, die einen Anhaltspunkt bieten, welche Art von Erklärungen oder Lösungen zutreffen könnten.

![:scale 80%](media\Cynefin_framework,_September_2006.png)

[25a]

##### Maintainability
Maintainability bezieht sich darauf, wie einfach es ist, eine Software zu warten und zu verbessern, nachdem sie entwickelt wurde. Hier sind einige Aspekte von Maintainability, die in Betracht gezogen werden sollten:

**Klarer Code:**
Gut geschriebener Code sollte klar und verständlich sein. Eine eindeutige Benennung von Variablen, Funktionen und Klassen trägt dazu bei, den Code leichter wartbar zu machen.

**Modularität:**
Die Software sollte in kleine, unabhängige Module aufgeteilt sein. Änderungen in einem Modul sollten keine unerwarteten Auswirkungen auf andere Teile des Systems haben.

**Dokumentation:**
Eine umfassende Dokumentation, einschließlich Kommentaren im Code sowie externer Dokumentation, erleichtert es Entwicklern, den Code zu verstehen und Änderungen vorzunehmen.

**Wiederverwendbarkeit:**
Die Möglichkeit, Code wiederzuverwenden, trägt dazu bei, Redundanzen zu vermeiden und die Wartbarkeit zu verbessern. Bibliotheken und Frameworks können ebenfalls die Wiederverwendbarkeit fördern.

**Testbarkeit:**
Testbare Software erleichtert die Identifizierung von Fehlern und die Validierung von Änderungen, ohne dass das gesamte System beeinträchtigt wird.

**Versionskontrolle:**
Die Verwendung von Versionskontrollsystemen wie Git ermöglicht es, Änderungen nachzuverfolgen, verschiedene Versionen zu vergleichen und bei Bedarf zu einem früheren Zustand zurückzukehren.

**Technologische Aktualisierungen:**
Die Fähigkeit, Technologien zu aktualisieren, um von neuen Funktionen, Leistungsverbesserungen und Sicherheitspatches zu profitieren, ist entscheidend für die langfristige Wartbarkeit.

[1b,2b]

#### Observability
Observability in Software-Systemen bezieht sich darauf, wie gut Entwickler und Betreiber den internen Zustand und das Verhalten eines Systems verstehen können. Hier sind einige Aspekte von Observability:

**Logging:**
Umfassende Protokollierung ist entscheidend, um Aktivitäten und Ereignisse im System aufzuzeichnen. Klare und aussagekräftige Protokolle erleichtern die Fehlerdiagnose und das Monitoring.

**Ereignisverarbeitung (Event Processing):**
Die Verarbeitung von Ereignissen ermöglicht es, auf wichtige systeminterne Vorgänge zu reagieren und darauf zu reagieren. Dies kann auch zur Erkennung von ungewöhnlichem Verhalten genutzt werden.

**Debugging-Möglichkeiten:**
Die Bereitstellung von Tools und Mechanismen zum Debuggen von Code in Produktionsumgebungen erleichtert die Identifizierung und Behebung von Fehlern.

**Visualisierung:**
Die Darstellung von Daten in übersichtlichen Dashboards und Diagrammen erleichtert das Verständnis des Systemverhaltens auf einen Blick.

**Dokumentation:**
Klare und aktuelle Dokumentation zu Systemarchitektur, Prozessen und Schnittstellen trägt dazu bei, dass Observability nicht nur auf vorhandene Kenntnisse angewiesen ist.

[1b,3b]

#### Reliability
Zuverlässigkeit (Reliability) in Software-Systemen bezieht sich darauf, dass ein System konsistent und fehlerfrei funktioniert. Hier sind einige Aspekte von Zuverlässigkeit in Software-Systemen:

**Fehlertoleranz:**
Die Fähigkeit eines Systems, trotz Fehlern oder Ausfällen in einem oder mehreren seiner Komponenten weiterhin zu funktionieren.

**Wiederherstellbarkeit (Recoverability):**
Die Fähigkeit, nach einem Fehlerzustand in einen normalen Betriebszustand zurückzukehren, ohne dabei Datenverlust oder andere negative Auswirkungen zu erleiden.

**Fehlererkennung und -überwachung:**
Systeme sollten Mechanismen zur kontinuierlichen Überwachung auf Fehler und ungewöhnliches Verhalten implementieren, um frühzeitig auf potenzielle Probleme aufmerksam zu werden.

**Skalierbarkeit:**
Ein zuverlässiges System sollte in der Lage sein, mit steigender Last oder wachsenden Anforderungen umzugehen, ohne dass dies zu Ausfällen oder Beeinträchtigungen führt.

**Monitoring und Alarme:**
Kontinuierliches Monitoring ermöglicht die frühzeitige Erkennung von Abweichungen im Systemverhalten. Alarme sollten ausgelöst werden, wenn kritische Parameter außerhalb vordefinierter Schwellenwerte liegen.

[8b]

#### Availability
**Uptime:**
Die Zeit, in der das System ohne Unterbrechung oder Ausfall online und verfügbar ist. Hohe Uptime-Zeiten sind ein Maß für die Verfügbarkeit.

**Lastenausgleich (Load Balancing):**
Verteilung des Datenverkehrs auf mehrere Server oder Ressourcen, um eine gleichmäßige Auslastung und Vermeidung von Überlastungen zu gewährleisten.

**Redundanz:**
Die Implementierung redundanter Hardware- oder Softwarekomponenten, um Ausfälle einzelner Teile zu kompensieren und die Verfügbarkeit zu erhöhen.

**Failover-Mechanismen:**
Automatische Umschaltung auf alternative Ressourcen oder Server, wenn ein Ausfall oder eine Beeinträchtigung erkannt wird.

**Schnelle Wiederherstellung (Rapid Recovery):**
Effiziente Mechanismen, um das System nach einem Ausfall oder einer Beeinträchtigung schnell wieder in den Normalbetrieb zu versetzen.

**Datenreplikation:**
Die Vervielfältigung von Daten auf mehreren Servern oder Standorten, um die Verfügbarkeit zu verbessern und Datenverlust zu verhindern.

[1b,4b]

#### Resilience
Resilienz in Software-Systemen bezieht sich darauf, wie gut ein System mit unerwarteten Fehlern oder Störungen umgehen kann, ohne dabei den gesamten Betrieb zu beeinträchtigen.
Das dieser Aspekt der Reliance sehr ähnlich ist hier die wichtigsten Punkte:

**Fehlerisolierung:**
Die Fähigkeit, Fehler auf spezifische Komponenten oder Dienste zu isolieren, um zu verhindern, dass sich Fehler auf das gesamte System ausbreiten.

**Robuste Kommunikation:**
Verlässliche Kommunikationsmechanismen, die auch bei Netzwerkproblemen oder Ausfällen zuverlässig funktionieren.

**Monitoring und Telemetrie:**
Echtzeitüberwachung und Erfassung von Telemetriedaten, um den Zustand des Systems zu verstehen und frühzeitig auf Anomalien hinzuweisen.

[1b,5b]

#### Performance

**Reaktionszeit:**
Die Reaktionszeit einer Anwendung ist die Zeitspanne zwischen einer Benutzeraktion und der entsprechenden Reaktion des Systems. Kürzere Reaktionszeiten tragen zu einer besseren Benutzererfahrung bei.

**Skalierbarkeit:**
Skalierbarkeit bezieht sich auf die Fähigkeit des Systems, mit zunehmender Last oder Anzahl von Benutzern umzugehen. Ein skalierbares System kann seine Leistungsfähigkeit durch Hinzufügen von Ressourcen oder Anpassen an Lastspitzen verbessern.

**Ressourcennutzung:**
Eine effiziente Nutzung von Ressourcen wie CPU, Arbeitsspeicher und Netzwerkbandbreite ist entscheidend. Eine optimale Ressourcennutzung gewährleistet eine effiziente Ausführung von Anwendungen und minimiert Engpässe.

**Datenbankleistung:**
Datenbankabfragen und -operationen können einen erheblichen Einfluss auf die Gesamtleistung haben. Optimierungen in Bezug auf Datenbankdesign, Indexierung und Abfrageeffizienz sind wichtig, um eine schnelle Datenverarbeitung sicherzustellen.

**Lasttests und Optimierung:**
Regelmäßige Lasttests ermöglichen es, die Leistungsfähigkeit eines Systems unter simulierten Bedingungen zu überprüfen. Basierend auf den Testergebnissen können gezielte Optimierungen vorgenommen werden, um Engpässe zu identifizieren und zu beheben.

[1b,6b]

#### Security und Safety
**Fehler- und Ausnahmebehandlung:**
Ein zuverlässiges System sollte angemessene Maßnahmen für die Erkennung, Behandlung und Protokollierung von Fehlern und Ausnahmen implementieren, um unvorhergesehene Zustände zu bewältigen und den Betrieb sicher fortzusetzen.

**Datenschutz und Vertraulichkeit:**
Sowohl die Sicherheit als auch die Sicherheit erfordern den Schutz sensibler Daten, um die Privatsphäre zu wahren und sicherzustellen, dass vertrauliche Informationen nicht in die falschen Hände geraten.

**Robuste Architektur und Redundanz:**
Die Implementierung von robusten Architekturen und Redundanzmechanismen unterstützt die Widerstandsfähigkeit gegenüber Fehlern, Ausfällen oder Angriffen, um einen kontinuierlichen und sicheren Betrieb zu gewährleisten.

**Sicherheitsüberprüfungen und Audits:**
Regelmäßige Überprüfungen, Audits und Penetrationstests sind notwendig, um potenzielle Sicherheitslücken zu identifizieren und zu beheben, und um sicherzustellen, dass das System den geltenden Sicherheitsstandards entspricht.

[1b,7b]

### Metriken zur Messung von Softwarequalität
Metriken zur Messung von Softwarequalität sind quantitative Maße, die dazu dienen, verschiedene Aspekte der Softwareentwicklung und -wartung zu bewerten.
Diese Metriken ermöglichen es Entwicklern, Managern und anderen Stakeholdern, die Qualität von Softwareprodukten zu überwachen, zu analysieren und zu verbessern.
Sie können sich auf verschiedene Dimensionen der Softwarequalität beziehen, darunter Code-Qualität, Leistung, Sicherheit, Wartbarkeit und mehr.
Metriken bieten eine objektive Grundlage für Entscheidungen im Entwicklungsprozess und tragen dazu bei, die Effizienz, Zuverlässigkeit und Benutzerfreundlichkeit von Softwareprodukten sicherzustellen.

[1b,9b]

#### Konventionelle Metriken
Konventionelle Metriken sind standardisierte Messgrößen, die in der Softwareentwicklung verwendet werden, um verschiedene Aspekte der Softwarequalität zu bewerten. Diese Metriken folgen oft anerkannten Standards und Vorgehensweisen.

**Zeilenanzahl (LOC - Lines of Code):**
Die Anzahl der Codezeilen in einem Programm. Diese Metrik kann auf verschiedene Weisen interpretiert werden, einschließlich der Codekomplexität.

**Zyklomatische Komplexität:**
Ein Maß für die Komplexität des Quellcodes, das auf der Anzahl der unabhängigen Pfade durch den Code basiert. Hohe zyklomatische Komplexität kann auf schwer zu verstehenden oder fehleranfälligen Code hinweisen.

**Testabdeckung:**
Der Prozentsatz des Codes, der während der Ausführung von Tests abgedeckt wird. Eine höhere Testabdeckung kann auf eine umfassendere Teststrategie hinweisen.

**Fehlerdichte:**
Die Anzahl der Fehler pro Zeile Code. Eine niedrige Fehlerdichte deutet auf einen stabilen und zuverlässigen Code hin.

**Durchschnittliche Zeit bis zum Fehler (MTTF - Mean Time To Failure):**
Die durchschnittliche Zeit zwischen dem Start der Software und dem Auftreten des ersten Fehlers.

**Durchschnittliche Wiederherstellungszeit (MTTR - Mean Time To Recovery):**
Die durchschnittliche Zeit, die benötigt wird, um die Software nach einem Fehler wiederherzustellen.

**Benutzerzufriedenheit:**
Bewertungen und Feedback der Benutzer zur Benutzerfreundlichkeit und Leistung der Software.

**Wartbarkeitsmetriken:**
Dazu gehören Metriken wie die durchschnittliche Zeit zur Behebung von Fehlern und die durchschnittliche Zeit zur Implementierung neuer Funktionen.

Viele dieser Metriken überschneiden sich auch mit denen eder DORA-Metriken zur Messung der Effizienz Softwareentwicklung,
da sich die Effizienz direkt auf die Qualität auswirkt.

[1b,9b]

##### McCabe-Metrik
Die McCabe-Metrik, auch als zyklomatische Komplexität bekannt, ist eine Softwaremetrik, die dazu dient, die Komplexität eines Software-Moduls zu messen. Diese Module können Funktionen, Prozeduren oder allgemein Code-Abschnitte sein.

Die Grundidee hinter dieser Software-Metrik ist, dass ein Modul ab einer bestimmten Komplexität für Menschen schwer verständlich wird. Die cyclomatic complexity wird als die Anzahl der linear unabhängigen Pfade auf dem Kontrollflussgraphen eines Moduls definiert. Diese Zahl stellt eine obere Schranke für die minimale Anzahl der Testfälle dar, die erforderlich sind, um eine vollständige Zweigabdeckung des Kontrollflussgraphen zu erreichen.

Über die Begriffe Zyklomatische Komplexität und Kontrollflussgraphen wird im Folgenden noch genauer eingegangen.

[10b]

##### Zyklomatische Komplexität
Die zyklomatische Komplexität eines Moduls wird durch die Anzahl der linear unabhängigen Pfade in seinem Kontrollflussgraphen bestimmt.

Der Kontrollflussgraph stellt die verschiedenen Wege dar, die der Programmfluss während der Ausführung des Codes nehmen kann. Die zyklomatische Komplexität misst im Wesentlichen, wie viele Entscheidungen (Verzweigungen, Schleifen, etc.) es im Code gibt. Je mehr Entscheidungen es gibt, desto höher ist die zyklomatische Komplexität.

Die zyklomatische Komplexität kann dazu verwendet werden, die Testbarkeit eines Softwaremoduls einzuschätzen. Hohe zyklomatische Komplexität kann darauf hinweisen, dass ein Modul schwieriger zu verstehen und zu testen ist. Es wird empfohlen, die zyklomatische Komplexität während des Softwareentwicklungsprozesses zu überwachen, um die Wartbarkeit und Qualität des Codes zu verbessern.

[11b]

##### Kontrollflussgraph
Ein Kontrollflussgraph ist ein gerichteter Graph, der dazu dient, den Prorgrammablauf eines Programms zu beschreiben.
Dieser besteht wie üblich aus Knoten und Kanten.
Die Knoten stellen dabei die Grundblöcke der Programms dar und die Kanten die übergänge zu weiteren Blöcken darstellen, wie z.B Schleifen oder Verzweigungen.

![:scale 80%](media\Kontrollflussgraph.png)

[12b,13b]

#### Objektorientierte Metriken
Die Objektorientierten Metriken berücksichten bei der Messung von der Software die Zusammenfassung von Datensturkturen und den dazugehörigen Methoden in Objekten.
Auch die Beziehungen zu anderen Objekten, sowie de Strukturmerkmale der Programmierung, wie die Kapselung, Vererbung, usw werden geprüft.
Die Messung der Qualität bezieht sich dann auf vier Bereiche:
Die Methoden, die Klassen, Vererbungshierarchie und die Aggregationsherarchien.

[14b]

##### Lack of Cohesion in Methods
"Lack of Cohesion in Methods" (LCOM) ist teil der objektorientierten Metrik zur Bewertung der Kohäsion in einem Softwaremodul oder einer Klasse. Hohe Kohäsion bedeutet, dass die Methoden in einer Klasse eng miteinander verbunden sind und gemeinsam an einem Ziel arbeiten. LCOM bewertet, wie stark die Methoden in einer Klasse miteinander interagieren. Niedrige LCOM-Werte zeigen eine starke Kohäsion an, während hohe Werte auf eine geringe Kohäsion und damit potenzielle Probleme bei Wartung und Verständnis des Codes hinweisen. In der Softwareentwicklung strebt man nach Klassen mit hoher Kohäsion für einen besseren, wartbaren Code.

[15b]
#### Beispiele
Hier ein Beispiel zur Lack of Cohesion:
Wir haben eine Klasse "OnlineShop" in denen es die Methoden BezahlungVerarbeiten, BestandUpdate und sendBestätigungsemail gibt.
Wenn die Lack of Cohesion analyse einen hohen LCOM Werte aufweißt, beduetet das, dass die Methoden nicht stark mit einander verbunden sind und man diese in verschiedene Klassen aufteilen sollte.
Außerdem würde dadurch die durchschnittliche Anzahl der Methoden pro Klasse (NOM) sinken, was auch ein Qualitätsmerkmal ist, da es komplexität verringert.

[16b]

### Modellierung und Visualisierung von Softwaresystemen
Zur Moduellierung und Visualisierung von Softwaresystemen gibt es verschiedene Modele
und Vorgehensweisen die im Folgenden Thematisiert werden.

#### Modelle
Ein Modell ist eine vereinfachte Darstellung eines Systems, das dazu dient, bestimmte Aspekte des Systems zu verstehen und zu analysieren. Modelle können verwendet werden, um die Struktur, das Verhalten und die Interaktionen eines Systems zu beschreiben. Sie können auch verwendet werden, um die Auswirkungen von Änderungen zu simulieren und zu verstehen.

**UML-Diagramme:**
Klassendiagramme, Aktivitätsdiagramme und Sequenzdiagramme sind sehr nützlich, um die Struktur und das Verhalten eines Systems zu verstehen. Sie bieten eine umfassende Sicht auf die Softwarearchitektur.

**Architekturdiagramme:**
Die Visualisierung der Systemarchitektur ist entscheidend, um eine klare Vorstellung von Komponenten, Schnittstellen und Abhängigkeiten zu vermitteln.

**Use-Case-Diagramme:**
Sie sind wichtig, um die Interaktionen zwischen dem System und den Benutzern zu verstehen und die funktionalen Anforderungen zu klären.

**Komponentendiagramme:**
Zeigen, wie verschiedene Teile des Systems zusammenarbeiten, und sind daher besonders für Entwickler und Architekten relevant.

**Zustandsdiagramme:**
Sind wichtig, um das Verhalten von Objekten in verschiedenen Zuständen zu verstehen, was besonders für Systeme mit komplexen Zustandsübergängen relevant ist.

**ER-Diagramme:**
In Datenbankanwendungen sind sie entscheidend, um die Beziehungen zwischen verschiedenen Datenentitäten zu klären.

[17b]

##### Descriptive vs rule-based modeling
**Deskriptive Modellierung:**

**Beschreibend:**
Deskriptive Modelle beschreiben das System, wie es ist, ohne dabei Einschränkungen oder Regeln vorzugeben.

**Flexibilität:**
Sie sind flexibel und können verschiedene Aspekte des Systems auf unterschiedliche Weisen darstellen.

**Visualisierung:**
Oft werden graphische Modelle verwendet, um komplexe Strukturen und Beziehungen leicht verständlich zu machen.

**Exploration:**
Gut geeignet für die Erkundung von Ideen, Konzepten und Strukturen, ohne sich von vornherein auf bestimmte Regeln festzulegen.

**Beispiele:**
Mind Maps, Concept Maps und Diagramme in der frühen Phase eines Projekts.


**Regelbasierte Modellierung:**

**Festgelegte Regeln:**
Regelbasierte Modelle legen spezifische Regeln, Einschränkungen oder Verhaltensmuster für das System fest.

**Strukturiert:**
Sie bieten eine strukturierte Herangehensweise, bei der klare Regeln und Anweisungen befolgt werden müssen.

**Automatisierung:**
Gut geeignet für die Automatisierung von Prozessen, da die Regeln in der Regel maschinenlesbar sind.

**Fehlervermeidung:**
Reduziert Spielraum für Interpretation und minimiert potenzielle Fehler, da die Modelle auf klaren Regeln basieren.


Beide Ansätze haben ihren Platz in der Modellierung, wobei deskriptive Modelle oft in frühen Phasen für die Ideenfindung verwendet werden, während regelbasierte Modelle in späteren Phasen eingesetzt werden, um spezifische Verhaltensweisen festzulegen.
Deskriptive Modelle bieten mehr Spielraum für Kreativität und Exploration, während regelbasierte Modelle Struktur und Klarheit bieten.

[1b,18b,19b]

#### UML
UML-Diagramme (Unified Modeling Language) sind eine standardisierte Methode zur grafischen Darstellung von Software-Designkonzepten. Sie bieten eine visuelle Sprache, um Struktur, Verhalten und Interaktionen von Systemen zu beschreiben. UML umfasst verschiedene Diagrammtypen, wie Klassendiagramme für Klassenstrukturen, Aktivitätsdiagramme für Abläufe und Use Case-Diagramme für Interaktionen mit Benutzern.

[1b,20b]

##### Statische und dynamische Diagrammtypen
Statische Diagrammtypen in UML repräsentieren die Struktur eines Systems und umfassen Klassendiagramme, Objektdiagramme und Paketdiagramme.Sie zeigen Entitäten und ihre Beziehungen im System.

Dynamische Diagrammtypen hingegen beschreiben den Verhaltensaspekt eines Systems. Hierzu gehören Aktivitätsdiagramme, Zustandsdiagramme und Sequenzdiagramme. Sie zeigen, wie Objekte interagieren und wie sich der Systemzustand im Laufe der Zeit ändert.

[1b,21b]

##### Zuordnung der UML-Diagrammtypen zu Phasen der Softwareentwicklung
UML-Diagrammtypen können verschiedenen Phasen der Softwareentwicklung zugeordnet werden:

**Anforderungsanalyse und Konzeptualisierung:**
Use Case Diagramme: Zeigen die Interaktionen zwischen System und Akteuren.
Klassendiagramme: Modellieren statische Strukturen, wie Klassen und ihre Beziehungen.

**Entwurf:**
Aktivitätsdiagramme: Visualisieren den Ablauf von Aktivitäten und Prozessen.
Zustandsdiagramme: Beschreiben den Lebenszyklus eines Objekts in Reaktion auf Ereignisse.

**Implementierung:**
Klassendiagramme: Werden weiter verfeinert, um die Details der Klassen, Methoden und Attribute zu zeigen.
Komponentendiagramme: Zeigen die physischen Module des Systems und deren Abhängigkeiten.

**Testen:**
Sequenzdiagramme: Visualisieren die Interaktionen zwischen Objekten über die Zeit.
Kommunikationsdiagramme: Ähnlich wie Sequenzdiagramme, zeigen aber andere Perspektiven der Kommunikation.

**Wartung und Weiterentwicklung:**
Klassendiagramme und Sequenzdiagramme: Werden aktualisiert, um Änderungen im System zu reflektieren.
Paketdiagramme: Zeigen die Organisation von Paketen und ihre Abhängigkeiten.

[22b]

##### Funktionale Modelle
In der Softwareentwicklung bezieht sich der Begriff "funktionale Module" auf unabhängige, abgeschlossene Einheiten oder Komponenten einer Software, die spezifische Funktionen oder Aufgaben ausführen. Funktionale Module werden erstellt, um den Grundsätzen der Modularität und Wiederverwendbarkeit zu entsprechen. Hier sind einige wichtige Aspekte funktionaler Module:

**Aufgabenspezifisch:**
Funktionale Module sind auf die Erfüllung spezifischer Aufgaben oder Funktionen ausgerichtet. Jedes Modul ist für eine bestimmte Funktionalität verantwortlich.

**Unabhängigkeit:**
Module sollten unabhängig voneinander sein, sodass Änderungen in einem Modul keine Auswirkungen auf andere Module haben. Dies fördert die Wartbarkeit und Erweiterbarkeit der Software.

**Kapselung:**
Jedes Modul sollte eine klare Schnittstelle haben, über die es mit anderen Modulen kommuniziert. Die inneren Details eines Moduls sollten für andere Module verborgen sein, um eine bessere Kapselung zu gewährleisten.

**Wiederverwendbarkeit:**
Durch die Schaffung von funktionalen Modulen können Entwickler Teile des Codes wiederverwenden, wenn ähnliche Funktionalitäten in verschiedenen Teilen der Software benötigt werden.

**Testbarkeit:**
Funktionsmodule erleichtern das Testen, da jede Funktion separat überprüft werden kann. Dies erleichtert die Fehlerfindung und die Gewährleistung der Qualität der Software.

**Skalierbarkeit:**
Durch die Verwendung funktionaler Module lässt sich die Software besser skalieren. Neue Funktionen können durch das Hinzufügen neuer Module implementiert werden, ohne bestehenden Code zu beeinträchtigen.

[1b,23b]

###### Use Case Diagramme
Use Case-Diagramme sind eine Art von UML-Diagrammen (Unified Modeling Language), die dazu verwendet werden, die Interaktionen zwischen einem System und seinen Benutzern oder anderen Systemen zu modellieren. Diese Diagramme bieten eine visuelle Darstellung der verschiedenen Anwendungsfälle (Use Cases), die ein System unterstützen sollte, und der Akteure, die an diesen Anwendungsfällen beteiligt sind.

**Akteure (Actors):**
Akteure sind externe Entitäten, sei es Benutzer oder andere Systeme, die mit dem System interagieren. Akteure repräsentieren typischerweise Rollen, die Benutzer in Bezug auf das System spielen.

**Anwendungsfälle (Use Cases):**
Ein Anwendungsfall repräsentiert eine spezifische Funktionalität oder eine Interaktion zwischen einem Akteur und dem System. Jeder Anwendungsfall beschreibt, wie das System auf eine bestimmte Anfrage oder Aktion eines Akteurs reagiert.

**Beziehungen:**
Die Beziehungen zwischen Akteuren und Anwendungsfällen werden durch Linien dargestellt. Eine Linie, die von einem Akteur zu einem Anwendungsfall führt, zeigt an, dass der Akteur in diesem Anwendungsfall involviert ist.

**Inklusion und Erweiterung:**
Use Case-Diagramme können auch die Beziehungen zwischen verschiedenen Anwendungsfällen darstellen. "Inklusion" zeigt an, dass ein Anwendungsfall einen anderen einschließt, während "Erweiterung" darauf hinweist, dass ein Anwendungsfall optional erweitert werden kann.

[1b,24b]

##### Strukturmodelle
Strukturmodelle in der Softwareentwicklung beschreiben die statischen Aspekte eines Systems, insbesondere die Organisation seiner Komponenten oder Module sowie deren Beziehungen zueinander. Diese Modelle helfen, die Architektur und Struktur eines Softwareprojekts zu verstehen. Hier sind einige gängige Arten von Strukturmodellen:

**Klassendiagramme:**
Klassendiagramme sind Teil der UML und zeigen die Klassen in einem System sowie ihre Attribute, Methoden und Beziehungen. Sie bieten einen Überblick über die Struktur der Daten und Funktionen in einem System.

**Paketdiagramme:**
Diese Diagramme zeigen, wie Klassen in Paketen organisiert sind. Ein Paket ist eine Sammlung von Klassen, die eine gemeinsame Funktionalität oder Verantwortlichkeit haben.

**Objektdiagramme:**
Objektdiagramme zeigen eine Momentaufnahme von Objekten und ihren Beziehungen zu einem bestimmten Zeitpunkt während der Laufzeit. Sie veranschaulichen die konkreten Instanzen von Klassen.

**Komponentendiagramme:**
Komponentendiagramme zeigen die physischen Komponenten eines Systems und deren Abhängigkeiten. Dies kann Dateien, Bibliotheken, ausführbare Dateien oder andere Bausteine umfassen.

**Deployment-Diagramme:**
#Diese Diagramme zeigen die Verteilung von Softwarekomponenten auf Hardwarekomponenten. Sie sind besonders relevant für verteilte Systeme.

[1b,25b]

###### Klassendiagramme
Ein Klassendiagramm in der UML ist eine grafische Darstellung der statischen Struktur eines Systems, das die Klassen, ihre Attribute, Methoden, Beziehungen und Vererbungshierarchien zeigt. Klassen repräsentieren Baupläne für Objekte, Attribute sind Eigenschaften dieser Klassen, und Methoden sind die Funktionen, die sie ausführen können. Assoziationen zeigen die Beziehungen zwischen Klassen, während Vererbung die Hierarchie und den Austausch von Eigenschaften zwischen Klassen darstellt. Klassendiagramme sind ein grundlegendes Werkzeug für die objektorientierte Modellierung und bieten eine visuelle Übersicht über die Struktur eines Systems.

[1b,26b]

###### Verteilungsdiagramme
Verteilungsdiagramme in der UML bieten eine grafische Darstellung der physischen Verteilung von Softwarekomponenten in einem Netzwerk. Sie zeigen Knoten, die Hardware oder Softwareumgebungen repräsentieren, und Artefakte, die die physischen Implementierungen von Komponenten darstellen. Verbindungen zwischen Knoten zeigen Netzwerkkommunikation oder Abhängigkeiten an. Verteilungsdiagramme ermöglichen es, die Architektur und den Einsatz von Software in verschiedenen Umgebungen zu planen und zu visualisieren.

[1b,27b]

##### Verhaltensmodelle
Verhaltensmodelle in der UML beschreiben das dynamische Verhalten eines Systems. Hierzu gehören Aktivitätsdiagramme, die den Ablauf von Aktivitäten und Workflows zeigen. Zustandsdiagramme modellieren den Lebenszyklus eines Objekts mit verschiedenen Zuständen und Übergängen. Use-Case-Diagramme definieren die Interaktionen zwischen einem System und seinen Benutzern. Diese Modelle bieten eine ganzheitliche Sicht auf das Verhalten und die Funktionalität eines Software- oder Informationssystems.
Im Folgenden werden einige arten im detail beschrieben.

[1b,28b]

###### Zustandsdiagramme
Zustandsdiagramme in der UML bieten eine visuelle Darstellung des Verhaltens von Systemen und Entitäten über verschiedene Zustände. Einige Aspekte von Zustandsdiagrammen sind:

**Zustände:** Die verschiedenen Phasen oder Bedingungen, in denen sich das System befinden kann.

**Übergänge:** Die möglichen Wege zwischen den Zuständen, die durch Ereignisse ausgelöst werden.

**Ereignisse:** Die Trigger oder Aktionen, die einen Übergang von einem Zustand zum anderen auslösen.

**Aktionen:** Die Aktivitäten, die beim Eintritt oder Verlassen eines Zustands ausgeführt werden können.

**Start- und Endzustände:** Zeigen den Beginn und das Ende des Lebenszyklus des Systems an.

**Hierarchie:** Die Möglichkeit, Zustände hierarchisch zu organisieren, um komplexe Systeme zu modellieren.

**Nebenläufigkeit:** Die Darstellung von gleichzeitig stattfindenden Zustandsänderungen im System.

**Bedingungen:** Die Festlegung von Bedingungen, unter denen bestimmte Übergänge stattfinden.

[1b,29b]

###### Aktivitätsdiagramme
Aktivitätsdiagramme in der UML sind dazu da, den Ablauf von Aktivitäten oder Geschäftsprozessen zu modellieren.

**Aktivitäten:** Die verschiedenen Aufgaben oder Operationen, die im Prozess ausgeführt werden.

**Aktionen:** Konkrete Schritte oder Operationen innerhalb einer Aktivität.

**Entscheidungen:** Verzweigungen im Ablauf, die durch Bedingungen gesteuert werden.

**Verbindungen:** Pfeile, die den Ablauf zwischen verschiedenen Aktivitäten und Aktionen zeigen.

**Start- und Endpunkte:** Markieren den Beginn und das Ende des Diagramms bzw. einer Aktivität.

**Gabelungen und Zusammenführungen:** Darstellung von parallelen Prozessen und ihrer Zusammenführung.

**Schleifen:** Wiederholte Ausführung bestimmter Aktivitäten basierend auf Bedingungen.

**Objekte und Ressourcen:** Die Einbindung von Objekten oder Ressourcen in den Ablauf.

**Flusssteuerung:** Die Kontrolle des Ablaufs durch Entscheidungen und Schleifen.

**Aktionsflüsse:** Die Reihenfolge, in der die Aktionen innerhalb einer Aktivität ausgeführt werden.

[1b,30b]

###### Sequenzdiagramme
Sequenzdiagramme in der UML dienen dazu, Interaktionen zwischen Objekten zeitlich geordnet darzustellen.

**Lebenslinien:** Vertikale Linien, die Objekte repräsentieren und ihren zeitlichen Verlauf anzeigen.

**Nachrichten:** Horizontale Pfeile, die Kommunikation oder Interaktionen zwischen Objekten repräsentieren.

**Aktivierungsboxen:** Rechteckige Boxen über den Lebenslinien, die anzeigen, wann ein Objekt aktiv ist und Nachrichten sendet oder empfängt.

**Fragmente:** Teile des Diagramms, die bedingte oder wiederholte Abläufe darstellen, wie z.B. Alternativen und Schleifen.

**Rückgaben:** Pfeile, die die Rückgabe von einer Aktivierungsbox zu einer vorherigen Position zeigen.

**Zusammenfassungen:** Gruppierungen von Nachrichten, um komplexe Interaktionen zu strukturieren und zu vereinfachen.

**Objekte:** Entitäten, die an der Interaktion teilnehmen, mit ihren Namen und optionalen Klassen.

**Aktionsauslöser:** Ereignisse, die den Beginn von Aktivitäten oder Nachrichten auslösen.

**Dauer:** Zeitliche Dauer von Aktivitäten und Interaktionen.

**Systemgrenzen:** Abgrenzungen, die den Anwendungsbereich der Interaktionen zeigen.

[1b,31b]

#### Software Architecture Documentation
Die Dokumentation von Softwarearchitekturen ist entscheidend, um ein umfassendes Verständnis für die Struktur und das Design eines Software-Systems zu vermitteln. Einige wichtige Punkte die Inhalt der Softwarearchitekturdokumentation sein sollten:

**Architekturbeschreibung:**
Eine umfassende Beschreibung der Architektur, einschließlich der wichtigsten Komponenten, deren Zusammenspiel und der zugrunde liegenden Designprinzipien.

**Architekturdiagramme:**
Visuelle Darstellungen, die die Struktur und Beziehungen der Softwarekomponenten verdeutlichen. Dazu gehören beispielsweise Klassendiagramme, Paketdiagramme und Sequenzdiagramme.

**Schnittstellen:**
Klare Spezifikationen der Schnittstellen zwischen verschiedenen Systemkomponenten, einschließlich Datenformate, Protokolle und API-Definitionen.

**Qualitätsattribute:**
Dokumentation der nicht-funktionalen Anforderungen, wie Leistung, Sicherheit, Wartbarkeit und Skalierbarkeit, sowie Maßnahmen zur Erfüllung dieser Anforderungen.

**Entscheidungslogik:**
Aufzeichnung von Architekturentscheidungen, um den Hintergrund und die Motivation hinter bestimmten Design- und Implementierungsentscheidungen zu verstehen.

**Muster und Best Practices:**
Integration bewährter Methoden, Entwurfsmuster und bewährter Praktiken in die Dokumentation, um die Wartbarkeit und Erweiterbarkeit des Systems zu fördern.

**Komponentenübersicht:**
Eine detaillierte Liste aller Hauptkomponenten und deren Funktionen im System.

**Abhängigkeiten:**
Eine Darstellung der Abhängigkeiten zwischen verschiedenen Komponenten und Modulen.

**Änderungshistorie:**
Eine Aufzeichnung aller Änderungen an der Architektur im Laufe der Zeit, um die Entwicklung und den Wandel des Systems nachvollziehbar zu machen.

**Deployment-Strategien:**
Informationen darüber, wie die Software in einer Produktionsumgebung bereitgestellt und skaliert wird.

[1b,32b]

##### arc42
Das arc42-Template ist ein bewährtes Dokumentationsformat für Softwarearchitekturen. Es strukturiert Architekturdokumente in 42 Kapiteln, die Aspekte von Anforderungen über Systemstruktur bis zu Qualitätsattributen abdecken. Durch diese klare Gliederung erleichtert es die umfassende und systematische Dokumentation von Softwarearchitekturen, fördert die Kommunikation im Entwicklungsteam und unterstützt die langfristige Wartbarkeit und Weiterentwicklung von Softwareprojekten. Es ist sowohl flexibel als auch umfassend und eignet sich für verschiedene Arten von Projekten und Architekturstilen.

[1b,33b]

## Referenzen

[1a]  : https://de.wikipedia.org/wiki/Softwaresystem

[2a]  : https://www.oec.uzh.ch/de/academic-programs/bachelor/it/ioe.html

[3a]  : https://de.itpedia.nl/2018/10/23/applicatie-systeem-tool-of-software-wat-is-wat/

[4a]  : https://www.christian-rehn.de/2010/11/12/se1-technische-systeme/

[5a]  : https://dimeb.informatik.uni-bremen.de/index.php?id=74&tx_ttnews[tt_news]=14&cHash=afede150dd

[6a]  : https://dewiki.de/Lexikon/Systemeigenschaften

[7a]  : https://www.managerseminare.de/Trainerkoffer/Tipps/Was-ist-kompliziert-was-ist-komplex-und-wie-erklaere-ich-das,4405

[8a]  : https://www.fh-muenster.de/eti/personen/professoren/wulff/adap-main.php

[9a]  : https://de.wikipedia.org/wiki/Lernendes_System

[10a] : https://de.wikipedia.org/wiki/Dynamisches_System_(Systemtheorie)

[11a] : https://de.wikipedia.org/wiki/Selektivit%C3%A4t_(Informatik)

[12a] : https://www.enzyklo.de/Begriff/Systemstruktur

[13a] : https://de.wikipedia.org/wiki/System

[14a] : https://digitaleneuordnung.de/blog/system-thinking/

[15a] : https://de.wikipedia.org/wiki/Systemdenken_(Systemtheorie)

[16a] : https://gfse.de/systemdenken-erklaert/prinzipien-des-systemdenkens.html

[17a] : https://chat.openai.com/c/c07d7810-1d5d-4510-ba84-2da6a5ae1401 frage: was sind intelligente softwaresysteme?

[18a] : https://de.wikipedia.org/wiki/Informationssystem

[19a] : https://chat.openai.com/c/23fa7c63-18e6-482b-a003-11dc4140cbba frage: was sind Softwaresystembausteine zb System, Subsystem, Modul, Paket, Komponente, Klasse, Interface, Funktion, etc.
[20a] : https://ambient.digital/wissen/blog/qualitaet-softwareentwicklung/#:~:text=Zum%20einen%20kann%20man%20Qualit%C3%A4t,die%20jeweils%20eigene%20Anforderungen%20haben.

[21a] : https://interim-cio.biz/artikel-projektsteuerung-teufelsquadrat

[22a] : https://inztitut.de/blog/glossar/iso-25010/

[23a] : https://de.wikipedia.org/wiki/FURPS

[24a] : https://de.wikipedia.org/wiki/Softwarequalit%C3%A4t

[25a] : https://de.wikipedia.org/wiki/Cynefin-Framework#:~:text=Das%20Cynefin%2DFramework%20%5Bk%C9%99',Erkl%C3%A4rungen%20oder%20L%C3%B6sungen%20zutreffen%20k%C3%B6nnten.

[26a] : https://innovative-trends.de/2014/12/28/no-silver-bullet-interessanter-historischer-software-engineering-artikel/

[27a] : https://www.ssoar.info/ssoar/bitstream/handle/document/63101/ssoar-2019-hellige-Software_Manufaktur_-_Software_Engineering.pdf;jsessionid=B600AE3A5E0E1A51AC944719BFD498B8?sequence=1


[1b] :https://chat.openai.com/

[2b] :https://de.wikipedia.org/wiki/Wartbarkeit

[3b] :https://www.elastic.co/de/what-is/observability

[4b] :https://inztitut.de/blog/glossar/availability/

[5b] :https://www.iks.fraunhofer.de/de/forschung/resilient-software-systems.html

[6b] :https://www.datacenter-insider.de/was-ist-performance-in-der-it-a-735949/

[7b] :https://www.microconsult.de/386-0-Qualitaet-und-Sicherheit.html

[8b] :https://chat.openai.com/: Nenne mir aspekte von reliability in softwaresystemen

[9b] :https://www.dev-insider.de/was-sind-softwaremetriken-a-813487/

[10b] :https://de.wikipedia.org/wiki/McCabe-Metrik

[11b] :https://www.dev-insider.de/was-ist-zyklomatische-komplexitaet-a-7fa40c670052685ff1c56d8169a79481/

[12b] :https://de.wikipedia.org/wiki/Kontrollflussgraph

[13b] :https://dewiki.de/Lexikon/Kontrollflussgraph

[14b] :https://www.itwissen.info/Objektorientierte-Software-Metrik.html

[15b] :https://www.itwissen.info/en/lack-of-cohesion-in-methods-LCOM-122383.html#gsc.tab=0

[16b] :https://chat.openai.com/: Gib mir ei grobes Beispiel ffür zur objektorientierten Metrik

[17b] :https://chat.openai.com/: Was für Modelle zur visualisierung von softwaresystemene gibt es?

[18b] :https://en.wikipedia.org/wiki/Rule-based_modeling

[19b] :https://www.sciencedirect.com/topics/computer-science/descriptive-model

[20b] :https://www.ibm.com/docs/de/rational-soft-arch/9.7.0?topic=diagrams-uml-models

[21b] :https://www.lucidchart.com/blog/de/typen-von-uml-diagrammen

[22b] :https://chat.openai.com/: Zuordnung der UML-Diagrammtypen zu Phasen der Softwareentwicklung

[23b] :http://gsb.download.bva.bund.de/BIT/V-Modell_XT_Bund/V-Modell%20XT%20Bund%20HTML/136ee1253ccddb89.html

[24b] :https://www.lucidchart.com/pages/de/uml-anwendungsfalldiagramm

[25b] :https://www.ibm.com/docs/de/engineering-lifecycle-management-suite/design-rhapsody/9.0.1?topic=rhapsody-structural-model

[26b] :https://de.wikipedia.org/wiki/Klassendiagramm

[27b] :https://www.google.com/search?q=UML+verteilunsdiagramme&rlz=1C1GCEA_enDE1022DE1022&oq=UML+verteilunsdiagramme&
gs_lcrp=EgZjaHJvbWUyBggAEEUYOdIBCDU0OTNqMGo0qAIAsAIA&sourceid=chrome&ie=UTF-8&safe=active&ssui=on

[28b] :https://www.tutorialspoint.com/de/object_oriented_analysis_design/ooad_uml_behavioural_diagrams.htm

[29b] :https://de.wikipedia.org/wiki/Zustandsdiagramm_(UML)

[30b] :https://www.lucidchart.com/pages/de/uml-aktivitatsdiagramme

[31b] :https://www.lucidchart.com/pages/de/uml-sequenzdiagramme

[32b] :https://www.johner-institut.de/blog/iec-62304-medizinische-software/software-architektur-dokumentation/

[33b] :https://www.arc42.de/overview/