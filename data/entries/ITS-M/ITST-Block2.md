---
layout: page
title: 2 ITS-M-T
---

## VPN

### VPN und VDI

- VDI: Virtual Desktop Infrastructure - Virtuelle Desktops, welche über ein Rechenzentrum zur Verfügung gestellt werden
- DaaS: Desktop as a Service - Bereitstellung eines Virtuellen Desktops über eine Cloud-Infrastruktur

|VPN|VDI|
|--|--|
|Datenverarbeitung auf Client-Maschine|Datenverarbeitung auf Virtual Desktop|
|Benötigt hohe Bandbreite|-|
|Daten werden lokal gespeichert|Daten liegen auf VD im RZ|
|Zugriff auf Anwendungen nur bei Kompatibilität mit Client-Betriebssystem|Zugriff auf Anwendungen auch von anderen Betriebssystemen aus möglich|
|Ver-/Entschlüsselung auf Netzwerkebene (Entschlüsselung bereits bei den Routern)|hohe Datensicherheit (erst auf Layer 7 des Anwenders entschlüsselt|
|relativ billig (Software auf Routern aktivieren/installieren)|teurer, zusätzliche Hard- unf Software|
||mehr Konfigurationsaufwand|

### AH und ESP

- AH: Authentication Header
- ESP: Encapsulating Security Payload
- AH authentifiziert IP-Pakete, verschlüsselt aber nicht
- ESP verschlüsselt IP-Pakete zusätzlich
- Im Tansportmodus werden die Daten eines IP-Pakets verschlüsselt
- Im Tunnelmodus wird das gesamte IP-Paket verschlüsselt (Header ausgetauscht)

[Hedgedoc](https://ip-generation.de/F2ThXrIGQJOopuFqHNrjkw)
