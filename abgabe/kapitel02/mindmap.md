## Kapitelüberschrift

**Autor:** Jannis Wilmsmeier

Folgende Mindmaps zeigen die Inhalte des Kapitels 2.

## Verteilte Softwaresysteme

```mermaid
mindmap
  STILL MISSING
    Origins
      Long history
      Popularisation
        British popular psychology author Tony Buzan
    Research
      On effectiveness<br/>and features
      On Automatic creation
        Uses
            Creative techniques
            Strategic planning
            Argument mapping
    Tools
      Pen and paper
      Mermaid
```

## Systemarchitektur verteilter Softwaresysteme

```mermaid
mindmap
  Systemarchitektur verteilter Softwaresysteme
    Systemarchitekturmuster
      Client Server
        Vorteile
          Skalierbarkeit
          Resourcennutzung
        Anwendungsbeispiele
          Outlook
          Thunderbird
        Web Architekturen
          PWA
            App-ähnliche Erfahrung
            Resourceneffizienz
            Offline-Fähigkeiten
            Push-Benachrichtigungen
            Ladezeit
          SPA
            eine HTML Seite
            dynamische Aktualisierung
            nahtlose Benutzererlebnisse
            schnelle Ansichtswechsel
          MPA
            Seiten laden seperat
            einfach zu entwickeln
            gute Benutzererfahrung
            SEO-freundlich
      Peer to peer
        Vorteile
          Gleichberechtigung
          dezentral
          ausfallsicher
          direkte Kommunikation
        Andwendungsbeispiele
          BitTorrent
          eDonkey
          einige IoT-Anwendungen
      Event Driven Architecture
        Event types (Klassifikation von Ereignissen)
          Systemereignisse
          Fehler- und Ausnahmeereignisse
        Message Broker (Vermittlung und Verteilung von Ereignissen)
        Kommunikation zwischen Anwengunen und Systemkomponenten
          ESB
            Integrationsplattform
              Verknüpfung von Anwendungen
              Nachrichtenvermittlung
              Routing
              Nachrichtenverarbeitung
              Anwendungsbeispiel
                E-Commerce-Plattform für Bestellungen + Lagerverwaltungssystem
          Message Queue
            Nachrichten temporär speichern/übertragen
            zuverlässige Kommunikation zwischen Anwendungen
            Anwendungsbeispiel
                Flugbuchungssystem + Sitzplatzbestätigung
    Modulare Architekturen
      Service oriented Architecture
        Vorteile
          wiederverwendbar
          lose Kopplung
          Interoperabilität
        Service Discovery
          Dienste identifzieren
          Dienste auffinden
          auf Dienste zugreifen
    Microservices
      Vorteile
        entkoppelt
        dezentral
        skalierbar
      Arten
        Monolith
          einzige Anwendungseinheit
          Kommunikation innerhalb der Anwendung
          schwer sklaierbar
          einfach in der Entwicklung
        Distributed Monolith
          Monolith auf mehreren Servern
          Kommunikation über Netzwerke
          begrent skaliberbar
        Microservice
          unabhängige Dienste
          definierte APIs oder Messaging-Protokolle
          unabhängig skalierbar
          wiederverwendbar
      Koordinationsansätze
        Choreography Pattern
          Interaktion/Kommunikation zwischen Diensten
          Dienste handeln autonom
          dezentrale Koordination
        Orchestration Pattern
          zentrale Koordination/Steuerung
          Orchestrator definiert Handlung von Diensten
      Service Mesh
        Proxies zwischen Mikrodiensten
        Verwaltung von Netzwerkaufgaben und -diensten
```

## Systemdesign

```mermaid
mindmap
  Systemdesign
    Komponenten
      API Gateway
        verwaltet APIs
      Proxy
        leitet Client-Anfragen an Backend-Server weiter
        Vorteile
          Lastenausgleich
          Caching
          Sicherheit
          vielseitig einsetzbar
      Reverse Proxy
        verarbeitet Client-Anfragen
        leitet an richtigen Backend-Server weiter
        Vorteile
          Sicherheit
          Leistungsverbessrung
      Load Balancer
        Verteilung von Datenverkehr
          Leistungssteigerung
          Ausfallsicherheit
    Skalierungsmuster
      Horizontale Skalierung
        mehr Server/Instanzen bereitstellen
        besonders hilfreich für parallele Verarbeitung
      Vertikale Skalierung
        vorhandende Resource wird verstärkt
        einzelne Instanz kann mehr Last bewältigen
      Replication
        Erstellen/Pflegen von Datenkopien
        verschiedene Standorte/Server
        Vorteile
          Leistung
          Verfügbarkeit
          Ausfallsicheheut
          Reduzierung von Latenz
      Partitioning
        teilen von Daten
        überschaubare Partitionen
      Sharding
        Aufteilung von Datenbanksätzen
        basiert auf Schlüsselwert
      Load Balancing
        Round robin
          verteilt Datenverkehr gleichmäßig
          ignoriert Auslastung
        Least Connections
          priorisiert weniger ausgelastete Server
        IP-Hash
          Server wird mittels Client-IP zugeteilt
        Random
      Caching
        Application Server Cache
          oft angefragte Daten im Arbeitsspeicher
        Globales Caching
          ein einziger Cache
        Distrbuted Caching
          Cache wird über mehrere Server/Knoten verteilt
        Hierarchisches Caching
          Kombination aus Local und Distributed Caching
        Content Delivery Network
          Spezialisierung verteilter Caches
      Skalierungswürfel
        Horizontale Skalierung
        Funktionale Aufteilung
        Datenpartitionierung
```
