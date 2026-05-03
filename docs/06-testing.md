# 🧪 Stufe 6: Setup testen & validieren

> **Der TÜV für dein Heimnetz**
> Nachdem du dein DNS-Setup optimiert hast, muss es sich im Praxistest beweisen. Werden Tracker blockiert? Bleiben deine DNS-Abfragen privat?

## Die besten Test-Tools

| Tool | Beschreibung |
| :--- | :--- |
| [d3ward Adblock Test](https://d3ward.github.io/toolz/adblock.html) | **Quick-Check:** Lädt hunderte Tracker. Ziel: **> 90%** |
| [Can You Block It?](https://canyoublockit.com/) | **Extreme Test:** Prüft auch kosmetische Filter & Popups. |
| [AdBlock Tester](https://adblock-tester.com/) | **Detail-Analyse:** Analyse verschiedener Werbeformate. |
| [Cover Your Tracks (EFF)](https://coveryourtracks.eff.org/) | **Privacy Fokus:** Tracking & Fingerprinting Schutz. |
| [DNS Leak Test](https://www.dnsleaktest.com/) | **Leak-Check:** Prüfe, ob dein ISP-Name erscheint. |

## Manueller Check via Kommandozeile

Um sicherzugehen, dass dein DNS-Server Werbedomains tatsächlich ins Leere laufen lässt, kannst du einen manuellen Abgleich machen. Öffne ein Terminal (PowerShell oder CMD) und frage eine bekannte Werbedomain ab:

```bash
nslookup doubleclick.net
```

### So interpretierst du das Ergebnis:

*   **✅ Erfolg (Blockiert):** Das Ergebnis zeigt als Adresse `0.0.0.0` oder `127.0.0.1` (oder die IP deines lokalen Blockers). Das bedeutet, die Anfrage wurde abgefangen.
*   **❌ Fehlgeschlagen (Aktiv):** Du siehst eine oder mehrere "echte" IP-Adressen von Google/Doubleclick. Dein Filter greift für diesen Client aktuell nicht.

---
<p align="center">
  <a href="00-vanilla-dns.md">Stufe 0</a> | <a href="01-alternative-dns.md">Stufe 1</a> | <a href="02-dns-verschluesselt.md">Stufe 2</a> | <a href="03-dns-verschluesselt-adblock.md">Stufe 3</a> | <a href="04-cloud-adblocker.md">Stufe 4</a> | <a href="05-selfhosting.md">Stufe 5</a> | Stufe 6 | <a href="07-sources.md">Stufe 7</a>
</p>
<p align="center">
  <a href="../README.md">🏠 Zurück zur Übersicht</a>
</p>
