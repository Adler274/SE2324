# Kapitel 6 

**Autor:** Simon Fedrau, Sascha Hahn

## Lernziele
***
* Welche Arten von Softwarelogiken gibt es
  * Wofür sind diese nützlich
* Was sind Multi-Tier Architekturen
  * Wofür werden diese Gebraucht





## Arten von Softwarelogik
***

### Domänenlogik (Domain logic)

Die Domänenlogik, auch als "Domain Logic" bezeichnet, ist ein zentraler Bestandteil der Softwarelogik, der sich auf die Umsetzung von Geschäftsregeln, -logik und -prozessen konzentriert. Sie bildet die Kernlogik einer Softwareanwendung und ist eng mit dem spezifischen Anwendungsbereich oder der "Domäne" verbunden, für die die Software entwickelt wird. Die Domänenlogik ist entscheidend, um sicherzustellen, dass die Software die Anforderungen und Geschäftsprozesse der jeweiligen Domäne korrekt und effektiv abbildet.

**Wichtige Aspekte der Domänenlogik:**

Geschäftsregeln: Die Domänenlogik implementiert die spezifischen Geschäftsregeln, die für die Domäne relevant sind. Das können komplexe Berechnungen, Validierungen, Entscheidungen und Workflows sein, die das Verhalten der Software gemäß den Anforderungen der Geschäftsdomäne steuern.

Objektmodellierung: Die Domänenlogik umfasst oft die Modellierung von Objekten, die die realen Entitäten der Geschäftsdomäne repräsentieren. Diese Objekte können zum Beispiel Kunden, Bestellungen, Produkte oder andere relevante Konzepte sein. Die Interaktionen und Beziehungen zwischen diesen Objekten werden in der Domänenlogik definiert.

Geschäftsprozesse: Die Domänenlogik beschreibt die Abläufe und Prozesse, die in der Geschäftsdomäne stattfinden. Dies kann den Lebenszyklus von Entitäten, den Workflow von Transaktionen oder andere geschäftsrelevante Prozesse umfassen.

Validierung: Während die Validierungslogik sicherstellt, dass die Daten den technischen Anforderungen entsprechen, kümmert sich die Domänenlogik um die Validierung im geschäftlichen Kontext. Sie überprüft, ob die Daten den Geschäftsregeln entsprechen und für die Verarbeitung oder Speicherung geeignet sind.

Entkopplung von Infrastrukturdetails: Die Domänenlogik ist so gestaltet, dass sie weitgehend unabhängig von den technischen Details der zugrunde liegenden Infrastruktur ist. Dies ermöglicht eine bessere Wartbarkeit und Flexibilität, da Änderungen in der Infrastruktur die Domänenlogik nicht wesentlich beeinflussen sollten.

Testbarkeit: Durch die klare Definition von Geschäftsregeln und Prozessen ist die Domänenlogik gut testbar. Dies erleichtert die Entwicklung von Testfällen, um sicherzustellen, dass die Software gemäß den Geschäftsanforderungen funktioniert.

Die Domänenlogik spielt eine Schlüsselrolle bei der Schaffung von Softwarelösungen, die den Geschäftszweck präzise widerspiegeln. Sie fördert eine saubere Trennung von Verantwortlichkeiten und ermöglicht eine klare Strukturierung der Software, was zu wartbaren, erweiterbaren und robusten Anwendungen führt.
[5a]

### Geschäftslogik (Business logic)

Die Geschäftslogik, auch als Business Logic bezeichnet, ist ein zentraler Bestandteil von Softwareanwendungen, der die Regeln und Prozesse definiert, die für die Verarbeitung von Geschäftsdaten und die Ausführung von Geschäftsfunktionen erforderlich sind. Sie bildet die Intelligenz hinter einer Anwendung und legt fest, wie bestimmte Aufgaben und Operationen im Kontext eines spezifischen Geschäftsbereichs durchgeführt werden sollen.

**wichtige Aspekte der Geschäftslogik:**

Regelbasierte Verarbeitung: Die Geschäftslogik besteht oft aus einer Sammlung von Regeln oder Bedingungen, die definieren, wie bestimmte Geschäftsprozesse ablaufen sollen. Diese Regeln können einfache "Wenn-Dann"-Anweisungen oder komplexe Algorithmen sein, die die Logik der Anwendung steuern.

Geschäftsprozesse: Die Geschäftslogik beschreibt die spezifischen Schritte und Abläufe, die in einer Anwendung verfolgt werden, um bestimmte Geschäftsaufgaben zu erledigen. Dies kann alles von einfachen Transaktionen bis zu komplexen Workflows umfassen.

Datenvalidierung: Die Geschäftslogik umfasst oft Mechanismen zur Überprüfung und Validierung von Daten. Das bedeutet, dass die eingegebenen Daten den erforderlichen Geschäftsregeln entsprechen müssen, um akzeptiert und verarbeitet zu werden.

Entscheidungsfindung: Die Geschäftslogik spielt eine entscheidende Rolle bei der Entscheidungsfindung in einer Anwendung. Dies kann bedeuten, dass aufgrund bestimmter Bedingungen unterschiedliche Aktionen ausgeführt werden oder dass automatisierte Entscheidungen getroffen werden, um den Geschäftsprozess voranzutreiben.

Unabhängigkeit von der Benutzeroberfläche: Die Geschäftslogik sollte idealerweise von der Benutzeroberfläche (UI) getrennt sein. Das bedeutet, dass die Regeln und Prozesse unabhängig von der Art und Weise, wie die Benutzer mit der Anwendung interagieren, definiert und ausgeführt werden können.

Insgesamt ist die Geschäftslogik entscheidend, um sicherzustellen, dass eine Softwareanwendung die Geschäftsanforderungen korrekt und effizient erfüllt.
[1a]

### Präsentationslogik (Presentation logic)

Die Präsentationslogik, auch als "Presentation Logic" bezeichnet, ist ein Bereich der Softwarelogik, der sich auf die Darstellung von Informationen für Benutzer konzentriert. Sie regelt die Art und Weise, wie Daten und Funktionen einer Software auf der Benutzeroberfläche präsentiert werden. Die Präsentationslogik spielt eine entscheidende Rolle für die Benutzererfahrung und das visuelle Design einer Anwendung.

**wichtige Aspekte der Präsentationslogik:**

Benutzeroberflächengestaltung: Die Präsentationslogik umfasst das Design und Layout der Benutzeroberfläche. Sie definiert, wie Informationen angezeigt werden, wo Benutzeroberflächenelemente platziert werden und wie der visuelle Fluss gestaltet ist.

Benutzerinteraktion: Diese Art der Logik kümmert sich um die Interaktion zwischen Benutzern und der Anwendung. Das beinhaltet die Handhabung von Benutzereingaben, das Auslösen von Aktionen in Reaktion auf Benutzeraktionen und die Navigation zwischen verschiedenen Ansichten oder Seiten.

Anzeige von Daten: Die Präsentationslogik regelt, wie Daten auf der Benutzeroberfläche präsentiert werden. Das kann das Formatieren von Texten, die Anzeige von Bildern, Tabellen oder Diagrammen und die dynamische Aktualisierung von Informationen umfassen.

Validierung auf der Benutzeroberfläche: Während die Validierungslogik sicherstellt, dass Daten auf technischer Ebene gültig sind, kümmert sich die Präsentationslogik um die Validierung auf der Benutzeroberfläche. Das beinhaltet das Anzeigen von Fehlermeldungen oder Warnungen, wenn Benutzereingaben nicht den erwarteten Kriterien entsprechen.

Feedback für den Benutzer: Die Präsentationslogik ist auch dafür verantwortlich, dem Benutzer Feedback zu geben. Das kann Statusmeldungen, Erfolgsmeldungen oder Fehlermeldungen umfassen, um den Benutzer über den Status seiner Aktionen zu informieren.

Anpassung und Personalisierung: Die Präsentationslogik ermöglicht oft auch die Anpassung der Benutzeroberfläche, um die Bedürfnisse verschiedener Benutzer oder Benutzergruppen zu berücksichtigen. Dies kann die Anpassung von Layouts, Farbschemata oder Anzeigeoptionen umfassen.

Barrierefreiheit: Inklusive Präsentationslogik berücksichtigt auch die Bedürfnisse von Benutzern mit unterschiedlichen Fähigkeiten. Sie stellt sicher, dass die Benutzeroberfläche barrierefrei ist und von allen Benutzern, unabhängig von ihren Fähigkeiten, genutzt werden kann.

Die Präsentationslogik arbeitet oft eng mit anderen Teilen der Softwarelogik, wie der Domänenlogik und der Infrastrukturlogik, zusammen, um eine nahtlose und effektive Benutzererfahrung zu gewährleisten. Eine gut gestaltete Präsentationslogik trägt dazu bei, dass Benutzer die Software intuitiv verstehen und effizient damit interagieren können.

[7a]
### Steuerungslogik (Control logic)

Die Steuerungslogik, auch als "Control Logic" bezeichnet, ist ein entscheidender Bestandteil der Softwarelogik. Sie ist dafür verantwortlich, den Ablauf und die Kontrolle von Anweisungen in einer Softwareanwendung zu regeln. Die Hauptziele der Steuerungslogik sind die Festlegung der Reihenfolge von Operationen, die Kontrolle von Entscheidungen und die Verwaltung des Programmflusses.

**Wichtige Aspekte der Steuerungslogik:**

Programmfluss: Die Steuerungslogik bestimmt die Reihenfolge, in der Anweisungen innerhalb eines Programms ausgeführt werden. Sie sorgt dafür, dass die Operationen in der richtigen Abfolge erfolgen, um die beabsichtigte Funktionalität zu gewährleisten.

Bedingte Anweisungen: Die Steuerungslogik enthält oft bedingte Anweisungen, die es der Software ermöglichen, unterschiedliche Pfade zu nehmen, abhängig von bestimmten Bedingungen. Zum Beispiel kann eine Anwendung basierend auf Benutzereingaben oder Systemzuständen unterschiedliche Operationen ausführen.

Schleifen: Steuerungslogik kann auch Schleifen enthalten, die es erlauben, eine Gruppe von Anweisungen wiederholt auszuführen, solange eine bestimmte Bedingung erfüllt ist. Dies ist nützlich für wiederholende Aufgaben oder Verarbeitungen von Daten.

Unterprogramme und Funktionen: Die Steuerungslogik kann auf Unterprogramme oder Funktionen verweisen, die spezifische Aufgaben ausführen. Dies fördert die Modularität und Wiederverwendbarkeit von Code.

Ausnahmehandling: Die Steuerungslogik behandelt oft auch Ausnahmen oder Fehler. Sie definiert, wie die Software auf unerwartete Situationen reagieren soll, um eine robuste und fehlertolerante Anwendung zu gewährleisten.

Ereignisgesteuerte Logik: In ereignisgesteuerten Systemen regelt die Steuerungslogik, wie die Software auf bestimmte Ereignisse reagiert. Dies kann Benutzerinteraktionen, Systemereignisse oder externe Datenereignisse umfassen.

Die Steuerungslogik ist entscheidend für die ordnungsgemäße Funktionsweise einer Softwareanwendung. Sie sorgt dafür, dass die verschiedenen Komponenten der Anwendung miteinander interagieren und die gewünschten Ergebnisse produzieren. Bei gut gestalteter Steuerungslogik ist der Code lesbar, wartbar und effizient.
[2a]

### Validierungslogik (Validation logic)

Die Validierungslogik, auch als "Validation Logic" bezeichnet, ist ein wichtiger Aspekt der Softwarelogik, der sich darauf konzentriert sicherzustellen, dass die von der Software verarbeiteten Daten den erforderlichen Anforderungen entsprechen und konsistent sind. Diese Art von Logik wird häufig in Form von Validierungsregeln implementiert, die überprüfen, ob die eingegebenen Daten gültig und akzeptabel sind, bevor sie weiterverarbeitet oder gespeichert werden.

**Wichtige Aspekte der  Validierungslogik:**

Dateneingabeüberprüfung: Die Validierungslogik prüft die Daten, die von Benutzern eingegeben oder aus anderen Quellen empfangen werden. Dies kann beinhalten, sicherzustellen, dass die Daten die richtigen Datentypen haben, bestimmte Längenbeschränkungen einhalten oder anderen vordefinierten Kriterien entsprechen.

Integritätsprüfung: Die Validierungslogik überprüft die Konsistenz und Integrität der Daten. Das kann bedeuten, dass Beziehungen zwischen verschiedenen Datenelementen oder -feldern überprüft werden, um sicherzustellen, dass sie logisch miteinander verbunden sind.

Formatüberprüfung: Validierungslogik kümmert sich auch oft um das Überprüfen des Formats von Daten. Dies kann beispielsweise das Überprüfen von Datumsformaten, Telefonnummern oder E-Mail-Adressen umfassen.

Geschäftsregelvalidierung: In vielen Anwendungen gibt es spezifische Geschäftsregeln, die eingehalten werden müssen. Die Validierungslogik implementiert diese Geschäftsregeln, um sicherzustellen, dass die Daten den Anforderungen des jeweiligen Geschäftsszenarios entsprechen.

Benutzereingabevalidierung: Bei Anwendungen mit Benutzeroberflächen überprüft die Validierungslogik die vom Benutzer eingegebenen Daten, bevor sie an die Anwendungslogik weitergeleitet werden. Dies dient dazu, die Datenqualität zu verbessern und Benutzerfehler zu minimieren.

Fehlerbehandlung und Rückmeldung: Wenn die Validierungslogik feststellt, dass Daten nicht den erforderlichen Standards entsprechen, löst sie Fehler aus und gibt Rückmeldungen an den Benutzer oder andere Teile der Software, um auf das Problem hinzuweisen.

Die Validierungslogik spielt eine entscheidende Rolle bei der Sicherstellung der Datenqualität und -konsistenz in einer Softwareanwendung. Durch die Implementierung klarer Validierungsregeln wird vermieden, dass fehlerhafte oder unzureichende Daten in die Anwendung gelangen, was die Zuverlässigkeit und Robustheit der Software verbessert.
[3a]

### Infrastrukturlogik (Infrastructure logic)

Die Infrastrukturlogik, auch als "Infrastructure Logic" bezeichnet, bezieht sich auf den Teil der Softwarelogik, der für die Interaktion mit der zugrunde liegenden Infrastruktur und den externen Ressourcen verantwortlich ist. Diese Infrastruktur umfasst Dinge wie Datenbanken, Netzwerke, Dateisysteme und andere externe Dienste oder Systeme, die von der Software genutzt werden.

**Wichtige Aspekte der Infrastrukturlogik:**

Datenbankzugriff: Die Infrastrukturlogik enthält oft Code, der den Zugriff auf Datenbanken ermöglicht. Dies kann das Lesen, Schreiben, Aktualisieren und Löschen von Daten umfassen. Die Logik sorgt dafür, dass die Software effizient mit der Datenbank kommuniziert und die notwendigen Datenintegritäts- und Transaktionseigenschaften gewährleistet sind.

Dateizugriff: Wenn die Software Dateien lesen oder schreiben muss, kümmert sich die Infrastrukturlogik um diesen Zugriff. Dies kann das Öffnen, Schließen, Lesen und Schreiben von Dateien oder das Arbeiten mit anderen Dateisystemoperationen umfassen.

Netzwerkkommunikation: In vielen Anwendungen ist die Infrastrukturlogik für die Kommunikation über Netzwerke verantwortlich. Das kann den Austausch von Daten zwischen verschiedenen Systemen oder Diensten umfassen, sei es lokal im Netzwerk oder über das Internet.

Externe Dienste: Wenn die Software externe Dienste oder APIs (Application Programming Interfaces) verwendet, kümmert sich die Infrastrukturlogik um die Integration und Kommunikation mit diesen Diensten. Das kann die Authentifizierung, Datenübertragung und Verarbeitung von API-Antworten einschließen.

Sicherheit: Die Infrastrukturlogik spielt auch eine Rolle bei der Implementierung von Sicherheitsmaßnahmen im Zusammenhang mit der Infrastruktur. Das kann die Verschlüsselung von Datenübertragungen, die Authentifizierung von Benutzern oder die sichere Handhabung von Zugriffsrechten umfassen.

Ressourcenverwaltung: Die Infrastrukturlogik ist oft für die effiziente Verwaltung von Ressourcen verantwortlich. Das kann die ordnungsgemäße Freigabe von Datenbankverbindungen, die Handhabung von Pools von Netzwerkverbindungen oder die Verwaltung von Datei-Handles umfassen.

Die Infrastrukturlogik ist entscheidend, um sicherzustellen, dass die Software reibungslos mit ihrer Umgebung interagiert und die erforderlichen Ressourcen effizient nutzt. Sie trägt dazu bei, die Trennung zwischen der eigentlichen Anwendungslogik und der zugrunde liegenden Infrastruktur aufrechtzuerhalten, was die Wartbarkeit und Skalierbarkeit der Software verbessert.

### Beispiele

**Validierungslogik**

Angenommen, man hat ein Anmeldeformular für Benutzer, die sich auf einer Website registrieren möchten. Die Validierungslogik könnte folgende Regeln umfassen:

Benutzername-Validierung:

Der Benutzername darf nur Buchstaben und Zahlen enthalten.
Die Länge des Benutzernamens muss zwischen 5 und 15 Zeichen liegen.
E-Mail-Validierung:

Die E-Mail-Adresse muss ein "@"-Zeichen enthalten.
Die E-Mail-Adresse muss eine gültige Domain haben.
Passwort-Validierung:

Das Passwort muss mindestens 8 Zeichen lang sein.
Es muss mindestens einen Großbuchstaben, einen Kleinbuchstaben und eine Zahl enthalten.
Wenn ein Benutzer versucht, sich zu registrieren, würde die Validierungslogik diese Regeln prüfen, um sicherzustellen, dass die eingegebenen Informationen den Anforderungen entsprechen. Wenn beispielsweise der eingegebene Benutzername weniger als 5 Zeichen hat, wird eine Fehlermeldung angezeigt, die den Benutzer darüber informiert, dass der Benutzername zu kurz ist. Gleiches gilt für die anderen Validierungsregeln.

Die Validierungslogik spielt eine wichtige Rolle, um sicherzustellen, dass die Daten, die von Benutzern eingegeben werden, korrekt und im erwarteten Format sind. Dies hilft, Datenintegrität zu gewährleisten und potenzielle Probleme oder Sicherheitslücken zu verhindern.


**Steuerungslogik**

Angenommen, man hat ein System für einen Online-Shop, und ein Kunde hat Produkte in seinen Warenkorb gelegt und möchte nun den Checkout-Prozess durchlaufen. Die Steuerungslogik könnte folgende Aufgaben umfassen:

Verfügbarkeitsprüfung:

Überprüfen, ob alle Produkte im Warenkorb noch auf Lager sind.
Preisberechnung:

Berechnen des Gesamtpreises der Produkte im Warenkorb, einschließlich etwaiger Rabatte oder Steuern.
Zahlungsbearbeitung:

Überprüfen der Zahlungsinformationen des Kunden, wie Kreditkartennummer und Gültigkeitsdatum.
Auslösen einer Transaktion mit dem Zahlungsanbieter.
Bestandsaktualisierung:

Aktualisieren des Lagerbestands nach einer erfolgreichen Bestellung, um sicherzustellen, dass Produkte, die gekauft wurden, aus dem Bestand entfernt werden.
Versandvorbereitung:

Initiieren der Versandvorbereitung, einschließlich der Erstellung von Versandetiketten und Benachrichtigung des Versanddienstleisters.
Bestätigung an den Kunden:

Versenden einer Bestätigungs-E-Mail an den Kunden mit Details zur Bestellung und voraussichtlichem Lieferdatum.
Die Steuerungslogik orchestriert also den gesamten Checkout-Prozess, indem sie sicherstellt, dass die notwendigen Schritte in der richtigen Reihenfolge durchgeführt werden. Sie prüft auch auf mögliche Fehlerbedingungen, wie eine abgelehnte Kreditkartenzahlung, und reagiert entsprechend, indem sie dem Benutzer eine Fehlermeldung anzeigt und den Bestellprozess stoppt.

In einem komplexeren System könnte die Steuerungslogik auch die Benutzerführung durch verschiedene Phasen des Checkouts steuern und Entscheidungen basierend auf Benutzeraktionen treffen.

**Domänenlogik**

Angenommen, man hat eintwickelt die Domänenlogik für die Funktion "Freunde hinzufügen" in einem sozialen Netzwerk. Die Domänenlogik könnte folgende Aspekte abdecken:

Freundschaftsanfrage senden:

Ein Benutzer A sendet eine Freundschaftsanfrage an Benutzer B.
Freundschaftsanfrage akzeptieren/ablehnen:

Benutzer B kann die Freundschaftsanfrage von Benutzer A akzeptieren oder ablehnen.
Benachrichtigungen:

Beide Benutzer erhalten Benachrichtigungen über den Status der Freundschaftsanfrage.
Freunde anzeigen:

Nachdem die Freundschaftsanfrage akzeptiert wurde, können Benutzer A und B nun die Aktivitäten des jeweils anderen sehen und als "Freunde" miteinander interagieren.
Freunde entfernen:

Benutzer A oder B können die Freundschaft auch wieder beenden, was bedeutet, dass sie nicht mehr als Freunde verbunden sind.
Die Domänenlogik definiert also, wie die Interaktionen im Kontext von Freundschaften in diesem sozialen Netzwerk ablaufen. Sie könnte sicherstellen, dass Freundschaftsanfragen nur an gültige Benutzer gesendet werden können, dass Benutzer Benachrichtigungen über Freundschaftsanfragen erhalten und dass die Sichtbarkeit von Aktivitäten zwischen Freunden gemäß den Datenschutzeinstellungen gesteuert wird.

Die Domänenlogik ermöglicht somit die korrekte und kohärente Verwaltung von Freundschaften im sozialen Netzwerk, wobei sie die spezifischen Regeln und Interaktionen im Kontext dieser Funktion definiert.


**Präsentationslogik**

Angenommen, man entwickelt die Präsentationslogik für eine To-Do-Liste-Anwendung. Die Präsentationslogik könnte folgende Aspekte abdecken:

Anzeigen von Aufgaben:

Die Präsentationslogik bestimmt, wie die Aufgaben in der Benutzeroberfläche dargestellt werden. Dies könnte eine Liste von Aufgaben mit Titel, Beschreibung und Fälligkeitsdatum sein.
Hinzufügen neuer Aufgaben:

Die Präsentationslogik steuert das Formular zum Hinzufügen neuer Aufgaben. Sie kann sicherstellen, dass alle erforderlichen Informationen eingegeben werden, bevor eine neue Aufgabe erstellt wird.
Status der Aufgaben:

Je nach Status einer Aufgabe (z. B. "In Bearbeitung", "Abgeschlossen") könnte die Präsentationslogik das Erscheinungsbild der Aufgabe anpassen. Abgeschlossene Aufgaben könnten beispielsweise durchgestrichen oder farblich hervorgehoben werden.
Filter und Sortierung:

Die Präsentationslogik ermöglicht es Benutzern, ihre Aufgaben nach verschiedenen Kriterien zu filtern (z. B. alle offenen Aufgaben, abgeschlossene Aufgaben) und sie nach verschiedenen Kriterien zu sortieren (z. B. nach Fälligkeitsdatum, nach Priorität).
Benachrichtigungen:

Die Präsentationslogik könnte Benachrichtigungen anzeigen, wenn eine Aufgabe bald fällig ist oder wenn eine Aufgabe abgeschlossen wurde.
In diesem Beispiel steuert die Präsentationslogik, wie die Benutzeroberfläche der To-Do-Liste aussieht und wie Benutzer mit den Aufgaben interagieren können. Sie sorgt dafür, dass die Informationen klar und ansprechend präsentiert werden und dass Benutzer die benötigten Aktionen leicht durchführen können.


#### Persistenz, Cache, Transaktion, Sicherheit, ...

**Persistenz**
Persistenz (von lateinisch persistere „verharren, stehen bleiben“) ist ein wesentlicher Begriff in der Informatik, der die Fähigkeit eines Systems beschreibt, den Zustand seiner Daten, Objektmodelle oder logischen Verbindungen über längere Zeiträume hinweg zu bewahren. Dies gilt insbesondere über geplante oder unvorhergesehene Programmabbrüche hinaus. Eine entscheidende Rolle dabei spielt die Erhaltung dieser Informationen auf nichtflüchtigen Speichermedien wie Festplatten, SSDs oder in Datenbanken.

Die Persistenz hat ihren Ursprung in der Notwendigkeit, Datenbestände und Anwendungsstatus dauerhaft zu speichern, um Informationen über längere Zeiträume hinweg verfügbar zu halten. Dies ist insbesondere wichtig, um sicherzustellen, dass Informationen nicht verloren gehen, wenn ein Computerprogramm beendet oder ein System heruntergefahren wird.

Es handelt sich hierbei um ein grundlegendes Konzept, das dazu beiträgt, die Kontinuität, Zuverlässigkeit und Verfügbarkeit von Informationen in der digitalen Welt zu gewährleisten. Es bildet die Grundlage für viele Anwendungen und Systeme, die über längere Zeiträume hinweg relevant bleiben müssen.
[10a]

**Cache** 
Was ist der Cache?
Ein Cache ist ein reservierter Speicherplatz, der temporäre Daten sammelt. Dieser wird entweder lokal auf Ihrem Computer, Smartphone oder anderen Medien erstellt, um Webseiten, Browser oder Apps schneller laden zu können. Greifen Sie bspw. regelmäßig auf eine Webseite zu, speichert Ihr Browser deren Inhalte im Cache ab. Für Sie als Nutzer ist dieser Zwischenspeicher nicht sichtbar und wird systemseitig angelegt. Rufen Sie die Seite nun erneut auf, werden die Inhalte schneller geladen.

Der Cache ist also ein Speicher, der den erneuten Zugriff durch eine lokale Zwischenspeicherung auf Ihrem PC oder Smartphone erleichtert. Dadurch werden nicht alle Daten bei jedem Öffnen neu heruntergeladen, sondern schnell von der eigenen Festplatte gelesen.

Caches bieten drei entscheidende Vorteile: Zunächst wird die Systemleistung verbessert, indem alles schneller lädt. Zweitens können Anwendungen teilweise offline arbeiten, falls Sie keinen Internetzugang haben, da wichtige Daten zwischengespeichert sind. Und drittens werden Daten zur späteren Verwendung gespeichert, damit ressourceneffizient die Daten nur einmal heruntergeladen werden müssen. Müssten Sie die Daten erneut laden, verbraucht das unnötig Akku bzw. Rechenpower. Trotz der Vorteile kann der Cache auch zu Problemen führen. Grund hierfür können fehlerhafte Daten im Cache sein oder dass der Cache einfach zu viel Speicherplatz einnimmt. Da hilft nur eins: Leeren Sie den Cache!

Um besser zu verstehen, wo der Cache in alltäglichen Anwendungen vorkommt, stellen wir Ihnen im Folgenden die drei häufigsten Beispielfälle zusammen:

Hardware
Internetbrowser
Apps

[11a]
**Transaktion**

In der Infrastrukturlogik bezieht sich der Begriff "Transaktion" auf einen Satz von Aktionen, die als eine zusammenhängende und unteilbare Einheit betrachtet werden. Eine Transaktion in diesem Kontext ist oft mit Änderungen oder Aktualisierungen in einem System verbunden, und sie wird entweder vollständig ausgeführt oder gar nicht. Das bedeutet, dass, wenn ein Teil der Transaktion aus irgendeinem Grund fehlschlägt, alle durchgeführten Änderungen rückgängig gemacht werden, um die Konsistenz der Infrastruktur sicherzustellen.

In der Welt der Datenbanken ist die Transaktionsverarbeitung weit verbreitet. Wenn beispielsweise eine Anwendung Daten in einer Datenbank ändert, könnten mehrere Datenbankoperationen als Teil einer Transaktion gruppiert werden. Wenn eine dieser Operationen scheitert, wird die gesamte Transaktion rückgängig gemacht, um sicherzustellen, dass die Datenbank in einem konsistenten Zustand bleibt.

In der Infrastrukturlogik kann die Verwendung von Transaktionen dazu beitragen, die Integrität und Konsistenz von Änderungen oder Konfigurationen in einem System sicherzustellen.

**Sicherheit**

Sicherheit in Bezug auf Infrastrukturlogik bezieht sich auf die Maßnahmen und Vorkehrungen, die getroffen werden, um die Integrität, Vertraulichkeit und Verfügbarkeit der Infrastruktur sicherzustellen. Hier sind einige Aspekte der Sicherheit in der Infrastrukturlogik:

Zugriffskontrolle: Die Verwaltung von Zugriffsrechten und -beschränkungen ist entscheidend, um sicherzustellen, dass nur autorisierte Personen oder Systeme auf kritische Teile der Infrastruktur zugreifen können.

Verschlüsselung: Die Verschlüsselung von Daten, insbesondere während der Übertragung über Netzwerke, ist wichtig, um sicherzustellen, dass sensible Informationen vor unbefugtem Zugriff geschützt sind.

Überwachung und Protokollierung: Das Überwachen von Aktivitäten in der Infrastruktur und das Protokollieren von Ereignissen helfen dabei, potenzielle Sicherheitsbedrohungen zu erkennen, zu verfolgen und darauf zu reagieren.

Sicherheitsupdates und Patch-Management: Die regelmäßige Aktualisierung von Software und das Einspielen von Sicherheitspatches sind wesentliche Maßnahmen, um Sicherheitslücken zu schließen und die Infrastruktur vor bekannten Bedrohungen zu schützen.

Firewalls und Netzwerksicherheit: Die Implementierung von Firewalls und anderen Netzwerksicherheitsmaßnahmen ist entscheidend, um unerwünschten Datenverkehr zu blockieren und die Integrität des Netzwerks zu gewährleisten.

Physische Sicherheit: Die physische Sicherheit von Serverräumen, Rechenzentren und anderen Infrastrukturelementen ist ebenso wichtig, um unbefugten Zugriff oder physische Bedrohungen zu verhindern.

Notfallwiederherstellung und Redundanz: Die Planung für Notfallsituationen und die Implementierung von Redundanzmechanismen helfen dabei, Ausfallzeiten zu minimieren und die Kontinuität der Infrastruktur sicherzustellen.

Die Sicherheit in der Infrastrukturlogik ist ein umfassendes Konzept, das mehrere Ebenen und Aspekte berücksichtigt, um eine robuste und geschützte Umgebung zu gewährleisten.

## Abbildung der Softwarearchitektur auf die Systemarchitektur


### Multi-Tier Architekturen

Eine Multi-Tier-Architecture ist eine mehrgliedrige Schichtenarchitektur, die die Prinzipien zur Strukturierung von Software-Architekturen definiert. Die hierarchische Strukturierung mittels Schichten ist ein häufig angewendetes Architekturmuster. 
Schichtenarchitektur (auch Schichtenmodell oder Schichtenmuster) ist ein häufig angewandtes Strukturierungsprinzip für die Architektur von Softwaresystemen. Dabei werden einzelne Aspekte des Softwaresystems konzeptionell einer Schicht (engl. tier oder layer) zugeordnet. Die erlaubten Abhängigkeitsbeziehungen zwischen den Aspekten werden bei einer Schichtenarchitektur dahingehend eingeschränkt, dass Aspekte einer höheren Schicht nur solche tieferer Schichten verwenden dürfen. Ein System mit Schichtenarchitektur bezeichnet man auch als „mehrschichtig“.
Die den Schichten zugeordneten Aspekte können dabei je nach Art des Systems oder Detaillierungsgrad der Betrachtung z. B. Funktionalitäten, Komponenten oder Klassen sein.
[8a]

#### Tiers vs. Layers (Stufen vs. Schichten)

**Tiers (Stufen):**

Definition: Tiers beziehen sich auf physisch getrennte Teile einer Anwendung, die auf verschiedenen Servern oder Hardware-Instanzen laufen können.

Verantwortlichkeiten: Jedes Tier hat seine spezifische Rolle und Verantwortlichkeiten. Typischerweise gibt es drei Haupttiers: Präsentationstier, Anwendungstier und Datenzugriffstier.

Physische Verteilung: Tiers implizieren eine physische Verteilung, was bedeutet, dass verschiedene Tiers auf unterschiedlichen Servern oder Hardware-Instanzen laufen können. Dies kann zur Verbesserung der Skalierbarkeit und Leistung beitragen.

**Layers (Schichten):**

Definition: Layers beziehen sich auf die logische Aufteilung einer Anwendung in verschiedene Schichten, wobei jede Schicht eine bestimmte Funktion oder Verantwortlichkeit hat.

Verantwortlichkeiten: Jede Schicht hat eine klare und abgegrenzte Aufgabe. Typische Schichten sind Präsentationsschicht, Anwendungsschicht und Datenzugriffsschicht.

Logische Struktur: Layers beschreiben die logische Struktur einer Anwendung. Diese Schichten sind auf demselben physischen Server implementiert und kommunizieren miteinander, um die Gesamtfunktionalität der Anwendung zu ermöglichen.

**Zusammenfassend:**
Tiers betonen die physische Verteilung und Trennung von Teilen einer Anwendung auf verschiedenen Servern, während Layers die logische Struktur einer Anwendung beschreiben, wobei verschiedene Schichten auf demselben Server implementiert sind. Es ist wichtig zu beachten, dass diese Begriffe in der Praxis oft miteinander verbunden sind, da eine Anwendung mehrere Schichten in einem Tier haben oder eine Schicht in mehreren Tiers verteilen kann.

[9a]

#### (Zwei|Drei|Vier)-Stufen-Architektur

**Zwei-Schichten-Architektur**

Die zweischichtige Architektur (englisch two tier architecture) besteht aus zwei Schichten. Da nur die höhere auf die niedrigere Schicht zugreifen darf, ist die niedrigere Schicht ein Dienstanbieter der höheren. Man spricht daher auch oft von einer Client-Server-Architektur.

Client-Server-Architekturen müssen nicht unbedingt mittels unterschiedlicher Rechner realisiert sein, vielmehr kann der Client auch als ein Software-Modul verstanden werden, das auf ein zweites Software-Modul auf demselben Rechner, meist innerhalb derselben Anwendung zugreift. Das in der Abbildung gegebene Beispiel greift jedoch auf eine rechnerseitige Client-Server-Architektur zurück.

Bei Architekturen wie in der Abbildung gegeben, wird die Rechenkapazität weitestgehend auf die Client-Rechner ausgelagert, um den Server zu entlasten. Traditionell kommt ein Fat Client und ein Fat Server zum Einsatz. Auf dem Server läuft eine Datenbankanwendung. Die Clients übernehmen dabei die Logik und die Darstellung der Benutzerschnittstelle.
[8a]

**Drei-Schichten-Architektur**

Die dreischichtige Architektur ist eine Architektur, die softwareseitig drei Schichten hat. Im Gegensatz zur zweischichtigen Architektur gibt es bei der dreischichtigen Architektur noch eine zusätzliche Schicht, oftmals die Logikschicht, welche die Datenverarbeitung vornimmt.

Eine typische Drei-Schichten-Architektur besteht aus den folgenden Schichten:

Präsentationsschicht: Auch Front-End bezeichnet, ist für die Repräsentation der Daten, Benutzereingaben und die Benutzerschnittstelle verantwortlich.
Logikschicht (application-server tier, Businessschicht, Middle Tier oder Enterprise Tier) – Sie beinhaltet alle Verarbeitungsmechanismen. Hier ist die Anwendungslogik vereint.
Datenhaltungsschicht (data-server tier, back end) – Sie enthält die Datenbank und ist verantwortlich für das Speichern und Laden von Daten.
Drei-Schichten-Architekturen bei verteilten Systemen

Mehrschichtige Systemarchitekturen wie die dreischichtige Architektur sind gut skalierbar, da die einzelnen Schichten logisch voneinander getrennt sind. So kann z.B bei verteilten Systemarchitekturen die Datenschicht auf einem zentralen Datenbank-Server laufen, die Logikschicht auf Workgroup-Servern, und die Präsentationsschicht befindet sich auf der jeweiligen Workstation des Benutzers.

Drei-Schichten-Architekturen innerhalb von Software-Systemen:
Die Architektur lässt sich auch innerhalb eines Software-Systems umsetzen, indem die Software-Module, welche für Präsentation, Anwendungslogik und persistente Speicherung von Daten zuständig sind, den einzelnen Schichten zugeordnet werden und gemäß der Schichteneinteilung voneinander entkoppelt werden. Neben einer Strukturierung gemäß dem Model-View-Controller-Architekturmuster gilt eine solche Drei-Schichten-Architektur üblicherweise als das Mindestmaß architektonischer Strukturierung, sofern keine zwingenden Gründe für andere Architekturentscheidungen vorliegen.
[8a]

**Vier-Stufen-Architektur**

Die Vier-Stufen-Architektur bezieht sich oft auf eine Struktur in Bezug auf Datenverarbeitung und -analyse. Hier sind die vier Stufen:

Datenerfassung (Data Collection): In dieser Phase werden Daten aus verschiedenen Quellen gesammelt. Dies können Sensoren, Benutzerinteraktionen, externe Systeme oder andere Datenquellen sein.

Datenverarbeitung (Data Processing): Die gesammelten Daten werden in dieser Stufe verarbeitet. Dies kann Filtern, Bereinigen, Transformieren und Aggregieren von Rohdaten umfassen. Ziel ist es, die Daten für die Analyse vorzubereiten.

Datenpräsentation (Data Presentation): Hier werden die verarbeiteten Daten visualisiert oder präsentiert. Das kann in Form von Berichten, Dashboards oder anderen Arten von Benutzeroberflächen sein, um die Informationen leicht verständlich und zugänglich zu machen.

Datenanalyse (Data Analysis): Die abschließende Stufe beinhaltet die eigentliche Analyse der Daten, um Muster, Trends oder Erkenntnisse zu identifizieren. Dies kann statistische Analysen, maschinelles Lernen oder andere Methoden umfassen, je nach den Zielen der Datenanalyse.

Diese Vier-Stufen-Architektur bietet eine strukturierte Herangehensweise an den gesamten Prozess der Datenverarbeitung, von der Erfassung bis zur Analyse und Präsentation von Informationen.

[13a]

#### Anwendungsbeispiele zu den jeweiligen Architekturen

**Zwei-Stufen-Architektur**
ToDo-Liste-Anwendung:

Datenerfassung (Stufe 1):

Der Benutzer öffnet die ToDo-Liste-Anwendung und fügt einen neuen Aufgabeneintrag hinzu.
Er gibt die Aufgabenbeschreibung, das Fälligkeitsdatum und andere relevante Informationen ein.

Datenverarbeitung (Stufe 2):

Die Anwendung nimmt die eingegebenen Daten, überprüft auf Vollständigkeit und Validität.
Sie speichert dann den neuen Auftrag in der Datenbank und aktualisiert die Benutzeroberfläche, um die aktualisierte ToDo-Liste anzuzeigen.
In diesem Beispiel besteht die erste Stufe darin, die Aufgabe und ihre Details zu erfassen. Die zweite Stufe umfasst die Verarbeitung dieser Informationen, einschließlich Validierung und Speicherung in einer Datenbank, gefolgt von der Aktualisierung der Benutzeroberfläche, um dem Benutzer die aktualisierte ToDo-Liste anzuzeigen.


**Drei-Stufen-Architektur**


Online-Shop:

Präsentationsschicht (Stufe 1):

Der Benutzer besucht die Website des Online-Shops und durchsucht die Produkte.
Er fügt ausgewählte Produkte zum Warenkorb hinzu und geht zur Kasse.
Anwendungsschicht (Stufe 2):

Die Anwendung verarbeitet die Auswahl des Benutzers, überprüft die Produktverfügbarkeit, berechnet den Gesamtpreis und verwaltet den Warenkorb.
Sie authentifiziert den Benutzer, wenn erforderlich, und initiiert den Zahlungsvorgang.
Datenzugriffsschicht (Stufe 3):

Die Anwendung greift auf die Produktinformationen und Bestelldaten in der Datenbank zu, um die Produktdetails anzuzeigen und Bestellungen zu speichern.
Transaktionsdaten wie Zahlungsinformationen werden sicher in der Datenbank gespeichert.
In diesem Szenario repräsentiert die erste Stufe die Benutzeroberfläche des Online-Shops, wo der Benutzer Produkte durchsucht und auswählt. Die zweite Stufe ist die Anwendungsschicht, die die Geschäftslogik verwaltet, Produktverfügbarkeit überprüft und den Bestellprozess leitet. Die dritte Stufe ist die Datenzugriffsschicht, die auf die Datenbank zugreift, um Produktinformationen zu laden und Transaktionen zu speichern.


**Vier-Stufen-Architektur**

Social Media Plattform:

Datenerfassung (Stufe 1):

Benutzer erstellen Konten auf der Plattform und geben persönliche Informationen wie Name, Profilbild und Interessen ein.
Benutzer veröffentlichen Beiträge, Fotos oder Videos.
Datenverarbeitung (Stufe 2):

Die Plattform verarbeitet die hochgeladenen Daten, überprüft auf Einhaltung der Nutzungsrichtlinien und führt eventuell automatisierte Moderation durch.
Die Plattform analysiert auch Benutzerinteraktionen, um personalisierte Inhalte anzuzeigen und Freundschaftsvorschläge zu generieren.
Datenpräsentation (Stufe 3):

Die verarbeiteten Daten werden in der Benutzeroberfläche präsentiert. Benutzer sehen ihren personalisierten Feed, Freundesaktivitäten und relevante Werbung.
Die Plattform bietet Funktionen zur Interaktion, wie das Liken, Kommentieren und Teilen von Beiträgen.
Datenanalyse (Stufe 4):

Die Plattform analysiert aggregierte Daten, um Trends im Benutzerverhalten zu identifizieren.
Diese Analysen können zur Verbesserung der Benutzererfahrung, Anpassung von Werbung und Identifikation von aufkommenden Trends verwendet werden.
In diesem Beispiel repräsentiert die erste Stufe die Datenerfassung durch Benutzeraktivitäten. Die zweite Stufe beinhaltet die Verarbeitung und Überprüfung dieser Daten. Die dritte Stufe präsentiert die verarbeiteten Daten in der Benutzeroberfläche, während die vierte Stufe Analysen durchführt, um Einblicke und Verbesserungen für die Plattform zu generieren.



## Referenzen

[1a] : https://de.wikipedia.org/wiki/Gesch%C3%A4ftslogik
[2a] : https://chat.openai.com/c/63c2b80e-a9dd-4735-8ea0-edad1bff8a7c frage : erkläre mir ausführlich die Steuerungslogik
[3a] : https://chat.openai.com/c/63c2b80e-a9dd-4735-8ea0-edad1bff8a7c frage : erkläre mir ausführlich was die Validierungslogik (Validation logic) ist
[4a] : https://chat.openai.com/c/63c2b80e-a9dd-4735-8ea0-edad1bff8a7c frage :erkläre mir ausführlich was Infrastrukturlogik (Infrastructure logic) ist
[5a] : https://chat.openai.com/c/63c2b80e-a9dd-4735-8ea0-edad1bff8a7c frage :erkläre mir ausführlich was die Domänenlogik (Domain logic) ist
[6a] :https://chat.openai.com/c/63c2b80e-a9dd-4735-8ea0-edad1bff8a7c frage: erkläre mir die Geschäftslogik (Business logic) ausführlich
[7a] : https://chat.openai.com/c/63c2b80e-a9dd-4735-8ea0-edad1bff8a7c frage : erkläre mir ausführlich was die  Präsentationslogik (Presentation logic) ist
[8a] : https://de.wikipedia.org/wiki/Schichtenarchitektur
[9a] : https://saipawan.wordpress.com/2015/08/19/whats-the-difference-between-layers-and-tiers/
[10a] : https://de.wikipedia.org/wiki/Persistenz_(Informatik)
[11a] : https://www.heise.de/tipps-tricks/Was-ist-ein-Cache-4932006.html
[12a] : https://chat.openai.com/?model=text-davinci-002-render-sha frage : was ist Sicherheit im Bezug auf Infrastrukturlogik 
[13a] : https://chat.openai.com/c/63c2b80e-a9dd-4735-8ea0-edad1bff8a7c : was ist eine vier stufen Archtiketur




