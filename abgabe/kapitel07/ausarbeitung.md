# Kapitel 7

**Autor:** Simon Fedrau, Sascha Hahn

## Lernziele




## Softwareentwurf

**Was ist ein Softwareentwurf?**

Die erfolgreiche Entwicklung von Software erfordert ein ineinandergreifendes Vorgehen, das verschiedene Phasen, Informationen und Entscheidungen miteinander verbindet. Der Softwareentwurf beschreibt dabei einen Bauplan, der sich mit der Realisierung von definierten Anforderungen durch die Definition der Infrastruktur als technische Basis,
der Softwarearchitektur und dem Entwurf von Teilsystemen, Komponenten, Modulen und Klassen beschäftigt.

Laut IEEE 1990 bezeichnet der Softwareentwurf den Prozess der Definition der Architektur, Komponenten, Schnittstellen und anderer Merkmale eines Software(teil)systems.¹ Und der Leitfaden der Softwaretechnik SWEBOK (Software Engineering Body of Knowledge), der 15 Wissensgebiete des Software Engineerings benennt, verordnet den Softwareentwurf implizit im Software Design. Dort werden Grundlagen und Schlüsselthemen, Struktur und Architektur der Software, Design der Benutzeroberfläche, Design-Notationen sowie Strategien und Methoden festgelegt.


Wie hilft der Software-Entwurf beim Programmieren?
Ein Software-Entwurf (der einfacheren Lesbarkeit halber hier mit Bindestrich, im Deutschen sonst auch oft Softwareentwurf) ist ein Hilfsmittel für Programmiererinnen und Programmierer. Dabei wird fachspezifisches Wissen angewandt, um einen Grundriss für die Projektarbeit anzugeben.


[1a] [2a]
## Tätigkeiten im Softwareentwurf

die Infrastruktur mit Hardware, Tools und Services (bspw. Entwicklungsumgebungen, Software Development Kits, Programmiersprachen, Bibliotheken), die von den Anwendern benutzt werden, um die Software zu entwickeln,
die Softwarearchitektur (bspw. Client-Server-Architektur, Web-Architektur oder service-orientierte Architektur) und zu verwendende Betriebssysteme, Netzwerkprotokolle, Datenbanksysteme, etc.
Teilsysteme sowie die Spezifikation der Schnittstellen,
Komponenten, Module und Klassen und deren Beziehungen untereinander.
Beim Softwareentwurf geht es also darum, eine gemeinsame Basis für die Softwareentwicklung und wichtige technische Zusammenhänge zu identifizieren und festzulegen. Ziel ist es, eine Grundlage zu definieren, die leicht zu verstehen, zu ändern, zu erweitern und zu warten ist. Die Kunst der Entwicklung liegt nachfolgend darin, eine stabile Lösung zu etablieren, die dennoch so flexibel ist, dass sie spätere Variabilität erlaubt.
[1a]


Fragestellungen sind hier beispielsweise
• Welche Verteilung des Systems wird benötigt?
Bei Webanwendungen wird heute in der Regel eine sogenannte 3-
Tier-Systemarchitektur verwendet, bei Anwendungen im Intranet
kommt aber auch eine Client/Server-Architektur in Betracht. Diese Entscheidung kann sich grundlegend auf den Bauplan, also den
Entwurf auswirken.
• Welche Hardware wird eingesetzt?
Bei einem System im technischen Bereich, denken wir wieder mal
an die Steuerung eines Airbags, kann der Typ des verwendeten
Microcontrollers einen wesentlichen Einfluss auf die zu konstruierende Software haben.
• Welcher Persistenzmechanismus ist erforderlich?
Bei vielen Anwendungen werden Daten langfristig gespeichert, also
ist zu überlegen, welcher Persistenzmechanismus eingesetzt werden soll: dateibasierte Speicherung? Datenbanksystem? NoSQLSpeicherung?
• Welche Betriebssysteme und Rechnernetze müssen unterstützt werden?
Eine Frage kann auch sein, auf welchen Betriebssystemen und mit
welchen Netzprotokollen die zu erstellende Software lauffähig sein
soll. . .

[3a]





## Entwurfsziele

Ausgehend von der Anforderungsanalyse und einer ersten Skizze des
zu konstruierenden Systems in der Szenarioanalyse, muss im Entwurf
festgelegt werden:
• Technische Basis/Infrastruktur
• Softwarearchitektur
• Entwurf der Komponenten und Klassen
Diese Überlegungen müssen in einer Weise notiert werden, dass sie den
Entwicklern zugänglich und verständlich sind. Sie müssen so vollständig und konsistent sein, dass eine arbeitsteilige Erstellung der Software
möglich wird.

[3a]

### Orthogonalität


In Bezug auf Softwareentwurf bezieht sich der Begriff "Orthogonalität" auf das Entwurfsziel der Unabhängigkeit oder Trennung von verschiedenen Aspekten oder Funktionen eines Systems. Eine orthogonale Struktur im Softwareentwurf bedeutet, dass Änderungen in einer Komponente oder einem Aspekt des Systems keine unerwarteten Auswirkungen auf andere Komponenten haben sollten. Es besteht also eine klare und saubere Trennung zwischen verschiedenen Funktionen oder Verantwortlichkeiten.

Die Idee der Orthogonalität basiert auf dem Prinzip der Entkopplung. Wenn verschiedene Aspekte eines Systems orthogonal sind, können sie unabhängig voneinander verändert werden, ohne dass dies zu unerwünschten Auswirkungen auf andere Teile des Systems führt. Dies trägt zur Wartbarkeit, Erweiterbarkeit und Flexibilität des Systems bei.

Ein Beispiel für Orthogonalität im Softwareentwurf könnte in der Trennung von Benutzeroberflächenlogik und Geschäftslogik liegen. Wenn diese beiden Aspekte orthogonal zueinander sind, kann die Benutzeroberfläche geändert werden, ohne dass dies Auswirkungen auf die Geschäftslogik hat, und umgekehrt.

Die Verfolgung von Orthogonalität als Entwurfsziel hilft, komplexe Systeme zu beherrschen und erleichtert die Wartung und Weiterentwicklung der Software, da Änderungen in einem Bereich nicht unvorhersehbare Auswirkungen auf andere Bereiche haben. Es trägt auch dazu bei, den Code sauberer und leichter verständlich zu machen.
[4a]

### Niedrige Kopplung
Niedrige Kopplung:
Es muss möglich sein, Subsystem A
weitgehend auszutauschen oder zu
verändern, ohne Subsystem B zu
verändern.
Änderungen von Subsystem B
sollten nur möglichst einfache
Änderungen in Subsystem A nach
sich ziehen.


Niedrige Kopplung:
• Kopplung = Abhängigkeiten
• Einzelne Struktureinheiten sollen möglichst unabhängig voneinander
sein.

[5a]

Keine Frage, egal wie gut man einen Architekturplan hinbekommt, es wird zwangsläufig zu
Abhängigkeiten zwischen den einzelnen Bausteinen kommen. Einfach weil die einzelnen
Features und Bausteine eines gesamten Systems nicht völlig isoliert voneinander existieren
können. Bei der Festlegung einer solchen Verbindung zweier Bausteine, Kopplung genannt,
ist es immer empfehlenswert, dies auf möglichst leichtgewichtige Art und Weise zu tun.
Dabei kann dies einerseits bedeuten, tendenziell eine eher geringe Anzahl solcher Verbindungen zu haben, andererseits aber auch, dass im Zuge dieser Abhängigkeiten eine Komponente möglichst wenige Annahmen von der anderen Komponente treffen sollte. 
[6a]



#### Arten: prozedural und objektorientiert

Niedrige Kopplung ist ein Prinzip im Softwareentwurf, das darauf abzielt, die Abhängigkeiten zwischen verschiedenen Modulen oder Komponenten eines Systems zu minimieren. Eine niedrige Kopplung trägt dazu bei, dass Änderungen in einem Teil des Systems nur minimale Auswirkungen auf andere Teile haben und erhöht die Wartbarkeit, Flexibilität und Erweiterbarkeit der Software. Es gibt zwei Hauptarten der Kopplung: prozedurale Kopplung und objektorientierte Kopplung.

Prozedurale Kopplung:
Datenkopplung: Zwei Module sind datengekoppelt, wenn sie Daten miteinander teilen. Das bedeutet, dass ein Modul auf Daten einer anderen Einheit zugreift, sei es durch den direkten Zugriff auf Variablen oder durch den Austausch von Daten über Parameter.

Kontrollkopplung: Kontrollkopplung tritt auf, wenn ein Modul Informationen über den Kontrollfluss eines anderen Moduls benötigt. Das kann durch das Übergeben von Steuerinformationen über Parameter oder durch den direkten Aufruf von Steuerstrukturen wie Bedingungen oder Schleifen geschehen.

Inhaltskopplung: Inhaltskopplung tritt auf, wenn ein Modul direkt auf den internen Code eines anderen Moduls zugreift, zum Beispiel durch das Analysieren oder Modifizieren von Variablen, die im Inneren des anderen Moduls definiert sind.

Objektorientierte Kopplung:
Datenkopplung: Ähnlich wie in der prozeduralen Kopplung teilen sich objektorientierte Module Daten. Dies kann durch das direkte Lesen oder Schreiben von Datenattributen eines anderen Objekts geschehen.

Methoden- oder Nachrichtenkopplung: Diese Art der Kopplung tritt auf, wenn ein Objekt eine Methode oder Nachricht eines anderen Objekts aufruft. Dies führt zu einer Abhängigkeit zwischen den beiden Klassen.

Vererbungskopplung: Vererbungskopplung entsteht, wenn eine Klasse von einer anderen erbt. Änderungen in der Basisklasse können Auswirkungen auf die abgeleiteten Klassen haben.

Um niedrige Kopplung zu erreichen, ist es wichtig, die verschiedenen Arten der Kopplung zu minimieren. In der objektorientierten Programmierung wird oft die Verwendung von Schnittstellen (Interfaces) empfohlen, um die Kopplung zu reduzieren, da dies den Austausch von Implementierungen erleichtert, ohne die Schnittstelle zu ändern.




### Hohe Kohäsion

Hohe Kohäsion:
Subsystem B darf keine Information
und Funktionalität enthalten, die zum
Zuständigkeitsbereich von A gehört
und umgekehrt.

Hohe Kohäsion:
• Kohäsion = "Zusammenhalt"
• Die Dinge sollen in Struktureinheiten zusammengefasst werden,
die inhaltlich zusammengehören.

[5a]



## Entwurfsprinzipien

### Abstraktion

Der Begriff Abstraktion wird in der Informatik sehr häufig eingesetzt und beschreibt die Trennung zwischen Konzept und Umsetzung. Strukturen werden dabei über ihre Bedeutung definiert, während die detaillierten Informationen über die Funktionsweise verborgen bleiben. Abstraktion zielt darauf ab, die Details der Implementierung nicht zu berücksichtigen und daraus ein allgemeines Schema zur Lösung des Problems abzuleiten. Ein Computerprogramm kann so unterschiedliche Abstraktionsebenen aufweisen, wobei auf jeder Ebene ein anderer Grad des Informationsgehaltes dem Programmierer preisgegeben wird. Eine Abstraktion auf niedriger Stufe beinhaltet Details zur Hardware, auf der das Programm läuft. Höher liegende Abstraktionsebenen beschäftigen sich dagegen mit der Geschäftslogik der Software.

Abstraktion beschäftigt sich also genau mit dem Detailgrad eines Objektes, der gerade im Kontext der aktuellen Perspektive benötigt wird, und kann auf die Daten sowie die Steuerung eines Programmes angewendet werden:
[7a]

### Modularität

Modularer Entwurf oder Modularität im Entwurf ist ein Entwurfsprinzip, das ein System in kleinere Teile unterteilt, die als Module bezeichnet werden (z. B. modulare Prozesskufen ), die unabhängig voneinander erstellt, geändert, ersetzt oder mit anderen Modulen oder zwischen verschiedenen Systemen ausgetauscht werden können.

Modularität bezieht sich auf die Aufteilung eines Systems in unabhängige, wiederverwendbare Module oder Komponenten. Jedes Modul erfüllt eine bestimmte Funktion oder Aufgabe und kann unabhängig entwickelt, getestet, gewartet und wiederverwendet werden. Dies erleichtert die Skalierbarkeit und Wartung des Systems.

[8a]


### Law of demeter

Das Gesetz von Demeter (englisch Law of Demeter, kurz LoD) ist eine Entwurfs-Richtlinie in der objektorientierten Softwareentwicklung. Sie besagt im Wesentlichen, dass Objekte nur mit Objekten in ihrer unmittelbaren Umgebung kommunizieren sollen. Dadurch soll die Kopplung (das heißt die Anzahl von Abhängigkeiten) in einem Softwaresystem verringert und somit die Wartbarkeit erhöht werden. Es wird deswegen manchmal auch als „Prinzip der Verschwiegenheit“ bezeichnet.

Die Law of Demeter (LoD) besagt, dass ein Modul nur mit seinen direkten Nachbarn kommunizieren sollte und nicht mit entfernten Modulen. Dies reduziert die Kopplung zwischen verschiedenen Teilen des Systems und verbessert die Wartbarkeit, da Änderungen in einem Modul weniger wahrscheinlich Auswirkungen auf andere Module haben.

[9a]


### Dependency Injection, Inversion of Control

**Inversion of Control**

Das Programmierprinzip "Inversion of Control" (IoC) bezeichnet die Umkehrung des herkömmlichen Kontrollflusses eines Programms. In einem traditionellen Ansatz ruft der vom Entwickler geschriebene Programmcode Ressourcen aus Bibliotheken auf, um diese zu nutzen, und die Objekte sind statisch miteinander verbunden.

Mit IoC greift der Kontrollfluss stattdessen dynamisch aus dem Framework auf den benutzerdefinierten Code des Entwicklers zu. Dabei sind Framework und benutzerdefinierter Code nur noch lose miteinander gekoppelt.

Die Vorteile von Inversion of Control sind vielfältig:

Locker gekoppelte Abhängigkeiten: Durch IoC sind die Abhängigkeiten zwischen verschiedenen Teilen des Codes locker gekoppelt. Dies erleichtert die Wartung und Änderungen, da ein Modul unabhängig von anderen entwickelt werden kann.

Entkoppelung von Implementierung und Ausführung: IoC ermöglicht eine klare Trennung zwischen der Implementierung einer Aufgabe und ihrer Ausführung. Dies führt zu besser wartbarem und erweiterbarem Code.

Leichtere Modularisierung: Programme können einfacher modular gestaltet werden, insbesondere bei komplexem Code. Module können unabhängiger voneinander gestaltet werden, was die Wartung und Entwicklung erleichtert.

Flexibilität bei Implementierungen: Durch die Entkopplung können wiederverwendbare Teile des Codes unabhängig entwickelt werden. Es wird einfacher, zwischen verschiedenen Implementierungen, beispielsweise von verschiedenen Frameworks, zu wechseln.

Einfacherer Austausch von Modulen: Der Austausch einzelner Module hat weniger unvorhergesehene Auswirkungen auf das Gesamtprojekt. Dies macht das System robuster gegenüber Änderungen und Erweiterungen.

Verbessertes Testen: Da Komponenten besser voneinander isoliert sind, wird das Testen der Software einfacher. Änderungen an einem Modul haben weniger wahrscheinlich Auswirkungen auf andere Teile des Systems.

Zusammengefasst bietet Inversion of Control eine flexible und wartungsfreundliche Herangehensweise an die Softwareentwicklung, bei der die Steuerung des Programms nicht mehr ausschließlich vom Entwickler, sondern auch vom Framework übernommen wird. Dies führt zu locker gekoppelten, modularen und leicht wartbaren Codebasen.

[10a]

**Dependency Injection**

Das Dependency Inversion Principle beschäftigt sich mit der Entkopplung von Softwaremodulen untereinander. Vereinfacht gesagt besagt es, dass zwei konkrete Klassen nicht direkt von einandere abhängen sollen (und damit eng gekoppelt sind), sondern die Abhängigkeit über ein Interface (eine abstrakte Struktur) realisiert werden sollte.

Es ist eines der fünf grundlegenden S.O.L.I.D.-Prinzipien, die Robert C. Martin in seinem Clean Code-Buch veröffentlicht hat.

Kokreter besagt es, dass high level-Module nicht direkt von low level-Modulen abhängen sollen.
Die Abhängigkeit soll also aufgelöst werden, in dem ein Interface die Abhängigkeit zwischen Client und Server entkoppelt. Das Interface wird von der High-Level-Klasse genutzt und von der Low-Level-Klasse implementiert:
[11a]


### Separation of Concerns

Trennung von Zuständigkeiten(Separation of Concerns) ist ein Konzept welches auf Datenkapselung aufbaut.

Die Idee besteht darin Zuständigkeiten Klassen zu zuordnen.

Alle Aufgaben die in einen Bereich fallen sollen möglichst von genau einer Klasse implementiert werden. Ziel ist es, dass unabhängige Dinge auch in der Implementierung unabhängig voneinander bleiben. Hierdurch

sinkt die Gesamtkomplexität und Systeme sind einfacher zu verstehen 
unterschiedliche Komponenten können unabhängig von einander gepflegt werden
Fehler in einem Bereich sollen sich möglichst nicht in einem anderen Bereich bemerkbar machen
Ziel ist es Klassen so zu modellieren, dass sie möglichst in sich abgeschlossen sind.

Ein Beispiel hierfür:

Die Webarchitektur
html (Hypertext Markup Language) ist die Seitenbeschreibungssprache
css (Cascading Style Sheets) ist die Sprache zur Beschreibung des Layouts der Seite (getrennt vom Inhalt)
http ist das Protokoll zur Übertragung der html Seiten (getrennt vom Inhalt)

[12a]

Ein Leitprinzip beim Entwickeln ist das Separation of Concerns. Dieses Prinzip macht geltend, dass Software basierend auf der Arbeit, die von dieser ausgeführt wird, getrennt werden soll. Ein Beispiel hierfür ist eine Anwendung, die Logik zur Identifizierung von wichtigen Elementen enthält, die dem Benutzer angezeigt werden sollen, und die diese Elemente in einer Art und Weise formatiert, sodass diese auffälliger werden. Das Verhalten, das dafür verantwortlich ist, welche Elemente formatiert werden, sollte von dem Verhalten getrennt werden, das für das Formatieren der Elemente verantwortlich ist, da diese Verhaltensweisen separate Aspekte sind, die nur zufällig miteinander in Verbindung stehen.

Anwendungen können – architektonisch gesehen – logisch erstellt werden, um diesen Prinzipien zu folgen, indem das grundlegende Geschäftsverhalten von der Infrastruktur und der Logik der Benutzeroberfläche getrennt wird. Im Idealfall sollten sich Geschäftsregeln und Logik in einem separaten Projekt befinden, das nicht von anderen Projekten in der Anwendung abhängig sein darf. Diese Trennung trägt dazu bei, dass das Geschäftsmodell leicht zu testen ist und sich weiterentwickeln kann, ohne dass es eng an die Details der Implementierung auf niedriger Ebene gekoppelt ist (sie ist auch dann hilfreich, wenn Infrastrukturbelange von Abstraktionen abhängen, die in der Geschäftsschicht definiert sind). Die Separation of Concerns spielt im Hinblick auf die Verwendung von Schichten in Anwendungsarchitekturen eine wichtige Rolle.
[16a]



### Keep It Stupid Simple

KISS ist ein Akronym und steht für “Keep It Simple and Stupid”, also “mache es so einfach wie möglich”. Da sich diese universelle Aussage auf sehr viele Bereiche und Situationen anwenden lässt, wird auch gerne vom KISS-Prinzip gesprochen. Als Prinzip rückt es die Einfachheit in den Fokus, sowohl als Mittel als auch als Ziel. Es fordert, Dinge nicht zu kompliziert zu sehen oder zu machen, und stets die einfachste Lösung für ein Problem zu suchen oder zu nutzen.

Das KISS-Prinzip wird Clarence Kelly Johnson zugeschrieben, einem Ingenieur, der in der Forschungs- und Konstruktionsabteilung SkunkWorks des Flugzeugbauers Lockheed Martin tätig war. Johnson formulierte 1996 die sogenannten Basic Operating Rules of Lockheeds SkunkWorks.¹ Interessanterweise taucht das Akronym KISS nicht ein einziges Mal in den Ausführungen auf.
[13a]
Das Prinzip KISS bedeutet, dass Systeme möglichst einfach und nicht
komplex sein sollen.
Dieses Prinzip hört sich einfach an, ist aber wirkungsvoll. Generell gilt, dass es in
einem komplexen System sehr schwierig sein kann, nachträglich Änderungen und Erweiterungen durchzuführen, ohne die Stabilität des Systems zu gefährden.

KISS fordert Einfachheit. Dieses Prinzip sollte beherzigt werden,
auch wenn seine Umsetzung nicht immer einfach ist.
Prinzipiell ist es leichter, beim Bau eines Systems eine komplexe
Systemarchitektur zu finden als eine besonders einfache. Vorsicht!
Vorteile von KISS sind:
• Einfachere Konstruktion des Systems
Einfache Systeme sind leichter zu verstehen, zu bauen, zu testen, zu ändern und
zu warten als komplexe Systeme.30

[14a]





### You Ain’t Gonna Need It

YAGNI ist ein Akronym und steht für “You Ain’t Gonna Need It”, also “Du wirst es nicht benötigen”. Es adressiert Entwickler, die gerne vorausdenken und zusätzliche Funktionen programmieren, in der Annahme, diese zu einem späteren Zeitpunkt zu benötigen.

Das YAGNI-Prinzip ist im Kontext des Extreme Programming (XP) entstanden und ist ein Prinzip von Clean Code. Es fordert, diese häufig gelebte Praxis zu unterbinden und lediglich die Features zu implementieren, die konkret benötigt, besprochen oder beauftragt wurden.

Das YAGNI-Prinzip und das KISS-Prinzip ergänzen sich. Das KISS-Prinzip – Keep It Simple and Stupid – sucht nach einer möglichst einfachen Lösung zu einer Aufgabenstellung. “Kompliziert kann jeder”, aber die Kunst liegt in der Einfachheit einer Lösung. Das YAGNI-Prinzip ergänzt KISS, in dem es die Frage “brauchen wir dies wirklich” stellt, und damit die Antwort in Richtung der Vermeidung von Aufwänden lenkt.

[15a]

### Don't repeat yourself

Don’t repeat yourself (DRY, englisch für „wiederhole dich nicht“; auch bekannt als once and only once „einmal und nur einmal“) ist ein Prinzip, das besagt, Redundanz zu vermeiden oder zumindest zu reduzieren. Es handelt sich hierbei auch um ein Prinzip von Clean Code.
[17a]

Die Anwendung sollte kein Verhalten angeben, das mit einem bestimmten Konzept in mehreren Bereichen im Zusammenhang steht, da diese Methode eine bekannte Fehlerquelle ist. Zu einem späteren Zeitpunkt können geänderte Anforderungen dazu führen, dass dieses Verhalten geändert werden muss. Es ist wahrscheinlich, dass mindestens eine Instanz des Verhaltens nicht aktualisiert werden kann, und das System wird sich inkonsistent verhalten.

Kapseln Sie die Logik in einem Programmierungskonstrukt anstatt sie zu duplizieren. Machen Sie dieses Konstrukt zur einzelnen Autorität über dieses Verhalten. Ein anderer Teil der Anwendung, die dieses Verhalten erfordert, verwendet dann dieses neue Konstrukt.
[16a]


### Composition Over Inheritance

Composition Over Inheritance betont die Verwendung von Komposition anstelle von Vererbung, um die Flexibilität und Wartbarkeit des Codes zu erhöhen. Anstatt Klassen hierarchisch zu erweitern, sollten sie durch die Kombination von kleineren, unabhängigen Klassen aufgebaut werden.

Bei diesem Entwurfsprinzip werden Algorithmen, die in einer Klasse Verwendung finden können, als separate Klassen entworfen, die vorzugsweise von Schnittstellen abgeleitet sind. Die Klassen, die eventuell einen dieser Algorithmen ausführen sollen, beinhalten eine Membervariable des Typs der gemeinsamen Schnittstelle, der (auch zur Laufzeit) einer dieser Algorithmen zugewiesen werden kann. Dadurch sind die Klassen von den Algorithmen und deren Details getrennt – weitere Entwicklungen und Änderungen an den Algorithmenklassen haben kaum Einfluss auf die Klasse, was Anpassungen unnötig macht. Dadurch wird der Code nicht verändert, was wiederum ein anderes Entwurfsprinzip, das Open-Closed-Prinzip, befürwortet.[1]



### Clean Code SOLID-Prinzipien

Um die Erstellung guten Codes zu erleichtern, wurden mehrere Prinzipien für die Softwareentwicklung formuliert. Diese können als eine Art Checkliste gesehen werden, die in der täglichen Arbeit des Entwicklers als Hilfe dienen, die eigene Arbeit zu reflektieren bzw. von vornherein Fehler und kritische Konstrukte zu vermeiden.

Prominente Vertreter solcher Prinzipien sind die SOLID-Prinzipien. SOLID wurde von Robert C. Martin geprägt. Es ist ein Akronym und steht für:

Single-Responsibility-Prinzip
Open-Closed-Prinzip
Liskovsches Substitutionsprinzip
Interface-Segregation-Prinzip
Dependency-Inversion-Prinzip
Wenn diese Prinzipien eingehalten werden, entsteht besserer Code, und die Software wird besser wartbar.
[19a]

#### Single Responsibility Principle
Das Single-Responsibility-Prinzip besagt, dass eine Klasse nur eine Verantwortlichkeit haben soll. Änderungen an der Funktionalität sollen nur Auswirkungen auf wenige Klassen haben. Je mehr Code geändert werden muss, desto höher ist das Fehlerrisiko.

Hält man sich nicht an dieses Prinzip, verursacht das zu viele Abhängigkeiten und hohe Vernetzung. Das ist wie im wirklichen Leben: Ab einer bestimmten Größe wird ein Universalwerkzeug unhandlich.

Wie kann erkannt werden, ob die Klasse mehr als eine Aufgabe erfüllt?
Die Klasse darf nur einen Grund zur Änderung haben. Wenn sich zwei Anforderungen ändern, darf nur eine davon eine Auswirkung auf die Klasse haben. Hat die Klasse mehrere Änderungsgründe, erfüllt sie zu viele Aufgaben.

Es ist also besser, viele kleine Klassen zu haben als wenige große.
Der Code wird dadurch nicht umfangreicher – er wird nur anders organisiert. Analogie aus dem Bastelkeller: Wenn alle Schrauben in einer Kiste liegen, ist es schwer, die Richtige zu finden. Sind sie gut sortiert auf mehrere Schachteln verteilt, geht das Suchen viel schneller. Genauso verhält es sich mit den Klassen.
[19a]


#### Open-Closed Principle

Nach dem Open-Closed-Prinzip soll eine Klasse offen für Erweiterungen, aber geschlossen gegenüber Modifikationen sein. Das Verhalten einer Klasse darf erweitert, aber nicht verändert werden. Dieses Prinzip hilft, Fehler in schon fertigen Codeteilen zu vermeiden. Wenn eine Erweiterung nur durch Änderungen innerhalb einer Klasse erreicht werden kann, ist die Gefahr sehr groß, dass durch die Änderung schon fertig implementierte Funktionen neue Fehler bekommen.

Das Open-Closed-Prinzip lässt sich normalerweise über zwei Wege erreichen:

Vererbung
Einsatz von Interfaces
Durch Einhalten dieses Prinzips können einer Applikation neue Funktionen hinzugefügt werden, ohne bestehende Klassen zu verändern.

Um einen eigenen Datentypen sortieren zu können, muss nicht die qsort-Funktion umgeschrieben werden. Der Algorithmus bleibt immer gleich. Der Anwender muss dem Algorithmus lediglich seine eigene Vergleichsfunktion übergeben. Damit wird eine Erweiterbarkeit erreicht, ohne den Algorithmus verändern zu müssen.



#### Liskov Substitution Principle

Das Liskovsche Substitutionsprinzip fordert, dass abgeleitete Klassen immer anstelle ihrer Basisklasse einsetzbar sein müssen. Subtypen müssen sich so verhalten wie ihr Basistyp. Das klingt selbstverständlich, aber ist es das auch? Der Compiler weiß, dass eine abgeleitete Klasse auch vom Typ der Basisklasse ist – also immer in diese konvertiert werden kann. Ist das ausreichend? Das Liskovsche Substitutionsprinzip geht weiter als der Compiler.
Wenn eine Methode einen Parameter vom Typ Base (aus Bild 1) erwartet, z.B. public void TuWasTolles(Base b), darf es keinen Unterschied machen, ob ein Objekt vom Typ Base oder vom abgeleiteten Typ Derived übergeben wird. In der Klasse Derived muss sichergestellt werden, dass das Verhalten aus Sicht der Methode TuWasTolles() identisch ist wie bei der Klasse Base.

Wenn z.B. die Methode der Basisklasse keine Exceptions wirft, darf auch die Methode der abgeleiteten Klasse keine Exceptions werfen. Eine abgeleitete Klasse darf ihre Basisklasse erweitern, aber nicht einschränken oder verändern. Leider wird dieses Prinzip oft missachtet. Unit-Tests können sicherstellen, dass nicht versehentlich ein Verstoß gegen das Liskovsche Substitutionsprinzip in die Software eingebaut wird.
[19a]


#### Interface Segregation Principle

Das Interface-Segregation-Prinzip besagt, dass ein Client nicht von den Funktionen eines Servers abhängig sein darf, die er gar nicht benötigt. Ein Interface darf demnach nur die Funktionen enthalten, die auch wirklich eng zusammengehören. Die Problematik ist, dass durch „fette“ Interfaces Kopplungen zwischen den ansonsten unabhängigen Clients entstehen.

Wird ein Aspekt des Interfaces verändert, hat das Auswirkung auf alle Clients – selbst wenn sie diesen Aspekt nicht nutzen. Ein anschauliches Beispiel liefert hier die AWT-Bibliothek von Java: Soll lediglich auf das Ereignis zum Schließen des Fensters reagiert werden, müssen alle Methoden des Interfaces WindowListener implementiert werden.
Was kann getan werden, wenn so ein Interface vorliegt und nicht geändert werden kann? Es kann ein Adapter eingesetzt werden (Adapter-Entwurfsmuster). Dieser Adapter implementiert alle Methoden des Interfaces mit einer Dummy-Implementierung und stellt diese virtuell zur Verfügung. Auch hier dient die AWT-Bibliothek von Java als Beispiel. Diese stellt solch einen Adapter für das vorher gezeigte Beispiel bereit.
[19a]

#### Dependency Inversion Principle

Das Dependency-Inversion-Prinzip besagt, dass Klassen auf einem höheren Abstraktionslevel nicht von Klassen auf einem niedrigen Abstraktionslevel abhängig sein sollen. Dabei geht es nicht darum, die Abhängigkeiten einfach umzudrehen. Abhängigkeiten zwischen Klassen soll es nicht mehr geben; es sollen nur noch Abhängigkeiten zu Interfaces bestehen (beidseitig). Interfaces sollen nicht von Details abhängig sein, sondern Details von Interfaces. Beispiel: Die Klassen in Bild 4 sind zu stark miteinander verkoppelt.
[19a]


### Jeweils Implementierungsbeispiel







## Entwurfsmuster (Design Patterns)
### Vergleich von Mustern, Algorithmen und Frameworks
### Entkopplungsmuster
#### Repository-, Plugin-, Bridge-, Visitor-Pattern
##### Entwurfsproblem, das die Entwurfsmuster lösen
##### UML-Diagramme zur Visualisierung der Entwurfsmuster
##### Klassendiagramm, Sequenzdiagramm
##### Anwendungsbeispiele
##### Implementierungsbeispiel
### Weitere Entwurfsmuster, die Sie als relevant erachten
#### (Bitte keine weiteren "Gang of Four Patterns")
## Entwurf des Datenmodells
### Domain-Driven Design
#### Domain vs. Model
#### Domain-Driven Design Prozess
#### Entities, value objects, aggregates, services, factories
#### Ubiquitäre Sprache
#### Anemic Domain Model
#### Beispiel, Vorteile, Nachteile
## Entwurf der Benutzerschnittstelle
### UI Modelling
#### Wireframe vs Storyboard vs Wireflow vs Mockup vs Prototyping
### Usability vs. User experience (UX) vs. Customer experience (CX)
### Nielsen's 10 Usability Heuristic Prinzipien für das UI-Design
### Shneidermans's 8 Golden Rules
### Norman's 7 Principles


## Zusammenfassung


## Referenzen

[1a] : https://t2informatik.de/wissen-kompakt/softwareentwurf/
[2a] : https://www.dev-insider.de/was-ist-ein-software-entwurf-a-ac9e018da98039bb8e4744beaa9a126f/
[3a] : https://esb-dev.github.io/mat/swt-entwurf-l.pdf
[4a] : https://chat.openai.com/c/e5ef4299-1f76-491e-b216-d702c8ec98ae frage: was ist was ist Orthogonalität im Entwurfsziel?
[5a] : https://www.isf.cs.tu-bs.de/cms/teaching/2012w/se1/VL5.pdf 
[6a] : https://beckassets.blob.core.windows.net/product/readingsample/23641827/23641827_leseprobe.pdf
[7a] : https://de.wikipedia.org/wiki/Abstraktion_(Informatik)
[8a] : https://de.wikipedia.org/wiki/Modularit%C3%A4t#Funktionsprinzipien
[9a] : https://de.wikipedia.org/wiki/Gesetz_von_Demeter#:~:text=Das%20Gesetz%20von%20Demeter%20(englisch,ihrer%20unmittelbaren%20Umgebung%20kommunizieren%20sollen.

[10a] : https://www.dev-insider.de/was-bedeutet-inversion-of-control-a-1110688/
[11a] : https://oer-informatik.de/dependency-injection
[12a] : http://www.scalingbits.com/java/javakurs1/oop/architektur
[13a] : https://t2informatik.de/wissen-kompakt/kiss-prinzip/
[14a] : Entwurfsprinzipien und Konstruktionskonzepte der Softwaretechnik : Link zum Buch : https://link.springer.com/chapter/10.1007/978-3-658-20055-8_3
[15a] : https://t2informatik.de/wissen-kompakt/yagni-prinzip/ 
[16a] : https://learn.microsoft.com/de-de/dotnet/architecture/modern-web-apps-azure/architectural-principles
[17a] : https://de.wikipedia.org/wiki/Don%E2%80%99t_repeat_yourself
[18a] : https://de.wikipedia.org/wiki/Komposition_an_Stelle_von_Vererbung
[19a] : https://www.microconsult.de/blog/2019/05/fl_solid-prinzipien/





