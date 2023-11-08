# Kapitel 6 

**Autor:** Simon Fedrau, Sascha Hahn

## Lernziele


## Arten von Softwarelogik
***



### Domänenlogik (Domain logic)

Die Domänenlogik, auch als "Domain Logic" bezeichnet, ist ein zentraler Bestandteil der Softwarelogik, der sich auf die Umsetzung von Geschäftsregeln, -logik und -prozessen konzentriert. Sie bildet die Kernlogik einer Softwareanwendung und ist eng mit dem spezifischen Anwendungsbereich oder der "Domäne" verbunden, für die die Software entwickelt wird. Die Domänenlogik ist entscheidend, um sicherzustellen, dass die Software die Anforderungen und Geschäftsprozesse der jeweiligen Domäne korrekt und effektiv abbildet.

Hier sind einige wichtige Aspekte der Domänenlogik:

Geschäftsregeln: Die Domänenlogik implementiert die spezifischen Geschäftsregeln, die für die Domäne relevant sind. Das können komplexe Berechnungen, Validierungen, Entscheidungen und Workflows sein, die das Verhalten der Software gemäß den Anforderungen der Geschäftsdomäne steuern.

Objektmodellierung: Die Domänenlogik umfasst oft die Modellierung von Objekten, die die realen Entitäten der Geschäftsdomäne repräsentieren. Diese Objekte können zum Beispiel Kunden, Bestellungen, Produkte oder andere relevante Konzepte sein. Die Interaktionen und Beziehungen zwischen diesen Objekten werden in der Domänenlogik definiert.

Geschäftsprozesse: Die Domänenlogik beschreibt die Abläufe und Prozesse, die in der Geschäftsdomäne stattfinden. Dies kann den Lebenszyklus von Entitäten, den Workflow von Transaktionen oder andere geschäftsrelevante Prozesse umfassen.

Validierung: Während die Validierungslogik sicherstellt, dass die Daten den technischen Anforderungen entsprechen, kümmert sich die Domänenlogik um die Validierung im geschäftlichen Kontext. Sie überprüft, ob die Daten den Geschäftsregeln entsprechen und für die Verarbeitung oder Speicherung geeignet sind.

Entkopplung von Infrastrukturdetails: Die Domänenlogik ist so gestaltet, dass sie weitgehend unabhängig von den technischen Details der zugrunde liegenden Infrastruktur ist. Dies ermöglicht eine bessere Wartbarkeit und Flexibilität, da Änderungen in der Infrastruktur die Domänenlogik nicht wesentlich beeinflussen sollten.

Testbarkeit: Durch die klare Definition von Geschäftsregeln und Prozessen ist die Domänenlogik gut testbar. Dies erleichtert die Entwicklung von Testfällen, um sicherzustellen, dass die Software gemäß den Geschäftsanforderungen funktioniert.

Die Domänenlogik spielt eine Schlüsselrolle bei der Schaffung von Softwarelösungen, die den Geschäftszweck präzise widerspiegeln. Sie fördert eine saubere Trennung von Verantwortlichkeiten und ermöglicht eine klare Strukturierung der Software, was zu wartbaren, erweiterbaren und robusten Anwendungen führt.
[5a]

### Geschäftslogik (Business logic)

Geschäftslogik (englisch business logic, auch Anwendungslogik) ist ein abstrakter Begriff in der Softwaretechnik, der eine Abgrenzung der durch die Aufgabenstellung selbst motivierten Logik eines Softwaresystems zu der notwendigen, technischen Logik zum Ziel hat. Allerdings ist der Begriff unscharf, da eine klare Trennung oft nicht möglich ist.

Eingeführt wurde der Begriff in Verbindung mit Schichtenarchitekturen, vor allem mit Aufkommen von Client-Server-Architekturen. Kontextuell ist die Geschäftslogik dabei in der Mitte angesiedelt, „oberhalb“ einer Datenhaltungsschicht und „unterhalb“ der Präsentationsschicht, also zwischen Datenbank und Benutzerschnittstelle.

Die Motivation bei Einführung des Begriffs liegt im Wesentlichen darin, dass man die Logik, die die eigentliche Problemstellung implementiert, von der Logik trennt, die die technischen Belange abdeckt. Dabei wird unterstellt, dass diese Anwendungsteile unterschiedlichen Änderungszyklen unterliegen und daher durch deren Trennung die Wartbarkeit des Softwaresystems verbessert wird.

In Verbindung mit der Objektorientierung wurde der Gedanke der Geschäftslogik zu sogenannten Geschäftsobjekten erweitert. Beim Model-View-Controller-Paradigma wird sie von einigen zum Model gezählt.
[1a]

Die Geschäftslogik, auch als Business Logic bezeichnet, ist ein zentraler Bestandteil von Softwareanwendungen, der die Regeln und Prozesse definiert, die für die Verarbeitung von Geschäftsdaten und die Ausführung von Geschäftsfunktionen erforderlich sind. Sie bildet die Intelligenz hinter einer Anwendung und legt fest, wie bestimmte Aufgaben und Operationen im Kontext eines spezifischen Geschäftsbereichs durchgeführt werden sollen.

Hier sind einige Schlüsselkonzepte, die die Geschäftslogik weiter erläutern:

Regelbasierte Verarbeitung: Die Geschäftslogik besteht oft aus einer Sammlung von Regeln oder Bedingungen, die definieren, wie bestimmte Geschäftsprozesse ablaufen sollen. Diese Regeln können einfache "Wenn-Dann"-Anweisungen oder komplexe Algorithmen sein, die die Logik der Anwendung steuern.

Geschäftsprozesse: Die Geschäftslogik beschreibt die spezifischen Schritte und Abläufe, die in einer Anwendung verfolgt werden, um bestimmte Geschäftsaufgaben zu erledigen. Dies kann alles von einfachen Transaktionen bis zu komplexen Workflows umfassen.

Datenvalidierung: Die Geschäftslogik umfasst oft Mechanismen zur Überprüfung und Validierung von Daten. Das bedeutet, dass die eingegebenen Daten den erforderlichen Geschäftsregeln entsprechen müssen, um akzeptiert und verarbeitet zu werden.

Entscheidungsfindung: Die Geschäftslogik spielt eine entscheidende Rolle bei der Entscheidungsfindung in einer Anwendung. Dies kann bedeuten, dass aufgrund bestimmter Bedingungen unterschiedliche Aktionen ausgeführt werden oder dass automatisierte Entscheidungen getroffen werden, um den Geschäftsprozess voranzutreiben.

Unabhängigkeit von der Benutzeroberfläche: Die Geschäftslogik sollte idealerweise von der Benutzeroberfläche (UI) getrennt sein. Das bedeutet, dass die Regeln und Prozesse unabhängig von der Art und Weise, wie die Benutzer mit der Anwendung interagieren, definiert und ausgeführt werden können.

Ein Beispiel für Geschäftslogik könnte in einem Online-Shopping-System liegen: Die Regel, dass ein Rabatt von 10% auf alle Artikel gewährt wird, wenn der Gesamtbetrag des Warenkorbs einen bestimmten Betrag übersteigt, repräsentiert einen Teil der Geschäftslogik.

Insgesamt ist die Geschäftslogik entscheidend, um sicherzustellen, dass eine Softwareanwendung die Geschäftsanforderungen korrekt und effizient erfüllt.


### Präsentationslogik (Presentation logic)

Die Präsentationslogik, auch als "Presentation Logic" bezeichnet, ist ein Bereich der Softwarelogik, der sich auf die Darstellung von Informationen für Benutzer konzentriert. Sie regelt die Art und Weise, wie Daten und Funktionen einer Software auf der Benutzeroberfläche präsentiert werden. Die Präsentationslogik spielt eine entscheidende Rolle für die Benutzererfahrung und das visuelle Design einer Anwendung.

Hier sind einige wichtige Aspekte der Präsentationslogik:

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

Hier sind einige Schlüsselaspekte der Steuerungslogik:

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

Hier sind einige Schlüsselaspekte der Validierungslogik:

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

Hier sind einige wichtige Aspekte der Infrastrukturlogik:

Datenbankzugriff: Die Infrastrukturlogik enthält oft Code, der den Zugriff auf Datenbanken ermöglicht. Dies kann das Lesen, Schreiben, Aktualisieren und Löschen von Daten umfassen. Die Logik sorgt dafür, dass die Software effizient mit der Datenbank kommuniziert und die notwendigen Datenintegritäts- und Transaktionseigenschaften gewährleistet sind.

Dateizugriff: Wenn die Software Dateien lesen oder schreiben muss, kümmert sich die Infrastrukturlogik um diesen Zugriff. Dies kann das Öffnen, Schließen, Lesen und Schreiben von Dateien oder das Arbeiten mit anderen Dateisystemoperationen umfassen.

Netzwerkkommunikation: In vielen Anwendungen ist die Infrastrukturlogik für die Kommunikation über Netzwerke verantwortlich. Das kann den Austausch von Daten zwischen verschiedenen Systemen oder Diensten umfassen, sei es lokal im Netzwerk oder über das Internet.

Externe Dienste: Wenn die Software externe Dienste oder APIs (Application Programming Interfaces) verwendet, kümmert sich die Infrastrukturlogik um die Integration und Kommunikation mit diesen Diensten. Das kann die Authentifizierung, Datenübertragung und Verarbeitung von API-Antworten einschließen.

Sicherheit: Die Infrastrukturlogik spielt auch eine Rolle bei der Implementierung von Sicherheitsmaßnahmen im Zusammenhang mit der Infrastruktur. Das kann die Verschlüsselung von Datenübertragungen, die Authentifizierung von Benutzern oder die sichere Handhabung von Zugriffsrechten umfassen.

Ressourcenverwaltung: Die Infrastrukturlogik ist oft für die effiziente Verwaltung von Ressourcen verantwortlich. Das kann die ordnungsgemäße Freigabe von Datenbankverbindungen, die Handhabung von Pools von Netzwerkverbindungen oder die Verwaltung von Datei-Handles umfassen.

Die Infrastrukturlogik ist entscheidend, um sicherzustellen, dass die Software reibungslos mit ihrer Umgebung interagiert und die erforderlichen Ressourcen effizient nutzt. Sie trägt dazu bei, die Trennung zwischen der eigentlichen Anwendungslogik und der zugrunde liegenden Infrastruktur aufrechtzuerhalten, was die Wartbarkeit und Skalierbarkeit der Software verbessert.



#### Persistenz, Cache, Transaktion, Sicherheit, ...






## Abbildung der Softwarearchitektur auf die Systemarchitektur



### Multi-Tier Architekturen

Multi-Tier-Architekturen sind eine Möglichkeit, Softwareanwendungen zu strukturieren. Stell sie dir wie einen Kuchen vor, der in verschiedene Schichten unterteilt ist. Jede Schicht erfüllt bestimmte Aufgaben und hat eine klare Schnittstelle zu den anderen Schichten.

Die gängigsten Schichten in einer Multi-Tier-Architektur sind:

Präsentationsschicht (Presentation Tier): Hier findet die Benutzeroberfläche statt, also das, was der Nutzer sieht und mit dem er interagiert.

Anwendungsschicht (Application Tier): Diese Schicht enthält die Geschäftslogik der Anwendung. Sie verarbeitet Benutzereingaben, führt Operationen durch und koordiniert die Datenverarbeitung.

Datenzugriffsschicht (Data Tier): Hier werden die Daten gespeichert und abgerufen. Datenbanken oder andere Datenspeicher liegen in dieser Schicht.

Der Vorteil dieser Struktur liegt in der klaren Trennung von Verantwortlichkeiten. Änderungen in einer Schicht haben minimale Auswirkungen auf die anderen Schichten. Das erleichtert die Wartung, Erweiterung und Skalierbarkeit von Anwendungen.


#### Tiers vs. Layers (Stufen vs. Schichten)




#### (Zwei|Drei|Vier)-Stufen-Architektur





#### Anwendungsbeispiele










![:scale 80%](media\Titelbild-devops-tools-definition-best-practice.png)

### Tabelle

| A          |     B       |           C               | 
|:----------:|:-----------:|:-------------------------:|
| Eins | Zwei | Drei |
| Vier | Fünf | Sechs |

## Links

[Markdown] ist eine Sprache, die nach HTML konvertiert werden kann. 

## Aufzählung

Es unterteilt sich in:

* A
  * A1
* B
  * B1
  * B2
* C


### Code

```javascript
public class A {
  Integer a;
  public A() {
    this.a = 1
  }
}
```


### Bilder

![](media/image.jpg)




## Referenzen

[1a] : https://de.wikipedia.org/wiki/Gesch%C3%A4ftslogik
[2a] : https://chat.openai.com/c/63c2b80e-a9dd-4735-8ea0-edad1bff8a7c frage : erkläre mir ausführlich die Steuerungslogik
[3a] : https://chat.openai.com/c/63c2b80e-a9dd-4735-8ea0-edad1bff8a7c frage : erkläre mir ausführlich was die Validierungslogik (Validation logic) ist
[4a] : https://chat.openai.com/c/63c2b80e-a9dd-4735-8ea0-edad1bff8a7c frage :erkläre mir ausführlich was Infrastrukturlogik (Infrastructure logic) ist
[5a] : https://chat.openai.com/c/63c2b80e-a9dd-4735-8ea0-edad1bff8a7c frage :erkläre mir ausführlich was die Domänenlogik (Domain logic) ist
[6a] :https://chat.openai.com/c/63c2b80e-a9dd-4735-8ea0-edad1bff8a7c frage: erkläre mir die Geschäftslogik (Business logic) ausführlich
[7a] : https://chat.openai.com/c/63c2b80e-a9dd-4735-8ea0-edad1bff8a7c frage : erkläre mir ausführlich was die  Präsentationslogik (Presentation logic) ist










