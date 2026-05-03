# Stufe 5: Self-Hosting (AdGuard Home & Pi-hole)

Für maximale Privatsphäre und absolute Kontrolle kannst du deinen eigenen DNS-Server in deinem Heimnetz betreiben. Hier verlassen deine DNS-Anfragen (sofern gewünscht) nie wirklich deine Kontrolle, und du bist nicht von Drittanbietern abhängig.

## Die Klassiker im Vergleich

### [AdGuard Home](https://adguard.com/adguard-home.html)
AdGuard Home ist die modernere Lösung. Es ist eine All-in-One-Binärdatei, die extrem einfach zu installieren ist und DoT/DoH nativ unterstützt.
*   **Vorteile:** Modernes Web-Interface, integrierte Unterstützung für verschlüsseltes DNS, einfache Handhabung von Client-spezifischen Regeln.
*   **Empfehlung:** Ideal für Einsteiger und Nutzer, die eine schicke Oberfläche suchen.

### [Pi-hole](https://pi-hole.net/)
Der Urvater der DNS-Adblocker. Pi-hole hat eine riesige Community und läuft auf fast jeder Hardware (besonders beliebt auf dem Raspberry Pi).
*   **Vorteile:** Extrem ressourcensparend, riesiges Ökosystem an Add-ons und Skripten.
*   **Hinweis:** Benötigt für verschlüsseltes DNS (DoT/DoH) oft Zusatzsoftware wie `unbound` oder `cloudflared`.

## Hardware-Optionen
1.  **Raspberry Pi:** Der Standardweg. Ein kleiner Pi Zero oder Pi 3/4/5 reicht völlig aus.
2.  **Docker:** Wenn du bereits ein NAS (Synology, QNAP) oder einen Heimserver hast, ist die Installation als Docker-Container am einfachsten.
3.  **Alte Hardware:** Auch ein alter Laptop oder Thin Client kann problemlos als DNS-Server dienen.

## Wie wird es in die Fritz!Box integriert?
Statt die Upstream-DNS-Server der Fritz!Box zu ändern, trägst du die IP deines Self-Hosted-Servers unter **Heimnetz -> Netzwerk -> Netzwerkeinstellungen -> IPv4-Konfiguration** als lokalen DNS-Server ein. So verteilt die Fritz!Box per DHCP direkt die IP deines Adblockers an alle Geräte im Netzwerk.

---
<p align="center">
  <a href="00-vanilla-dns.md">0</a> | <a href="01-alternative-dns.md">1</a> | <a href="02-dns-verschluesselt.md">2</a> | <a href="03-dns-verschluesselt-adblock.md">3</a> | <a href="04-cloud-adblocker.md">4</a> | **5** | <a href="06-testing.md">6</a> | <a href="07-sources.md">7</a>
</p>
<p align="center">
  <a href="../README.md">🏠 Zurück zur Übersicht</a>
</p>
