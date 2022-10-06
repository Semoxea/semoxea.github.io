---
layout: page
title: 1 ITS-GR
---

## Betriebssysteme

### Microsoft Windows vs Linux

![Windows](../images/windows.png)

Microsoft erlaubt keinen direkten Zugriff auf das Betriebssystem Windows. Selbst Admins werden vom Betriebssystem berechtigt, direkter Zugriff existiert nicht.

### Linux Berechtigungen

Beispiel: Datei bla.txt hat die Rechte 754 <br>
Bedeutung:  user darf r, w, x
            group darf r, x
            alle anderen r

### Befehle in Linux

|Beschreibung|Befehl|
|--|--|
|Rechte angeben/ändern|chmod|
|Auflisten der Rechte|ls -l|
|Ändern des Eigentümers|chown|
|Ändern der Gruppe|chgrp|
|Wechseln von Verzeichnissen|cd|

### Befehle in VI

Befehlskontext mit ESC öffnen

|Beschreibung|Befehl|
|--|--|
|:w|speichern|
|:q|verlassen|
|:q!|verlassen erzwingen|
|/...|nach ... suchen|
|dd|Zeile löschen|
|i|insert|

## Skripting in Linux

- Erste Zeile wird "Shebang"-Zeile genannt
- In der Shebang-Zeile wird die zu verwendende Shell angegeben
- #! /bin/bash (für standard-shell)

|Syntax|Bedeutung|
|--|--|
|#!|Shell-Angabe|
|#|Kommentar|
|$xxx|Ansprache der davor definierten Variable xxx|
|+%x|Formatierungsoption des vorangegangenen Befehls mit Parameter x|

- Variablendeklarationen dürfen keine Leerzeichen enthalten (z.B. varname = xxx)
- Variableninitialisierungen mit Leerzeichen (für Parameter für vordefinierte Befehle) müssen mit **\`**    **\`** (Backticks, nicht Quotation Marks) umrahmt werden

---

## Netzwerk

- Im physischen Bereich (MAC-Adressenbasiert) wird zuerst die Ziel-MAC und dann die Quell-MAC angegeben (z.B: im Frame-Header).
- Im logischen Bereich (IP-Adressenbasiert) wird zuerst die Quell-IP und dann die Ziel-IP angegeben.
- Der Portbereich ist festgelegt auf 16 Bit (65536 (0-65535) verfügbare Ports, davon die ersten 1024 well-known Ports)
- Es können 4096 VLANs über die VLAN-Erweiterung im Frame-Header addressiert werden (die ersten zwei Byte sind für den Tag Protocol Identifier (TPID) - Bei VLANs 0x8100, die letzten 12 Bit für VLAN ID (-> max 4096))

### Aufbau eines Frames

![Frameaufbau](../images/frame.png)

### Frame vs Paket vs Segment

|Frame|Paket|Segment|
|--|--|--|
|Dateneinheit des Data Link Layers|Dateneinheit der Netzwerkschicht|Dateneinheit der Transportschicht|
|Layer 2|Layer 3|Layer 4|
|MAC-basiert|IP-basiert||

### TCP-Flags

- Zustandssignal
- Immer 1 Bit groß (Zustand ist an oder aus)
- Für 3-Wege-Handshake (SYN, SYN-ACK, ACK)

### PAT - Port Address Translation

Beispiel: Paket wird von PC 1 in internem Netz an Server 1 in externem Netz geschickt.

- Standardgateway ersetzt bei Paketerhalt die Quell-IP und -Port durch seine externe Schnittstelle und einem neuen Quellport für das Netz von Server 1
- Standardgateway setzt für den neuen Port eine Zuordnung zu PC 1 und dem ursprünglichen Port (Router-interne Liste)
- Bei Antwort wird anhand des Portabgleichs mit der internen Liste das richtige Ziel (PC 1 mit Quell-Port) zugeordnet
- Listeneintrag mit "Ersatzport" wird gelöscht

### NAT - Network Address Translation

- Selber Vorgang wie bei PAT, allerdings kann immer nur eine IP-Addresse ersetzt werden
- Agiert nur auf IP-Addressen-Basis, ohne Ports

---

## Backup

### Vollsicherung

|Vorteile|Nachteile|
|--|--|
|||

### Differentielle Sicherung

Eine Vollsicherung wird als Basis zur differentiellen Sicherung benötigt.

|Vorteile|Nachteile|
|--|--|
|Point-In-Time Recovery ab letzter Vollsicherung|Für Recovery ist Vollsicherung und differentielle Sicherung notwendig|
|weniger Zeitaufwand|Doppelte Datensicherung (Datensatz wurde in dem Zeitraum mehrmals geändert)|

### Inkrementelle Sicherung

Eine Sicherung wird als Basis zur inkrementellen Sicherung benötigt, da immer nur die Änderungen zur letzten Sicherung gesichert werden.

|Vorteile|Nachteile|
|--|--|
|Backup benötigt weniger Speicherplatz|alle inkrementellen Sicherungen werden zur Recovery benötigt|
|sehr schnelle Backuperstellung||

### Archivbit

Das Archivbit (auch Archiv-Attribut) ist ein Dateiattribut, das in Microsoft-Betriebssystemen genutzt wird, um neu angelegte oder veränderte Dateien zu kennzeichnen. Datensicherungsprogrammen kann damit signalisiert werden, dass die Datei noch nicht gesichert bzw. seit der letzten Sicherung modifiziert wurde.
