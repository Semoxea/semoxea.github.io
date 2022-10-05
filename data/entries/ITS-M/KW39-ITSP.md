---
layout: page
title: ITS-M-P Block 1
---

## Routerkonfiguration

- PC1 (Clientwoman) in 192.168.0.xxx
- PC2 (KK) in 192.168.10.xxx

### Initialkonfiguration

- Router anschließen (Strom, PCs per Ethernet, Internetanschluss an Port 5) und einschalten
- TeraTerm starten, Einstellungen öffnen -> Serieller Port -> Baud Rate 115200
- Einloggen mit admin admin
- Switchen auf Webkonsole (-> Standard IP-Adresse des Routers ist 192.168.0.254)
- Einloggen mit admin admin
- admin PW ändern (z.B. Admin12345)

### DHCP

- neuen IP-Pool anlegen (Netz aus dem die Adressen zugewiesen werden dürfen)
- unter DHCP-Konfiguration der Schnittstelle einen IP-Pool zuweisen
- Externe Schnittstelle (en1-4) auf DHCP einstellen (LAN -> IP-Konfiguration -> en1-4 -> Addressmodus DHCP)
