# Stufe 4: Cloud-Adblocker (NextDNS & AdGuard DNS)

Wenn dir die einfachen Filterlisten nicht ausreichen und du volle Kontrolle über dein Netzwerk haben möchtest, ohne eigene Hardware zu betreiben, sind Cloud-Adblocker die perfekte Wahl. Diese Dienste bieten dir ein persönliches Dashboard, in dem du genau sehen kannst, welche Anfragen blockiert wurden, und eigene Regeln erstellen kannst.

## Warum Cloud-Adblocker?
*   **Individuelle Filterlisten:** Wähle aus Hunderten von spezialisierten Listen (z.B. für Smarthome, Gaming oder soziale Medien).
*   **Whitelisting:** Erlaube gezielt Domains, die von Standardfiltern blockiert werden.
*   **Statistiken:** Erhalte Einblick in das Datenaufkommen und die Blockierrate deines Netzwerks.
*   **Kindersicherung:** Sperre bestimmte Apps oder Webseiten zeitgesteuert.

## Beliebte Anbieter

### [NextDNS](https://nextdns.io/)
NextDNS gilt als der Goldstandard für Cloud-DNS. Es bietet eine extrem intuitive Benutzeroberfläche und Serverstandorte weltweit (auch in Deutschland).
*   **Vorteil:** Sehr einfach einzurichten, bietet spezialisierte Profile für verschiedene Geräte.
*   **Kosten:** Kostenloses Kontingent (ca. 300.000 Anfragen/Monat), danach kostenpflichtig.

### [AdGuard DNS](https://adguard-dns.io/)
AdGuard ist bekannt für seine starken Werbeblocker-Apps und bietet mit seinem Cloud-DNS eine ebenso solide Lösung an.
*   **Vorteil:** Sehr familienfreundlich, einfache Konfiguration der Kindersicherung.
*   **Besonderheit:** Gute Integration in andere AdGuard-Produkte.

## Einrichtung
1.  Erstelle ein Konto beim Anbieter deiner Wahl.
2.  Konfiguriere deine gewünschten Filterlisten im Dashboard.
3.  Trage die bereitgestellten DoT-Hostnamen in deiner Fritz!Box ein (wie in [Stufe 2](02-dns-verschluesselt.md) beschrieben).
4.  Verknüpfe ggf. deine IP-Adresse im Dashboard (nur bei IPv4 ohne DoT nötig).

---
<p align="center">
  <a href="00-vanilla-dns.md">0</a> | <a href="01-alternative-dns.md">1</a> | <a href="02-dns-verschluesselt.md">2</a> | <a href="03-dns-verschluesselt-adblock.md">3</a> | **4** | <a href="05-selfhosting.md">5</a> | <a href="06-testing.md">6</a> | <a href="07-sources.md">7</a>
</p>
<p align="center">
  <a href="../README.md">🏠 Zurück zur Übersicht</a>
</p>
