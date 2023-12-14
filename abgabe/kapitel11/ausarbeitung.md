# Kapitel 11

**Autor:** Simon Fedrau, Sascha Hahn

## Lernziele

* Software Development Lifecycle (SDLC)
  * Phasen im Software-Lebenszyklus
  * Klassische (sequenzielle) Vorgehensmodelle
  * Agile Vorgehensmodelle
  * Evolutionäre Vorgehensmodelle
  * Vergleich der Vorgehensmodelle  
* Wartung von Software (Software Maintainance)
  * Definition Software-Wartung und Legacy-Code
  * Evolution von Software


## Software Development Lifecycle (SDLC)
***

Der Softwareentwicklungszyklus ist der kosteneffektive und zeitsparende Prozess, den Entwicklungsteams verwenden, um hochwertige Software zu entwerfen und zu entwickeln. Das Ziel des SDLC ist es, die Projektrisiken durch vorausschauende Planung zu minimieren, damit die Software die Erwartungen der Kunden während der Produktion und darüber hinaus erfüllt. Diese Methodik umreißt eine Reihe von Schritten, die den Softwareentwicklungsprozess in Aufgaben unterteilen, die Sie zuweisen, abschließen und messen können.


[1a]

### Phasen im Software-Lebenszyklus
***

Anforderungsanalyse und -spezifikation:
In dieser Phase werden die Anforderungen an die Software erfasst und analysiert. Es wird definiert, welche Funktionen die Software haben soll und welche Anforderungen sie erfüllen muss.

Entwurf:
Auf Grundlage der Anforderungen wird ein Design für die Software erstellt. Dies umfasst die Struktur, Architektur und das Datenmodell der Software.


Implementierung (Programmierung):
In dieser Phase wird der eigentliche Code der Software geschrieben und getestet. Es erfolgt die Umsetzung des zuvor erstellten Designs.

Test:
Die Software wird ausgiebig getestet, um sicherzustellen, dass sie den Anforderungen entspricht und fehlerfrei funktioniert. Dies beinhaltet oft verschiedene Arten von Tests, wie z. B. Einheitstests, Integrationstests und Systemtests.

Bereitstellung (Deployment):
Die Software wird für die Nutzung freigegeben und auf den Zielsystemen installiert. Dies kann in einer Produktionsumgebung oder für Endbenutzer erfolgen.

Wartung und Aktualisierung:
Nach der Bereitstellung erfordert die Software in der Regel Pflege. Dies kann Fehlerbehebungen, Sicherheitsupdates und die Implementierung neuer Funktionen umfassen.

![:scale 50%](media\Softwarelebenszyklus.png)

[1a]

### Klassische (sequenzielle) Vorgehensmodelle
***

Ein Vorgehensmodell zur Softwareentwicklung ist ein für die Softwareentwicklung angepasstes Vorgehensmodell in der Anwendungsentwicklung. Es ist ein standardisierter, organisatorischer Rahmen für den idealen Ablauf eines Entwicklungsprojektes und dient dazu, die Softwareentwicklung übersichtlicher zu gestalten und in der Komplexität beherrschbar zu machen.

Ein Vorgehensmodell ist eine abstrakte Darstellung eines Softwareprozesses. Der Prozess wird hierbei immer nur aus einer bestimmten Perspektive dargestellt. Daher beinhaltet ein Vorgehensmodell immer nur einen Teil der Informationen über den Prozess. Dies hat allerdings den Vorteil, dass die den einzelnen Softwareprozessen zugrunde liegenden Prinzipien übersichtlich und verständlich dargestellt werden können. 

[2a]

#### Wasserfallmodell
***
Ein Wasserfallmodell ist ein lineares (nicht iteratives) Vorgehensmodell, das insbesondere für die Softwareentwicklung verwendet wird und das in aufeinanderfolgenden Projektphasen organisiert ist. Wie bei einem Wasserfall mit mehreren Kaskaden „fallen“ die Ergebnisse einer Stufe nach unten in die nächste und sind dort verbindliche Vorgaben.

In einem Wasserfallmodell hat jede Phase vordefinierte Start- und Endpunkte mit eindeutig definierten Ergebnissen. Meist beschreibt das Modell auch einzelne Aktivitäten, die zur Herstellung der Ergebnisse durchzuführen sind. Zu bestimmten Meilensteinen und am jeweiligen Phasenende werden die vorgesehenen Entwicklungsdokumente im Rahmen des Projektmanagements verabschiedet.

Der Name Wasserfall kommt von der häufig gewählten grafischen Darstellung der als Kaskade angeordneten Projektphasen. In der betrieblichen Praxis ist es traditionell ein weitverbreitetes Vorgehensmodell, von dem es viele Varianten gibt. 


![:scale 50%](media\Waterfall_model.png)

[3a]

#### V-Modell
***

Das V-Modell, ist ein Softwareentwicklungsmodell, das auf dem Wasserfallmodell basiert. Es wurde entwickelt, um einen klaren Zusammenhang zwischen den Entwicklungsphasen und den zugehörigen Testphasen herzustellen. Das V-Modell repräsentiert die Verbindung zwischen den Entwicklungsphasen auf der linken Seite des "V" und den entsprechenden Testphasen auf der rechten Seite des "V". Es betont die Wichtigkeit von Tests während des gesamten Softwareentwicklungszyklus.

Die Hauptmerkmale des V-Modells sind:

* Entwicklungsphasen:

Anforderungsanalyse und -definition
Systementwurf
Architekturentwurf
Modulentwurf
Codierung
Diese Phasen entsprechen im Wesentlichen den Schritten im Wasserfallmodell.

* Testphasen:

Komponententest
Integrationstest
Systemtest
Abnahmetest
Jede Entwicklungsphase ist mit einer entsprechenden Testphase verknüpft. Während der Entwicklungsphasen werden die zugehörigen Tests vorbereitet, und die eigentlichen Tests werden während der Testphasen durchgeführt.

Der Gedanke hinter dem V-Modell ist, dass die Qualitätskontrolle durch den gesamten Softwareentwicklungsprozess hindurch erfolgen sollte und nicht erst am Ende, wie es im reinen Wasserfallmodell der Fall ist. Durch die enge Verknüpfung von Entwicklungs- und Testaktivitäten soll die frühzeitige Erkennung und Behebung von Fehlern ermöglicht werden.

![:scale 50%](media\v-modell.jpg)

[4a]

### Agile Vorgehensmodelle
***

Der eindeutige Mehrwert der agilen Vorgehensmodelle besteht darin, dass sich durch ihre iterative Entwicklung, das kurzfristige Feedback der Kunden und die intensive Kommunikation der gesamte Entwicklungsprozess sehr schlank und flexibel gestaltet. Durch die Konzentration auf eine schnelle Auslieferung von funktionsfähigen Inkrementen wird weniger Wert auf eine detaillierte Dokumentation und mehr auf Entwicklung & Test gelegt.

![:scale 50%](media\Vorgehensmodelle.JPG)

[5a] [6a]

#### PDCA-Zyklus
***

Der PDCA-Zyklus, auch bekannt als Deming-Zyklus, ist ein Managementansatz für kontinuierliche Verbesserung. Die vier Phasen sind:

* Plan (Planen): Festlegung von Zielen und Entwickeln eines Umsetzungsplans.

* Do (Umsetzen): Ausführung des Plans, um gewünschte Verbesserungen zu erzielen.

* Check (Überprüfen): Messen und Bewerten der Ergebnisse im Vergleich zu den Zielen.

* Act (Handeln): Auf Grundlage der Überprüfung werden Entscheidungen getroffen, und der Plan wird angepasst, um den Prozess weiter zu verbessern.


Der PDCA-Zyklus ist ein iterativer Prozess, der sicherstellt, dass kontinuierliche Verbesserungen vorgenommen werden, indem Erfahrungen aus vorherigen Zyklen genutzt werden.


![:scale 20%](media\PDCA_Zirkel.png)

[7a] [8a]

#### OODA loop
***

Der OODA-Loop (Observation, Orientation, Decision, Action) ist ein Konzept, das ursprünglich vom Militärstrategen und Fliegerass Colonel John Boyd entwickelt wurde. Es beschreibt einen zyklischen Entscheidungsprozess, der darauf abzielt, sich schnell an sich ändernde Bedingungen anzupassen. Obwohl der OODA-Loop ursprünglich für den militärischen Kontext konzipiert wurde, hat er auch Anwendung in anderen Bereichen gefunden, einschließlich Software Engineering.

Im Kontext der Softwareentwicklung und des Projektmanagements könnte der OODA-Loop folgendermaßen angewendet werden:

Observation (Beobachtung):

Erfassung von Informationen über den aktuellen Zustand des Projekts oder der Softwareentwicklung. Dies kann das Überwachen von Fortschritten, das Sammeln von Feedback und das Erkennen von Problemen oder Chancen umfassen.
Orientation (Orientierung):

Analyse und Bewertung der gesammelten Informationen. In diesem Schritt wird versucht, ein umfassendes Verständnis der Situation zu entwickeln, einschließlich der Identifikation von Mustern, Problemen oder neuen Anforderungen.
Decision (Entscheidung):

Basierend auf der Analyse werden Entscheidungen getroffen. Dies können Anpassungen am Projektplan, Änderungen in den Anforderungen, Ressourcenallokation oder andere strategische Entscheidungen sein.
Action (Handlung):

Umsetzung der getroffenen Entscheidungen durch konkrete Maßnahmen. Dies könnte die Aktualisierung von Code, die Neuplanung von Aufgaben oder die Umsetzung neuer Funktionen umfassen.
Der OODA-Loop ist besonders relevant in agilen Entwicklungsumgebungen, wo sich Anforderungen schnell ändern können. Die Idee ist, dass Teams, die in der Lage sind, den OODA-Loop effizient zu durchlaufen, besser in der Lage sind, sich an unvorhergesehene Änderungen anzupassen und innovative Lösungen zu finden.

Es ist wichtig zu beachten, dass der OODA-Loop als Denkrahmen dient und nicht strikt lineare oder starre Schritte vorschreibt. Teams können den Zyklus iterativ durchlaufen und so kontinuierlich lernen und verbessern.

![:scale 50%](media\ooda-loop.png)

[9a]

#### Stacey-Matrix
***

Die Stacey-Matrix ist ein Modell zur Einschätzung von Aufgaben und Problemen basierend auf Unsicherheit und Eindeutigkeit. Hier sind die Bereiche:

Einfach (Simple):

Klare Definition und verständliche Ursache-Wirkungs-Beziehungen. Bewährte Lösungen können direkt angewendet werden.
Kompliziert (Complicated):

Komplexere Aufgaben, erfordern Fachkenntnisse. Es gibt klare Ursache-Wirkungs-Beziehungen, aber spezialisiertes Wissen ist notwendig.
Komplex (Complex):

Viele Unsicherheiten und keine klaren Ursache-Wirkungs-Beziehungen. Lösungen müssen iterativ entwickelt werden, oft durch Experimentieren und Lernen.
Chaotisch (Chaotic):

Hohe Unsicherheit und fehlende Muster. Keine klaren Ursache-Wirkungs-Beziehungen. Sofortiges Handeln ist oft erforderlich, bevor eine geplante Vorgehensweise entwickelt werden kann.


![:scale 50%](media\stacey_Matrix.png)

[10a]

#### 4 Werte und 12 Prinzipien
***


Die 4 Werte und 12 Prinzipien sind Grundlagen des Agilen Manifests, das die Kernprinzipien der agilen

Softwareentwicklung beschreibt. Das Agile Manifest wurde im Jahr 2001 von einer Gruppe von Softwareentwicklern erstellt, um eine flexiblere und kundenorientierte Herangehensweise an die Softwareentwicklung zu fördern. Hier sind die 4 Werte und 12 Prinzipien des Agilen Manifests:

**Die 4 Werte des Agilen Manifests:**

* Individuen und Interaktionen mehr als Prozesse und Werkzeuge

* Funktionierende Software mehr als umfassende Dokumentation

* Zusammenarbeit mit dem Kunden mehr als Vertragsverhandlung

* Reagieren auf Veränderung mehr als das Befolgen eines Plans


**Die 12 Prinzipien des Agilen Manifests**

* Zufriedenstellung des Kunden durch kontinuierliche Lieferung wertvoller Software

* Änderungen in den Anforderungen auch spät im Entwicklungsprozess willkommen heißen

* Funktionierende Software ist das Hauptmaß für Fortschritt

* Nachhaltiges Tempo für die Entwickler

* Gute Zusammenarbeit zwischen Entwicklern und Kunden

* Baue Projekte rund um motivierte Einzelpersonen und gebe ihnen das Umfeld und die Unterstützung, die sie benötigen

* Direkte Kommunikation von Angesicht zu Angesicht wird als effektivste Methode angesehen

* Funktionierende Software ist das wichtigste Fortschrittsmaß

* Ständige Aufmerksamkeit für technische Exzellenz und gutes Design

* Einfachheit – die Kunst, die Menge nicht getaner Arbeit zu maximieren – ist wesentlich

* Die besten Architekturen, Anforderungen und Entwürfe entstehen aus selbstorganisierten Teams

* In regelmäßigen Abständen reflektieren und denken, wie die Effektivität verbessert werden kann

[24a]

#### Anti patterns
***

* Planungsverweigerung

* Alles für den Kunden

* Konkurrierende Kräfte

* Sprechender Code ist genügend Dokumentation

* Allzeit änderungsbereit

* Unzuverlässigkeitsformel: Spontanität = Agilität

* I believe in Miracles

* Der „agile Ad-hoc-Prozess“


![:scale 20%](media\antipattern.jpg)


[22a]

#### XP, Scrum, Kanban (jeweils kurze Darstellung)
***

**Extreme Programming (XP):**
Extreme Programming (XP) ist eine agile Softwareentwicklungsmethode, die auf Praktiken wie kontinuierlichem Feedback, gemeinsamer Verantwortung, Flexibilität und hoher Kommunikation basiert. XP betont die Zusammenarbeit im Team, die Kundenbeteiligung und die schnelle Anpassung an sich ändernde Anforderungen. Schlüsselpraktiken von XP umfassen Paarprogrammierung, Testgetriebene Entwicklung (TDD), kontinuierliche Integration und kurze Entwicklungszyklen (Iterations).

**Scrum:**
Scrum ist ein agiles Rahmenwerk für die Entwicklung und das Management von Produkten. Es organisiert die Arbeit in kurzen, wiederholbaren Entwicklungszyklen, sogenannten Sprints, die in der Regel zwei bis vier Wochen dauern. Scrum definiert klare Rollen wie den Product Owner, den Scrum Master und das Entwicklungsteam. Es beinhaltet Artefakte wie das Product Backlog, das Sprint Backlog und den Increment. Scrum betont die Zusammenarbeit, Transparenz und kontinuierliche Verbesserung.

**Kanban:**
Kanban ist ein agiles Ansatz, der auf der visuellen Darstellung von Arbeit basiert. Auf einem Kanban-Board werden Aufgaben in Spalten organisiert, die den verschiedenen Phasen des Entwicklungsprozesses entsprechen, z. B. "To Do", "In Progress" und "Done". Das Ziel ist es, den Workflow zu visualisieren, Engpässe zu identifizieren und eine kontinuierliche Verbesserung zu fördern. Kanban ermöglicht eine flexible Anpassung an sich ändernde Anforderungen und eine gleichmäßige Arbeitsbelastung.

[11a]

### Evolutionäre Vorgehensmodelle
***

Evolutionäres Design ist ein Entwurfsansatz in der Softwareentwicklung und kommt überwiegend im Kontext des Extreme Programming zum Einsatz. Im Gegensatz zu geplantem Design propagieren die Befürworter des evolutionären Ansatzes die Entwicklung eines Softwaresystems in kleinen Schritten. Designelemente werden nur dann eingebaut, wenn sie zur Erfüllung der augenblicklichen Anforderungen wirklich notwendig sind. Design for the future wird vermieden, stattdessen vertraut man darauf, dass ein einfacher Entwurf sich auch auf einfache Weise an neue Anforderungen anpassen lässt. Die Weiterentwicklung des Design erfolgt durch Refaktorisierung. 

[12a]

#### Prototyping (Prototype Model)
***

Prototyping bzw. Prototypenbau ist eine Methode der Softwareentwicklung, die schnell zu ersten Ergebnissen führt und frühzeitiges Feedback bezüglich der Eignung eines Lösungsansatzes ermöglicht. Dadurch ist es möglich, Probleme und Änderungswünsche frühzeitig zu erkennen und mit weniger Aufwand zu beheben, als es nach der kompletten Fertigstellung möglich gewesen wäre.

  Ziel: Anhand der Grundfunktionalitäten die Akzeptanz beim Nutzer und die Notwendigkeit ergänzender Funktionen zu überprüfen
  Wichtigstes Ergebnis: Ein Programm mit den Grundfunktionalitäten

Beim evolutionären Prototyping wird die Anwendung nach und nach erweitert. Dabei werden vor allem die Rückmeldungen der zukünftigen Nutzer bzw. des Auftraggebers genutzt. Der Prototyp wird dabei stets lauffähig gehalten und bis zur Produktreife weiterentwickelt. 


[13a]

### Vor und Nachteile der Vorgehensmodelle
***

**Agile Vorgehensmodelle:**

| Vorteile                        | Nachteile                                |
|---------------------------------|------------------------------------------|
| Hohe Flexibilität und Anpassung | Mögliche Komplexität in großen Projekten |
| Enge Kundenbeteiligung          | Hohe Anforderungen an Teammitglieder     |
| Kontinuierliche Lieferung       | Möglicher Mangel an umfassender Dokumentation |
| Fokus auf Wert durch funktionierende Software |                                        |
| Schnelle Markteinführung        |      |         |              


**Evolutionäre Vorgehensmodelle:**

| Vorteile                        | Nachteile                                |
|---------------------------------|------------------------------------------|
| Schrittweise Verbesserungen     | Zeit- und Ressourcenaufwand              |
| Flexibilität                    | Mögliche Dokumentationsherausforderungen |
| Frühzeitiges Kundenfeedback     | Eventuell begrenzte Kundenbeteiligung    |
| Fokussiert auf Prototyping      |          


**Klassische (Sequenzielle) Vorgehensmodelle:**

| Vorteile                        | Nachteile                                |
|---------------------------------|------------------------------------------|
|  Klare Struktur und Planung    |   Geringe Anpassungsfähigkeit an Änderungen           |
|  Umfassende Dokumentation                  | Lange Entwicklungszyklen |
|  Gut geeignet für stabile Anforderungen    |  Geringe Kundenbeteiligung während der Entwicklung   |
         

[14a]

#### Empfehlungen, unter welchen Bedingungen welches Vorgehensmodell sinnvoll ist
***

* Klassische (sequenzielle) Vorgehensmodelle:

    Bedingungen:
        Stabile Anforderungen: Wenn die Anforderungen gut verstanden und stabil sind, eignet sich ein sequenzielles Modell.
        Geringe oder keine Änderungserwartung: Wenn nicht erwartet wird, dass sich die Anforderungen während des Entwicklungsprozesses erheblich ändern.

* Agile Vorgehensmodelle:

    Bedingungen:
        Dynamische Anforderungen: Wenn die Anforderungen sich ändern oder nicht vollständig vor Projektbeginn bekannt sind.
        Kundeninteraktion und -beteiligung: Wenn eine enge Zusammenarbeit mit dem Kunden und schnelle Anpassungen wichtig sind.
        Inkrementelle Entwicklung: Wenn die schrittweise Bereitstellung von Funktionen bevorzugt wird.

* Evolutionäre Vorgehensmodelle:

    Bedingungen:
        Komplexe Projekte: Bei komplexen Projekten mit unsicheren Anforderungen, bei denen eine schrittweise Entwicklung bevorzugt wird.
        Forschung und Entwicklung: In Fällen, in denen die Entwicklung als Forschungsprozess betrachtet wird und iterative Prototypen wichtig sind.


[23a]

## Wartung von Software (Software Maintainance)
***

Die Wartung von Software, auch als Software Maintenance bekannt, bezieht sich auf den Prozess der Modifikation und Pflege einer Softwareanwendung nach ihrer ursprünglichen Entwicklung und Bereitstellung. Dieser Lebenszyklusaspekt ist entscheidend, um sicherzustellen, dass die Software effizient funktioniert, aktuell bleibt und den sich ändernden Anforderungen und Umgebungen gerecht wird. Die Softwarewartung umfasst verschiedene Aktivitäten, die im Allgemeinen in vier Kategorien unterteilt werden:

1. Korrigierende Wartung (Corrective Maintenance):
Ziel: Behebung von Fehlern oder Mängeln in der Software.
Aktivitäten: Identifikation, Analyse und Beseitigung von Fehlern, um die Softwarestabilität zu gewährleisten.
2. Adaptive Wartung (Adaptive Maintenance):
Ziel: Anpassung der Software an Änderungen in der Umgebung, wie Betriebssystem-Upgrades oder Hardwareänderungen.
Aktivitäten: Anpassung von Codes und Funktionen, um die Kompatibilität und Leistung sicherzustellen.
3. Perfective Wartung (Perfective Maintenance):
Ziel: Verbesserung der Softwareleistung, Funktionalität oder Benutzerfreundlichkeit.
Aktivitäten: Hinzufügen neuer Funktionen, Optimierung von Algorithmen oder Verbesserung der Benutzeroberfläche.
4. Preventive Wartung (Preventive Maintenance):
Ziel: Verhinderung zukünftiger Probleme oder Fehlfunktionen.
Aktivitäten: Überprüfung und Aktualisierung von Codes, um potenzielle Probleme zu identifizieren und zu beheben, bevor sie auftreten.

[15a] [16a]

### Definition Software-Wartung und Legacy-Code
***

**Software-Wartung** 
In der Softwaretechnik bezeichnet der Begriff Softwarewartung „die Veränderung eines Softwareprodukts nach dessen Auslieferung, um Fehler zu beheben, Performanz oder andere Attribute zu verbessern oder Anpassungen an die veränderte Umgebung vorzunehmen. In Deutschland wird darüber hinaus geregelt: „Die Aufgabe der Wartung umfasst sämtliche Maßnahmen zur Erhaltung der Funktionsfähigkeit der eingesetzten IT-Verfahren und Software. Hierzu gehören auch erforderliche fachliche und technische Anpassungen der IT-Infrastruktur.. Diese gesetzliche Regelung grenzt hierbei bewusst die Softwarepflege gegenüber der Softwarewartung durch Fokussierung auf den Erhalt der Funktionsfähigkeit ab. 

[17a]

**Legacy-Code**

Der Begriff Altsystem oder Legacy-System oder im engeren Sinne Legacy-Code bezeichnet in der Informatik eine etablierte, historisch gewachsene Anwendung im Bereich Unternehmenssoftware. Das englische Wort legacy ist in diesem Kontext ein weitgehend wertfreier Fachbegriff. Er kann aber umgangssprachlich auch negativ im Sinne einer lästigen „Hinterlassenschaft“ oder „Altlast“ im übertragenen Sinne verwendet werden. 

[18a]

### Evolution von Software
***

Software-Evolution ist ein Begriff aus der Softwaretechnik, im Speziellen aus der Softwarewartung, und beschreibt den Prozess, der folgt, nachdem ein Softwaresystem entwickelt und ausgeliefert wurde. Nach Auslieferung und Benutzung kommen neue Anforderungen dazu und alte Anforderungen verändern sich. Teile des Softwaresystems müssen möglicherweise korrigiert werden, da Fehler auftreten, die zuvor nicht bemerkt wurden. Das System muss an eine neue Plattform adaptiert werden. Die Performance muss verbessert werden und andere nichtfunktionale Anforderungen müssen überprüft werden.

[19a]

#### Ursachen für Änderungen an Software
***

  * Fehlerkorrektur (Bugfixing): Software enthält oft Fehler, die während oder nach der Entwicklung entdeckt werden. Änderungen sind erforderlich, um diese Fehler zu beheben und die Software zu stabilisieren.

  * Neue Anforderungen: Kunden oder Benutzer können neue Anforderungen oder Funktionen an die Software stellen. Entwickler müssen die Software aktualisieren, um diesen neuen Anforderungen gerecht zu werden.

  * Verbesserungen und Optimierungen: Auch wenn die Software funktioniert, können Entwickler Verbesserungen vornehmen, um die Leistung, Effizienz oder Benutzerfreundlichkeit zu steigern.

  * Sicherheitsaktualisierungen: Wenn Sicherheitslücken entdeckt werden, müssen Softwareentwickler entsprechende Aktualisierungen bereitstellen, um die Software vor möglichen Angriffen zu schützen.

  * Technologischer Fortschritt: Neue Technologien oder Plattformen können verfügbar werden, und die Software muss möglicherweise angepasst werden, um mit den neuesten Entwicklungen Schritt zu halten.

  * Gesetzliche Anforderungen: Änderungen an Software können notwendig sein, um gesetzlichen Bestimmungen oder regulatorischen Anforderungen zu entsprechen.

  * Hardwareänderungen: Wenn sich die zugrunde liegende Hardware ändert, kann es erforderlich sein, die Software anzupassen, um weiterhin kompatibel zu bleiben.

  * Benutzerfeedback: Rückmeldungen von Benutzern können dazu führen, dass Entwickler Änderungen vornehmen, um die Benutzererfahrung zu verbessern oder auf bestimmte Bedürfnisse einzugehen.

  * Lebenszyklus-Management: Software unterliegt einem Lebenszyklus, der Wartung, Unterstützung und schließlich die Ablösung durch eine neue Version oder ein neues Produkt umfassen kann.

[20a]

#### Arten von Änderungen an Software
***
Die Klassifizierung von Softwareänderungen nach ihrer Art erfolgt oft anhand von vier Haupttypen, korrektive, präventive, perfektionierende und adaptive Änderungen. 



##### Korrektive, präventive, perfektionierende, adaptive Änderungen
***

  * Korrektive Änderungen:
      Ziel: Behebung von Fehlern oder Bugs in der Software.
      Warum: Diese Änderungen werden vorgenommen, um Probleme zu lösen, die während der Entwicklung oder nach der Bereitstellung entdeckt wurden.

  * Präventive Änderungen:
      Ziel: Vermeidung potenzieller zukünftiger Probleme oder Risiken.
      Warum: Diese Änderungen werden durchgeführt, um mögliche Fehler oder Schwachstellen zu identifizieren und zu beheben, bevor sie zu ernsthaften Problemen führen.

  * Perfektionierende Änderungen:
      Ziel: Verbesserung der Leistung, Benutzerfreundlichkeit oder anderer Aspekte der Software, die nicht unbedingt mit Fehlern zusammenhängen.
      Warum: Dies kann aufgrund von Benutzerfeedback, neuen Designprinzipien oder dem Wunsch nach kontinuierlicher Verbesserung geschehen.

  * Adaptive Änderungen:
      Ziel: Anpassung der Software an veränderte Umgebungen, Plattformen oder Anforderungen.
      Warum: Änderungen sind erforderlich, um die Software mit neuen Technologien, Betriebssystemversionen oder sich ändernden Anforderungen in Einklang zu bringen.

[21a]

## Referenzen

[1a]  : https://aws.amazon.com/de/what-is/sdlc/

[2a]  : https://de.wikipedia.org/wiki/Vorgehensmodell_zur_Softwareentwicklung

[3a]  : https://de.wikipedia.org/wiki/Wasserfallmodell

[4a]  : https://de.wikipedia.org/wiki/V-Modell

[5a]  : https://fh-bielefeld-mif-sw-engineerin.gitbooks.io/klausurthemen/content/continuous-software-engineering/Agile-Vorgehensmodelle.html#:~:text=Agile%20Vorgehensmodelle%20sind%20eine%20Methode,%2DAufwand%20verbunden%20sind%2C%20abl%C3%B6sen.

[6a]  : https://www.rewion.com/agiles-it-projektmanagement-vorgehensmodelle/

[7a]  : https://de.wikipedia.org/wiki/Demingkreis

[8a]  : https://karrierebibel.de/pdca-zyklus/

[9a]  : https://waydev.co/ooda-agile-data-driven/

[10a] : https://digitaleneuordnung.de/blog/stacey-matrix/

[11a] : https://www.heise.de/blog/Extreme-Programming-Scrum-Kanban-was-fuer-wen-4951363.html

[12a] : https://de.wikipedia.org/wiki/Evolution%C3%A4res_Design

[13a] : https://de.wikipedia.org/wiki/Prototyping_(Softwareentwicklung)

[14a] : https://chat.openai.com/ frage: Schreib mir einen Vergleich zwischen den Agilen Vorgehensmodellen  und den Evolutionären Vorgehensmodellen 

[15a] : https://cpl.thalesgroup.com/de/software-monetization/four-types-of-software-maintenance

[16a] : https://www.geeksforgeeks.org/software-engineering-software-maintenance/

[17a] : https://de.wikipedia.org/wiki/Softwarewartung

[18a] : https://de.wikipedia.org/wiki/Altsystem

[19a] : https://de.wikipedia.org/wiki/Software-Evolution#:~:text=Software%2DEvolution%20ist%20ein%20Begriff,und%20alte%20Anforderungen%20ver%C3%A4ndern%20sich.

[20a] :  https://chat.openai.com/  frage: was sind Ursachen für Änderungen an Software?

[21a] : https://cpl.thalesgroup.com/de/software-monetization/four-types-of-software-maintenance

[22a] : https://entwickler.de/agile/agile-anti-patterns-001

[23a] : https://www.rewion.com/klassisches-it-projektmanagement/

[24a] : https://www.wrike.com/de/blog die-4-werte-und-12-prinzipien-des-agilen-projektmanagements/
