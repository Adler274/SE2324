## Verteilte Softwaresysteme

**Def.:** Ein verteiltes SoftwareSystem, ist ein ComputerSystem
bei welchem die Software Komponenten über mehrere Rechner/Server 
verteilt sind. Dem Anwender erscheint dies als ein einziges System.

### Eigenschaften, Vorteile, Nachteile
Verteilte Systeme ermöglichen es die Leistungsfähigkeit eines Systems zu erhöhen, indem die Aufgaben auf mehrere Rechner verteilt werden. Die Rechner sind über Netzwerke und dem Internet miteinander verbunden und kommunizieren über bestimmte protokolle miteinander.
Im Nachfolgenden sind einige Vor- und Nachteile aufgelistet.


| Vorteile|Nachteile|
|:-------|:-------|
|**Skalierbarkeit:** <br> Bei steigenden Anforderungen ist das erweitern von hardware Komponenten einfacher umzusetzen|**Komplexität:**<br>Kommunikation aufwändig mit speziellen Protokolen und Techniken<br>Koordinierung von Aktivitäten:Mechanismen zur Synchronisation und Koordininierung<br>|
|**AusfallSicherheit:** <br> Bei Ausfall einzelner Komponenten ist das System nicht zwingengt komplett beeinträchtigt sondern nur Teilweise.Außerderm kann das System so gebaut werden dass mehrere Komponenten die gleiche Aufgabe erfüllen und bei Ausfällen entprächend ein anderes Gerät übernimmt|==>**Ausfallerkennung - Leslie Lamport:**<br>A distributed system is one in which the failure of a computer which you didn't even know existd can render your own computer unusable.<br> **1.** Es existsieren trotzdem abhängigkeiten, die einen stark beeinträchtigen können<br> **2.** Bei sehr großen System kann sich die suche nach dem Fehler über eine große Anzahl von Rechner als sehr zeit- und kostspielig herausstellen.|
|**Transparenz**:<br> Entwickler und Benutzer müssen nicht wissen wie bestimmte Eigenschafte auf die einzelnen Rchner verteilt sind.(Ortstransparenz, Zugriffsttransparenz, Replikationstransparenz, Namenstransparenz)|**Datensicherheit:**Daten müssen massiver gegen Angriffe geschnützt werden, da es mehrere Angriffspunkte gibt.|
|**Heterogenität:**<br>das System kann aus verschiedenen Hardware- und Softwarekomponenten besteht, was mehr möglichkeiten bietet.|


### Motivation (Warum man Verteilung braucht)
Wie schon bei den Vor- und Nachteilen zu sehen bieten verteilte Systeme viele möglichkeiten zur Systemverbesserung, wie z.B. die Skalierbarkeit, Ausfallsicherheit, Transparenz und Heterognetität. Diese Eigenschaften sind in der heutigen Zeit sehr wichtig, da die Anforderungen an die Systeme immer weiter steigen. Verteilte Systeme sind zwar deutlich komplexer und aufwändiger zu entwickeln, bieten aber die Möglichkeiten große Systeme anforderungsgerecht aufzubauen.

### Distributed vs decentralized
Wie wir schon wissen beziehen sich Distributed(Verteilte) Systeme auf die Verteilung der Software auf physisch getrennte Geräte.
Jetzt stellt sich die Frage was mit einem dezentrallene System gemeint ist. Ein dezentrallenes System ist ein System, bei dem die *Entscheidungen* nicht von einer zentralen Instanz getroffen werden, sondern von mehreren/verteilten Instanzen.
Beispiele hierfür sind z.B. Cryptowährungen oder allgemein die Blockchain-Technologie. Hierbei werden die Entscheidungen von mehreren Instanzen getroffen, die sich gegenseitig überprüfen und somit die Sicherheit des Systems gewährleisten.[3]

### Concurrent vs parallel



## Referenzen
[1]: https://www.youtube.com/watch?v=MYjQWiDDdVQ&list=PLcVYkCRLcLtGHzfmkfYjdN8Ai9tkHaHvi&index=2
[2]: https://www.youtube.com/watch?v=RR_iiLYTdDM
[3]: https://www.hivenet.com/post/decentralized-or-distributed-whats-the-big-difference#:~:text=In%20a%20decentralized%20system%2C%20control,sharing%20of%20resources%20and%20workloads.
