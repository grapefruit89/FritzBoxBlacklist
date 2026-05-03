# Fritz!Box: DNS-Grundlagen
[⬅️ Zurück zur Übersicht](../README.md)

Die Fritz!Box ist das Herzstück deines Heimnetzes. Um die DNS-Einstellungen zu ändern, musst du wissen, wo sich die entsprechenden Menüs befinden.

## Wo finde ich die Einstellungen?

### 1. Upstream DNS (Für die ganze Box)
Diese Einstellungen gelten für alle Geräte, die keine eigenen DNS-Server konfiguriert haben.
*   **Pfad:** `Internet` -> `Zugangsdaten` -> `DNS-Server`
*   **Optionen:** Hier kannst du IPv4- und IPv6-Adressen festlegen sowie **DNS over TLS (DoT)** aktivieren.

### 2. Lokaler DNS-Server (DHCP)
Hier sagst du der Fritz!Box, welche DNS-IP sie per DHCP an deine Geräte verteilen soll (wichtig für Pi-hole/AdGuard Home).
*   **Pfad:** `Heimnetz` -> `Netzwerk` -> `Netzwerkeinstellungen` -> Schaltfläche `IPv4-Einstellungen`
*   **Feld:** `Lokaler DNS-Server`

### 3. Kindersicherung (Blacklist)
Dies ist die alte Methode mit dem 500-Einträge-Limit.
*   **Pfad:** `Internet` -> `Filter` -> `Listen` -> `Gesperrte Internetseiten`

## Wichtige Tipps
*   **Erweiterte Ansicht:** Stelle sicher, dass oben rechts in der Fritz!Box-Oberfläche die "Erweiterte Ansicht" aktiviert ist, sonst fehlen einige Menüpunkte.
*   **IPv6 nicht vergessen:** Wenn dein Anschluss IPv6 nutzt (was fast immer der Fall ist), musst du auch dort einen DNS-Server eintragen, sonst erfolgt die Abfrage einfach über den Provider-Standardweg.

---

<p align="center">[⬅️ Stufe 7 (Quellen)](07-sources.md) | [Manuelles Setup ➡️](manual-client-setup.md)</p>

[⬅️ Zurück zur Übersicht](../README.md)
