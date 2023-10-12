---
title: Von BIOS bis OS
layout: default
# permalink: bios_os
toc: true
---


<!-- TOC -->

- [Betriebssysteme](#betriebssysteme)
  - [Definition](#definition)
  - [Komponenten](#komponenten)
    - [Kernel](#kernel)
    - [Systembibliotheken und APIs](#systembibliotheken-und-apis)
  - [Arten](#arten)
    - [Microsoft Windows](#microsoft-windows)
    - [Unix](#unix)
    - [Linux](#linux)

<!-- /TOC -->

## Betriebssysteme

### Definition

Ein Betriebssystem (OS, von englisch Operating System) dient als Schnittstelle zwischen Computerhardware und dem Computerbenutzer. Es bietet eine Reihe von Diensten und Funktionen, die für die effiziente, sichere und benutzerfreundliche Ausführung von Hardware und Software erforderlich sind.
Es verwaltet die Systemressourcen und stellt diese in Anwendungsprogrammen zur Verfügung

### Komponenten

#### Kernel

Der Kernel ist das Herzstück des Betriebssystems und läuft im privilegierten Modus/. Er ist verantwortlich für die direkte Interaktion mit der Hardware und bietet grundlegende Dienste für alle anderen Teile des Systems. Die Hauptaufgaben des Kernels umfassen:

- Prozessverwaltung: Erzeugung, Beendigung und Scheduling von Prozessen
- Speicherverwaltung: Verwaltung des physischen und virtuellen Speichers
- Dateisystem: Verwaltung der Dateien und Verzeichnisse
- Gerätetreiber: Interaktion mit Hardwarekomponenten wie CPU, Speicher, Festplatten, Netzwerkkarten usw.
- Netzwerk: Protokollstacks und Netzwerkschnittstellen
- Interprozesskommunikation (IPC): Mechanismen, um die Kommunikation zwischen den laufenden Prozessen zu ermöglichen

#### Systembibliotheken und APIs

Systembibliotheken bieten eine Reihe von Funktionen und Diensten, die die Interaktion mit dem Kernel vereinfachen. Diese Bibliotheken stellen eine Anwendungsprogrammierschnittstelle (API) zur Verfügung, die von Anwendungsprogrammen verwendet wird, um auf die Dienste des Kernels zuzugreifen.

### Arten

#### Microsoft Windows

- closed-source
- kostenpflichtig

#### Unix

- closed-source
- kostenpflichtig
- wird meist für Server/Enterprise-Umgebungen verwendet
- z.B. z/OS (IBM Großrechner), macOS, OracleLinux

#### Linux

- open-source
- kostenlos
- findet meist privat Anwendung
- z.B. Ubuntu, Debian, Android
