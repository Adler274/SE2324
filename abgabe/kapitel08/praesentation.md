class: center, middle

## [Software Engineering](../../praesentationen.html)

#### Kapitel 8
Wael Eskeif, Angelo Mavridis
---

# Inhalt
 ---
 * Use Cases

 * User Stories

---
# Use Cases
***

**Es handelt sich um eine schriftliche Anleitung, die erklärt, wie Benutzer Aufgaben auf Ihrer Website durchführen können**

![](media/use-cases.jpeg)

---

### Der Unterschied zwischen Systemkontext und Systemgrenze
 ---

| Kriterium       | Systemkontext                                                              | Systemgrenze                                                             |
|-----------------|----------------------------------------------------------------------------|--------------------------------------------------------------------------|
| **Bedeutung**   | Beschreibt, wie ein System mit seiner Umgebung interagiert.                | Definiert die Grenze zwischen dem System und seinem Umfeld.              |
| **Ziele**       | Bestimmt die Funktionalitäten des Systems und die Schnittstellen zu        | Trennt das System von seiner Umgebung, um den Entwicklungsrahmen         |
|                 | externen Systemen.                                                         | klar abzugrenzen und nicht beeinflussbare Umgebungsaspekte               |
|                 |                                                                            | auszuschließen.                                                          |

---
### Szenario
 ---
* Kontextanalyse

* Stakeholder-Analyse

* Anforderungen identifizieren

* Risikobewertung


![:scale 90%](media/szenario.jpg)

---
### Spezifikation
 ---
- Kontextanalyse

- Schnittstellen

- Stakeholder

- Anforderungen

- Use Case Diagramme


![:scale 70%](media/User-Story.PNG)

---
### User Stories
***
![:scale 80%](media/storiesVScase.png)

---
### Persona vs Theme vs Epic vs User Story vs Task
 ---

 - **Persona**: Fiktive Darstellung eines typischen Nutzers, hilft, Nutzerbedürfnisse zu verstehen.
     
 - **Theme**: Hochrangiges Ziel oder Fokus, das verschiedene Aspekte des Projekts umfasst.
     
 - **Epic**: Große, breite Anforderung, die in kleinere Teile aufgeteilt wird, oft über mehrere Sprints hinweg.
     
 - **User Story**: Detaillierte Anforderung aus Nutzerperspektive, spezifisch und mit klaren Erfolgskriterien.
     
 - **Task**: Konkrete Arbeitsschritte innerhalb einer User Story, sehr spezifisch und ausführungsorientiert.

---
### Functional User Story vs. Technical User Story
 ---
| Aspekt                 | Funktionale User Story                      | Technische User Story                       |
|------------------------|--------------------------------------------|--------------------------------------------|
| **Fokus**              | Auf Benutzerbedürfnisse und -erfahrungen    | Auf technische Implementierung und Lösungen |
| **Zielgruppe**         | Endbenutzer, Geschäftsanalysten, Stakeholder| Entwickler, technische Teams                |
| **Beschreibung**       | Beschreibt, was der Benutzer tun möchte     | Beschreibt, wie etwas technisch umgesetzt wird|

---

### Bestandteile einer User Story
 ---
1. Rolle (Wer):
  * späterer Nutzer der zu entwickelnden Lösung.

2. Funktion (Was): 
  * Erwartung des späteren Nutzers an die Software.

3. Nutzen (Warum)
  * späterer Mehrwert der zu entwickelnden Lösung.


![:scale 60%](media/User-Stories-SoMe.jpg)

---
### Der Unterschied zwischen Ready und Done
 ---
| Kriterium      | Definition of Ready                           | Definition of Done      |
|----------------|-------------------------------------------------------|-----------------------------------------------------|
| **Zweck**      | Stellt sicher, dass ein Arbeitspaket startklar ist.   | Definiert, wann ein Arbeitspaket vollendet ist.     |
| **Inhalt**     | Klare Anforderungen, Ressourcenverfügbarkeit,         | Erfüllte Anforderungen, erfolgreiche Tests,         |
|                | Stakeholder-Zustimmung.                               | finale Integration und Dokumentation.              |
| **Wichtigkeit**| Vermeidet Arbeitsbeginn an unzureichend vorbereiteten Aufgaben. | Sichert Qualität und Klarheit über die Fertigstellung von Aufgaben.|                              

---
### Prinzipien für effektive ("gute") User Stories
 ---
- Spezifisch und Verständlich
- Benutzerzentriert
- Kurz
- Realisierbar
- Testbar
- Wertvoll
- Priorisiert
- Verhandelbar
- Unabhängig
---
### Formulierungsfehler, die zu vagen ("schlechten") User Stories führen
 ---
- Vermeiden von zu großem Umfang
- Klarheit des Problems
- Unabhängigkeit von Anforderungsdokumenten
- Berücksichtigung nicht-funktionaler Anforderungen
- Vermeidung konkreter Lösungswege
---
### Card, Conversation, Confirmation
 ---

| Three C's         | Beschreibung                                                               |
|-------------------|----------------------------------------------------------------------------|
| **Card**          | - Symbolisiert die User Story selbst.                                      |
|                   | - Dient als Erinnerungshilfe und Übersicht über die Anforderung.           |
|                   | - Beinhaltet grundlegende Informationen wie Titel und kurze Beschreibung.  |
| **Conversation**  | - Bezieht sich auf die Diskussionen um die User Story.                     |
|                   | - Wichtiger Bestandteil für das Verständnis und die Klärung der Details.   |
|                   | - Umfasst Fragen, Antworten und Vereinbarungen zwischen Team und Stakeholdern.|
| **Confirmation**  | - Bestätigung, dass die Anforderungen erfüllt sind.                        |
|                   | - Oft durch Akzeptanzkriterien definiert.                                  |
|                   | - Stellt sicher, dass alle Parteien ein gemeinsames Verständnis haben.     |

---
### INVEST-Kriterien
***

![](media/Invest.png)

---
### User-Stories vs. Use Case
 ---

| Kriterium    | User Stories                                                 | Use Cases                                              |
|--------------|--------------------------------------------------------------|--------------------------------------------------------|
| Format   | Kurz, narrativ; "Als [Rolle], möchte ich [Aktion], um [Nutzen]." | Ausführlicher, detaillierte Systeminteraktionen.       |
| Fokus    | Benutzerzentriert, Wert für Endbenutzer.                     | Funktionalität und Systemabläufe.                      |
| Detailgrad | Weniger detailliert, fokussiert auf "Was" und "Warum".     | Detailliert, spezifische Schritte/Abläufe.             |
| Flexibilität | Anpassbar, offen für Diskussionen.                         | Festgelegt, wenig Änderungsspielraum.                  |
| Einsatz  | In agilen Methoden wie Scrum, Kanban.                        | In traditionellen Ansätzen wie dem Wasserfallmodell.   |
| Ziel     | Schnelle, iterative Entwicklung, Benutzerbedürfnisse.       | Klare Definition von Systemanforderungen und -abläufen. |

---
### Was ist Misuse Stories?
***

 Sind kurze narrative Szenarien, die potenzielle Missbrauchs- und Angriffswege in einem Softwaresystem beschreiben. Sie dienen dazu, Sicherheitsrisiken und Schwachstellen zu identifizieren, um präventive Maßnahmen in der Softwareentwicklung zu ergreifen.

---
### Was ist Priorisierung?
***

Bestimmt die Reihenfolge, in der Aufgaben, Features oder User Stories bearbeitet werden.

---
### Was ist Schätzung?
***


Bezieht sich die Schätzung auf den Prozess der Bewertung des Aufwands und der Zeit, die benötigt werden, um bestimmte Aufgaben, Features oder User Stories zu implementieren.

---
### Aspekte der Schätzung
***

- Team-Basiert
- Relative Schätzung
- Planungspoker
- Historische Daten
- Iterative Anpassung
- Transparenz und Kommunikation
---
### Story Mapping
***

![](media/StoryMapping.png)

---
class: center, middle

# Fragen?

---

# Quellen
***

- Department of Health and Human Services. (o. D.). Use cases | Usability.gov. https://www.usability.gov/how-to-and-tools/methods/use-cases.html.
- t2informatik GmbH. (2023, 8. Juni). Was ist der Systemkontext? - Wissen kompakt - T2Informatik. https://t2informatik.de/wissen-kompakt/systemkontext/.
- kathrin.hubli@fhnw.ch. (2020, 18. Juni). Systemgrenzen und Modellierung von Systemen - Wirtschaftsinformatik reloaded. Wirtschaftsinformatik reloaded. https://www.fhnw.ch/plattformen/iwi/2020/06/17/homeoffice-und-onlinekonferenzen-4-9-2-3-2-7/.
- Was ist der Systemkontext? (2023, 31. Oktober). microTOOL. https://www.microtool.de/wissen-online/was-ist-der-systemkontext/.
- Was ist ein Use Case-Diagramm? (2023, 31. Oktober). microTOOL. https://www.microtool.de/wissen-online/was-ist-ein-use-case-diagramm/.
- Theme vs Epic vs user story vs task. (o. D.). https://www.visual-paradigm.com/scrum/theme-epic-user-story-task/.
- Krieger, F. (2023, 3. April). User Story - Definition, Aufbau und Beispiele. https://www.brainformatik.com/blog/user-story/

---
- t2informatik GmbH. (2023b, September 11). Was sind akzeptanzkriterien? - Wissen kompakt - T2Informatik. https://t2informatik.de/wissen-kompakt/akzeptanzkriterien/.
- Wynhoven, D. (2023, 12. Mai). Akzeptanzkriterien: So erfüllen Sie Kundenanforderungen. Me & Company. https://www.me-company.de/magazin/akzeptanzkriterien/#:~:text=Akzeptanzkriterien%20sollten%20einfach%20zu%20verstehen,wie%20die%20Kund*innen%20hat.
- Die Produktwerker. (2023, 30. August). Gute User Stories schreiben bzw. formulieren - die Produktwerker. https://produktwerker.de/herausforderung/gute-user-stories-schreiben-formulieren/#:~:text=Zu%20den%20wichtigsten%20Eigenschaften%20einer,die%20Prinzipien%20des%20Akronyms%20INVEST.
- Was macht eine schlechte User Story aus?.https://bbv-software.de/user-stories/.
- Von Bittenfeld, P. H. (2011, 9. März). Die drei CS einer User Story: card, conversation, confirmation. Nachrichten, Tipps & Anleitungen für Agile, Entwicklung, Atlassian-Software (JIRA, Confluence, Bitbucket, . . .) und Google Cloud. https://blog.seibert-media.net/blog/2011/03/09/user-story-scrum-card-conversation-confirmation/.
- User story vs use case for agile software development. (o. D.). https://www.visual-paradigm.com/guide/agile-software-development/user-story-vs-use-case/.
- User story oder Use case? Was denn nun? (o. D.). Software Quality Lab. https://www.software-quality-lab.com/wissen/blog/blogeintrag/user-story-oder-use-case-was-denn-nun/.

---

- Wikipedia contributors. (2023c, November 1). Misuse case. Wikipedia. https://en.wikipedia.org/wiki/Misuse_case#From_use_to_misuse_case
- Rassek, A. (2020, 30. Oktober). Priorisierung: so einfach ist das mit Prioritäten! karrierebibel.de. https://karrierebibel.de/priorisierung/.
- Was ist Agiles Schätzen? (2023, 29. Juni). it-agile GmbH. https://www.it-agile.de/agiles-wissen/agile-teams/was-ist-agiles-schaetzen/.
- Story mapping. (2023, 29. Juni). it-agile GmbH. https://www.it-agile.de/agiles-wissen/agiles-produktmanagement/story-mapping/.

---


![](media/use-cases.jpeg)