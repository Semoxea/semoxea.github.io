---
layout: page
title: 1 ITS-M-P
---

## Routerkonfiguration

- PC1 (Clientwoman) in 192.168.0.xxx
- PC2 (KK) in 192.168.10.xxx
- PC3 (LF) in 192.168.20.xxx
- Router: R001 Router 6 Box

### Initialkonfiguration

- Router anschließen (Strom, PCs per Ethernet, Internetanschluss an Port 5) und einschalten
- TeraTerm starten, Einstellungen öffnen -> Serieller Port -> Baud Rate 115200
- Einloggen mit admin admin
- Switchen auf Webkonsole (-> Standard IP-Adresse des Routers ist 192.168.0.254)
- Einloggen mit admin admin
- admin PW ändern (z.B. Admin12345)
- Physical Interfaces -> Schnittstellen festlegen
- LAN -> IP Configuration -> Schnittstellen bearbeiten -> Statische IP für Router in diesem Netz festlegen (254), trusted setzen

### DHCP

- neuen IP-Pool anlegen (Netz aus dem die Adressen zugewiesen werden dürfen, ohne Netzadresse und Routeradresse (1-253))
- unter DHCP-Konfiguration der gewünschten Schnittstelle einen IP-Pool zuweisen (neu anlegen wenn notwendig)
- für alle PCs einen IP-Pool anlegen und DHCP konfigurieren
- Externe Schnittstelle (en1-4) auf DHCP einstellen (LAN -> IP-Konfiguration -> en1-4 -> Addressmodus DHCP)

### SNMP

- Simple Network Management Protocol
