class: center, middle

## [Software Engineering](../../praesentationen.html)

#### Kapitel 5

# DevOps und DevSecOps

Sascha Hahn,Simon Fedrau

---
# Inhalt
***
1. DevOps
  1. Kultur, Ziele, Vorteile, Praktiken

  1. DevOps Teams

  1. DevOps Pipelines und Automation

1. DevSecOps
1. Zusammenfassung
1. Quellen

---
### DevOps
***

![:scale 80%](media\Titelbild-devops-tools-definition-best-practice.png)

DevOps ist eine Sammlung unterschiedlicher technischer Methoden und eine Kultur zur Zusammenarbeit zwischen Softwareentwicklung und IT-Betrieb.

---
### Kultur
***

![:scale 70%](media\DevOps_Culture.jpg)
---
### Ziele
***
Das große Ziel von DevOps ist die Schaffung eines wiederholbaren Systems, das Automatisierung nutzt und kontinuierliche Verbesserungen ermöglicht, um qualitativ hochwertige Produkte schnell und einfach zu liefern.

![:scale 60%](media\Titelbild-devops-tools-definition-best-practice.png)
---
### Vorteile von DevOps
***

 - Verstärkte Zusammenarbeit und Vertrauensbildung  

 - Förderung klügerer und transparenterer Arbeitsweisen  

 - Beschleunigte Release-Zyklen                         

 - Verkürzte Reaktionszeiten bei Problemen               

 - Bessere Bewältigung unvorhergesehener Aufgaben        

 - Steigerung der Produktivität                         
 - Häufigere Releases durch Automatisierung und Tools   
 - Verkürzter Feedbackprozess für schnellere Problembehebung 

 - Anpassungsfähigkeit und agile Priorisierung            

---
### Praktiken
***

* DevOps Praktiken sind meist eine Reihe von Aktionen, die in einer bestimmten Reiehnfolge ausgeführt werden.
* DevOps Praktiken sind dafür gemacht, bestimmte Phasen innerhalb eines Prozesses zu beschleunigen

---
### DevOps Teams
***

**Teamzusammensetzung**

* DevOps-Teams setzen auf Mitglieder mit Fachkenntnissen in Softwareentwicklung und Operations.
* Teammitglieder haben unterschiedliche Stärken, von der Code-Erstellung bis zur Betriebsführung und Infrastrukturverwaltung.
* Das Spektrum kann Release-Manager und Automatisierungsarchitekten umfassen.

**Qualifikationen für DevOps-Teammitglieder**

* Solide technische Fähigkeiten: Umfassen Kenntnisse in Entwicklung und Betrieb, Automatisierung, Infrastruktur, und mehr.

* Effektive Kommunikation: Wichtige Fähigkeit zur Koordination und Zusammenarbeit im Team.

* Bereitschaft zur Teamarbeit: DevOps erfordert enge Zusammenarbeit und gemeinsame Verantwortung.

* Anpassungsfähigkeit: Die Fähigkeit, sich an neue Technologien und Methoden anzupassen, ist entscheidend.

---
### Rollen 
***

* DevOps-Ingenieur

* Release-Manager
* Automatisierungsarchitekt

* Softwareentwickler/Tester

* Sicherheits- und Compliance-Ingenieur

* UX-Ingenieur

---

### DevOps Pipelines und Automation
***
* DevOps-Pipelines und Automation sind zentrale Konzepte in der DevOps-Methodik, die darauf abzielen, Softwareentwicklung und -bereitstellung zu automatisieren und zu optimieren. 
* Eine DevOps-Pipeline ist eine Reihe von Automatisierungsprozessen, die den gesamten Lebenszyklus der Softwareentwicklung und -bereitstellung abdecken

* Continuous Integration, Delivery und Deployment stellen Schlüsselstellen in der Pipeline dar

![:scale 60%](media\devops_circle.png)

---
### Continuous Integration
***

* Frühe Integration: Entwickler tragen regelmäßig und frühzeitig Änderungen zum Gesamtsystem bei.

* Erfolgreicher Build und Tests: Sicherstellen, dass der Code erfolgreich kompiliert und alle Tests bestanden werden.

* Reduzierte Fehlersuche: Weniger Code muss bei Problemen analysiert werden, da Ursachen schneller ermittelt werden.

* Effiziente Problemlösung: Frühe Integration erleichtert die frühzeitige Fehlererkennung und effiziente Problembehebung.

![:scale 60%](media\Coninous Inegration.png)

---
### Continuous Delivery
***

**Was ist Continuous Delivery?**

* Automatisiert Freigabeprozesse

* Teamweit geteilte Verantwortung

**Vorteile von Continuous Delivery**

* Besseres Verständnis für geschäftliche Anforderungen

* Integration von Softwareentwicklungsmethoden
* Automatisierung und Stabilität

**CD-Prozess**

* Automatische Bereitstellung

* Steigerndes Vertrauen in Produktqualität

---

### Continuous Deployment
***
**Was ist Continuous Deployment?**

* Automatische Übernahme von Builds in die Produktion.

* Änderungen gelangen sofort zur Benutzergemeinschaft nach erfolgreichen Tests.

**Vorteile von Continuous Deployment**
* Verkürzte Feedback-Schleife.

* Früher Einblick in das Verhalten von Änderungen in der realen Welt.
* Keine Kompromisse bei der Qualität.

---
### Releasing vs Deployment
***

**Deployment**

* Installiert und macht die entwickelte Software lauffähig.
* Kann in verschiedenen Umgebungen erfolgen (Entwicklung, Test, Produktion).
* Durchgeführt von DevOps-Teams oder Systemadministratoren.

**Releasing**

* Freigabe einer stabilen Version für den allgemeinen Gebrauch oder bestimmte Zielgruppen.
* Kann Aktualisierungen, Bugfixes oder neue Funktionen enthalten.
* Geschäftliche Entscheidung mit Beteiligung von Produktmanagern, Qualitätsprüfern und technischen Teams.

**Unterscheidung**

* Deployment ist eine technische Aktion.
* Release ist eine geschäftliche Entscheidung.
* Beeinflusst Planung, Koordination und Kommunikation in DevOps-Umgebungen.

---

### Semantic Versioning
***

* MAJOR wird erhöht, wenn API-inkompatible Änderungen veröffentlicht werden.

* MINOR wird erhöht, wenn neue Funktionalitäten, die kompatibel zur bisherigen API sind, veröffentlicht werden, 
* PATCH wird erhöht, wenn die Änderungen ausschließlich API-kompatible Bugfixes umfassen.

![:scale 70%](media\semver.png)

---

### Deployment strategies
***

**Was sind Bereitstellungsstrategien?**

* Methoden, die von DevOps-Teams verwendet werden, um erfolgreich eine neue Version ihrer Softwarelösung zu implementieren.

* Regeln, wie der Netzwerkverkehr in einer Produktionsumgebung von der alten zur neuen Version umgestellt wird.

* Beeinflussen Ausfallzeiten und Betriebskosten je nach spezifischen Anforderungen und Prioritäten.

---
### Blue-Green( Rot/Schwarz)

**Was ist Blau/Grün-Deployment?**

* Neue Version läuft parallel zur alten Version.
* Load Balancer leitet Datenverkehr automatisch um.

**Hauptvorteile**
* Keine Ausfallzeiten: Schneller Wechsel ohne Unterbrechung.

* Sofortiges Rollback: Schnelle Rückkehr zur alten Version bei Problemen.
* Umgebungstrennung: Minimiert Risiko während der Bereitstellung.

![:scale 60%](media\BlueGreenDeployment.png)

---
### Canary
***
**Was ist Canary-Deployment?**

* Neue Version wird schrittweise mit älterer Version getestet.
* Produktionsverkehr wird allmählich von der älteren zur neueren Version umgeleitet.

**Hauptvorteile**

* Testen des Live-Produktionstraffics: Echter Produktionsverkehr zur Fehlererkennung nutzen.
* Schnelles Rollback: Bei Problemen einfach zur älteren Version zurückkehren.
* Keine Ausfallzeiten: Live-Produktionstraffic ohne Unterbrechungen umleiten.

![:scale 30%](media\canary.jpeg)
---
### Feature flags(Feature Toggles)
***

**Was sind Feature Toggles?**

* Technik zur Entkopplung der Softwarebereitstellung von der Freigabe.
* Alternative zu Feature Branches für beschleunigte Entwicklung.
* Ermöglicht das Verbergen neuer oder unvollständiger Funktionen in der Benutzeroberfläche.

* Keine Notwendigkeit für Branches und Code-Merges.
* Schrittweises Aktivieren von Funktionen.
* Unterstützt A/B-Tests und schrittweise Bereitstellung.
* Entwickler umgeben Features im Code mit if-else-Strukturen.

```java
if( useNewAlgorithm ){
      return enhancedSplineReticulation();
}
else{
      return oldFashionedSplineReticulation();
    }

```
---
### CI/CD-Tools
***

* Zentrale Automatisierungswerkzeuge.
* Koordinieren alle Phasen Ihrer Pipeline.

* Kontrollieren Builds, Tests, Releases und Feedback.

* Effizienz und Zuverlässigkeit hängen vom Tool ab.

* Unterschiedliche Tools bieten verschiedene Funktionen und Integrationen.

**Beispiele**

* Jenkins

* GitHub-Actions

* AWS CodePipeline

---

### CI Server
***
* Der CI-Server (oder Build-Server) spielt eine Schlüsselrolle bei der Implementierung und Verwaltung des gesamten Prozesses. Er dient als Bindeglied zwischen den einzelnen Phasen der Pipeline, indem er gemäß Ihrer Geschäftslogik automatisierte Aufgaben koordiniert und Feedback sammelt und bereitstellt.

**Jenkins:**

* Open-Source CI/CD-Tool.
* Automatisierung von Build-, Test- und Bereitstellungsprozessen.
* Umfangreiche Plugin- und Erweiterungsoptionen.

GitHub Actions:

* In GitHub integrierte CI-Workflow-Plattform.
* Erstellung und Ausführung von Tests in GitHub-Repositorys.
* Unterstützung für GitHub-gehostete oder selbst gehostete Umgebungen.
* Integration in GitHub-Ereignisse (z.B., Code-Push, Webhooks).
* Ergebnisse der CI-Tests direkt in Pull Requests sichtbar.

---
### Secrets management
***

**Was sind Secrets?**

* Nicht-menschliche privilegierte Anmeldedaten.
* Zugriffsschlüssel für sensible Daten und Ressourcen.
Beispiele: Passwörter, Zertifikate, SSH-Schlüssel, API-Schlüssel.
**Secrets Management:**

* Bewährte Praxis in der Cybersicherheit.
* Konsistente Umsetzung von Sicherheitsrichtlinien für nicht-menschliche Identitäten.
* Gewährleistung des authentifizierten und autorisierten Zugriffs auf Ressourcen.

Schritte im Secrets Management:

* Authentifizierung aller Zugriffsanfragen mit nicht-menschlichen Anmeldedaten.
* Umsetzung des Prinzips des geringsten Privilegs (Least Privilege).
* Regelmäßige Rotation von Secrets und Anmeldedaten.
* Automatisierung und konsistente Zugriffsrichtlinien.
* Entfernung von Secrets aus Code und Konfigurationsdateien.

---
# Zusammenfassung
***
* DevOps fördert die Produktivität 
* Continous Integration setzt darauf frühzeitig den Code zu intigrieren
* Continuous Delivery stellt durch Automatisierung den Code jederzeit bereit
* Continuous Deployment übergibt automatisiert den Code in die Produktionsumgebung
* Korrekte Versionierung hilft uns allen
* Blue-Green Deployment betreibt zwei identische Produktionsumgebungen, wobei eine als Rollback genutzt werden kann
* Canary Deployment ist die Auslieferung von Features an eine begrenzte Gruppe
* Feature flags sind im Grunde Schalter die einen Code freischalten/einschalten 
* Ein CI-Server ist eine Software die Builds und Tests verwaltet
* Secrets Management ist das Verwalten von sensiblen Informationen(Passwörter, Zugangsdaten, etc...)
---
# Zusammenfassung
***




---
class: center, middle

# Fragen?

---
# Quellen
***

[1a]  : https://de.wikipedia.org/wiki/DevOps
[2a]  : https://www.atlassian.com/de/devops  
[3a]  : https://www.ibm.com/de-de/topics/devops
[4a]  : https://www.atlassian.com/de/devops/what-is-devops/devops-culture
[5a]  : https://mindsquare.de/knowhow/devops/#vorteile
[6a]  : https://weissenberg-group.de/was-ist-devops/#:~:text=Das%20ultimative%20Ziel%20einer%20DevOps,schneller%20und%20einfacher%20zu%20liefern.
[7a]  : https://www.atlassian.com/de/devops/frameworks/team-structure#:~:text=DevOps%2DTeams%20bestehen%20normalerweise%20aus,der%20Verwaltung%20der%20Infrastruktur%20auskennen.
[8a]  : https://www.objectivity.de/blog/aufbau-einer-effizienten-devops-teamstruktur/
[9a]  : https://www.atlassian.com/de/devops/devops-tools/devops-pipeline#:~:text=Was%20ist%20die%20DevOps%2DPipeline,f%C3%BCr%20eine%20Produktionsumgebung%20arbeiten%20k%C3%B6nnen.
[10a] : https://www.jetbrains.com/de-de/teamcity/ci-cd-guide/continuous-integration-vs-delivery-vs-deployment/
[11a] : https://dakitec.de/software-entwicklung/deployment#:~:text=Das%20Deployment%20zielt%20darauf%20ab,dem%20Produktivsystem%20einer%20bestimmten%20Version.
[12a] : https://chat.openai.com/c/65fcfde4-4f21-4912-bcd4-c5b175833b7c frage: was ist der unterschied zwischen release und deployment im DevOps bereich
[13a] : https://semver.org/
[14a] : https://www.plutora.com/blog/deployment-strategies-6-explained-in-depth
[15a] : https://cloud.google.com/architecture/application-deployment-and-testing-strategies?hl=de
[16a] : https://entwickler.de/devops/roadmap-einer-spannenden-reise
[17a] : https://www.jetbrains.com/de-de/teamcity/ci-cd-guide/ci-cd-tools/#:~:text=Ein%20CI%2FCD%2DTool%20leistet,dem%20Ver%C3%B6ffentlichen%20von%20Artefakten%20und
[18a] : https://docs.github.com/de/actions/automating-builds-and-tests/about-continuous-integration
[19a] : https://www.jetbrains.com/de-de/teamcity/ci-cd-guide/ci-cd-tools/servers/#:~:text=Der%20CI%2DServer%20(oder%20Build,und%20Feedback%20sammelt%20und%20bereitstellt.
[20a] : https://www.cyberark.com/de/what-is/secrets-management/#:~:text=Was%20ist%20Secrets%2DManagement%3F,Sicherheitsrichtlinien%20f%C3%BCr%20nicht%20menschliche%20Identit%C3%A4ten.
[21a] : https://www.dev-insider.de/die-ideale-devops-teamstruktur-a-862217/
[22a] : https://chat.openai.com/c/9ed09955-46c1-45b9-b032-ec8ee9756bab frage: was sind gängige DevOps team Strukturen?
