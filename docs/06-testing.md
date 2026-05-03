# Stufe 6: Setup testen & validieren

Nachdem du dein neues DNS-Setup eingerichtet hast, solltest du prüfen, ob alles wie gewünscht funktioniert. Werden die Werbeserver blockiert? Ist die Verbindung verschlüsselt?

## Die besten Test-Tools

### 1. [d3ward Adblock Test](https://d3ward.github.io/toolz/adblock.html)
Dieser Test lädt eine Vielzahl bekannter Tracker und Werbedomains direkt in deinem Browser.
*   **Ziel:** Ein Wert über 80% ist sehr gut. Über 90% ist exzellent (kann aber zu Overblocking führen).

### 2. [DNS Leak Test](https://www.dnsleaktest.com/)
Prüfe, welcher DNS-Anbieter tatsächlich antwortet.
*   **Erwartung:** Es sollte nur der von dir gewählte Anbieter (z.B. Mullvad, NextDNS, dnsforge) erscheinen. Wenn der Name deines Internetanbieters (ISP) auftaucht, hast du ein "DNS-Leak".

### 3. [1.1.1.1 Help Tool](https://1.1.1.1/help)
Cloudflare bietet ein detailliertes Diagnose-Tool an, das auch für andere Anbieter funktioniert.
*   **Wichtig:** Prüfe die Zeilen "Using DNS over TLS (DoT)" oder "Using DNS over HTTPS (DoH)". Hier sollte "Yes" stehen, wenn du Verschlüsselung aktiviert hast.

### 4. [Check My DNS (Mullvad)](https://mullvad.net/check)
Ein einfacher Check von Mullvad, der dir sofort sagt, ob du deren DNS nutzt und ob Leaks vorhanden sind.

## Manueller Test (Kommandozeile)
Du kannst auch direkt prüfen, ob eine bekannte Werbedomain blockiert wird. Öffne ein Terminal (CMD/PowerShell) und tippe:
`nslookup doubleclick.net`

*   **Blockiert:** Antwortet meist mit `0.0.0.0` oder `127.0.0.1`.
*   **Nicht blockiert:** Zeigt eine echte IP-Adresse an.

---
<p align="center">
  <a href="05-selfhosting.md">⬅️ Zurück</a> | <a href="../README.md">🏠 Übersicht</a> | <a href="07-sources.md">Weiter ➡️</a>
</p>
