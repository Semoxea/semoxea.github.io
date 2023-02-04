---
layout: page
title: 1 ITS-B-P
---

## Firewall

### Routerkonfiguration

||Action|Source|Destination|Service(Port)|
|--|--|--|--|--|
|1|accept|LAN|WAN|443|
|2|accept|LAN|WAN|80|
|3|accept|LAN local|WAN|53|
|4|deny|Any|Any|21|
|5|accept|192.168.0.100 /24|LAN|23|
|6|reject|Any|Any|21|
|7|accept|LAN|LAN|all|
|8|accept|LAN|LAN local|53|
|10|deny|Any|Any|all|
<!--|8|accept|LAN local|LAN|67|-->

Regel 4 braucht man aufgrund der default-Regel 10 nicht extra, da alle Verbindungen standardmäßig verboten werden
