# 🛡️ Stufe 3: Quick Start – Werbung & Tracking netzweit blocken

[⬅️ Zurück zur Übersicht](../README.md)

Stufe 3 ist das „Sorglos-Paket“ für 90% aller Anwender. Wir kombinieren die Verschlüsselung aus Stufe 2 mit mächtigen, serverseitigen Werbe- und Trackingfiltern.

> [!TIP]
> **Die Metapher:** Stell dir Stufe 3 wie einen **bewachten Wohnpark mit Pförtner** vor. Der Pförtner (DNS-Server) kennt nicht nur die Adresse, sondern lässt bekannte „Hausierer“ (Werbeserver) und „Stalker“ (Tracker) gar nicht erst durch das Tor in dein Heimnetz.

---

## Die besten Anbieter für die FritzBox

| Anbieter | Herkunft | DoT-Hostname | Besonderheit | Finanzierung & Quellcode |
| :--- | :---: | :--- | :--- | :--- |
| **Mullvad (Ads)** | ![SE](https://flagcdn.com/w20/se.png) | `adblock.dns.mullvad.net` | Extrem schnell, Fokus Privacy | Abo-Modell (VPN), Open Source |
| **dnsforge.de** | ![DE](https://flagcdn.com/w20/de.png) | `dnsforge.de` | Non-Profit, keine Logs | Spenden, Open Source |
| **AdGuard DNS** | ![CY](https://flagcdn.com/w20/cy.png) | `dns.adguard-dns.com` | Sehr aggressive Filter | Freemium, Teilweise OS |
| **CleanBrowsing** | ![US](https://flagcdn.com/w20/us.png) | `family-filter-dns.cleanbrowsing.org` | Fokus Jugendschutz | Paid (Business), Closed Source |

---

## Anleitung: So richtest du es ein

Die Einrichtung erfolgt zentral in deiner Fritz!Box und gilt sofort für alle Geräte im WLAN und LAN.

1. Logge dich in deine FritzBox ein (`http://fritz.box`).
2. Navigiere zu **Internet** -> **Zugangsdaten** -> **DNS-Server**.
3. Aktiviere den Haken bei **DNS über TLS (DoT) aktiv**.
4. Unter **Auflösungsnamen der zu verwendenden DNS-Server** trägst du die Hostnamen ein (einer pro Zeile).
   
   **WICHTIG:** Trage nur den Hostnamen ein (z.B. `dnsforge.de`), keine IP-Adressen und kein `:853`.
   
5. Haken setzen bei: „Zertifikatsprüfung für verschlüsselte Abfrage im DNS (DoT) erzwingen“.
6. Klicke auf **Übernehmen**.

---

## Woher weiß ich, dass es klappt?

Besuche die folgenden Testseiten. Wenn dort Werbung blockiert wird, ist dein Setup aktiv:

- **[d3ward Adblock Test](https://d3ward.github.io/toolz/adblock.html):** Zielwert > 90% für ein perfektes Setup.
- **[AdGuard Testseite](https://adguard.com/de/adblock-tester/test.html):** Prüft die Filterwirksamkeit direkt im Browser.

---

<p align="center">
  <a href="00-vanilla-dns.md">Stufe 0</a> | <a href="01-alternative-dns.md">Stufe 1</a> | <a href="02-dns-verschluesselt.md">Stufe 2</a> | Stufe 3 | <a href="04-cloud-adblocker.md">Stufe 4</a> | <a href="05-selfhosting.md">Stufe 5</a> | <a href="06-testing.md">Stufe 6</a> | <a href="07-sources.md">Stufe 7</a>
</p>
<p align="center">
  <a href="../README.md">🏠 Zurück zur Übersicht</a>
</p>
