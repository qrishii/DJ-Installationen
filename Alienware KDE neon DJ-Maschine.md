# Alienware KDE neon DJ-Maschine

## Version 1.0.0 – Stable

> **Ein Revitalisierungsprojekt auf Basis eines Alienware m17x (2008)**
>
> *Revitalisierung statt ersetzen.*

## German Draft

Eine stabile Linux-DJ-Plattform auf Basis eines Alienware m17x aus dem Jahr 2008.

Dieses Projekt dokumentiert die Modernisierung und Optimierung eines 1.Gen. Alienware-Notebooks in eine extraordinäre und stabile DJ-Maschine unter Linux. Ziel war nicht maximale Rechenleistung, sondern eine solide Audio-Plattform mit geringer Systemlast, hoher Beständigkeit und nachhaltigem Upcycling hochwertiger Hardware.

Nach Abschluss aller Optimierungen arbeitet das System im Langzeittest stabil, knisterfrei und mit hervorragender Audioqualität.

## Fotos

![Setup Weitwinkel](am17_weit.jpg)

Das Masterpice im Bilderrahmen ist von trootootoo 

![Setup Weitwinkel](am17_m.jpg) 

---

## Projektziel

Ziel des Projekts war der Aufbau einer möglichst schlanken und stabilen Linux-DJ-Plattform.

Die Maschine wird ausschließlich für folgende Aufgaben eingesetzt:

- Mixxx DJ Software
- Audioausgabe
- Musikverwaltung
- Wartung und Systemupdates

Eine Internetverbindung wird ausschließlich für Wartung, Updates und Softwareinstallation verwendet.

Prioritäten des Projekts:

- Stabilität vor maximaler Leistung
- geringe Systemlast vor unnötigen Funktionen
- Reparierbarkeit vor Austausch
- nachhaltige Nutzung vorhandener Hardware

---

## Projektstatus

**Version 1.0.0 – Stable**

Das Projektziel wurde erreicht.

Die Basisplattform ist vollständig optimiert und erfolgreich im Langzeittest erprobt.

Ab dieser Version erfolgen keine grundlegenden Änderungen am Betriebssystem.

Künftige Arbeiten betreffen ausschließlich:

- funktionale Erweiterungen
- Aktualisierung einzelner Komponenten
- Weiterentwicklung der Dokumentation

---

## Hardware-Upgrade

Die Modernisierung erfolgte mit Komponenten, die für den Alienware m17x (2008) heute noch verfügbar waren und ohne aufwendige Umbauten integriert werden konnten.

| Komponente | Upgrade | Kosten |
|------------|---------|-------:|
| SSD | Samsung 870 EVO 500 GB | ca. 90 € |
| Arbeitsspeicher | Erweiterung von 2 GB auf 4 GB | ca. 10 € |

**Gesamtinvestition:** ca. **100 €**

Mit diesen beiden Upgrades entstand aus einem Alienware m17x (2008) eine vollständig einsatzfähige Linux-DJ-Maschine.

---

## Wirtschaftlichkeit

Dieses Projekt zeigt, dass hochwertige Hardware auch nach vielen Jahren sinnvoll weiter genutzt werden kann.

### Vorteile

- erste Alienware-Generation erhalten
- Investition von lediglich ca. 100 €
- reparaturfreundliche Hardware
- Verlängerung der Nutzungsdauer
- nachhaltige Wiederverwendung vorhandener Komponenten

Die Entscheidung gegen eine Neuanschaffung war keine Einschränkung, sondern eine bewusste technische und wirtschaftliche Entscheidung.

---

## Gehäuse und Design

Ein wesentlicher Faktor für den Erhalt des Systems ist das außergewöhnliche Gehäusedesign des frühen Alienware m17x.

Besondere Merkmale:

- Magnesium-Aluminium-Gehäuse
- gummierte **„Stealth Black Soft-Touch“**-Oberfläche
- matte, reflexionsarme Oberfläche
- griffige Haptik
- robuste Konstruktion
- dezentes, funktionales Erscheinungsbild

Modelle mit dieser Gehäuseausführung sind heute selten.

Der Erhalt des Systems war daher nicht nur eine technische, sondern auch eine ästhetische Entscheidung.

---

## Hardware

| Komponente | Spezifikation |
|------------|---------------|
| Modell | Alienware m17x (2008) |
| CPU | Intel Core 2 Duo P8400 |
| Kerne | 2 |
| Taktfrequenz | 2,26 GHz |
| RAM | 3,8 GiB |
| SSD | Samsung 870 EVO 500 GB |
| GPU | AMD Mobility Radeon |
| Grafikspeicher | 512 MB |

## Betriebssystem

| Komponente | Version |
|------------|---------|
| Distribution | KDE neon |
| Kernel | 7.0.0-28-generic |
| Audio-System | PipeWire |
| Session Manager | WirePlumber |
| Echtzeit-Unterstützung | RTKit |
| DJ-Software | Mixxx 2.5.6 |

Das System wurde ausschließlich für den DJ-Betrieb optimiert.

---

## Kernel

Während der Entwicklung wurden mehrere Linux-Kernel erfolgreich getestet.

| Kernel | Status |
|---------|--------|
| 7.0.0-28-generic | **Produktiv** |
| 6.8.0-134-lowlatency | erfolgreich getestet |
| 6.17.0-40-generic | erfolgreich getestet |

Der produktive Betrieb erfolgt mit dem **Linux 7.0.0-28-generic**-Kernel.

Nach den durchgeführten Tests bot dieser Kernel die beste Kombination aus Stabilität, Kompatibilität und Audioleistung für den vorgesehenen Einsatzzweck.

---

## Systemoptimierung

Der Schwerpunkt der Optimierung lag auf einer stabilen Audioverarbeitung bei möglichst geringer Systemlast.

Optimierungsziele:

- geringe Hintergrundaktivität
- konstante CPU-Leistung
- stabile Audiowiedergabe
- kurze Bootzeit
- reproduzierbares Systemverhalten

---

## CPU

### Governor

```bash
performance
```

Ergebnis:

- konstante CPU-Leistung
- keine CPU-Peaks im Normalbetrieb
- stabile Audioverarbeitung

Die CPU erwies sich im Verlauf der Analyse nicht als limitierender Faktor.

---

## Bootzeit

Analyse:

```bash
systemd-analyze
```

| Bereich | Zeit |
|---------|-----:|
| Kernel | ca. 6 Sekunden |
| Userspace | ca. 18 Sekunden |
| Gesamt | ca. 24 Sekunden |

Für ein System aus dem Jahr 2008 stellt dies ein sehr gutes Ergebnis dar.

---

## Arbeitsspeicher

| Bereich | Wert |
|---------|-----:|
| Gesamter RAM | 3,8 GiB |
| Belegt | ca. 1,4 GiB |
| Verfügbar | ca. 2,4 GiB |
| Swap | 8,4 GiB |

Während des DJ-Betriebs erfolgt keine erkennbare Swap-Nutzung.

---

## Deaktivierte Dienste

### Drucksystem

Deaktiviert:

```text
cups.service
cups.path
cups-browsed.service
```

Status:

```text
masked
```

Da keine Druckfunktion benötigt wird.

### Samba

Deaktiviert:

```text
nmbd.service
samba-ad-dc.service
```

Status:

```text
masked
```

Aktiv:

```text
smbd.service
```

Die Freigabe bleibt für eine spätere Übertragung von Musikdateien über das Netzwerk erhalten.

---

## Audio-System

Verwendete Komponenten:

- PipeWire
- WirePlumber
- RTKit
- ALSA

Diese Kombination ermöglicht eine moderne Linux-Audioverwaltung bei hoher Stabilität und guter Kompatibilität mit Mixxx.

---

## Mixxx-Start

Mixxx wird mit folgendem Umgebungsparameter gestartet:

```bash
PA_ALSA_PLUGHW=1
```

Im KDE-Menü-Editor wird der Parameter unter **Befehlszeilen-Argumente** eingetragen.

Dadurch kann Mixxx das Master-Audiointerface stabil über ALSA öffnen, ohne das man es bei jedem Start manuell eintragen muss.

---

## Audio-Hardware

| Funktion | Gerät | Native Samplerate |
|----------|-------|------------------:|
| Master | USB Audio Device | 46.875 Hz |
| Cue | C-Media USB Soundkarte für Headphone | 44.100 Hz / 48.000 Hz |

Startparameter:

```bash
PA_ALSA_PLUGHW=1
```

Dadurch kann Mixxx das Master-Gerät stabil öffnen.

---

## Mixxx

| Bereich | Einstellung |
|---------|-------------|
| Version | 2.5.6 |
| Audio API | ALSA |
| Decks | 4 |
| Master | USB Audio Device |
| Cue | C-Media USB Headphone |

Ergebnis:

- stabiler Vier-Deck-Betrieb
- stabile Master-Ausgabe
- stabiles Kopfhörer-Vorhören
- sehr geringe CPU-Auslastung
- fehlerfreier Einzelbetrieb beider USB-Audiointerfaces

---

## Analyse

Während der Entwicklung wurden systematisch untersucht:

- CPU-Leistung
- Arbeitsspeicher
- Linux-Kernel
- PipeWire
- WirePlumber
- ALSA
- Mixxx
- unterschiedliche USB-Sampleraten

CPU, Kernel, Arbeitsspeicher und allgemeine Systemleistung konnten als Hauptursache der ursprünglichen Audioprobleme ausgeschlossen werden.

## Langzeittest

Nach Abschluss aller Optimierungen wurde das System über einen längeren Zeitraum unter realen Einsatzbedingungen getestet.

Konfiguration:

| Gerät | Lautstärke |
|--------|-----------:|
| USB Audio Device | 90 % |
| C-Media USB Headphone | 90 % |

Ergebnis:

- stabiler Vier-Deck-Betrieb
- gleichzeitiger Betrieb beider USB-Audiointerfaces
- stabile Master-Ausgabe
- stabiles Kopfhörer-Vorhören
- keine CPU-Peaks
- kein Audioknistern
- keine Aussetzer
- hervorragende Klangqualität

---

## Technische Erkenntnisse

Die Entwicklung verlief in mehreren aufeinander aufbauenden Analyse- und Testphasen.

Untersucht wurden unter anderem:

- CPU-Leistung
- Arbeitsspeicher
- Linux-Kernel
- Audio-Stack
- Mixxx
- USB-Audiointerfaces
- unterschiedliche native Sampleraten

Mehrere Arbeitshypothesen konnten im Verlauf der Untersuchungen ausgeschlossen oder angepasst werden.

Die erreichte Stabilität entstand nicht durch eine einzelne Änderung, sondern durch den Einklang aller vorgenommenen Optimierungen.

### Gerätepegel

Während der Fehlersuche wurden die Gerätepegel beider USB-Audiointerfaces
testweise auf 50 % reduziert.

Nach weiteren Langzeittests konnten beide Geräte dauerhaft mit **90 %**
betrieben werden, ohne dass CPU-Peaks oder Audioknistern erneut auftraten.

Die zwischenzeitliche Reduzierung der Gerätepegel erwies sich damit als
wertvoller Zwischenschritt der Analyse, nicht jedoch als notwendige
Betriebseinstellung.

---

## Projektergebnis

Mit einer Gesamtinvestition von rund **100 €** entstand aus einem Alienware m17x (2008) eine stabile Linux-DJ-Maschine für den produktiven Einsatz.

Erreicht wurden:

- stabile Linux-Plattform
- moderne Audio-Infrastruktur
- geringe Systemlast
- kurze Bootzeit
- stabiler Langzeitbetrieb
- hervorragende Audioqualität
- nachhaltige Weiterverwendung hochwertiger Hardware

---

## Projektphilosophie

Dieses Projekt zeigt, dass hochwertige Hardware auch nach vielen Jahren sinnvoll weiter genutzt werden kann.

Der Fokus lag nicht auf maximaler Rechenleistung, sondern auf Stabilität, Reparierbarkeit und nachhaltiger Nutzung.

Aus einem Alienware m17x (2008) entstand Schritt für Schritt eine stabile Linux-DJ-Maschine für den produktiven Einsatz.

---

## Die Magie des Projekts

Die eigentliche Magie lag nicht in einem einzelnen Fix.

Sie entstand aus Disziplin, Geduld und den richtigen Intuitionen in Interaktion von Mensch, Soft- und Hardware.

Aus vielen kleinen Beobachtungen, Tests und Erkenntnissen entwickelte sich Schritt für Schritt eine stabile und reproduzierbare Lösung.

---

> **Version 1.0.0 – Stable**

> *Revitalisierung statt ersetzen.*



# Alienware KDE neon DJ machine

## Version 1.0.0 – Stable

> **A refurbishment project based on an Alienware m17x (2008)**
>
> *Revitalize instead of replacing.*

## English Draft

A stable Linux DJ platform based on an Alienware m17x from 2008.

This project documents the modernization and optimization of a 1st-generation Alienware notebook into an extraordinary and stable DJ machine running Linux. The goal was not maximum computing performance, but a solid audio platform with low system load, high reliability, and sustainable upcycling of high-quality hardware.

After completion of all optimizations, the system operates stably, crackle-free, and with excellent audio quality during long-term testing.

## Photos

![Setup Wide Angle](am17_weit.jpg)

The masterpiece in the picture frame is by trootootoo.

![Setup Wide Angle](am17_m.jpg)

---

## Project Goal

The goal of the project was to build a Linux DJ platform that was as lean and stable as possible.

The machine is used exclusively for the following tasks:

* Mixxx DJ software
* Audio output
* Music management
* Maintenance and system updates

An Internet connection is used exclusively for maintenance, updates, and software installation.

Project priorities:

* stability over maximum performance
* low system load over unnecessary functions
* repairability over replacement
* sustainable use of existing hardware

---

## Project Status

**Version 1.0.0 – Stable**

The project goal has been achieved.

The base platform has been fully optimized and successfully tested under long-term conditions.

From this version onward, no fundamental changes will be made to the operating system.

Future work will focus exclusively on:

* functional extensions
* updating individual components
* further development of the documentation

---

## Hardware Upgrade

The modernization was carried out using components that were still available for the Alienware m17x (2008) and could be integrated without extensive modifications.

| Component | Upgrade                   |        Cost |
| --------- | ------------------------- | ----------: |
| SSD       | Samsung 870 EVO 500 GB    | approx. €90 |
| RAM       | Upgrade from 2 GB to 4 GB | approx. €10 |

**Total investment:** approx. **€100**

With these two upgrades, an Alienware m17x (2008) was transformed into a fully operational Linux DJ machine.

---

## Cost Efficiency

This project demonstrates that high-quality hardware can still be put to meaningful use many years later.

### Advantages

* preservation of the first Alienware generation
* investment of only approx. €100
* repair-friendly hardware
* extended service life
* sustainable reuse of existing components

The decision not to purchase a new machine was not a limitation, but a deliberate technical and economic decision.

---

## Chassis and Design

A major factor in preserving the system is the exceptional chassis design of the early Alienware m17x.

Distinctive features:

* magnesium-aluminum chassis
* rubberized **"Stealth Black Soft-Touch"** surface
* matte, low-reflection finish
* grippy tactile feel
* robust construction
* understated, functional appearance

Models with this chassis finish are rare today.

Preserving the system was therefore not only a technical decision, but also an aesthetic one.

---

## Hardware

| Component       | Specification          |
| --------------- | ---------------------- |
| Model           | Alienware m17x (2008)  |
| CPU             | Intel Core 2 Duo P8400 |
| Cores           | 2                      |
| Clock speed     | 2.26 GHz               |
| RAM             | 3.8 GiB                |
| SSD             | Samsung 870 EVO 500 GB |
| GPU             | AMD Mobility Radeon    |
| Graphics memory | 512 MB                 |

## Operating System

| Component         | Version          |
| ----------------- | ---------------- |
| Distribution      | KDE neon         |
| Kernel            | 7.0.0-28-generic |
| Audio system      | PipeWire         |
| Session manager   | WirePlumber      |
| Real-time support | RTKit            |
| DJ software       | Mixxx 2.5.6      |

The system was optimized exclusively for DJ operation.

---

## Kernel

Several Linux kernels were successfully tested during development.

| Kernel               | Status              |
| -------------------- | ------------------- |
| 7.0.0-28-generic     | **Production**      |
| 6.8.0-134-lowlatency | successfully tested |
| 6.17.0-40-generic    | successfully tested |

Production operation uses the **Linux 7.0.0-28-generic** kernel.

After the tests performed, this kernel offered the best combination of stability, compatibility, and audio performance for the intended use case.

---

## System Optimization

The focus of the optimization was stable audio processing with the lowest possible system load.

Optimization goals:

* low background activity
* consistent CPU performance
* stable audio playback
* short boot time
* reproducible system behavior

---

## CPU

### Governor

```bash
performance
```

Result:

* consistent CPU performance
* no CPU peaks during normal operation
* stable audio processing

During the course of the analysis, the CPU proved not to be a limiting factor.

---

## Boot Time

Analysis:

```bash
systemd-analyze
```

| Area      |               Time |
| --------- | -----------------: |
| Kernel    |  approx. 6 seconds |
| Userspace | approx. 18 seconds |
| Total     | approx. 24 seconds |

For a system from 2008, this is a very good result.

---

## RAM

| Area      |           Value |
| --------- | --------------: |
| Total RAM |         3.8 GiB |
| Used      | approx. 1.4 GiB |
| Available | approx. 2.4 GiB |
| Swap      |         8.4 GiB |

No noticeable swap usage occurs during DJ operation.

---

## Disabled Services

### Printing System

Disabled:

```text
cups.service
cups.path
cups-browsed.service
```

Status:

```text
masked
```

Because no printing functionality is required.

### Samba

Disabled:

```text
nmbd.service
samba-ad-dc.service
```

Status:

```text
masked
```

Active:

```text
smbd.service
```

The file-sharing capability remains available for future transfer of music files over the network.

---

## Audio System

Components used:

* PipeWire
* WirePlumber
* RTKit
* ALSA

This combination provides modern Linux audio management with high stability and good compatibility with Mixxx.

---

## Mixxx Startup

Mixxx is started with the following environment parameter:

```bash
PA_ALSA_PLUGHW=1
```

In the KDE Menu Editor, the parameter is entered under **Command-line Arguments**.

This allows Mixxx to open the master audio interface reliably through ALSA without requiring manual entry every time it is started.

---

## Audio Hardware

| Function | Device                               |    Native Sample Rate |
| -------- | ------------------------------------ | --------------------: |
| Master   | USB Audio Device                     |             46.875 Hz |
| Cue      | C-Media USB Soundkarte für Headphone | 44.100 Hz / 48.000 Hz |

Startup parameter:

```bash
PA_ALSA_PLUGHW=1
```

This allows Mixxx to open the master device reliably.

---

## Mixxx

| Area      | Setting               |
| --------- | --------------------- |
| Version   | 2.5.6                 |
| Audio API | ALSA                  |
| Decks     | 4                     |
| Master    | USB Audio Device      |
| Cue       | C-Media USB Headphone |

Result:

* stable four-deck operation
* stable master output
* stable headphone cueing
* very low CPU utilization
* error-free individual operation of both USB audio interfaces

---

## Analysis

During development, the following areas were systematically investigated:

* CPU performance
* RAM
* Linux kernel
* PipeWire
* WirePlumber
* ALSA
* Mixxx
* different USB sample rates

CPU, kernel, RAM, and overall system performance could be ruled out as the primary cause of the original audio problems.

## Long-Term Test

After completion of all optimizations, the system was tested over an extended period under real-world operating conditions.

Configuration:

| Device                | Volume |
| --------------------- | -----: |
| USB Audio Device      |    90% |
| C-Media USB Headphone |    90% |

Result:

* stable four-deck operation
* simultaneous operation of both USB audio interfaces
* stable master output
* stable headphone cueing
* no CPU peaks
* no audio crackling
* no dropouts
* excellent sound quality

---

## Technical Findings

Development proceeded through several consecutive phases of analysis and testing.

The following areas were investigated, among others:

* CPU performance
* RAM
* Linux kernel
* audio stack
* Mixxx
* USB audio interfaces
* different native sample rates

Several working hypotheses were ruled out or adjusted during the course of the investigation.

The achieved stability did not result from a single change, but from the interaction of all optimizations that were implemented.

### Device Levels

During troubleshooting, the device levels of both USB audio interfaces were temporarily reduced to 50%.

After further long-term testing, both devices could be operated permanently at **90%** without CPU peaks or audio crackling recurring.

The temporary reduction of the device levels therefore proved to be a valuable intermediate step in the analysis, but not a necessary operating setting.

---

## Project Result

With a total investment of around **€100**, an Alienware m17x (2008) was transformed into a stable Linux DJ machine for productive use.

Achieved:

* stable Linux platform
* modern audio infrastructure
* low system load
* short boot time
* stable long-term operation
* excellent audio quality
* sustainable continued use of high-quality hardware

---

## Project Philosophy

This project demonstrates that high-quality hardware can still be put to meaningful use many years later.

The focus was not on maximum computing performance, but on stability, repairability, and sustainable use.

Step by step, an Alienware m17x (2008) was transformed into a stable Linux DJ machine for productive use.

---

## The Magic of the Project

The real magic was not in a single fix.

It emerged from discipline, patience, and the right intuitions in the interaction between human, software, and hardware.

From many small observations, tests, and insights, a stable and reproducible solution emerged step by step.

---

> **Version 1.0.0 – Stable**

> *Revitalization instead of replacement.*

