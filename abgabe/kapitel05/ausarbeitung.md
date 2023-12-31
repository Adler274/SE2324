# DevOps

**Autor:** Sascha Hahn, Simon Fedrau


## Lernziele

* Warum DevOps so förderlich für die Softwareentwicklung ist
* Was eine DevOps Pipeline ist
* Was für Deployment strategies es gibt
* Wie versioniert man richtig
* Was ist Secrets Management
* Was ist CALMAS und dessen Vorversionen
* Was macht man mit dem SPACE und DevEx Framework
* Was sind die Bewertungskriterien der DORA-Metriken
und welche Risiken gibt es
* Was ist DevSecOps und welche Vorteile hat es
    * Welche Sicherheitsrisiken gibt es und was bringt einem STRIDE dabei


## DevOps
***
Unter DevOps versteht man eine umfassende Praxis, die verschiedene Techniken, Werkzeuge und eine kulturelle Ausrichtung umfasst. Ziel ist die Automatisierung und nahtlose Integration der Abläufe zwischen den Teams, die Software entwickeln, und den Teams, die für die IT-Infrastruktur verantwortlich sind. Im Mittelpunkt dieses Ansatzes stehen die Befähigung der Teams, eine reibungslose Kommunikation und Zusammenarbeit über Teamgrenzen hinweg sowie die Automatisierung von technologischen Prozessen.

Die DevOps-Bewegung nahm ihren Anfang etwa um das Jahr 2007. Sie entstand, als die Communities im Bereich Softwareentwicklung und IT-Betrieb Bedenken bezüglich des herkömmlichen Entwicklungsmodells äußerten. In diesem traditionellen Modell arbeiteten Entwickler, die den Code erstellten, isoliert von den Operations-Teams, die für die Bereitstellung und Unterstützung der Software zuständig waren. Der Begriff "DevOps," eine Zusammensetzung der Wörter "Development" und "Operations," spiegelt den Prozess der nahtlosen Integration beider Fachbereiche in einen fortlaufenden, kontinuierlichen Arbeitsprozess wider.
[1a] [2a]

![:scale 50%](media\Titelbild-devops-tools-definition-best-practice.png)


### Kultur, Ziele, Vorteile, Praktiken
***
**Kultur** 

In der organisatorischen Dimension erfordert DevOps eine kontinuierliche Kommunikation, Zusammenarbeit und eine geteilte Verantwortung aller Beteiligten im Software-Bereitstellungsprozess. Das schließt nicht nur die Teams für Softwareentwicklung und IT-Betrieb ein, sondern bezieht auch Sicherheits-, Compliance-, Governance-, Risiko- und Geschäftsleitungsteams mit ein. Ziel ist es, schnelle und fortlaufende Innovationen zu fördern und von Anfang an die Qualität der Software sicherzustellen.

In den meisten Fällen gelingt dies am besten, wenn bestehende Abteilungsbarrieren abgebaut werden, um funktionsübergreifende und autonome DevOps-Teams zu schaffen. Diese Teams können von Anfang bis Ende an Code-Projekten arbeiten, angefangen bei der Planung bis hin zum Feedback, ohne auf Übergaben an andere Teams oder auf deren Genehmigungen angewiesen zu sein. Innerhalb des agilen Entwicklungsansatzes bilden die geteilte Verantwortlichkeit und die enge Zusammenarbeit die Grundlage für einen gemeinsamen Fokus auf das Produkt, was letztendlich zu wertvollen Ergebnissen führt.

Auf technischer Ebene erfordert DevOps ein starkes Engagement für die Automatisierung von Prozessen, die es ermöglicht, Projekte nahtlos innerhalb und zwischen den Arbeitsabläufen zu bewegen. Zusätzlich sind kontinuierliches Feedback und die Durchführung von Messungen unerlässlich. Diese Elemente ermöglichen es den Teams, ihre Entwicklungszyklen fortlaufend zu beschleunigen und die Qualität sowie Leistung der Software kontinuierlich zu verbessern.

[3a] [4a]

**Ziele**

Das große Ziel einer DevOps-Pipeline ist die Schaffung eines wiederholbaren Systems, das die Automatisierung nutzt und kontinuierliche Verbesserungen ermöglicht, um qualitativ hochwertige Produkte schnell und einfach zu liefern.
[6a]

**Vorteile**

Die grundlegenden Vorteile von DevOps umfassen eine verstärkte Zusammenarbeit und das Aufbauen von Vertrauen, die Förderung von klügeren und transparenteren Arbeitsweisen, beschleunigte Release-Zyklen, verkürzte Reaktionszeiten bei Problemen und eine verbesserte Bewältigung unvorhergesehener Aufgaben.

Durch die Implementierung der DevOps-Methode können Teams ihre Produktivität steigern und den Weg zu häufigeren Releases ebnen, indem sie auf Automatisierung und standardisierte Tools setzen. Eine erhöhte Transparenz führt dazu, dass der Feedbackprozess verkürzt wird, wodurch Probleme und Aufgaben schneller identifiziert und angegangen werden können. Dank etablierter Prozesse und einer flexiblen, agilen Priorisierung, die sich an den Verlauf des Projekts anpasst, sind Teams in der Lage, unerwartete Aufgaben effektiver zu bewältigen, ohne dabei die geplanten Aufgaben aus den Augen zu verlieren.
[5a]


**Praktiken**

* DevOps Praktiken sind meist eine Reihe von Aktionen, die in einer bestimmten Reiehnfolge ausgeführt werden.
* DevOps Praktiken sind dafür gemacht, bestimmte Phasen innerhalb eines Prozesses zu beschleunigen

* Erstellen von Code-Repositories
* Quellcode-Kontrolle
* Code-Validierungstests
* Erstellung von Softwarepaketen
* Kontinuierliche Tests
* Kontinuierliche Integration (CI)
* Kontinuierliche Delivery
* Kontinuierliche Deployment

[23a]

### DevOps Teams
***
DevOps-Teams setzen in der Regel auf Mitglieder, die sowohl über Fachkenntnisse im Bereich Softwareentwicklung als auch im Operations-Bereich verfügen. Einige Teammitglieder mögen hervorragend in der Code-Erstellung sein, während andere ihre Stärken eher in der Betriebsführung und der Infrastrukturverwaltung haben. Dieses Spektrum kann auch Release-Manager umfassen, die die Koordination und Verwaltung von Anwendungen von der Entwicklung bis zur Produktion übernehmen, sowie Automatisierungsarchitekten, die für die Wartung und Automatisierung der Continuous Integration/Continuous Deployment (CI/CD)-Pipeline des Teams verantwortlich sind.

Welche Qualifikationen sind erforderlich, um einem DevOps-Team beizutreten? Die Anforderungen für eine Tätigkeit in einem DevOps-Team entwickeln sich ständig weiter, bedingt durch neue Technologien und Methoden. Dennoch zeichnen sich kompetente DevOps-Profis immer durch ähnliche Eigenschaften aus. Solide technische Fähigkeiten, effektive Kommunikation, die Bereitschaft zur Teamarbeit und die Fähigkeit zur Anpassung sind einige der wichtigsten Merkmale, die fähige DevOps-Fachleute auszeichnen.
[7a]

#### Struktur, Rollen, Verantwortlichkeiten
***

**Struktur** 

Welche DevOps-Teamstruktur implementiert werden soll, hängt von zahlreichen Faktoren ab. Das sind beispielsweise die Anzahl der Produkte, an denen ein Unternehmen arbeitet, die technische Führung und die Fähigkeit von Entwicklungs- und Operations-Teams, Prozesse aufeinander abzustimmen.
Es ist wichtig zu verstehen, dass nicht jedes Team dieselben Ziele verfolgt oder dieselben Praktiken und Tools verwendet. Selbst die Art und Weise, wie ein Team zusammengesetzt ist, sollte nicht standardisiert werden. Je nach den Umständen des Unternehmens und seinem Drang, sich zu verändern, benötigen verschiedene Teams unterschiedliche Strukturen. DevOps-Teams in zwei unterschiedlichen Unternehmen können sich massiv voneinander unterscheiden.

**Cross-Functional Teams (Funktionsübergreifende Teams):**
 In dieser Struktur sind DevOps-Teams funktionsübergreifend zusammengesetzt, was bedeutet, dass sie Mitglieder aus den Bereichen Entwicklung, IT-Betrieb und manchmal auch Sicherheit und Qualitätssicherung (QA) umfassen. Diese Teams arbeiten gemeinsam an einem Produkt oder Projekt und teilen die Verantwortung für die gesamte Bereitstellungspipeline.

**Embedded DevOps:**
 In diesem Modell werden DevOps-Praktiken direkt in die einzelnen Entwicklungsteams eingebettet. Jedes Entwicklungsteam übernimmt die Verantwortung für die Bereitstellung, Überwachung und Wartung seiner Anwendungen. Dies fördert eine enge Zusammenarbeit zwischen Entwicklern und Betriebsmitarbeitern.

**Zentralisierte DevOps-Teams:**
 Hier gibt es ein zentrales DevOps-Team, das für die Bereitstellung und Wartung von Infrastruktur und Werkzeugen verantwortlich ist. Die einzelnen Entwicklungsteams nutzen diese Ressourcen, um ihre Anwendungen zu entwickeln und bereitzustellen.

**Hybride Strukturen:**
 Einige Organisationen kombinieren verschiedene Elemente der oben genannten Modelle, um ihren spezifischen Anforderungen gerecht zu werden. Zum Beispiel könnten sie funktionsübergreifende Teams für bestimmte Projekte haben und gleichzeitig eine zentrale Infrastrukturverwaltung aufrechterhalten.

[7a] [21a] [22a]


**Rollen**
***

**DevOps-Ingenieur** 
Ein DevOps-Ingenieur zeichnet sich durch Expertise sowohl in der Softwareentwicklung als auch im IT-Betrieb aus und ist versiert im Einsatz neuer Technologien. Diese Rolle ist dafür zuständig, die Anforderungen von Projekten zu identifizieren und die Tools, die im Team verwendet werden, zu optimieren. DevOps-Ingenieure übernehmen die Verantwortung für die Bereitstellung der notwendigen Umgebung, die Konfiguration von Entwicklungs- und Bereitstellungspipelines sowie die Implementierung von Automatisierungslösungen. Darüber hinaus tragen sie dazu bei, das passende Team zusammenzustellen, effektive Prozesse zu definieren und sicherzustellen, dass alle erforderlichen Funktionen im gesamten Lebenszyklus eines Software-Releases nahtlos integriert sind.

**Release-Manager**
In der DevOps-Teamstruktur liegt die Verantwortung dieser Rolle im Management des gesamten Release-Lebenszyklus, beginnend bei der Entwicklung bis hin zur Auslieferung. Release-Manager gewährleisten einen reibungslosen Ablauf in jeder Phase des Prozesses und überwachen Feedback und Schlüsselkennzahlen.

**Automatisierungsarchitekt**
Die Hauptaufgabe eines Automatisierungsarchitekten besteht darin, bestehende Prozesse zu analysieren und Wege zu finden, um die Time-to-Market zu verkürzen, die Bereitstellungshäufigkeit zu erhöhen und die Mean Time To Recovery (MTTR) zu minimieren. Sie setzen bewährte Praktiken ein, um Prozesse zu rationalisieren und zu automatisieren, wodurch manuelle Aufgaben reduziert werden. Das übergeordnete Ziel besteht darin, die Effizienz des Lieferprozesses zu steigern. In vielen Fällen kann diese Verantwortung jedoch von der gesamten DevOps-Gruppe geteilt werden oder in die Zuständigkeit des DevOps-Ingenieurs fallen.

**Softwareentwickler/Tester**
Wie bei anderen DevOps-Rollen ist ein Entwickler/Tester während des gesamten Produktlebenszyklus aktiv. Sie schreiben Code für neue Produkte und Funktionen, führen Tests und Bereitstellungen durch und überwachen die Produktleistung.

**Sicherheits- und Compliance-Ingenieur**
Die Aufgabe dieses Fachmanns besteht darin, die Sicherheit der DevOps-Umgebung zu überwachen. Der Sicherheits- und Compliance-Experte arbeitet eng mit dem Entwicklungsteam zusammen, um Sicherheitsmaßnahmen in die CI/CD-Pipeline zu integrieren und die Sicherheit von Daten und Produkten sowie die Einhaltung aller erforderlichen Vorschriften sicherzustellen. Diese Rolle kann auch Teil der Verantwortung eines technischen Architekten sein.

**UX-Ingenieur**
Diese Rolle hat einen starken Bezug zur Qualitätssicherung und legt großen Wert auf die Benutzererfahrung. Die UX-Profis überprüfen, ob die Produktmerkmale den etablierten Standards entsprechen und stellen sicher, dass sie benutzerfreundlich sind und ein exzellentes Kundenerlebnis bieten.

[8a]

### DevOps Pipelines und Automation
***

DevOps-Pipelines und Automation sind zentrale Konzepte in der DevOps-Methodik, die darauf abzielen, Softwareentwicklung und -bereitstellung zu automatisieren und zu optimieren. Eine DevOps-Pipeline ist eine Reihe von Automatisierungsprozessen, die den gesamten Lebenszyklus der Softwareentwicklung und -bereitstellung abdecken
[9a]

#### Continuous Integration, Delivery und Deployment
***
Continuous Integration, Continuous Delivery und Continuous Deployment sind Ansätze, die darauf abzielen, den Prozess der Software-Veröffentlichung zu beschleunigen, indem sie Feedback-Zyklen verkürzen und wiederkehrende Aufgaben automatisieren. Diese Methoden spielen eine zentrale Rolle bei der Umsetzung des agilen Prinzips, bei dem es darum geht, wertvolle und funktionsfähige Software in kurzen Intervallen bereitzustellen, um eine kontinuierliche Verbesserung zu ermöglichen.
[10a]

**Continuous Integration**

Durch Continuous Integration tragen die einzelnen Mitwirkenden ihre Änderungen regelmäßig und frühzeitig zum Gesamtsystem bei. Dies geschieht, indem sie mindestens einmal täglich ihre Änderungen in das Versionskontrollsystem einchecken und dabei sicherstellen, dass der Build erfolgreich durchgeführt wird und alle Tests bestanden werden. Dieser Ansatz reduziert die Menge an Code, die bei einem Problem analysiert werden muss, um die Ursache zu finden. Darüber hinaus ermöglicht die zeitnahe Rückmeldung, dass Probleme schneller behoben werden können, da die Entwickler immer noch frisch im Gedächtnis haben, was sie kürzlich getan haben.

Die Begründung für diese Vorgehensweise ist recht simpel. Wenn man die Integration aufschiebt, bis der gesamte Code fertig ist, besteht die hohe Wahrscheinlichkeit, dass erhebliche Anstrengungen erforderlich sind, um den Code überhaupt kompilieren und ausführen zu können. Softwareentwicklung ist von Natur aus komplex. Selbst wenn ein ausführliches Design im Voraus erstellt wurde, ist es äußerst schwierig, Probleme zu vermeiden und präzise vorherzusagen, wie die verschiedenen Logikteile miteinander interagieren werden. Mit zunehmendem Umfang des Codes steigt die Komplexität, und entsprechend aufwändiger wird es, Änderungen vorzunehmen, wenn Probleme auftreten.

[10a]

**Continuous Delivery**

Continuous Delivery ersetzt manuelle Schritte, die für die Freigabe eines Software-Builds für die Produktionsumgebung erforderlich sind, durch einen automatisierten Prozess. Früher erfolgte oft eine Übergabe von der Entwicklungsabteilung an die Testabteilung und von dort an das Release-Management. Doch durch Continuous Delivery übernimmt das gesamte Team, bestehend aus Mitgliedern unterschiedlicher Disziplinen, die Verantwortung für den gesamten Prozess, einschließlich Build, Tests und Bereitstellung. Dies bringt mehrere Vorteile mit sich:

Besseres Verständnis für geschäftliche Anforderungen: 
Da die traditionellen Abteilungsgrenzen aufgebrochen werden, erhält das Entwicklungsteam einen besseren Einblick in die geschäftlichen und operativen Anforderungen, die erfüllt werden müssen, um das Produkt den Benutzern bereitzustellen.

Integration von Softwareentwicklungsmethoden: 
Dies ermöglicht die Integration von Methoden aus der Softwareentwicklung in einen normalerweise manuellen und oft zeitaufwändigen Prozess.

Automatisierung und Stabilität: 
Die Automatisierung der Schritte zur Bereitstellung eines Produkts beschleunigt nicht nur den Prozess, sondern verringert auch das Risiko von Fehlern. Das Produkt wird dadurch stabiler und zuverlässiger.

Die genauen Schritte für die Bereitstellung von Software und die Phasen in der Delivery-Pipeline variieren je nach den geschäftlichen und Nutzungsanforderungen. Allerdings durchläuft Software normalerweise mindestens eine Vorproduktionsumgebung vor dem eigentlichen Release.

Diese Vorproduktionsumgebungen können vielfältig gestaltet sein. Sie können Testumgebungen mit zusätzlichen Teststufen für Sicherheit, Last oder Leistung sein, Sandbox-Umgebungen, in denen Support- und Vertriebsteams mit neuen Funktionen vertraut gemacht werden, oder Akzeptanztestumgebungen, in denen Qualitätssicherungs- und Produktexperten überprüfen, ob die geplanten Änderungen wie erwartet funktionieren.
Bei Continuous Delivery wird jeder erfolgreiche Build automatisch in jeder Vorproduktionsumgebung bereitgestellt, wobei das Vertrauen in die Produktqualität mit jeder Phase zunimmt.
[10a]

**Continuous Deployment**

Wenn ein Build alle vorangehenden Phasen der Pipeline erfolgreich durchläuft, wird er automatisch in die Produktion übernommen. Dies bedeutet, dass jede Änderung sofort den Weg zu Ihrer Benutzergemeinde findet, sobald die Software alle Tests bestanden hat. Durch Continuous Deployment wird die Feedback-Schleife zwischen Codeänderung und Produktionseinsatz verkürzt, sodass Ihr Team einen frühzeitigen Einblick in das Verhalten der Änderungen in der realen Welt erhält, ohne Kompromisse bei der Qualität eingehen zu müssen.

Auch wenn die automatisierte Bereitstellung von Software für die Produktion nicht für jedes Produkt und jede Organisation geeignet ist, lohnt es sich, die dazu erforderlichen Schritte zu betrachten, da jedes einzelne Element bereits für sich genommen wertvoll ist.
[10a]

#### Releasing vs Deployment
***
Das Deployment zielt darauf ab, die entwickelte Software auf dem Zielsystem zu installieren und lauffähig zu machen.
Eine Software-Version ist ein Entwicklungsstand zu einem bestimmten Zeitpunkt. Ein Release ist ein Deployment auf dem Produktivsystem einer bestimmten Version.


**Deployment**
Das Deployment, auch Verteilung oder Bereitstellung der Software, ist ein Schritt der Softwareentwicklung, der darauf abzielt, die entwickelte Software auf dem Zielsystem zu installieren und lauffähig zu machen.

Die Bereitstellung bedeutet nicht, dass das Projekt damit bereits abgeschlossen ist. Denn zum einen kann ein Deployment auch regelmäßig erfolgen und zum anderen kann Software nicht nur auf das Produktivsystem, sondern auch auf dem Entwicklungs- oder Testsystem verteilt werden, auf dem Entwickler ihre Änderungen ausprobieren oder mit dem Kunden testen könne

Ort: Deployment erfolgt normalerweise in spezifischen Umgebungen, wie beispielsweise Entwicklung, Test oder Produktion. Es kann auch intern in der Entwicklungs- oder Testumgebung stattfinden, bevor es in die Produktion übergeht.
Beteiligte: Das Deployment kann von DevOps-Teams oder Systemadministratoren durchgeführt werden, um sicherzustellen, dass die Software auf den Zielsystemen ordnungsgemäß installiert und konfiguriert ist.


[11a] [12a]

**Releasing**

Zweck: Ein Release bezieht sich auf die Freigabe einer bestimmten Version einer Anwendung oder eines Softwareprodukts für den allgemeinen Gebrauch oder für bestimmte Zielgruppen. Ein Release ist eine geschäftliche Entscheidung, bei der eine Version als stabil und bereit für die Verwendung angesehen wird.
Ort: Ein Release kann in verschiedenen Umgebungen bereitgestellt werden, einschließlich Produktion. Es bezieht sich jedoch auf die Freigabe der Software im Allgemeinen und kann auch Aktualisierungen, Bugfixes oder neue Funktionen enthalten.
Beteiligte: Die Freigabeentscheidung wird normalerweise von den Geschäftseinheiten getroffen, wobei verschiedene Stakeholder wie Produktmanager, Qualitätsprüfer und technische Teams involviert sind. Das Release-Management spielt eine Schlüsselrolle bei der Planung und Koordinierung von Releases.
[11a] [12a]


In Zusammenfassung bezieht sich Deployment auf die technische Aktion des Verteilens und Aktivierens von Code oder Anwendungen in bestimmten Umgebungen, während Release die geschäftliche Entscheidung darstellt, eine bestimmte Version der Software für die Verwendung freizugeben. Die Unterscheidung zwischen diesen beiden Konzepten ist wichtig, da sie die Planung, Koordination und Kommunikation zwischen den verschiedenen Teams und Stakeholdern in DevOps-Umgebungen beeinflusst.


#### Semantic Versioning
***

Semantic Versioning, ist ein Konzept zur Versionsverwaltung von Software, das darauf abzielt, die Bedeutung von Änderungen an der Software zu kommunizieren.
Es erleichtert die Entscheidung, ob ein Update durchgeführt werden sollte, und minimiert das Risiko von Inkompatibilitäten.
Es legt fest, wie Versionen nummeriert werden sollen, um die Art der Änderungen an der Software zu kennzeichnen.

Auf Grundlage einer Versionsnummer von MAJOR.MINOR.PATCH werden die einzelnen Elemente folgendermaßen erhöht:

MAJOR wird erhöht, wenn API-inkompatible Änderungen veröffentlicht werden.
MINOR wird erhöht, wenn neue Funktionalitäten, die kompatibel zur bisherigen API sind, veröffentlicht werden, 
PATCH wird erhöht, wenn die Änderungen ausschließlich API-kompatible Bugfixes umfassen.

[13a]

#### Deployment strategies
***
Eine Bereitstellungsstrategie ist eine Methode, die von DevOps-Teams verwendet wird, um eine neue Version ihrer bereitgestellten Softwarelösung erfolgreich in Betrieb zu nehmen. Diese Strategien regeln, wie der Netzwerkverkehr in einer Produktionsumgebung von der alten Version auf die neue Version umgestellt wird. Je nach den spezifischen Anforderungen und Schwerpunkten eines Unternehmens kann die Wahl der Bereitstellungsstrategie erheblichen Einfluss auf Ausfallzeiten und Betriebskosten haben.
[14a]
#### Blue-Green( Rot/Schwarz)
***
Bei der Blau/Grün-Bereitstellung läuft die neue Version der Software parallel zur alten Version. Nachdem die neue Version erfolgreich getestet und zertifiziert wurde, dass sie alle Anforderungen erfüllt, übernimmt ein Load Balancer automatisch den Datenverkehr von der älteren Version auf die neuere Version.

Hauptvorteile:
Keine Ausfallzeiten: Mit der Blau/Grün-Bereitstellung ist ein schneller Wechsel ohne Ausfallzeiten möglich.
Sofortiges Rollback: Während des Bereitstellungsprozesses kann jederzeit ein Rollback durchgeführt werden. Hierzu wird der Load Balancer so konfiguriert, dass der Datenverkehr zurück zur blauen Umgebung geleitet wird. Die Auswirkungen auf die Ausfallzeit beschränken sich auf die Zeit, die benötigt wird, um den Verkehr in die blaue Umgebung zu verschieben, nachdem ein Problem erkannt wurde.
Trennung der Umgebungen: Die Blau/Grün-Bereitstellung gewährleistet, dass das Starten einer parallelen grünen Umgebung keine Auswirkungen auf Ressourcen hat, die die blaue Umgebung unterstützen. Diese Trennung reduziert das Risiko während der Bereitstellung.

Hinweise:
Kosten und operativer Aufwand: Die Anwendung des Blau/Grün-Bereitstellungsmusters kann mit höherem operativem Aufwand und erhöhten Kosten verbunden sein, da doppelte Umgebungen mit identischer Infrastruktur gewartet werden müssen.
Abwärtskompatibilität: Blaue und grüne Bereitstellungen können Datenpunkte und Datenspeicher gemeinsam nutzen. Daher ist es ratsam sicherzustellen, dass beide Versionen der Anwendung das Schema des Datenspeichers und das Format der Datensätze unterstützen. Diese Abwärtskompatibilität ist erforderlich, wenn ein nahtloser Wechsel zwischen den beiden Versionen bei einem Rollback erfolgen soll.
Umstellung: Wenn Sie die aktuelle Version außer Betrieb nehmen möchten, wird empfohlen, einen angemessenen Verbindungsausgleich für laufende Transaktionen und Sitzungen zu ermöglichen. Dieser Schritt gewährleistet, dass Anfragen, die von der aktuellen Bereitstellung verarbeitet werden, ordnungsgemäß abgeschlossen oder beendet werden können.


[14a] [15a]

#### Canary
***
Die Canary-Bereitstellung ist eine Strategie, bei der das Bereitstellungsteam die neue Version der Software einrichtet und schrittweise den Produktionsverkehr von der älteren Version auf die neuere Version umstellt. Während des Bereitstellungsprozesses kann zu einem bestimmten Zeitpunkt die ältere Version beispielsweise 90 % des gesamten Datenverkehrs für die Software bewältigen, während die neuere Version 10 % des Datenverkehrs hostet. Mit dieser Bereitstellungstechnik können die DevOps-Ingenieure die Stabilität der neuen Version testen, indem sie den Live-Datenverkehr einer ausgewählten Gruppe von Endbenutzern auf verschiedenen Ebenen verwenden, die sich im Laufe der Produktion verändern.

Hauptvorteile:
Möglichkeit zum Testen des Live-Produktionstraffics: Anstelle einer reinen Simulation in einer Staging-Umgebung können Sie mit Canary-Tests den Live-Produktionstraffic verwenden. Bei Canary-Rollouts entscheiden Sie, in welchem Umfang Sie die neue Anwendung bei jedem Schritt freigeben und wann Sie den nächsten Schritt in einem Release auslösen. Der Canary-Test erfordert ausreichend Traffic, um Probleme zweifelsfrei zu erkennen.
Schnelles Rollback: Sie können schnell ein Rollback durchführen, indem Sie den Nutzertraffic zur älteren Version der Anwendung zurückleiten.
Keine Ausfallzeiten: Mit Canary-Releases können Sie den Live-Produktionstraffic ohne Unterbrechungen an verschiedene Versionen der Anwendung weiterleiten.

Hinweise:
Langsame Einführung: Bei jedem schrittweisen Release ist ein Monitoring über einen angemessenen Zeitraum erforderlich, wodurch sich der gesamte Release verzögern kann. Canary-Tests können oft mehrere Stunden dauern.
Beobachtbarkeit: Die effektive Umsetzung von Canary-Tests erfordert die Möglichkeit, Ihre Infrastruktur und Ihr Anwendungspaket effizient zu überwachen. Die Implementierung eines robusten Monitorings kann einen erheblichen Aufwand erfordern.
Abwärtskompatibilität und Sitzungstreue: Wie bei Rolling Updates können auch bei Canary-Tests Risiken in Bezug auf Abwärtskompatibilität und Sitzungspersistenz auftreten, da während der Bereitstellung der Canary-Version in der Umgebung mehrere Anwendungsversionen ausgeführt werden.

[14a] [15a]


#### Feature flags
***
Feature Toggles, auch als "Feature Flags" bezeichnet, sind eine Technik, um die Bereitstellung von Software von der Freigabe zu entkoppeln und bieten eine Alternative zu Feature Branches. Diese Methode beschleunigt die Entwicklung, da sie das Erstellen von Branches und das Zusammenführen von Code überflüssig macht. Dadurch können viele kleine inkrementelle Versionen einer Software bereitgestellt werden, da Entwicklern ermöglicht wird, neue oder unvollständige Funktionen zu verbergen, so dass sie in der Benutzeroberfläche nicht sichtbar sind. Dies wird oft als "In-Code Branching" bezeichnet.

Es gibt Frameworks wie togglz [5], die eine benutzerfreundliche Oberfläche bieten, um alle Schalter zu verwalten, zu aktivieren oder zu deaktivieren, möglicherweise in Verbindung mit einer speziellen Freigabestrategie. Dabei ist es möglich, eine Funktion nur für ausgewählte Benutzer bereitzustellen, beispielsweise anhand von Kriterien wie Namen, IP-Adresse oder Standort, oder schrittweise mit einem kleinen Prozentsatz (ähnlich dem Canary Deployment). Mit diesem Ansatz kann A/B-Testing durchgeführt werden, bei dem eine Funktion nur für einen Teil der Benutzer aktiviert wird, um zu überprüfen, ob die Änderung akzeptiert wird. Wenn ein Feature Fehler verursacht oder nicht wie erwartet funktioniert, kann der Schalter deaktiviert werden, und die Entwickler können an einem neuen Inkrement für die Bereitstellung arbeiten. Dieses Verhalten wird als "fix forward" bezeichnet und bedeutet, dass es keine Notwendigkeit für Rollbacks gibt. Das kann viel Zeit sparen, da die Vorbereitung von Datenbankskripten, um auf die vorherige Version zurückzukehren, entfällt. Schließlich können Feature-Schalter auch verwendet werden, um eine Anwendung in den Wartungsmodus zu versetzen.

Entwickler müssen den Einstiegspunkt eines Features in ihrem Code mit einem if-else-Konstrukt umgeben, wie im folgenden Beispiel dargestellt:

```java
if (Features.ENABLE_IMPORT.isActive()) {
  LOG.info("IMPORT gestartet");
  try {
    Future<Boolean> future = importService.holeDatenVonOnlineAntrag();
    // Weitere Verarbeitung
  } catch (Exception e) {
    // Fehlerbehandlung
  }
} else {
  LOG.info("IMPORT nicht möglich");
}
```
Ein Codeblock, der mithilfe eines Schalters deaktiviert wurde, ist ähnlich wie auskommentierter Code.

Es ist wichtig sicherzustellen, dass die Schalter entfernt werden, sobald sie nicht mehr benötigt werden, da ansonsten toter Code entsteht, der zu technischen Schulden führen kann. Feature Toggles können in einer Datenbank oder als Konfigurationseigenschaft in einer Konfigurationsdatei gespeichert werden.

[16a]

#### CI/CD-Tools
***
Ein CI/CD-Tool spielt eine entscheidende Rolle beim Management, der Koordination und der Automatisierung der verschiedenen Phasen in der Pipeline. Dies umfasst das Initiieren des Prozesses nach einem Commit, die Steuerung des Build-Vorgangs, die Durchführung automatisierter Tests, das Veröffentlichen von Artefakten und das Erfassen sowie Weiterleiten von Feedback.
Die Auswahl des geeigneten Tools für Continuous Integration (CI) oder Continuous Development/Delivery (CD) ist ein entscheidender Schritt bei der Implementierung Ihrer CI/CD-Pipeline.
[17a]

#### CI Server (Jenkins, Github-Actions, etc.)
***
Der CI-Server ist in der Regel ein zentraler Bestandteil des Tools und spielt eine Schlüsselrolle bei der Koordination der kontinuierlichen Integration. Er gewährleistet, dass Code-Änderungen regelmäßig überwacht, getestet und bereitgestellt werden. Dies trägt dazu bei, die Softwarequalität zu verbessern und die Entwicklungsprozesse effizienter zu gestalten.

Der CI-Server, auch als Build-Server bekannt, ist entscheidend für die Implementierung und Verwaltung des gesamten Prozesses. Er fungiert als Verbindungsglied zwischen den einzelnen Phasen der Pipeline, koordiniert automatisierte Aufgaben gemäß Ihrer Geschäftslogik und sammelt sowie liefert Feedback.

Jenkins: Jenkins ist eines der führenden Open-Source-Tools für CI/CD. Der Jenkins-Server ermöglicht die Automatisierung von Build-, Test- und Bereitstellungsprozessen und bietet eine breite Palette von Plugins und Erweiterungsmöglichkeiten.

GitHub Actions: GitHub Actions bietet CI-Workflows an, die Code in Ihrem Repository erstellen und Tests ausführen können. Diese Workflows können auf GitHub-gehosteten virtuellen Maschinen oder auf selbst gehosteten Computern ausgeführt werden. Sie können den CI-Workflow so konfigurieren, dass er bei bestimmten GitHub-Ereignissen, wie einem Code-Push in das Repository, einem festen Zeitplan oder einem externen Ereignis, basierend auf Webhooks, ausgelöst wird.

GitHub führt die CI-Tests durch und stellt die Ergebnisse im Pull Request bereit, sodass Sie feststellen können, ob die Änderungen im Branch Fehler verursachen. Nachdem alle CI-Tests in einem Workflow erfolgreich bestanden wurden, können die eingereichten Änderungen von einem Teammitglied überprüft oder in den Hauptzweig übernommen werden. Wenn ein Test nicht besteht, kann die Ursache in einer der vorgenommenen Änderungen liegen.
[19a] [18a]
        
#### Secrets management
***
Was sind Secrets?
"Secrets" sind nicht-menschliche privilegierte Anmeldedaten, die im Wesentlichen als vertrauliche Informationen dienen und als Schlüssel fungieren, um auf geschützte Ressourcen oder sensible Daten in Tools, Anwendungen, Containern und in DevOps- sowie Cloud-nativen Umgebungen zuzugreifen.

Zu den gängigsten Arten von Secrets gehören:

Anmeldedaten privilegierter Accounts:
Passwörter
Zertifikate
SSH-Schlüssel
API-Schlüssel
Verschlüsselungsschlüssel
Was ist Secrets Management?
Secrets Management wird in der Cybersicherheitsbranche als bewährte Praxis angesehen und ermöglicht Unternehmen, Sicherheitsrichtlinien für nicht-menschliche Identitäten konsequent umzusetzen. Secrets Management bietet die Gewissheit, dass Ressourcen in sämtlichen Tool-Stacks, Plattformen und Cloud-Umgebungen nur authentifizierten und autorisierten Benutzern zugänglich sind.

Im Allgemeinen umfasst Secrets Management die folgenden Schritte. Viele dieser Ansätze und Techniken werden auch verwendet, um privilegierten Zugriff für menschliche Benutzer zu schützen:

Authentifizierung aller Zugriffsanfragen, bei denen nicht-menschliche Anmeldedaten verwendet werden.
Durchsetzung des Prinzips des geringsten Privilegs (Least Privilege).
Umsetzung rollenbasierter Zugriffskontrolle (Role-Based Access Control, RBAC) und regelmäßige Rotation von Secrets und Anmeldedaten.
Automatisierung des Secrets Management und Anwendung konsistenter Zugriffsrichtlinien.
Verfolgung aller Zugriffe und Erstellung eines umfassenden Audit-Trails.
Entfernung von Secrets aus Code, Konfigurationsdateien und anderen ungeschützten Bereichen.

[20a]

### CAMS, CALMS, CALMAS
CAMS, CAMLS und CALMAS sind konzeptionelle Rahmen, die sich auf die Integration zwischen Entwicklern (Softwareentwicklern) und IT-Betriebsteams (IT-Operatoren) in der Softwareentwicklung konzentrieren.
CALMAS ist eine erweiterte Version dieser Rahmen, die sechs Schlüsselaspekte hervorhebt:
Kultur (Culture), Automatisierung (Automation), Schlankheit (Lean), Messung (Measurement), Agilität (Agile) und Teilen (Sharing). Diese Aspekte spielen eine entscheidende Rolle bei der Förderung der Zusammenarbeit, der Effizienz und der Qualität in der Softwareentwicklung.
Während CAMS und CAMLS wichtige Grundlagen bieten, hebt CALMAS die Bedeutung von Agilität und Wissensaustausch hervor, um die Integration zwischen Entwicklung und Betrieb zu optimieren.
Dieser ganzheitliche Ansatz zielt darauf ab, die Entwicklererfahrung zu verbessern und den Wertstrom in der Softwareentwicklung zu optimieren.
[4b,12b]

* **Culture:** Unternehmensweite geltende Werte, Überzeugungen und Haltungen. Beschreiben das Handeln in Entwicklung und Betrieb.

* **Automation:** Alles was Automatisiert werden kann sollte auch Atomatisiert werden.
    * Fehler reduzierung, und optimisierung 

* **Lean:** Überschuss reduzieren bei einhaltung der gewüschten Ergebnisse.
    * Meetings veringern, Teams verkleinern, Werkzeuge auf ein Minimum reduzieren

* **Measurement:** Messen der Effizienz und Qualität der Softwareentwicklung, durch Sammeln von Daten um Systeme und Ereignisse seinsehbar und transparent zu gestallten.

* **Agile:** Agile Entwicklungsmethoden, wie Scrum, Kanban, XP, etc.

* **Sharing:** Wissen und Informationen Abteilungs übergeifend teilen und weitergeben.

### SPACE Framework
"SPACE" ist ein Framework zur Verbesserung der Softwareentwicklungseffizienz.
Es wurde von Nicole Forsgren entwickelt, die später bei den DORA-Metriken erneut auftaucht.
"SPACE" steht für fünf Schlüsselaspekte der Produktivität: Zufriedenheit und Wohlbefinden, Leistung, Aktivität, Kommunikation und Zusammenarbeit, sowie Effizienz und Flow.
Dieses Framework bietet eine umfassende Perspektive auf die Produktivität in der Softwareentwicklung und zielt darauf ab, Verbesserungen in diesen Bereichen zu fördern.

[5b,12b]

### DevEx Framework
Das DevEx Framework, abgekürzt für "Developer Experience" (Entwicklererfahrung), dreht sich um die Wahrnehmung der Entwickler hinsichtlich dessen, wie sie sich fühlen, was sie denken und wie sie ihre Arbeit bewerten.
DevEx umfasst drei Kernpunkte:

Feedback-Loops: Schnelles Feedback ist entscheidend, um die Effizienz zu steigern.
Dies beinhaltet die Vermeidung von Verzögerungen bei der Veröffentlichung von Funktionen und die Förderung einer reibungslosen und schnellen Arbeitsweise durch effektive Kommunikation.

Cognitive Load: Mit der raschen Entwicklung in der Softwareentwicklung ist die Komplexität und die kognitive Belastung der Entwickler gestiegen.
Eine höhere kognitive Belastung führt zu mehr Fehlern und einer langsameren Entwicklung.

Flow-State: Dies ist ein mentaler Zustand, in dem eine Person vollständig in eine Aktivität vertieft ist.
Dies umfasst die Minimierung von Unterbrechungen und übermäßigen Besprechungen sowie die Unterstützung dieses Zustands durch Automatisierung und klare Zielsetzungen.

[6b,12b]
### DORA Metriken
Die DORA-Metriken sind Metriken zur Messung der Softwareentwicklungseffizienz.
Menschen sind sehr aber sehr komplex, daher ist es schwierig, die Effizienz zu messen.
DORA-Metriken sind ein Versuch, die Effizienz zu messen und durch sie zu verbessern. Sie bieten dabei keinen Nachteil zwischen Software  Geschwindigkeit und Qualität.


Die DORA-Metriken sind enstanden, durch die sammlung und analyse von Daten der Praktiken der Softwarebereitstellung.
Die Ergebisse dieser Analysen waren dabei die bei weitem gründlichste Untersuchung der Effinzienz und Qualität in der Softwareentwicklung.
Dies waren die State of DevOps Reports.
Ein paar Jahre später entwickelten Nicole Forsgren, Jez Humble und Gene Kim die DORA Metriken.
Durch die State of DevOps Reports kann man sicher sagen dass die DORA Metriken State of the Art sind.
Die DORA Metriken sind durch Folgende Aspekte charakterisiert:

[1b,3b,12b]
#### Deployment Frequency
Deplyment Frequency ist ein Indikator für die Geschwindigkeit der Softwareentwicklung.
Es misst die Kosten der Entwicklung in bezug auf Geld aber auch Zeit und Arbeitskraft.
Besonders wird aber damit die Rate in der neue Features veröffentlicht werden gemessen.

[3b,12b]
#### Change Lead Time
Die Change Lead Time auch ein Indikator für die Geschwindigkeit der Softwareentwicklung.
Es beinhlatet die Zeit zwischen dem Beginn einer Änderung und der erfolgreichen Nutzung in der Produktion.
Auch her geht es um die Kosten der Entwicklung.

[3b,12b]
#### Mean Time to Restore
Die Mean Time to Restore gibt an wie lange es dauert ein Problem zu beheben, bzw. die Software wieder in einen funktionierenden Zustand zu bringen.
Dieser Aspekt überprüft die Code Qualität, da durch einen sauberen und lesnaren code Fehler deutlich schneller erkannt und behoben werden können.

[3b,12b]
#### Change Failure Rate
Die Change Failure Rate ist ein auch Indikator für die Qualität der Softwareentwicklung.
Sie misst die Anzahl der Änderungen/Features, die zu einem Problem oder Ausfall führen.
Die Change Failure Rate beschreibt somit die Quantität der Ausfälle, während die Mean Failure die Qualität/Schwere der Ausfälle beschreibt.

[3b,12b]
### Ziel
Die DORA Metriken sollen die Effizienz der Softwareentwicklung messen 
und damit auf lange Sicht den Erfolg des Projektes steigern und nicht kurzfristig Features um Features zu veröffentlichen.

[3b,12b]
### Falsche Interpretation
Die DORA Metriken werden oft falsch interpretiert, da der Mensch dazu neigt sich nur auf die Bewertung zu konzentrieren und verliert, damit das eigenetliche Ziel aus den Augen.
Zum Beispiel gibt es Fälle in dennen Entwickler die Change Failure Rate einfach nur als BugCount gesehen haben und diesen dann einfach nur reduziert haben, indem die nur die wichtigsten Bugs bearbeitet wurden.

[3b,12b]
## DevSecOps
* DevSecOps steht für Development, Security und Operations.
* DevSecOps ist eine Praxis bei der man Sicherheits Test in jeden Entwicklungsschritt einbaut.
* fördert Zusammenarbeit zwischen Entwicklern, Sicherheitsspezialisten und Betriebsteams zu fördern.
* Sicherheit wird hier zu einem früheren Zeitpunkt in den Entwicklungsprozess integriert.

DevSecOps steht für Development, Security und Operations. Es ist eine Praxis, die darauf abzielt, Sicherheit in den gesamten Lebenszyklus der Anwendungsentwicklung zu integrieren. DevSecOps fördert die Zusammenarbeit zwischen Entwicklern, Sicherheitsspezialisten und Betriebsteams, um die Sicherheit zu verbessern. Es ist eine Erweiterung von DevOps, die Sicherheit zu einem früheren Zeitpunkt in den Entwicklungsprozess integriert.

[7b,12b]
### "Shift left"-testing
Shift Left Testing ist eine der Methoden von DevSecOps.
Entwickler überprüfen ihre Software auf Sicherheitslücken, bevor sie in die Produktion geht. Das Antipatter dazu wäre "Shift right"-testing, bei dem die Software erst in der Produktion auf Sicherheitslücken überprüft wird oder schlimmer dass die Kunden die Sicherheitslücken erst entdecken.

[7b,12b]
### Sicherheitsziele der Kryptographie
Sicherheitsziele sind im Allgemeinene Richtilinien an ein System, um schtützenswerte Güter zu schützen.
In der Computersicherheit sind das die Vertraulichkeit, Integrität und Verfügbarkeit von Daten.
Gefährdung dieser geschieht meist bei der übertragung von Daten.
Für die Meisten dieser Ziele schafft Kryptographie abhilfe.

[8b,12b]
#### Authentizität, Integrität, Verbindlichkeit, Zurechenbarkeit, Vertraulichkeit, Verfügbarkeit
Sicherheitsziele können in einge unter Katogorien eingeteilt werden.

* **Authentizität:** Echtheit, Überprüfbarkeit und Vertrauenswürdigkeit von Daten
* **Integrität:** Daten sind unverändert und unverfälscht
* **Verbindlichkeit:** durchgeführte Handlungen können nicht abgestritten werden können. z.b. bei elekrtonischem Abschulss eines Vertrages(Signatur)
* **Zurechenbarkeit:** Handlungen müssen eine Person zugerechnet werden können
* **Vertraulichkeit:** Daten dürfen nur von Autorisitirten Personen eingesehen und verändert werden.
* **Verfügbarkeit:** Vermeidung von Systemausfällen, Zugriff auf Daten muss gewährleistet sein.

[8b,12b]
### Threat Modeling (Bedrohungsmodellierung)
Bedrohungmodellierung ist eine Prozess bei dem potentielle Bedrohungen für ein System indentifiziert und bewertet wird.
Auch das Fehlen von entsprechender Schutmaßnahmen wird dabei berücksichtigt.
Gegenmanßnahmen werden hiernach priorisiert und implementiert.

[9b,12b]
#### STRIDE
Einer der Mothden zur Bedrohungsmodellierung ist STRIDE.
STRIDE ist ein Model zur Klassifizierung von folgenden Bedrohungen Spoofing, Tampering, Repudiation, Information Disclosure, Denial of Service und Elevation of Privilege.

* **Spoofing:** Fälschung von Identitäten. Angriff auf Accont eines anderen Benutzers oder eigenene Identität fälschen. 
* **Tampering:** Veränderung von Daten in einer Datenbank oder im Netzwerkverkehr.
* **Repudiation:** Verschleiern von bösartigen Handlungen in einem System.
* **Information Disclosure:** Unbefugter Zugriff auf Daten.
* **Denial of Service:** Verhindern der Verfügbarkeit eines Systems, durch zum Beispiel überlastung(eher bekannt als DDos Attacke)
* **Elevation of Privilege:** Unerlaubte erweiterung von Zufgriffsrechten.

[10b,11b,12b]
## Referenzen
***
[1a]  : https://de.wikipedia.org/wiki/DevOps<br>
[2a]  : https://www.atlassian.com/de/devops<br>
[3a]  : https://www.ibm.com/de-de/topics/devops<br>
[4a]  : https://www.atlassian.com/de/devops/what-is-devops/devops-culture<br>
[5a]  : https://mindsquare.de/knowhow/devops/#vorteile<br>
[6a]  : https://weissenberg-group.de/was-ist-devops/#:~:text=Das%20ultimative%20Ziel%20einer%20DevOps,schneller%20und%20einfacher%20zu%20liefern<br>
[7a]  : https://www.atlassian.com/de/devops/frameworks/team-structure#:~:text=DevOps%2DTeams%20bestehen%20normalerweise%20aus,der%20Verwaltung%20der%20Infrastruktur%20auskennen<br>
[8a]  : https://www.objectivity.de/blog/aufbau-einer-effizienten-devops-teamstruktur/<br>
[9a]  : https://www.atlassian.com/de/devops/devops-tools/devops-pipeline#:~:text=Was%20ist%20die%20DevOps%2DPipeline,f%C3%BCr%20eine%20Produktionsumgebung%20arbeiten%20k%C3%B6nnen<br>
[10a] : https://www.jetbrains.com/de-de/teamcity/ci-cd-guide/continuous-integration-vs-delivery-vs-deployment/<br>
[11a] : https://dakitec.de/software-entwicklung/deployment#:~:text=Das%20Deployment%20zielt%20darauf%20ab,dem%20Produktivsystem%20einer%20bestimmten%20Version<br>
[12a] : https://chat.openai.com/c/65fcfde4-4f21-4912-bcd4-c5b175833b7c<br>
    frage: was ist der unterschied zwischen release und deployment im DevOps bereich<br>
[13a] : https://semver.org/<br>
[14a] : https://www.plutora.com/blog/deployment-strategies-6-explained-in-depth<br>
[15a] : https://cloud.google.com/architecture/application-deployment-and-testing-strategies?hl=de<br>
[16a] : https://entwickler.de/devops/roadmap-einer-spannenden-reise<br>
[17a] : https://www.jetbrains.com/de-de/teamcity/ci-cd-guide/ci-cd-tools/#:~:text=Ein%20CI%2FCD%2DTool%20leistet,dem%20Ver%C3%B6ffentlichen%20von%20Artefakten%20und<br>
[18a] : https://docs.github.com/de/actions/automating-builds-and-tests/about-continuous-integration<br>
[19a] : https://www.jetbrains.com/de-de/teamcity/ci-cd-guide/ci-cd-tools/servers/#:~:text=Der%20CI%2DServer%20(oder%20Build,und%20Feedback%20sammelt%20und%20bereitstellt<br>
[20a] : https://www.cyberark.com/de/what-is/secrets-management/#:~:text=Was%20ist%20Secrets%2DManagement%3F,Sicherheitsrichtlinien%20f%C3%BCr%20nicht%20menschliche%20Identit%C3%A4ten<br>
[21a] : https://www.dev-insider.de/die-ideale-devops-teamstruktur-a-862217/<br>
[22a] : https://chat.openai.com/c/9ed09955-46c1-45b9-b032-ec8ee9756bab frage: was sind gängige DevOps team Strukturen?<br>
[23a] : https://kruschecompany.com/de/devops-guide/#DevOps_als_Prozesse_und_Praktiken<br><br>


[1b] :https://chat.openai.com/<br>
[2b] :https://blog.up bound.io/developers-and-operators-complicated-relationship<br>
[3b] :https://www.youtube.com/watch?v=hbeyCECbLhk<br>
[4b] : https://www.computerweekly.com/de/definition/CALMS#:~:text=CALMS%20ist%20ein%20konzeptioneller%20Rahmen,)%20und%20Sharing%20(Austausch)<br>
[5b] :https://www.swarmia.com/blog/space-framework/?utm_term=space%20framework&utm_campaign=SRH-SPACE-EU-EN&utm_source=adwords&utm_medium=ppc&hsa_acc=6644081770&hsa_cam=19643106124&hsa_grp=145044312719&hsa_ad=646821562962&hsa_src=g&hsa_tgt=kwd-567479290791&hsa_kw=space%20framework&hsa_mt=e&hsa_net=adwords&hsa_ver=3&gad_source=1&gclid=Cj0KCQjwtJKqBhCaARIsAN_yS_lvUSBQFNwT_lFYrpV_pLv4g7HcPFGqhDenxk8YrhUgQVOY5uuql88aAvDAEALw_wcB<br>
[6b] :https://queue.acm.org/detail.cfm?id=3595878<br>
[7b] :https://aws.amazon.com/de/what-is/devsecops/#:~:text=building%20the%20software.-,What%20does%20DevSecOps%20stand%20for%3F,they%20are%20building%20software%20applications<br>
[8b] :https://www.identible.de/glossar/sicherheitsziele.html<br>
[9b] :https://en.wikipedia.org/wiki/Threat_model<br>
[10b] :https://de.wikipedia.org/wiki/STRIDE_(IT-Sicherheit)<br>
[11b] :https://geballte-sicherheit.de/threat-modelling-bedrohungsanalyse-4-teil-ermittlung-und-einstufung-von-bedrohungen/<br>
[12b] :Teilweise Formulierung von Git-Hub Co-Piolot<br>