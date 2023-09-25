---
layout: page
title: IT-Sicherheit Praxis
---
- [VMs](#vms)
  - [Routerkonfiguration](#routerkonfiguration)
  - [Initialkonfiguration](#initialkonfiguration)
  - [DHCP](#dhcp)
  - [SNMP](#snmp)
- [Firewall](#firewall)
  - [Access List Test 1](#access-list-test-1)
  - [Access List DMZ](#access-list-dmz)
  - [Troubleshooting](#troubleshooting)

---

## VMs

### Routerkonfiguration

- PC1 (Clientwoman) in 192.168.0.xxx
- PC2 (KK) in 192.168.10.xxx
- PC3 (LF) in 192.168.20.xxx
- Router: R001 Router 6 Box

### Initialkonfiguration

- Router anschließen (Strom, PCs per Ethernet, Internetanschluss an Port 5) und einschalten
- TeraTerm starten, Einstellungen öffnen -> Serieller Port -> Speed 115200
- Einloggen mit admin admin
- Switchen auf Webkonsole (-> Standard IP-Adresse des Routers ist 192.168.0.254)
- Einloggen mit admin admin
- admin PW ändern (z.B. Admin12345)
- NAT für Schnittstelle en1_4 aktivieren
- LAN -> IP Configuration -> en1_4 Address Mode DHCP (automatische Zuweisung der Router-IP & DNS-Adressmitteilung)
- IP Pools für die Schnittstellen definieren
- DHCP für Schnittstellen aktivieren
- 
- Firewall -> Schnittstellen -> Gruppierungen können angelegt werden für Schnittstellen
- Firewall -> Richtlinien -> Aktivieren
  
<!-- 
- Physical Interfaces -> Schnittstellen festlegen 
- LAN -> IP Configuration -> Schnittstellen bearbeiten -> Statische IP für Router in diesem Netz festlegen (254), trusted setzen
-->

### DHCP

- neuen IP-Pool anlegen (Netz aus dem die Adressen zugewiesen werden dürfen, ohne Netzadresse und Routeradresse (1-253))
- unter DHCP-Konfiguration der gewünschten Schnittstelle einen IP-Pool zuweisen (neu anlegen wenn notwendig)
- für alle PCs einen IP-Pool anlegen und DHCP konfigurieren
- Externe Schnittstelle (en1-4) auf DHCP einstellen (LAN -> IP-Konfiguration -> en1-4 -> Addressmodus DHCP)

### SNMP

- Simple Network Management Protocol

---

## Firewall

### Access List Test 1

||Action|Source|Destination|Service(Port)|
|--|--|--|--|--|
|1|accept|LAN|WAN|443|
|2|accept|LAN|WAN|80|
|3|accept|LAN local|WAN|53|
|4|reject|Any|Any|23|
|5|accept|LAN|LAN local|53|
|6|accept|192.168.0.100/32|LAN|23|
|7|deny|Any|Any|all|
<!--8|accept|LAN local|LAN|67-->

FTP-Regel für Deny braucht man aufgrund der default-Regel 10 nicht extra, da alle Verbindungen standardmäßig verboten werden.
Accept auf LAN zu LAN nicht notwendig, wenn keine VLANs konfiguriert sind -> Kommunikation über Switches, nicht über Router

### Access List DMZ



### Troubleshooting

Mit Firewall vom Webinterface ausgeschlossen?

-> TeraTerm -> Firewall -> Adminstatus = disabled
