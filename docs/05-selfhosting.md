# 🏠 Stufe 5: Self-Hosting (AdGuard Home & Pi-hole)

[⬅️ Zurück zur Übersicht](../README.md)

Die Königsdisziplin. Hier holst du dir die volle Souveränität zurück. Deine DNS-Anfragen verlassen dein Haus nicht mehr unkontrolliert, und du bist nicht mehr auf das Wohlwollen von Cloud-Anbietern angewiesen.

> [!TIP]
> **Die Metapher:** Das ist der **eigene Pförtner an deiner Grundstücksgrenze**. Er gehört dir, er wohnt bei dir, und er fragt niemanden um Erlaubnis. Er kennt jeden im Haus und weiß genau, wer rein darf und wer draußen bleiben muss.

## Die Platzhirsche im Vergleich

| System | Metapher | Stärken | DoT/DoH nativ | Zielgruppe |
| :--- | :--- | :--- | :---: | :--- |
| [**AdGuard Home**](https://adguard.com/adguard-home.html) | Der moderne Allrounder | All-in-One, schickes UI | ✅ Ja | Einsteiger & Komfort-Suchende |
| [**Pi-hole**](https://pi-hole.net/) | Der robuste Veteran | Riesige Community, sparsam | ❌ (via Plugin) | Bastler & Puristen |

---

## Hardware-Optionen

*   **Der Klassiker:** Ein **Raspberry Pi** (schon ein alter Pi 3 oder ein günstiger Pi Zero reichen völlig aus).
*   **Der Server-Weg:** Als **Docker-Container** auf einem NAS (Synology, QNAP, Unraid).
*   **Upcycling:** Ein alter Laptop oder ein ausrangierter Thin Client (z. B. Futro, Wyse).

---

## Integration in die Fritz!Box (Der wichtigste Schritt)

Es gibt zwei Wege, deinen eigenen Pförtner einzubinden. **Weg B ist der empfohlene Weg.**

### Weg A: Als Upstream-Server (Global)
Die Fritz!Box fragt bei jeder externen Anfrage deinen Server.
*   **Nachteil:** In den Statistiken deines Servers siehst du nur die IP der Fritz!Box, nicht das einzelne Endgerät.

### Weg B: Per DHCP-Option (Empfohlen)
Die Fritz!Box sagt jedem Gerät im Netz: "Frag direkt meinen Pförtner unter der IP `192.168.178.X`".
1. Gehe zu **Heimnetz -> Netzwerk -> Netzwerkeinstellungen**.
2. Klicke auf **IPv4-Einstellungen** (oder IPv6).
3. Trage die lokale IP deines Servers bei **Lokaler DNS-Server** ein.
*   **Vorteil:** Du siehst in deinem Dashboard exakt, welches Gerät (Handy, TV, Laptop) gerade welche Anfragen stellt.

---
<p align="center">
  <a href="00-vanilla-dns.md">Stufe 0</a> | <a href="01-alternative-dns.md">Stufe 1</a> | <a href="02-dns-verschluesselt.md">Stufe 2</a> | <a href="03-dns-verschluesselt-adblock.md">Stufe 3</a> | <a href="04-cloud-adblocker.md">Stufe 4</a> | Stufe 5 | <a href="06-testing.md">Stufe 6</a> | <a href="07-sources.md">Stufe 7</a>
</p>
<p align="center">
  <a href="../README.md">🏠 Zurück zur Übersicht</a>
</p>
