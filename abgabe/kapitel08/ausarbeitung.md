# Ausarbeitung 8
**Autor:** Simon Fedrau, Sascha Hahn

## Lernziele:

* Lernen, was Use Cases ist und welche Ziele er hat.
* Wissen, was hinter INVEST steckt.
* Unterscheiden zwischen einen guten und schlechten User Storys
* Welche Methoden gibt es bei Requirements Engineering
* Welche Anforderungen gibt es
* Wie macht man eine gute Anforderungsanalyse
* Welche Arten der Dokumentation der Anforderungen gibt es

## Requirements Engineering
Bei Requirements Engineering handelt es sich um einen Prozess, der die Anforderungen an ein System oder eine Software erfasst, analysiert, dokumentiert und verwaltet.
Es ist ein wichtiger Bestandteil des Softwareentwicklungsprozesses, da es sicherstellt, dass das entwickelte System die Bedürfnisse und Erwartungen der Stakeholder erfüllt.
Wichtiger Bestandteil ist die Anforderungen genau zu erfassen, diese so gut es geht zu spezifizieren und zu verwalten.
[1a]

### Definition für "Anforderung" ("Requirement")
Anforderungen sind formulierte Bedingungen oder Spezifikationen, die beschreiben, welche Funktionen, Eigenschaften oder Qualitätsmerkmale ein System oder Produkt erfüllen oder besitzen muss, um den Bedürfnissen und Erwartungen der Stakeholder gerecht zu werden.
Anforderungen können unterschiedliche Formen annehmen, darunter funktionale Anforderungen, nichtfunktionale Anforderungen, Benutzeranforderungen und Systemanforderungen auf die später noch eingegangen werden.
In der Praxis können Anforderungen verschiedenen Stufen von abstraktion und Detail beinhlten.
[2a]

### Problemraum vs. Lösungsraum
Bei dem Problemraum handelt es sich um die Zielsetzung und die Anforderungen an das System.
Der Lösungsraum beschreibt entspricht der Realisierung/Architektur, also wie die definierten Ziele des Problemraums umgesetzt werden.
Bestimmte Anweundungsfälle können den Problemraum beschreiben, um die Erfordernisse einzugrenzen.
[3a]

### Arten von Anforderungen
Wie bereits erwähnt kann man Anforderungen in verscheidenen Kathegorien einteilen.
Darunter Fallen zum Beispiel Funktionale und  Nicht-funktionale Anforderungen.

#### Funktional
Funktionale Anforderungen haben einen direkten Bezug zur Zweckbestimmung(was das Produkt machen soll) zu dem Produkt.
Sie sind Produkt spezifisch und beschreiben die Funktionen, die ein bestimmtes Produkt erfüllen soll.
**Beispiel:**
Eine Software soll einen Wert X nach einer Formel auch genau 4 nachkommstellen berechnen.
[4a]

#### Nicht-funktional
Nicht-funktionale Anforderungen sind meist unspezifisch für ein bestimmtes Produkt
und gelten allgemein für eine Reihe von Produkten.
Es sins quasi generelle Rahmenbedingungen die generell eingahelten werden sollten.
**Beispiele:**
* Dei Software muss mindestens nach 10ms auf eine Eingabe reagieren.
* Die Software muss auf allen gängigen Browsern laufen.
* Die Software muss in der Lage sein 1000 Anfragen pro Sekunde zu verarbeiten.
[4a]

###### Qualitätsanforderungen
Qualitätsanforderungen sind spezifische Anforderungen an ein System, die sich auf qualitative Aspekte beziehen, die die Leistung, Zuverlässigkeit, Effizienz und Benutzbarkeit des Systems betreffen.
Qualitätsanforderungen lassen sich meist mit der übergruppe der Nicht-funktionalen Anfordereungen zuordnen.
Qualitätsanforderungen sind entscheidend, um sicherzustellen, dass ein Softwareprodukt nicht nur funktioniert, sondern auch bestimmte Qualitätsstandards erfüllt. Diese Anforderungen sind oft eng mit den Erwartungen und Bedürfnissen der Benutzer, Stakeholder und des Unternehmens verbunden.
[4a]

###### Randbedingungen
Der Begriff "Randbedingungen" bezieht sich auf die äußeren Umstände, Rahmenbedingungen oder Voraussetzungen, die Einfluss auf ein System oder Projekt haben. Diese Bedingungen können die Entwicklung, Implementierung oder Nutzung eines Systems beeinflussen.
z.B:
* Das System muss mit einer bestimmten Version eines Datenbankmanagementsystems kompatibel sein.
* Die Implementierung der neuen Softwareversion muss bis zum Ende des Quartals abgeschlossen sein.
* Das Budget für die Entwicklung des Systems ist begrenzt,
und das Projekt muss innerhalb dieser finanziellen Vorgaben bleiben.

[4a]
###### Rechtlich-vertragliche Anforderungen
Wie der Name bereits ähnen lässt, behndeln die Rechtlich-vertragliche Anforderungen die spezifischen Vorgaben und Verfplichtungen
die durch Vorschriften oder vertragliche Vereinbarungen festgelegt sind.
Diese Anforderungen sind entscheidend, um sicherzustellen, dass die entwickelte Software den rechtlichen Rahmenbedingungen entspricht und dass alle vertraglichen Vereinbarungen eingehalten werden.
Beispiele für solche sind Datenschutzbestimmungen, Urheberrechtsbestimmungen oder Haftungsfragen.

[4a]
###### Technologische Anforderungen
Technologische Anforderungen in Requirements Engineering beziehen sich auf die spezifischen technischen Voraussetzungen, die erfüllt sein müssen, damit das System erfolgreich entwickelt, implementiert und betrieben werden kann. Diese Anforderungen umfassen Aspekte wie Hardware, Software, Datenbanken, Netzwerke und andere technologische Ressourcen.

[4a]
###### Anforderungen an die Benutzungsoberfläche
Anforderungen an die Benutzeroberfläche (UI) beschreiben die Anforderungen an die Benutzerfreundlichkeit und das Design der Benutzeroberfläche eines Systems. Diese Anforderungen sind wichtig, um sicherzustellen, dass das System für die Benutzer einfach zu bedienen und zu navigieren ist und dass die Benutzeroberfläche ein positives Benutzererlebnis bietet.

[4a]

### Merkmale "guter" Anforderungen
Anforderungen sollten **Atomar** beschrieben sein, das heißt sie sollten unteilbar sein und
nicht mehrere Anforderungen in sich vereinen.
Sie sollten in einer Iteration abgeschlossen werden können.

Außerdem sollten sie **eindeutig** sein, was eine selbstverständliche annahme ist.
Genau heißt das aber, dass die eine einheitliche Interpretation bieten sollen und
keine zweifel bei dem verständniss der Anforderung aufkommen sollten.

**Testbarkeit** ist auch ein wichtiger Punkt. Damit die Anforderung auch im nachhinein überprüft werden kann,
muss der Aspekt der von der Anforderung beschrieben wird verifiziert und validiert werden können.

Als letzten müssen Anforderungen **notwendig** sein, damit man nicht unnötige Anforderungen hat
und in einem haufen an Anforderungen untergeht. Solche Anforderungen würden viel Zeit kosten, da man sie
umständlich herausfiltern muss.

[5a]
### Anforderungsanalyse
Um mit einem Projekt anzufngen müssen Anforderungen erstmal analysiert werden.
Nach der erstellung der Anforderungen müssen sie klassifiziert und bewertet werden.
Das heißt, dass sie in den bereits beschriebenen Kategorien eingeordnet werden und ihnen eine Priorität zugewiesen wird.
Außerdem werden sie auf Vollständigkeit überprüft und Durchgängigkeit.

Als nächstes werden die Anforderungen detailiert beschrieben und schrifflich festgehalten.
Hier werden auch wieder Anwedungsfälle beschrieben, die die Anforderungen genauer beschreiben.

Ein letzter optionaler Schritt ist Anforderungen kontinuierlich während der Implementation zu überprüfene und zu verbessern.
So können sich neue Projektzyklen ergeben, die neue Anforderungen mit sich bringen.

[6a]
##### Motivation (Warum macht man das überhaupt?)
Ziel einer Anfordereungsanalyse ist es, diese in ein durchfürhbares Projekt umzuwandeln.
Sie werden konkretisiert, strukturiert und geprüft um die sicherzustellen, dass es keine Wiedersprüche enstehen,
die Anforderungen umsetzbar sind und die Anforderungen vollständig sind.
Andernfalls kann es dazu führen, dass in Mitten der Entwicklung neue Anforderungen auftauchen
oder Anforderungen rausgeworfen werden, da sie als nicht umsetzbar erachtet werden,
was den Projektvortschritt zurückwerfen kann.
[7a]

##### Herausforderungen und Probleme bei der Anforderungsanalyse
Wenn wichtige Stakeholder nicht ausreichend in den Analyseprozess eingebunden sind, besteht die Gefahr, dass wichtige Anforderungen übersehen oder falsch verstanden werden.
Außerdem können Stakeholder notwendige Änderungen der Anforderungen nicht annehmen oder akzeptieren, wenn sie nicht ausreichend in den Prozess eingebunden sind oder das Know-How haben.

Ach Fehlende Fachkentnisse innerhalb des Entwicklungs-Teams können zu Missverständnissen und Fehlinterpretationen führen, was zu falschen Anforderungen und einer schlechten Umsetzung führen kann.

Eine Erfolgreiche Anforderungsanalyse erfodert eine gute, reibungslose Kommunikation zwischen allen Stakeholdern und dem Entwicklungsteam. Auch kontinuierliches Feedback sind ein Schlüsselaspekt.
[8a]

##### Stakeholder
In den letzten Kapiteln wurde bereits mehrmals der Begriff "Stakeholder" erwähnt, welcher Die Anfoderungen an ein Projekt stellt, aber wer sind eigentlich Stakeholder?
Stakeholder sind Personen oder Organistionen die von dem Ergebniss eines Projekts betroffen sind oder einen Einfluss auf das Projekt haben. Sie verfolgen individuelle Interessen und versuchen die Projektleitung zu ihrem vorteil zu "beeinflussen".
Stakeholder sind können z.B Kunden, Geschäftsführer, Entwickler, Tester, Marketing, Vertrieb, etc. sein.
Das heißt im Umkehrschluss, dass jeder ein Stakeholder sein kann, der von dem Projekt betroffen ist.
Stakeholder ist einfach nur ein allgemeiner Begriff der nicht eine bestimmmte Role in der Entwicklung beschreibt.
[9a]

##### SMART-Ziele
SMART ist ein Akronym für die Kriterien, die ein Ziel erfüllen sollte, um effektiv zu sein.
Es besteht aus folgenden Kriterien:

Die Ziele sollten **Spezifisch** sein, das heißt sie sollten klar und konkret formuliert sein.
Sie sollten **Messbar** sein und zuordenbar **"Assignable"** sein. Es muss also für jede Anforderung einen klaren Verantwortlichen geben.
Die Ziele sollten **Realistisch** sein, sie müssen mit den Mitteln, Randbedingungen und der Zeit erreichbar sein.
Als letzten sollten sie **Terminiert** (Time-related) sein, das heißt sie sollten einen klaren Zeitrahmen und Deaadline haben.
[10a]

##### Anforderungsquellen und Ermittlungstechniken
Anforderunungsquellen und Ermittlungstechniken beschreiben woher oder von wem die Anforderungen überhaupt erstellt werden.
Anforderungen können aus verschiedenen Quellen stammen, wie z.B. aus dem Kunden, dem Entwicklerteam, Berechtgen, Interviews, 
generell Beobachtungen, Brainstorming oder auch aus der Konkurrenz (Wettbewerbsanalyse).

Techniken um an Anforderungen zu kommen sind z.B. Use-Case Analysen, Storybording, Prototyping, Fragebogen oder andere Kreativitätstechniken.

[11a]
##### Anforderungskategorien nach Kano
Kategorien von Anforderungen wurden bereits erklärt, nun soll es aber um die Kategorien nach Kano geheb,
welche besonders die Anforderungen der Kunden umfassen.
Bei dem Kano modell geht es nähmlich um den Zusammenhang zwischen der Zufriedenheit des Kunden und der Erfüllung derer Anforderungen.
Das hört sich etwas redundant an, es geht aber im Grunde darum, dass zum Beispiel Anforderungen, die der Kunde als selbstverständlich erachtet noch nicht zu seiner Zufriedenheit führen müssen. Anders gesagt die beseitigung von Buggs führt nicht zu einer höheren Zufriedenheit.
Man muss also eine gute Mitte finden die bestimmte grund Erwartungen erfüllen aber auch eigene mit einbringen, die den Kunden positiv überraschen.

[12a]

##### Phasen und Haupttätigkeiten
Die Anforderungsanalyse kann in mehrere Phasen und Haupttätigkeiten unterteilt werden.
Als erstes werden die relevanten Stakeholder identifiziert und Ziele der Anforderungsanalyse festgelegt.
Als nächstes werden Zeit und Recourcen des Projektes geplannt, um Anforderungen richtig bewerten zu können.
Jetzt werden auch tatsächlich die Anforderungen erfasst. Dies geschieht durch die wie bereits aufgeführten Techniken und Quellen.
Auch werden bereits vorhandene Dokumente und Prjekte analysiert, um allgemeine Anforderungen festzulegen.
Dannach werden Anforderungsdokumente erstellt, die alle gesammelten Anforderungen strukturiert und verständlich darstellen.
Dabei werden auch Anwendungsfälle und Use-Cases mit eingebracht.
Die Anforderungen werden anschließend priorisiert und spezifiziert, sowie validiert und verifiziert.
Als letztes wird Feedback der Stakeholder eingholt und die Anfoderungen freigegeben.

[4a]

#### Dokumentation und Spezifikation von Anforderungen
Im folgenden werden Aspekte der Dokumentation und Spezifikation von Anforderungen erläutert.
Dabei werden verschiedene Methoden und Techniken vorgestellt die Anforderungen zu kathegorisieren, sturkturieren
und zu verwalten.

##### Lastenheft und Pflichtenheft
Lastenheft und Pflichtenheft sind Dokumente, die die Anforderungen an ein System oder eine Software beschreiben.
Als erstes wird hierbei das Lastenheft erstellt.
Diese wird hauptsächlich vom Kunden erstellt und beschreibt die rohen Anforderungen aus Sicht des Kunden.
Das Lastenheft beinhltet Kontextinformationen zu z.B. Unternehmensgröße oder IT-Infrastuktur des Kunden, sowie Funktionale und nicht funktionale Anforderungen.

Nachdem das Lastenheft bei dem Entwickler angekommen ist wird die Anforderungsanalyse begonnen.
Während dieser wird das Pflichtenheft erstellt. Dieses beinhaltet dann auch die technischen Anforderungen und die Umsetzung dieser.
Es ist nur für die Implementierung und die Abnahme des Systemes relevnat.
Außerdem ist das Pflichtenheft auch rechtlich bindend, der Kunde muss also das  Pflichtenheft abnehmen.
Es stellt sozusgen die Funktionen und Eigenschaften des Systems für den Kunden dar.

[13a]

##### Business Requirement Document (BRD) vs
Bei dem Business Requirement Document werden Informationen wie der Projekthintergrund, die Ziele, der Umfang, die beteiligten Stakeholder und ihre spezifischen Anforderungen, funktionale und nicht-funktionale Aspekte, Risiken, Annahmen, der Zeitplan, das Budget und andere relevante Details festgehalten.
Das BRD dient als zentrales Referenzdokument für alle Projektbeteiligten und bildet die Grundlage für die Planung, Umsetzung und Überwachung des Projekts.
Es unterstützt auch das Änderungsmanagement, indem es einen Prozess für die Handhabung von Anpassungen oder Ergänzungen zu den Anforderungen bereitstellt.
Anders als beim Lasten- und  Pflichtenheft konzentriert sich das BRD darauf warum das Projekt durchgeführt wird, welche Probleme es lösen soll und welche Chancen es bietet.
[14a]

##### Functional Requirement Document (FRD) vs
Das FRD beschreibt die spezifische funktionale Anforderungen an ein Projekt oder System . Anders als das Business Requirement Document (BRD), das die geschäftlichen Anforderungen und Ziele eines Projekts im Allgemeinen abdeckt, konzentriert sich das FRD auf die konkreten Funktionen und Features, die das Endprodukt bereitstellen soll.
Im Detail beschreibt es die funktionalen Anforderungen, die detailierten spezifikationen der Funktionen und die Testanforderungen.
[15a]

##### Software Requirement Specification (SRS)
Das SRS dient als formale Referenz für alle Beteiligten im Softwareentwicklungsprozess, einschließlich Entwicklern, Designern, Testern und anderen Stakeholdern. Es beinhaltet alle Anforderungen, sowie die Zielsetzung und Probleme die das System lösen soll,
die Anforderungen an die Benutzeroberfläche, die Systemarchitektur, die Datenbankstruktur, die Sicherheitsanforderungen, die Leistungsanforderungen, die Qualitätssicherungs- und Testanforderungen, die Anforderungen an die Dokumentation und die Anforderungen an die Wartung und das Support.

Bei dem SRS werden also alle Aspekte des Prjekts beschrieben und richtet sich demnach auch an alle beteiligten,
wie Entwickler, Tester, Designer, Stakeholder, etc.
[16a] 

## Use Cases

 **Es handelt sich um eine schriftliche Anleitung, die erklärt, wie Benutzer Aufgaben auf Ihrer Website durchführen können**

[1b]

## Systemkontext und Systemgrenze

  **Systemkontext**: Dies umfasst die Darstellung der Wechselwirkung eines Systems mit seiner Umgebung.

  **Systemgrenze**: Es markiert dabei die Abgrenzung zwischen dem analysierten System und seiner Umgebung


![](media/System.png)


|            |Systemkontext |Systemgrenze |
|---         |---           | ----        |
|       |  Definiert, welche Funktionen das System bereitstellen soll, sowie die Schnittstellen zu externen Systemen       |     Isoliert das geplante System von seiner Umgebung, wodurch der anpassbare Teil der Entwicklung von Aspekten in der Umgebung abgegrenzt wird, die durch den Entwicklungsprozess nicht verändert werden.        |

[7b] [5b]

### Ziele






### Szenario
***

* **Kontextanalyse:**
  Es wird untersucht wie das System mit der Umgebung interagiert. Zu betrachten sind auch externe Faktoren wie andere Systeme, Benutzer oder auch Umwelteinflüssen

* **Stakeholder-Analyse:**
  Erkennung und Zuordnung von Personen oder Gruppen, die ein Interesse am System haben, dazu gehören Nutzer, Kunden, Lieferanten und andere relevante Parteien.

* **Anforderungen identifizieren:**
  Aufnahme und Analyse der Bedürfnisse sowie Erwartungen der Stakeholder, um sicherzustellen, dass das System in der Lage ist, diesen Anforderungen gerecht zu werden.

* **Risikobewertung:** 
  Analyse möglicher Risiken sowohl innerhalb als auch außerhalb des Systems. Dies beinhaltet technische, betriebliche und organisatorische Risiken.

![:scale 90%](media/szenario.jpg)


### Spezifikation
  Bestimmt die Umgebung und den Umfang eines Systems. Dies beinhaltet:

  Systemgrenzen: Klare Definitionen, die die Abgrenzungen des Systems festlegen, was inbegriffen ist und was außerhalb liegt.


  * Kontextanalyse: Beschreibung, wie das System mit seiner Umgebung (andere Systeme, Benutzer, externe Faktoren) interagiert.
   
  * Schnittstellen: Identifizierung und Beschreibung der Berührungspunkte mit externen Elementen oder Systemen.

  * Stakeholder: Auflistung und Beschreibung der betroffenen oder beteiligten Parteien.

  * Anforderungen: Zusammenfassung der funktionalen und nichtfunktionalen Anforderungen, die durch den Kontext und die Grenzen des Systems beeinflusst werden.
 

### Use Case Diagramm

  Ein Use Case-Diagramm (auch Anwendungsfalldiagramm genannt) ist ein Verhaltensdiagramm und visualisiert die von außen sichtbare Interaktion von Akteuren mit dem zu entwickelnden System. Das Diagramm besteht aus dem System, zugehörigen Anwendungsfällen und Akteuren und setzt diese miteinander in Beziehung:
 [1b]


![](media/User-Story.PNG)


## User Stories

  Eine User Story ist eine informelle, allgemeine Erklärung eines Software-Features, die aus der Sicht des Endbenutzers verfasst wurde. Ihr Zweck ist es, zu zeigen, welchen Wert ein Software-Feature für einen Kunden hat.


### Persona vs Theme vs Epic vs User Story vs Task

  * Persona: Fiktive Darstellung eines typischen Nutzers, hilft, Nutzerbedürfnisse zu verstehen.
  
  * Theme: Hochrangiges Ziel oder Fokus, das verschiedene Aspekte des Projekts umfasst.
  
  * Epic: Große, breite Anforderung, die in kleinere Teile aufgeteilt wird, oft über mehrere Sprints hinweg.
  
  * User Story: Detaillierte Anforderung aus Nutzerperspektive, spezifisch und mit klaren Erfolgskriterien.
  
  * Task: Konkrete Arbeitsschritte innerhalb einer User Story, sehr spezifisch und  ausführungsorientiert.

[9b] [14b] 

### Functional User Story vs. Technical User Story
    
  * Funktionale User Story: 
  Konzentriert sich auf die Benutzererfahrung und -bedürfnisse, beschreibt, was der Benutzer mit dem System tun können soll.

  * Technische User Story: 
  Fokussiert auf interne technische Aspekte wie Architektur und Performance, wichtig für die Systementwicklung und -wartung, aber oft nicht direkt sichtbar für den Endbenutzer.

 ---


### Aufbau / Bestandteile einer User Story

  Der Aufbau einer User Story umfasst drei wesentliche Elemente:
     
  * Rolle (Wer): Der zukünftige Nutzer der zu entwickelnden Lösung.

  * Funktion (Was): Die Erwartungen des zukünftigen Nutzers an die Software.

  * Nutzen (Warum): Der spätere Mehrwert der zu entwickelnden Lösung.


[10b]

### Definition of ready vs Definition of Done



  |       |      Ready     |     Done      |
  |   ---    |      ---     |    ---       | 
  |  Zweck     |    Bestimmt, wann eine User Story oder ein Arbeitselement bereit ist, in den Entwicklungsprozess aufgenommen zu werden.  | Legt fest, wann eine User Story oder ein Arbeitselement als abgeschlossen betrachtet werden kann.     |
  |       Inhalt        |      Enthält Kriterien, die sicherstellen, dass die Arbeit gut definiert, verstanden und planbar ist. Dies kann beinhalten, dass die User Story klar formuliert ist, Akzeptanzkriterien hat, durch das Team geschätzt wurde, und dass alle notwendigen Informationen verfügbar sind.        |        Enthält eine Liste von Kriterien, die erfüllt sein müssen, bevor eine Arbeit als "fertig" betrachtet wird. Diese können Aspekte wie Code-Reviews, Testing, Dokumentation, Einhaltung von Coding-Standards und Kundenzufriedenheit umfassen.             |
  |         Wichtigkeit           |        Stellt sicher, dass die Teams nicht mit unklaren oder unvollständigen Anforderungen arbeiten, was zu Verzögerungen oder Qualitätsproblemen führen könnte.              |           Stellt die Qualität und Vollständigkeit der gelieferten Arbeit sicher und verhindert, dass unvollendete Features in späteren Phasen des Projekts Probleme verursachen.           |



### Akzeptanzkriterien mit Beispielen

  Sind bestimmte Voraussetzungen, die ein Arbeitsergebnis erfüllen muss, damit es von Kund*innen akzeptiert und abgenommen wird.

  Bsp:
    User Story: "Als Besucher eines Online Shops möchte ich die angebotenen Waren nach Kategorien filtern können, um nicht alle Produkte durchzugucken, sondern will schnell meine Produkte finden."
    
  * Akzeptanzkriterien:
    * Produkte können nach Kategorien wie 'Bekleidung', 'Musik' und 'Wohnen' gefiltert werden.
    * Die Filterung zeigt sofort die relevanten Produkte an.
    * Filtereinstellungen bleiben während der  Browsersession erhalten.

[11b]

### Prinzipien für effektive ("gute") User Stories

  * Spezifisch und Verständlich: Deutliche und leicht verständliche Formulierungen, die von allen Teammitgliedern klar nachvollzogen werden können.
  * Benutzerzentriert: 
  Der fokus sollte auf dem Nutzer und seinen Bedürfnissen liegen.
  * Kurz: 
  sollten sehr kurz und pregnant sein.
  * Realisierbar: 
  Es sollte technisch und zeitlich im Rahmen der Projektressourcen liegen.

  * Testbar: 
  Die Akzeptanzkriterien sollten klar sein, um die FErtigstellung überprüfen zu können.

  * Wertvoll: 
  Es sollte ein durchaus erkennbarer Mehrwert für den Endbenutzer geliefert werden.

  * Priorisiert: 
  Wichtige und Dringliche Punkte sind klar erkennbar.
  
  * Verhandelbar: 
  Offen gegenüber Anpassungen sowie Verfeinerungen im Prozess.  
  
  * Unabhängig: 
  Möglichst unabhängig von anderen Stories, um einzeln entwickelt werden zu können.

[22b]

### Formulierungsfehler, die zu vagen ("schlechten") User Stories führen

* Unklare Beschreibung:
    * Fehler: "Benutzer soll Funktion X verbessern."


* Allgemeine Aussagen:
    * Fehler: "Verbessere das Design."

* Fehlende Spezifität:
    * Fehler: "Benutzer soll neue Funktion verwenden können."

* Unkonkrete Akteure:
    * Fehler: "Admin soll auf das Dashboard zugreifen können."
    Korrektur: "Der Systemadministrator soll über ein sicheres Login auf das Administrator-Dashboard zugreifen können."

* Ungenügende Akzeptanzkriterien:
    * Fehler: "Benutzer soll Produkt kaufen können."

* Fehlende Kontextinformationen:
    * Fehler: "Benutzer soll auf die Benachrichtigung reagieren."
    

* Mangelnde Priorisierung:
    * Fehler: "Benutzer soll neue Funktionen nutzen können."
    
* Vage Zeitvorgaben:
    * Fehler: "Implementiere Funktion X schnell."

[3b] 

### Card, Conversation, Confirmation
    
  * **Card:** 
    * User Stories sollten kurz und klar sein und auf einer Karteikarte festgehalten werden. Wenn der  Platz auf der Karte nicht ausreicht, ist die Story wahrscheinlich zu umfangreich. Die Karte dient als Erinnerung an die wichtigsten vereinbarten Punkte.

  * **Conversation:** 
    * Wichtiger als die schriftliche Festlegung ist der Austausch zwischen dem Kunden und dem   Entwicklungsteam. User Stories werden oft in Gesprächen, Workshops und Planungssitzungen diskutiert, um ein gemeinsames Verständnis zu schaffen. Zusätzliche Dokumentationen wie Mockups können zur Klärung beitragen.

  * **Confirmation:** 
    * Für jede User Story werden verbindliche Akzeptanzkriterien definiert, die vor Beginn der  Umsetzung festgelegt werden. Diese Kriterien dienen als Basis für die Abnahme der implementierten Story, wobei Akzeptanztests zur Überprüfung der Erfüllung dieser Kriterien nützlich sind.

[15b]

### INVEST-Kriterien
    

  ![](media/Invest.png)

[13b]

### User-Stories vs. Use Case

  |             |      User Stories    |      Use Cases    |
  |    ---      |    ---               |     ---           | 
  |      **Format**      |        Kurz und narrativ, folgen oft dem Schema „Als Rolle, möchte ich Aktion, um  Nutzen.“              |       Ausführlicher und strukturierter, beschreiben Interaktionen zwischen Benutzern und dem System.            | 
  |        **Fokus**     |          Stark benutzerzentriert, betonen den Wert oder Nutzen für den Endbenutzer.            |        Auf die Funktionalität und die Abläufe innerhalb des Systems.           | 
  |        **Detailgrad**     |             In der Regel weniger detailliert, eher auf das "Was" und "Warum" als auf das "Wie" konzentriert.         |          In der Regel detaillierter, beschreiben spezifische Schritte oder Abläufe.          | 
  |      **Flexibilität**       |         Sind offen für Diskussionen und können sich während des Entwicklungsprozesses anpassen.              |         Eher festgelegt, mit weniger Spielraum für Änderungen während der Entwicklung.          | 
  |           **Einsatz**              |           Häufig in agilen Entwicklungsmethoden verwendet, wie Scrum oder Kanban.               |          Oft in traditionelleren, plangetriebenen Entwicklungsansätzen wie dem Wasserfallmodell.           |
  |              **Ziel**           |         Schnelle, iterative Entwicklung mit Fokus auf Benutzerbedürfnissen.                |      Klare Definition der Systemanforderungen und -abläufe.               |


  [17b]

  #### Misuse Stories

  Sind kurze narrative Szenarien, die potenzielle Missbrauchs- und Angriffswege in einem Softwaresystem beschreiben. Sie dienen dazu, Sicherheitsrisiken und Schwachstellen zu identifizieren, um präventive Maßnahmen in der Softwareentwicklung zu ergreifen.

[18b]

  #### Priorisierung

  Bestimmt die Reihenfolge, in der Aufgaben, Features oder User Stories bearbeitet werden. Sie basiert auf Faktoren wie dem geschäftlichen Wert, Kundenbedürfnissen, Abhängigkeiten zwischen Aufgaben, Risiken, Kosten-Nutzen-Analyse, Dringlichkeit, Teamkapazität und Stakeholder-Input. Effektive Priorisierung sorgt dafür, dass wichtige und wertvolle Aspekte des Projekts zuerst angegangen werden. 

[19b]
  #### Schätzung

  Bezieht sich die Schätzung auf den Prozess der Bewertung des Aufwands und der Zeit, die benötigt werden, um bestimmte Aufgaben, Features oder User Stories zu implementieren.
 
  * Aspekte der Schätzung:

    * Team-Basiert: 
    Schätzungen werden oft vom Entwicklungsteam durchgeführt, da sie die nötige Erfahrung und Kenntnisse über die technischen Anforderungen und Herausforderungen haben.

  * Relative Schätzung: 
    * Anstatt spezifische Stunden oder Tage anzugeben, verwenden Teams oft relative Schätzungsmethoden wie Story Points oder T-Shirt-Größen, um die Komplexität im Vergleich zu bekannten Aufgaben zu bewerten.

  * Planungspoker: 
    * Eine beliebte Technik in agilen Methoden, bei der Teammitglieder ihre Schätzungen durch Karten mit Zahlen oder Story Points anzeigen und dann über Abweichungen diskutieren, um einen Konsens zu finden.

  * Historische Daten: 
    * Frühere Erfahrungen und historische Daten von ähnlichen Projekten oder Aufgaben können als Referenz für Schätzungen verwendet werden.

  * Iterative Anpassung: 
    * Schätzungen können und sollten im Laufe des Projekts angepasst werden, wenn mehr Informationen verfügbar sind oder sich die Bedingungen ändern.

  * Transparenz und Kommunikation: 
    * Offene Kommunikation über Unsicherheiten und Risiken während des Schätzungsprozesses ist wichtig, um realistische Erwartungen zu setzen.

* Story Mapping:
  * Ist eine Technik, mit der ausgehend von der User Experience das Big Picture der Anforderungen übersichtlich dargestellt werden kann. Dabei bleibt stets der Kundenfokus erhalten.
    
     ![](media/StoryMapping.png)

[23b]

---

### Wiederholungsfragen

* **Priorisierung**
  * Was versteht man unter Priorisierung in der Softwareentwicklung?
  * warum ist sie wichtig?

* **Prinzipien für effektive ("gute") User Stories**
  * Was ist das Hauptziel einer effektiven User Story in der agilen Softwareentwicklung?
  * Warum ist es wichtig, dass User Stories unabhängig voneinander sind?

* **Formulierungsfehler, die zu vagen ("schlechten") User Stories führen**
  * Was sind die Hauptmerkmale einer "vagen" User Story?
  * Welche Rolle spielen Akzeptanzkriterien bei der Vermeidung vager User Stories?


## **Quellenverzeichnis**

[1a] :https://academy.technikum-wien.at/ratgeber/was-ist-requirements-engineering/

[2a] :https://chat.openai.com/: Definition von Anforderung in bezug auf Requirements Engineering

[3a] :https://cdn.vector.com/cms/content/consulting/publications/RequirementsEngineering_WhitePaper_DE_2017.pdf

[4a] :https://www.johner-institut.de/blog/iec-62304-medizinische-software/funktionale-und-nicht-funktionale-anforderungen/#:~:text=Funktionale%20Anforderungen%20sind%20Anforderungen%20mit,die%20Zuverl%C3%A4ssigkeit%20und%20das%20Zeitverhalten.

[5a] :https://visuresolutions.com/de/blog/high-quality-requirements-attributes/

[6a] :https://visuresolutions.com/de/blog/high-quality-requirements-attributes/

[7a] :https://www.microtech.de/blog/anforderungsanalyse/#:~:text=Das%20Ziel%20einer%20Anforderungsanalyse%20ist,zudem%20in%20einem%20Lastenheft%20festhalten.

[8a] :https://visuresolutions.com/de/requirements-management-traceability-guide/biggest-challenges-of-requirements-management/

[9a] :https://www.projektmagazin.de/glossarterm/stakeholder

[10a] : https://projekte-leicht-gemacht.de/blog/methoden/projektziele/die-smart-formel/

[11a] :https://chat.openai.com/ : Anforderungsquellen und Ermittlungstechniken

[12a] :https://www.qz-online.de/a/grundlagenartikel/kundenanforderungen-kano-modell-309690

[13a] :https://www.applus-erp.de/ressourcen/blog/lastenheft-und-pflichtenheft-was-ist-der-unterschied/#:~:text=Aus%20Sicht%20des%20Kunden%20dokumentiert,des%20abgeschlossenen%20Vertrags%20erbringen%20muss.

[14a] :https://document360.com/blog/business-requirement-document/#:~:text=Business%20Requirement%20Documents%20(BRD)%20are,RFP)%20for%20a%20new%20project.

[15a] :https://www.jamasoftware.com/requirements-management-guide/writing-requirements/functional-requirements-examples-and-templates

[16a] :https://www.perforce.com/blog/alm/how-write-software-requirements-specification-srs-document#:~:text=Tool%20for%20SRS-,What%20Is%20a%20Software%20Requirements%20Specification%20(SRS)%20Document%3F,stakeholders%20(business%2C%20users).


[1b]  : https://www.microtool.de/wissen-online/was-ist-ein-use-case-diagramm/

[2b]  : https://t2informatik.de/wissen-kompakt/use-case-diagramm/

[3b]  : https://chat.openai.com/c/f8ca6995-a5d5-47ff-ba20-c3cb31905501 frage : was sind Formulierungsfehler, die zu vagen ("schlechten") User Stories führen

[4b]  : https://www.usability.gov/how-to-and-tools/methods/use-cases.html.

[5b]  : https://t2informatik.de/wissen-kompakt/systemkontext/.

[6b]  : https://www.fhnw.ch/plattformen/iwi/2020/06/17/homeoffice-und-onlinekonferenzen-4-9-2-3-2-7/.

[7b]  : https://www.microtool.de/wissen-online/was-ist-der-systemkontext/.

[8b]  : https://www.microtool.de/wissen-online/was-ist-ein-use-case-diagramm/.

[9b]  : https://www.visual-paradigm.com/scrum/theme-epic-user-story-task/.

[10b] : https://www.brainformatik.com/blog/user-story/

[11b] : https://t2informatik.de/wissen-kompakt/akzeptanzkriterien/.

[12b] : https://www.me-company.de/magazin/akzeptanzkriterien/#:~:text=Akzeptanzkriterien%20sollten%20einfach%20zu%20verstehen,wie%20die%20Kund*innen%20hat.

[13b] :  https://produktwerker.de/herausforderung/gute-user-stories-schreiben-formulieren/#:~:text=Zu%20den%20wichtigsten%20Eigenschaften%20einer,
die%20Prinzipien%20des%20Akronyms%20INVEST.

[14b] : https://bbv-software.de/user-stories/.

[15b] : https://blog.seibert-media.net/blog/2011/03/09/user-story-scrum-card-conversation-confirmation/.

[16b] : https://www.visual-paradigm.com/guide/agile-software-development/user-story-vs-use-case/.

[17b] : https://www.software-quality-lab.com/wissen/blog/blogeintrag/user-story-oder-use-case-was-denn-nun/.

[18b] : https://en.wikipedia.org/wiki/Misuse_case#From_use_to_misuse_case

[19b] : https://karrierebibel.de/priorisierung/.

[20b] : https://www.it-agile.de/agiles-wissen/agiles-produktmanagement/story-mapping/.
