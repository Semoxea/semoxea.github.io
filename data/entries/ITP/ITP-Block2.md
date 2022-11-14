---
layout: page
title: 2 ITP
---

## Projekt Serverraumüberwachung

### Hardware

- schwimmer
- luftfeuchtigkeit
- ds18s20 (temp)
- eingabetaster
- akustisch & lichtanzeige

### Erforderliche Überwachung

- Wassereinbruch
- starker Temperaturanstieg/Feuer
- Temperatur relevanter Geräte
- Zutrittskontrolle
- Interneterreichbarkeit

### Umfeld

- kleiner Serverraum (20m²) mit 6 Serverracks
- Feuerschutztür
- mit "Kältegang"
- vergitterte Fenster (Kellerraum)
- simple Videoüberwachung vorhanden
- kleinere mittelständische Firma
  - Ziel: IT Grundschutz für eine zukünftige Zertifizierung
- Grundversorgung steht bereit (Steckdosen, Kabellage, Switches)

### Personas

- Herr Bambus
- 34 Jahre
- verheiratet
- Abitur
- Systemadministrator
- 60.285€
- Administriert die gegebene Hardware und führt Wartungen/Instandhaltung durch
- Aufrüstung veralteter HW gewünscht, Neue HW zu teuer
- Umfeld in der Werkstatt des Rechenzentrums ist eher spärlich eingerichtet, keine passenden Schraubendreher, defekte Akkuschrauber
- wird ständig für falsche/unnötige Wartungsalarme gerufen, wünscht sich Sensordaten für genauere Informationen über Raum & Geräte vom Arbeitsplatz aus

---

- Frau Bambusbjörn
- 54 Jahre
- ledig
- mittlere Reife
- Systemraumüberwachung
- 51.104€
- Überwacht zurzeit Systeme semi-manuell (Kameraraum), hat aber auch andere Verantwortlichkeiten (z.B. Lobby)
- kritische Alarme sollen zukünftig direkt an Herrn Bambus geleitet werden um Falschmeldungen zu reduzieren

### Stakeholder

- Geschäftsleitung
- Mitarbeiter der Technik, der Netzwerktechnik under der Sicherheit
- Unbefugte

### Backlog

- Sensoren Anbinden
- Datenverarbeitung
  - Transfer in Datenbank 
- Visuelle Aufbereitung
- Alarme steuern
- Strom-überwachung
  - Stromausfall  
