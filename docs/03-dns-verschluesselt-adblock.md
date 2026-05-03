# Etappe 3: Quick Start – Werbung & Tracking netzweit blocken

Das ist das "Sorglos-Paket". Wir nutzen verschlüsseltes DNS (DoT) kombiniert mit mächtigen Werbefiltern.

## Die besten Anbieter für die FritzBox

| Anbieter | DoT-Hostname | Besonderheit |
| :--- | :--- | :--- |
| **Mullvad (Ads)** | `adblock.dns.mullvad.net` | Extrem schnell, sehr guter Werbefilter. |
| **dnsforge.de** | `dnsforge.de` | Deutscher Server, sehr privatsphäre-freundlich. |

## Anleitung: So richtest du es ein

1. Logge dich in deine FritzBox ein (`http://fritz.box`).
2. Navigiere zu `Internet` -> `Zugangsdaten` -> `DNS-Server`.
3. Aktiviere den Haken bei **DNS über TLS (DoT) aktiv**.
4. Unter **Auflösungsnamen der zu verwendenden DNS-Server** trägst du die Hostnamen ein (einer pro Zeile).
   
   **WICHTIG:** Trage nur den Hostnamen ein, **keine** IP-Adressen und **keine** Portnummern (kein `:853`).
   
   *Beispiel für dein Feld:*
   ```text
   adblock.dns.mullvad.net
   dnsforge.de
   ```

5. Haken setzen bei: "Zertifikatsprüfung für verschlüsselte Abfrage im DNS (DoT) erzwingen".
6. Klicke auf `Übernehmen`.

## Woher weiß ich, dass es klappt?
Besuche die Seite [d3ward.github.io/toolz/adblock.html](https://d3ward.github.io/toolz/adblock.html). Wenn dort über 90% geblockt werden, ist dein Setup perfekt!

---
<p align="center">
  <a href="02-dns-verschluesselt.md">⬅️ Zurück</a> | <a href="../README.md">🏠 Übersicht</a> | <a href="04-cloud-adblocker.md">Weiter ➡️</a>
</p>
