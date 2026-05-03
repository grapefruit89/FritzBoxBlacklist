# Etappe 2: DNS verschlüsseln (DoT & DoH)

Normale DNS-Anfragen sind wie Postkarten: Jeder zwischen dir und dem DNS-Server kann sie lesen (dein Provider, dein Arbeitgeber, Hacker im WLAN). Um das zu verhindern, gibt es Verschlüsselung.

## Was ist DoT und DoH?

1.  **DoT (DNS over TLS):** Die DNS-Anfrage wird in einen verschlüsselten Tunnel (TLS) gepackt. Das ist der Goldstandard für Router wie die FritzBox.
2.  **DoH (DNS over HTTPS):** Die Anfrage wird in normalen Web-Traffic (HTTPS) versteckt. Das nutzen vor allem Browser (Chrome/Firefox) intern.

## Warum verschlüsseln?
Selbst wenn du einen privaten DNS-Anbieter nutzt, könnte dein Internetanbieter die unverschlüsselten Anfragen einfach "mitlesen" oder sogar manipulieren. Mit DoT ist damit Schluss.

## Praxis: DoT in der FritzBox aktivieren (Beispiel: Quad9)

Quad9 ist ein hervorragender Anbieter aus der Schweiz, der vor allem bösartige Domains (Malware) blockiert.

1. Gehe in deiner FritzBox auf `Internet` -> `Zugangsdaten` -> `DNS-Server`.
2. Scrolle runter zu **DNS über TLS (DoT)**.
3. Setze den Haken bei "DNS über TLS (DoT) aktiv".
4. Gib unter "Auflösungsnamen der zu verwendenden DNS-Server" folgendes ein:
   `dns.quad9.net`
5. Klicke auf `Übernehmen`.

Ab jetzt stellt deine FritzBox alle DNS-Anfragen verschlüsselt an Quad9.

---
[⬅️ Zurück zur Übersicht](../README.md)
