# Alienware m17x (2008) als verblüffende Linux DJ-Maschine

## Projektziel

Dieses Projekt dokumentiert den Umbau und die Optimierung eines 1.GENERATION Alienware m17x aus dem Jahr 2008 zu einer extraordinären Linux-basierten DJ-Maschine. Einer der Hauptgründe für die weitere Benutzung der Maschine ist sein subtileres, unterkühlteres Äußeres mit einer gummierter „Stealth Black Soft-Touch“-Oberfläche, in die wir uns verliebt haben.

Der Schwerpunkt liegt auf:

- Wiederverwendung sehr guter Hardware
- Open-Source-Software
- Linux Audio
- Mixxx DJ Software
- PipeWire / ALSA Optimierung
- Low-Latency-Audio

---

# Hardware

## Notebook

- Modell: Alienware m17x (2008)
- CPU: Intel Core 2 Duo P8400 @ 2.26 GHz
- CPU-Kerne: 2
- Arbeitsspeicher: 3.6 GiB RAM (aufgerüstet)
- SSD: Samsung 870 EVO 500 GB (aufgerüstet)
- GPU: AMD Mobility Radeon (512 MiB)

---

# Betriebssystem

## Linux

Distribution:

- KDE Neon

Kernel aktuell: 7.0.0-28-generic

Installierter Low-Latency-Kernel: 6.8.0-134-lowlatency


---

# DJ-Software

## Mixxx

Version: Mixxx 2.4

Verwendung:

- Master-Ausgabe über USB Audio Device
- Kopfhörer-Vorhören über Mini USB Soundkarte

---

# Audio-Hardware

## Geräte

### Master-Ausgang

USB Audio Device

ALSA-Erkennung: USB Audio Device at usb-0000:00:1d.0-2

Eigenschaften: Format:
S16_LE
Channels: 2
Rates: 46875
Bits: 16

---

### Kopfhörer

C-Media Mini USB Soundkarte

---

# Problem

Mixxx erkannte das USB Audio Device unter ALSA: hw:1,0


Beim Öffnen trat folgende Fehlermeldung auf: Invalid sample rate

Ursache:

Das USB-Gerät unterstützt nur: 46875 Hz

und nicht die üblichen Standardraten: 44100 Hz, 48000 Hz

## Meine Setup Fotos

![Setup Weitwinkel](am17_weit.jpg)

Das Masterpice im Bilderrahmen ist von trootootoo <a href="https://www.facebook.com/andytrootootoo" target="_blank" rel="noopener noreferrer">Folge uns auf Facebook</a>   

![Setup Weitwinkel](am17_m.jpg) 

---

# Analyse

Überprüfung mit:

```bash
cat /proc/asound/card1/stream0

Ergebnis:
Rates: 46875
Direkter ALSA-Zugriff: hw:CARD=Device,DEV=0
funktionierte nicht zuverlässig.

 Lösung

Die ALSA-plughw-Konvertierung aktivieren: export PA_ALSA_PLUGHW=1
Danach starten: mixxx
Ergebnis:

Master-Ausgabe funktioniert
Kopfhörer-Vorhören funktioniert
Mixxx 2.4 läuft stabil

KDE Menü Starter

Damit Mixxx automatisch mit der richtigen Umgebung startet:
bash -c "export PA_ALSA_PLUGHW=1; mixxx"

Weitere geplante Optimierungen:
Low-Latency-Kernel testen
KDE Dienste analysieren
RAM-Verbrauch reduzieren
PipeWire Latenz untersuchen
Bootzeit optimieren

Status

Aktuell:

✅ KDE Neon läuft
✅ Mixxx 2.4 läuft
✅ USB Master Output funktioniert
✅ Kopfhörer-Monitoring funktioniert
✅ 1.GENERATION Hardware erfolgreich wiederverwendet

Projektstatus:
Work in Progress


---


technischen Daten des Alienware:

Software:

KDE neon User Edition
KDE-Plasma-Version: 6.7.3
KDE-Frameworks-Version: 6.28.0
Qt-Version: 6.11.1
Kernel-Version: 7.0.0-28-generic (64-bit)
Grafik-Plattform: Wayland

Hardware:

Prozessoren: 2 × Intel® Core™2 Duo CPU     P8400  @ 2.26GHz
Arbeitsspeicher: 4 GiB (3,8 GiB nutzbar)
Grafikprozessor: AMD RV670
Hersteller: alienware - nicht DELL!
Produktname: Alienware M17 (Ripley-Design)
Systemversion: W841.B10

das Leben ist lustig




