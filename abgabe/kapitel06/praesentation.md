class: center, middle

## [Software Engineering](../../praesentationen.html)

#### Kapitel 6

# Arten von Softwarelogik, Softwarearchitekturen, Abbildung der Softwarearchitektur auf die Systemarchitektur

Simon Fedrau, Sascha Hahn

---
# Inhalt
***

1. Arten von Softwarelogik

  1. Beispiele dazu   

1. Abbildung der Softwarearchitektur auf die Systemarchitektur 

  1. Multi-Tier Architekturen

  1. Anwendungsbeispiele 

1. Softwarearchitekturen

  1. Vorteile, Nachtile, Motivtion

  1. Domänenzentrische Architektur
    
    1. Onion Architecture

    1. Hexagonale Architektur

1. Zusammenfassung

1. Quellen

---
## Arten von Softwarelogik

---

### Domänenlogik (Domain logic)
***

**Definition:**
* Kernlogik der Software
* Fokussiert auf Geschäftsregeln

**Aspekte der Domänenlogik:**

* Geschäftsregeln:
  * Komplexe Berechnungen und Entscheidungen
  
**Objektmodellierung:**
* Repräsentation realer Entitäten
* Definition von Interaktionen

**Geschäftsprozesse:**
* Abläufe in der Geschäftsdomäne

**Entkopplung von Infrastrukturdetails:**
  * Unabhängigkeit von technischen Details

[5a] [14a]

---
### Geschäftslogik (Business Logic)
***
**Definition:**

* Zentraler Bestandteil von Softwareanwendungen
* Definiert Regeln und Prozesse für Geschäftsdatenverarbeitung

**Wichtige Aspekte:**

* Regelbasierte Verarbeitung:
  * "Wenn-Dann"-Anweisungen, Algorithmen

**Geschäftsprozesse:**
  * Schritte und Abläufe für Aufgaben
* Datenvalidierung:
  
**Entscheidungsfindung:**
  * Bedingte Aktionen, automatisierte Entscheidungen

* Unabhängigkeit von UI

**Rolle der Geschäftslogik:**
  * Korrekte, effiziente Erfüllung von Geschäftsanforderungen
[1a]

---
### Präsentationslogik (Presentation Logic)
***
**Definition:**
  * Fokussiert auf Darstellung von Informationen für Benutzer
  * Gestaltet Benutzeroberfläche und visuelles Design

**Benutzerinteraktion:**
  * Eingaben, Aktionen, Navigation

**Anzeige von Daten:**
  * Formatierung, Bilder, Tabellen, dynamische Aktualisierung
* Validierung auf Benutzeroberfläche

**Feedback für Benutzer:**
  * Statusmeldungen, Erfolg/Fehlermeldungen

**Rolle der Präsentationslogik:**
* Entscheidend für Benutzererfahrung und intuitives Softwareverständnis
* Zusammenarbeit mit Domänen- und Infrastrukturlogik
[7a]

---

### Steuerungslogik (Control Logic)
***
**Steuerungslogik**, auch als "Control Logic" bezeichnet, ist entscheidend für die Softwarelogik. Ihre Verantwortung liegt in der Regelung von Anweisungen in einer Softwareanwendung.

**Wichtige Aspekte:**
 * Programmfluss: Bestimmt Ausführungsreihenfolge von Anweisungen.
 * Bedingte Anweisungen: Ermöglichen verschiedene Pfade basierend auf Bedingungen.
 * Schleifen: Wiederholte Ausführung von Anweisungen unter Bedingung.
 * Unterprogramme und Funktionen: Förderung von Modularität und Wiederverwendbarkeit.
 * Ausnahmehandling: Behandlung von unerwarteten Situationen für Robustheit.
 * Ereignisgesteuerte Logik: Regelt Reaktionen auf Ereignisse.

Die Steuerungslogik gewährleistet eine ordnungsgemäße Funktionsweise der Softwareanwendung, Interaktion zwischen Komponenten und gewünschte Ergebnisse. Eine gut gestaltete Steuerungslogik sorgt für lesbaren, wartbaren und effizienten Code.

[2a]
---

### Validierungslogik (Validation Logic)
***
Die **Validierungslogik**, ist ein zentraler Aspekt der Softwarelogik, der darauf abzielt, die Qualität und Konsistenz der verarbeiteten Daten sicherzustellen.

**Wichtige Aspekte:**
* Dateneingabeüberprüfung: Prüfung von Benutzer- oder Quellendaten auf Datentypen, Längenbeschränkungen und andere Kriterien.
* Integritätsprüfung: Überprüfung der Konsistenz und logischen Verbindungen zwischen Datenelementen oder -feldern.
* Formatüberprüfung: Sicherstellung der korrekten Formate von Daten, wie Datumsformaten oder E-Mail-Adressen.
* Geschäftsregelvalidierung: Implementierung von Geschäftsregeln, um Daten an die Anforderungen des jeweiligen Szenarios anzupassen.
* Benutzereingabevalidierung: Verbesserung der Datenqualität durch Überprüfung von Benutzereingaben in Anwendungen mit Benutzeroberflächen.
* Fehlerbehandlung und Rückmeldung: Auslösung von Fehlern und Bereitstellung von Rückmeldungen bei Nichterfüllung der Standards.

[3a]

---
### Infrastrukturlogik (Infrastructure Logic)

Die **Infrastrukturlogik**, auch als "Infrastructure Logic" bezeichnet, befasst sich mit der Interaktion der Softwarelogik mit der zugrunde liegenden Infrastruktur und externen Ressourcen.

**Wichtige Aspekte:**
* Datenbankzugriff: Effiziente Kommunikation für Lesen, Schreiben, Aktualisieren und Löschen von Daten mit Datenbanken.
* Dateizugriff: Verwaltung von Lese-, Schreib-, Öffnungs- und Schließoperationen für Dateien und Dateisysteme.
* Netzwerkkommunikation: Verantwortlich für den Datenaustausch zwischen Systemen über lokale Netzwerke oder das Internet.
* Externe Dienste: Integration und Kommunikation mit externen Diensten und APIs, einschließlich Authentifizierung und Datenübertragung.
* Sicherheit: Implementierung von Sicherheitsmaßnahmen wie Datenverschlüsselung, Benutzerauthentifizierung und Zugriffsrechte.
* Ressourcenverwaltung: Effiziente Verwaltung von Ressourcen wie Datenbankverbindungen, Netzwerkverbindungen und Datei-Handles.

Die Infrastrukturlogik ist entscheidend für eine reibungslose Interaktion der Software mit ihrer Umgebung. Sie trägt dazu bei, die Trennung zwischen Anwendungslogik und Infrastruktur aufrechtzuerhalten, was die Wartbarkeit und Skalierbarkeit der Software verbessert.

[4a]
---
### Persistenz und Cache
***
**Persistenz**

Persistenz beschreibt die Fähigkeit eines Systems, den Zustand seiner Daten, Objektmodelle oder logischen Verbindungen über längere Zeiträume hinweg zu bewahren. Informationen werden auf nichtflüchtigen Speichermedien wie Festplatten, SSDs oder in Datenbanken erhalten. Dies gewährleistet Kontinuität, Zuverlässigkeit und Verfügbarkeit von Informationen in der digitalen Welt.

[10a]

#### Cache

**Cache**
Ein Cache ist ein reservierter Speicherplatz für temporäre Daten, lokal auf Ihrem Gerät erstellt. Dies ermöglicht schnellere Ladezeiten von Webseiten, Browsern oder Apps. Caches verbessern die Systemleistung, ermöglichen teilweise Offline-Funktionalität und speichern Daten zur Ressourceneffizienz.
Beispiele:
- Hardware
- Internetbrowser

[11a]
---
### Transaktion
***

In der Infrastrukturlogik bezieht sich der Begriff "Transaktion" auf einen Satz von Aktionen, der als zusammenhängende und unteilbare Einheit betrachtet wird. Eine Transaktion wird vollständig oder gar nicht ausgeführt, um Konsistenz sicherzustellen. In Datenbanken wird dies häufig genutzt, wo bei einem Fehler alle Änderungen rückgängig gemacht werden.

---
### Sicherheit
***


Sicherheit in der Infrastrukturlogik umfasst Maßnahmen für Integrität, Vertraulichkeit und Verfügbarkeit:
- Zugriffskontrolle
- Verschlüsselung
- Überwachung und Protokollierung
- Sicherheitsupdates und Patch-Management
- Firewalls und Netzwerksicherheit
- Physische Sicherheit
- Notfallwiederherstellung und Redundanz

Sicherheit ist ein umfassendes Konzept für eine robuste und geschützte Infrastruktur.

---
### Beispiel Validierungslogik 
***

Anmeldeformular für Benutzer, die sich auf einer Website registrieren möchten.

**Benutzername-Validierung:**
- Der Benutzername darf nur Buchstaben und Zahlen enthalten.
- Benutzername muss zwischen 5 und 15 Zeichen liegen.

**E-Mail-Validierung:**
- Die E-Mail-Adresse muss ein "@"-Zeichen enthalten.
- Die E-Mail-Adresse muss eine gültige Domain haben.

**Passwort-Validierung:**
- Das Passwort muss mindestens 8 Zeichen lang sein.
- Es muss mindestens einen Großbuchstaben, einen Kleinbuchstaben und eine Zahl enthalten.

---
### Beispiel Steuerungslogik
***

System für einen Online-Shop, und ein Kunde hat Produkte in seinen Warenkorb gelegt und möchte nun den Checkout-Prozess durchlaufen. 

* Verfügbarkeitsprüfung

* Preisberechnung
  * Berechnen des Gesamtpreises der Produkte im Warenkorb, einschließlich etwaiger Rabatte oder Steuern.

* Zahlungsbearbeitung
  * Überprüfen der Zahlungsinformationen des Kunden, wie Kreditkartennummer und Gültigkeitsdatum.
  * Auslösen einer Transaktion mit dem Zahlungsanbieter.

* Bestandsaktualisierung
  * Aktualisieren des Lagerbestands nach einer erfolgreichen Bestellung, um sicherzustellen, dass Produkte, die gekauft wurden, aus dem Bestand entfernt werden.

* Versandvorbereitung und Bestätigung an den Kunden

---

### Domänenlogik
***

Angenommen, man hat entwickelt die Domänenlogik für die Funktion "Freunde hinzufügen" in einem sozialen Netzwerk. 

* Freundschaftsanfrage senden:
  * Ein Benutzer A sendet eine Freundschaftsanfrage an Benutzer B.

* Freundschaftsanfrage akzeptieren/ablehnen:
  * Benutzer B kann die Freundschaftsanfrage von Benutzer A akzeptieren oder ablehnen.

* Benachrichtigungen:
  * Beide Benutzer erhalten Benachrichtigungen über den Status der Freundschaftsanfrage.

* Freunde anzeigen:
  * Nachdem die Freundschaftsanfrage akzeptiert wurde, können Benutzer A und B nun die Aktivitäten des jeweils anderen sehen und als "Freunde" miteinander interagieren.

---
### Präsentationslogik
***

Angenommen, man entwickelt die Präsentationslogik für eine To-Do-Liste-Anwendung. Die Präsentationslogik könnte folgende Aspekte abdecken:

* Anzeigen von Aufgaben:
  * Die Präsentationslogik bestimmt, wie die Aufgaben in der Benutzeroberfläche dargestellt werden

* Hinzufügen neuer Aufgaben:*
  * Die Präsentationslogik steuert das Formular zum Hinzufügen neuer Aufgaben.

* Status der Aufgaben:
  * Je nach Status einer Aufgabe (z. B. "In Bearbeitung", "Abgeschlossen") könnte die Präsentationslogik das Erscheinungsbild der Aufgabe anpassen.

* Filter und Sortierung:
  * Die Präsentationslogik ermöglicht es Benutzern, ihre Aufgaben nach Kriterien zu filtern z.B  abgeschlossene Aufgaben

---
## Softwarearchitekturen
***
* Architektur eines Softwaresystems
* grober Zusammenhang/Verbindung zwischen Komponenten
* keine Details, grobe Struktur um Anforderungen zu erfüllen

[1b]

---

### Vergleich, Vorteile, Nachteile, Motivation
***
* **Vorteile:**<br>
 * klare Strukutur
 * Leicht zu verstehen -> einfache Kommunikation über Probleme und Features
 * Dokumentation
 * Einfachere Erweiterbarkeit und Wiederverwendbarkeit

* **Nachteile:**<br>
 * Hoher initaler Zeitaufwand
 * Bei häufiger anforderungs Änderung, ist starre Struktur von Nachteil
 * unnötiger Aufwand bei zu komplizierter Architektur

* **Ziel:**<br>
    Struktuierung dess Sysems um übersicht zu behalten.
    Wartbarkeit, Erweiterbarkeit und Wiederverwendbarkeit verbessern. 

[1b,2b]

---

### Schichtenarchitektur (Layered Architektur)
***
Eine Schichtenarchitektur besteht aus mehreren Schichten, welche jeweils eine bestimmte Aufgabe erfüllen.
Meist werden 3 Grundlegende Schichten verwendet.

**GUI-Schicht:** Zuständig für die **Darstellung und Manipultion** der Daten, Schnittstelle zwischen Benutzer und Fachkonzeptschicht.

**Fachkonzeptschicht:** Zuständig für die **Verwaltung** der Daten
**Datenhaltungsschicht:** **Speicherung** der Daten

<br>

**(Server, Client, Datenbank)**

[3b]

---

#### Azyklische Abhängigkeiten
***
* Vermeiden von zyklischen Abhängigkeiten
* Zyklische Abhängigkeiten führen zu Problemen
 * abhänigkeiten im Kries -> Ausfall einer Komponente führt zum Ausfall aller anderen

* #### Ziel: so wenig bzw. einfachste Abhängigkeiten

[4b]

---

### Domänenzentrische Software-Architekturen
***
Domain-driven Design(DDD) ist eine Ansatz der Softwareentwicklung, bei dem die Probleme der Geschätsbereiche in den Vordergrund gestellt werden, um sie besser zu verstehen und zu Lösen.<br>

Dies wird umgesetzt durch die verwendung einer einheitlichen Sprache (Fachbegiffe) unter den verschiedenen Geschäftsbereichen.<br>

Mit DDD wird die Geschäftslogik klar in der Software representiert, um die Zusammenarbeit zu fördern.

[5b]

---

#### Onion Architecture
***
* Komponenten sind in konzentrische Ringe gegliedert.
* äußere Ringe greifen nur auf innere zu
* innerer Ring enthält die Geschäftslogik(kernkomponente)

Trennung zwischen Geschäftslogik und Anwendungslogik.
Liegt im innersten, da sie sich am wenigstens ändert.

[6b]

---

#### Ports And Adapters Architecture (Hexagonale Architektur)
***
Das System ist in los gekoppelte Komponenten aufgeteilt.
Kern ist in der Mitte und ist mit den anderen Komponenten durch eine Schicht von Adaptern verbunden.

##### Core logic
***
* Kern ist getrennt von den äußeren Komponenten
 * flexible änderung der Datenquelle
* Geschäftslogik weiß nichts über äußere Komponenten

[7b]
---

##### Ports
***
Ports sind die Schnittstellen mit denen der Kern mit den äußeren Komponenten intergiert.<br>

Die Ports erlauben Daten in den Kern zu schreiben und aus dem Kern zu lesen und sind somit bi-direktional.

**Inbound:** Ports mit denen der Kern funktionalitätet den äuußeren Freigibt.<br>

**Outbound:** Ports mit denen der Kern Daten an die äußeren Komponenten sendet.
 * (lesen von Datenbanken)

[7b]

---

##### Adapters
***
Die Adapter bilden eine Schicht um den funktions Kern.<br>
Diese sind nicht ein Teil des Kernes aber ineragieren mit diesem.<br>
Dabei gibt es zwei Arten von Adptern

**Driving (primary) Adapters** benutzen Inbound Ports um Events auszulösen.<br>
 * z.B. Knopfdruck
 * sind Komponenten wie API-UI, Konsole oder Test Scripts

**Driven (secondary) Adapters** benutzen Outbound Ports um Events zu verarbeiten.<br>
 * greifen auf Datenbanken, Dateisysteme oder andere APIs zu.

[7b]

---

#### Clean Architecture als Realisierung der hexagonalen Architektur
***
Clean Architecture iset eine spezifische Realisiereung der hexagonalen Architektur.

* Geschäftslogik, Anwendungslogik und externe Infrastruktur klar getrennt.
 * Geschäftslogik im inneren Ring
 * Anwendungslogik im mittleren Ring
 * Externe Infrastruktur im äußeren Ring
  * mittlerer und äußerer Ring durch Adapter/Schnittstellen-Ring verbunden
* Abhängigkeiten nur von außen nach innen,<br>
Geschänftslogik am stabilsten(Onion Ring)

[6b]

---

### Vergleich der Ansätze, Vorteile, Nachteile
***
Der Vorteil aller Ansätze ist, dass sie die Software in verschiedene Komponenten aufteilen, um die Wartbarkeit, Erweiterbarkeit und Wiederverwendbarkeit zu verbessern.<br>
Das System ist dadurch robuster da einzelnen ausfälle nicht das gesamte System zum absturz bringen.<br>
Auch Abhängigkeiten sind klar definiert, um zum Beispiel zyklische Agbhängigkeiten zu vermeiden.<br>
Alle Ansätze Zielen auch darauf ab, das System flexibel zu gestllten und einfach testbar zu machen.<br>


Ein klarer Vorteil bei der hexagonalen Architektur ist natürlich dass die abhängigkeiten durch bestimmte Arten von Adaptern/Ports bestimmt sind.<br>
Dafür hat die Onion Ring Architektur den Vorteil, dass die Kommunikation nur von außen nach innen geschehen kann, was die Komplexität reduziert und die Komponenten, mit dem größten risiko der Änderung, auch am einfachsten ist zu ändern.

---

#### Multi-Tier Architekturen
***
Eine Multi-Tier-Architektur ist eine mehrgliedrige Schichtenarchitektur, die die Prinzipien zur Strukturierung von Software-Architekturen definiert. Die hierarchische Strukturierung mittels Schichten ist ein häufig angewendetes Architekturmuster. 

**Schichtenarchitektur (auch Schichtenmodell oder Schichtenmuster):**
- Ein häufig angewandtes Strukturierungsprinzip für die Architektur von Softwaresystemen.
- Konzeptionelle Zuordnung einzelner Aspekte des Softwaresystems zu Schichten (engl. tier oder layer).
- Erlaubte Abhängigkeitsbeziehungen werden eingeschränkt, sodass Aspekte höherer Schichten nur solche tieferer Schichten verwenden dürfen.
- Ein System mit Schichtenarchitektur wird auch als „mehrschichtig“ bezeichnet.

**Zugeordnete Aspekte:**
- Je nach Art des Systems oder Detaillierungsgrad der Betrachtung können den Schichten zugeordnete Aspekte Funktionalitäten, Komponenten oder Klassen sein.
[8a]

---
#### Tiers vs. Layers (Stufen vs. Schichten)

**Tiers (Stufen):**
- Tiers beziehen sich auf physisch getrennte Teile einer Anwendung, die auf verschiedenen Servern oder Hardware-Instanzen laufen können.
- Jedes Tier hat spezifische Rollen und Verantwortlichkeiten, typischerweise Präsentationstier, Anwendungstier und Datenzugriffstier.
- Tiers implizieren eine physische Verteilung für verbesserte Skalierbarkeit und Leistung.

**Layers (Schichten):**
- Layers beziehen sich auf die logische Aufteilung einer Anwendung in verschiedene Schichten mit klaren Funktionen und Verantwortlichkeiten.
- Jede Schicht hat eine klare und abgegrenzte Aufgabe, typischerweise Präsentationsschicht, Anwendungsschicht und Datenzugriffsschicht.
- Layers beschreiben die logische Struktur einer Anwendung, implementiert auf demselben physischen Server.

**Zusammenfassend:**
- Tiers betonen die physische Verteilung auf verschiedenen Servern.
- Layers beschreiben die logische Struktur auf demselben Server.
- Diese Begriffe sind in der Praxis oft miteinander verbunden
[9a]

---

### Zwei-Schichten-Architektur
***
Die zweischichtige Architektur, auch als Two-Tier Architecture bekannt, besteht aus zwei Schichten. Hierbei darf nur die höhere Schicht auf die niedrigere zugreifen, wodurch die niedrigere Schicht als Dienstanbieter für die höhere fungiert. Diese Architektur wird oft als Client-Server-Architektur bezeichnet.

- **Definition:** Zwei Schichten, wobei die höhere auf die niedrigere zugreift.
- **Ausführung:** Kann auf einem einzelnen Rechner oder über verschiedene Rechner realisiert werden.
- **Aufgabenverteilung:** Der Server übernimmt die Datenbankanwendung, während die Clients Logik und Benutzeroberfläche bereitstellen.

Die zweischichtige Architektur ermöglicht eine Auslagerung der Rechenkapazität auf die Client-Rechner, um den Server zu entlasten. Dies ist besonders in Client-Server-Architekturen verbreitet, bei denen der Server als Dienstanbieter für die Clients fungiert.
[8a]

---

### Drei-Schichten-Architektur

Die dreischichtige Architektur ist eine Software-Architektur mit drei Schichten, die jeweils spezifische Aufgaben übernehmen.

- **Präsentationsschicht (Front-End):**
  - Verantwortlich für die Repräsentation von Daten und Benutzerschnittstelle.
  
- **Logikschicht (Application-Server Tier):**
  - Enthält alle Verarbeitungsmechanismen und vereint die Anwendungslogik.
  
- **Datenhaltungsschicht (Back End):**
  - Beinhaltet die Datenbank und ist für das Speichern und Laden von Daten zuständig.

[8a]
---
### Vier-Stufen-Architektur
***
Die Vier-Stufen-Architektur konzentriert sich auf die Strukturierung von Datenverarbeitung und -analyse und besteht aus folgenden Stufen:

1. **Datenerfassung (Data Collection):**
   - Sammeln von Daten aus verschiedenen Quellen wie Sensoren, Benutzerinteraktionen oder externen Systemen.

2. **Datenverarbeitung (Data Processing):**
   - Verarbeitung der gesammelten Daten, einschließlich Filtern, Bereinigen, Transformieren und Aggregieren von Rohdaten.

3. **Datenpräsentation (Data Presentation):**
   - Visualisierung oder Präsentation der verarbeiteten Daten. Dies kann durch Berichte, Dashboards oder andere Benutzeroberflächen erfolgen.

4. **Datenanalyse (Data Analysis):**
   - Durchführung der eigentlichen Datenanalyse, um Muster, Trends oder Erkenntnisse zu identifizieren. 
[13a]

---
#### Zwei-Stufen-Architektur Anwendungsbeispiel
***

**ToDo-Liste-Anwendung:**

1. **Datenerfassung (Stufe 1):**
   - Der Benutzer öffnet die ToDo-Liste-Anwendung und fügt einen neuen Aufgabeneintrag hinzu.
   - Eingabe von Aufgabenbeschreibung, Fälligkeitsdatum und anderen relevanten Informationen.

2. **Datenverarbeitung (Stufe 2):**
   - Die Anwendung nimmt die eingegebenen Daten entgegen, überprüft auf Vollständigkeit und Validität.
   - Speicherung des neuen Auftrags in der Datenbank und Aktualisierung der Benutzeroberfläche zur Anzeige der aktualisierten ToDo-Liste.

*Beispiel:*
Die erste Stufe erfasst die Aufgabe und ihre Details, während die zweite Stufe die Verarbeitung dieser Informationen umfasst. Dies beinhaltet Validierung, Speicherung in der Datenbank und die Aktualisierung der Benutzeroberfläche, um dem Benutzer die aktualisierte ToDo-Liste anzuzeigen.


---
#### Drei-Stufen-Architektur Anwendungsbeispiel
***

**Online-Shop:**

1. **Präsentationsschicht (Stufe 1):**
   - Der Benutzer besucht die Website des Online-Shops und durchsucht die Produkte.
   - Auswahl von Produkten, Hinzufügen zum Warenkorb und Weiterleitung zur Kasse.

2. **Anwendungsschicht (Stufe 2):**
   - Die Anwendung verarbeitet die Benutzerauswahl, überprüft Produktverfügbarkeit, berechnet den Gesamtpreis und verwaltet den Warenkorb.
   - Authentifizierung des Benutzers, wenn erforderlich, und Initiierung des Zahlungsvorgangs.

3. **Datenzugriffsschicht (Stufe 3):**
   - Zugriff auf Produktinformationen und Bestelldaten in der Datenbank für Produktanzeige und Bestellspeicherung.
   - Sicherer Datenbankzugriff für die Speicherung von Transaktionsdaten wie Zahlungsinformationen.


---

#### Vier-Stufen-Architektur Anwendungsbeispiel

Social Media Plattform:

1. **Datenerfassung (Stufe 1):**
   - Benutzer erstellen Konten und geben persönliche Informationen ein.
   - Veröffentlichung von Beiträgen, Fotos oder Videos.

2. **Datenverarbeitung (Stufe 2):**
   - Plattform verarbeitet Daten, überprüft Einhaltung der Richtlinien und führt Moderation durch.
   - Analyse von Benutzerinteraktionen für personalisierte Inhalte und Freundschaftsvorschläge.

3. **Datenpräsentation (Stufe 3):**
   - Präsentation verarbeiteter Daten in der Benutzeroberfläche.
   - Benutzer sehen personalisierten Feed, Freundesaktivitäten und relevante Werbung.

4. **Datenanalyse (Stufe 4):**
   - Analyse aggregierter Daten, um Trends im Benutzerverhalten zu identifizieren.
   
---
class: center, middle

# Fragen?

---
# Quellen
***
[1a] : https://de.wikipedia.org/wiki/Gesch%C3%A4ftslogik

[2a] : https://chat.openai.com/c/63c2b80e-a9dd-4735-8ea0-edad1bff8a7c frage : erkläre mir ausführlich die Steuerungslogik

[3a] : https://chat.openai.com/c/63c2b80e-a9dd-4735-8ea0-edad1bff8a7c frage : erkläre mir ausführlich was die Validierungslogik (Validation logic) ist

[4a] : https://chat.openai.com/c/63c2b80e-a9dd-4735-8ea0-edad1bff8a7c frage :erkläre mir ausführlich was Infrastrukturlogik (Infrastructure logic) ist

[5a] : https://chat.openai.com/c/63c2b80e-a9dd-4735-8ea0-edad1bff8a7c frage :erkläre mir ausführlich was die Domänenlogik (Domain logic) ist

[6a] :https://chat.openai.com/c/63c2b80e-a9dd-4735-8ea0-edad1bff8a7c frage: erkläre mir die Geschäftslogik (Business logic) ausführlich

---

# Quellen
***

[7a] : https://chat.openai.com/c/63c2b80e-a9dd-4735-8ea0-edad1bff8a7c frage : erkläre mir ausführlich was die  Präsentationslogik (Presentation logic) ist

[8a] : https://de.wikipedia.org/wiki/Schichtenarchitektur

[9a] : https://saipawan.wordpress.com/2015/08/19/whats-the-difference-between-layers-and-tiers/

[10a] : https://de.wikipedia.org/wiki/Persistenz_(Informatik)

[11a] : https://www.heise.de/tipps-tricks/Was-ist-ein-Cache-4932006.html

[12a] : https://chat.openai.com/?model=text-davinci-002-render-sha frage : was ist Sicherheit im Bezug auf Infrastrukturlogik 

[13a] : https://chat.openai.com/c/63c2b80e-a9dd-4735-8ea0-edad1bff8a7c : was ist eine vier stufen Archtiketur

[14a] : https://books.google.de/books?id=QCwgBAAAQBAJ&pg=PA388&lpg=PA388&dq=Dom%C3%A4nenlogik&source=bl&ots=QltYgvCEo1&sig=ACfU3U3Rv0MK78S1RoblZXifT6o8YxevtQ&hl=de&sa=X&ved=2ahUKEwi2pLvr87aCAxXjgv0HHUU9AeQQ6AF6BAgvEAM#v=onepage&q=Dom%C3%A4nenlogik&f=false

---

# Quellen
***
[1b] :https://gi.de/informatiklexikon/software-architektur

[2b] :https://chat.openai.com/: Was sind Vor und Nachteile von Softwarearchitektur

[3b] :https://studyflix.de/informatik/schichtenarchitektur-i-604

[4b] :https://www.heise.de/blog/Zyklische-Abhaengigkeiten-eine-Architektur-Todsuende-4061803.html

[5b] :https://entwickler.de/ddd/einfuhrung-in-die-konzepte-von-domain-driven-design-001

[6b] :https://www.innoq.com/de/blog/2018/02/ddd-mit-onion-architecture-umsetzen/

[7b] :https://medium.com/idealo-tech-blog/hexagonal-ports-adapters-architecture-e3617bcf00a0

[8b] :https://dev.to/dyarleniber/hexagonal-architecture-and-clean-architecture-with-examples-48oi