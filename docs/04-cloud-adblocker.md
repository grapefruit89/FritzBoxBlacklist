# ☁️ Stufe 4: Cloud-DNS mit Profil – Maximale Kontrolle

[⬅️ Zurück zur Übersicht](../README.md)

Wenn dir die festen Filterlisten aus Stufe 3 nicht ausreichen und du volle Kontrolle über dein Netzwerk haben möchtest, ohne eigene Hardware zu betreiben, sind Cloud-Adblocker die perfekte Wahl.

> [!TIP]
> **Die Metapher:** Das ist der **Bodyguard mit Fernbedienung**. Er steht vor deinem Haus, aber du kannst ihm per App jederzeit sagen: „Lass heute niemanden von Facebook rein“ oder „Zeig mir mal die Liste, wer heute alles geklingelt hat“.

> [!WARNING]
> **Jurisdiktion:** Beachte, dass NextDNS (USA) und ControlD (Kanada) der Jurisdiktion der „Five Eyes“ unterliegen. Für maximale Privatsphäre gegenüber staatlichen Akteuren sind europäische Lösungen (Stufe 3 oder 5) vorzuziehen.

---

## Anbieter mit persönlichem Dashboard

Diese Dienste bieten dir ein Web-Interface, in dem du genau sehen kannst, welche Anfragen blockiert wurden, und eigene Regeln erstellen kannst.

| Anbieter | Herkunft | DoT-Hostname | Besonderheit | Finanzierung & Quellcode |
| :--- | :---: | :--- | :--- | :--- |
| [**NextDNS**](https://nextdns.io/) | ![US](https://flagcdn.com/w20/us.png) | `[ID].dns.nextdns.io` | Goldstandard, App-Blocking | Freemium, Closed Source |
| [**AdGuard DNS**](https://adguard-dns.io/) | ![CY](https://flagcdn.com/w20/cy.png) | `[ID].adguard-dns.com` | Sehr familienfreundlich | Freemium, Teilweise OS |
| [**ControlD**](https://controld.com/) | ![CA](https://flagcdn.com/w20/ca.png) | `[ID].controld.com` | Mächtige Geo-Optionen | Paid, Closed Source |

---

## Die Vorteile von Profilen

*   **Granulare App-Sperren:** Sperre Dienste wie TikTok, Roblox oder Tinder mit einem einzigen Klick für das gesamte Netzwerk.
*   **Echtzeit-Statistiken:** Erhalte Einblick in das Datenaufkommen und die Blockierrate deines Netzwerks.
*   **Eigene Whitelists:** Erlaube gezielt Domains, die von Standardfiltern fälschlicherweise blockiert werden.
*   **Kindersicherung:** Erstelle Zeitpläne für den Internetzugriff bestimmter Geräte.

---

## Einrichtung
1. Erstelle ein Konto beim Anbieter deiner Wahl.
2. Konfiguriere deine gewünschten Filterlisten und Optionen im Dashboard.
3. Trage die bereitgestellten DoT-Hostnamen in deiner Fritz!Box ein (wie in [Stufe 3](03-dns-verschluesselt-adblock.md) beschrieben).
4. **WICHTig:** Bei IPv4-Verbindungen ohne DoT musst du ggf. deine IP-Adresse im Dashboard verknüpfen (DDNS). Bei Nutzung von DoT in der Fritz!Box ist dies meist nicht nötig, da das Profil über den Hostnamen identifiziert wird.

---

<p align="center">
  <a href="00-vanilla-dns.md">Stufe 0</a> | <a href="01-alternative-dns.md">Stufe 1</a> | <a href="02-dns-verschluesselt.md">Stufe 2</a> | <a href="03-dns-verschluesselt-adblock.md">Stufe 3</a> | Stufe 4 | <a href="05-selfhosting.md">Stufe 5</a> | <a href="06-testing.md">Stufe 6</a> | <a href="07-sources.md">Stufe 7</a>
</p>
<p align="center">
  <a href="../README.md">🏠 Zurück zur Übersicht</a>
</p>
