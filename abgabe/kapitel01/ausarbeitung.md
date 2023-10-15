## Verteilte Softwaresysteme

**Def.:** Ein verteiltes SoftwareSystem, ist ein ComputerSystem
bei welchem die Software Komponenten über mehrere Rechner/Server 
verteilt sind. Dem Anwender erscheint dies als ein einziges System.

### Eigenschaften, Vorteile, Nachteile
Die Rechner sind über Netzwerke und dem Internet miteinander verbunden.



| Vorteile|Nachteile|
|:-------|:-------|
| **Skalierbarkeit:** <br> Bei steigenden Anforderungen ist das erweitern von hardware Komponenten einfacher umzusetzen|**Komplexität:**<br>* Kommunikation aufwändig mit speziellen Protokelen und Techniken * |
|**AusfallSicherheit:** <br> Bei Ausfall einzelner Komponenten ist das System nicht zwingengt komplett beeinträchtigt sondern nur Teilweise.Außerderm kann das System so gebaut werden dass mehrere Komponenten die gleiche Aufgabe erfüllen und bei Ausfällen entprächend ein anderes Gerät übernimmt|==>**Ausfallerkennung - Leslie Lamport:**<br>A distributed system is one in which the failure of a computer which you didn't even know existd can render your own computer unusable.<br> **1.** Es existsieren trotzdem abhängigkeiten, die einen stark beeinträchtigen können<br> **2.** Bei sehr großen System kann sich die suche nach dem Fehler über eine große Anzahl von Rechner als sehr zeit- und kostspielig herausstellen.|
|**Transparenz**:<br> Entwickler und Benutzer müssen nicht wissen wie bestimmte Eigenschafte auf die einzelnen Rchner verteilt sind.(Ortstransparenz, Zugriffsttransparenz, Replikationstransparenz, Namenstransparenz)||
|||


### Motivation (Warum man Verteilung braucht)
### Distributed vs decentralized
### Concurrent vs parallel
