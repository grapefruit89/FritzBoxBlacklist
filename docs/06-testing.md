# 🧪 Stufe 6: Setup testen

Dein Setup steht? Hervorragend. Jetzt müssen wir sicherstellen, dass dein neuer „Pförtner“ auch wirklich seine Arbeit macht. Ein Werbeblocker, der nichts blockt, ist nur Ballast.

> [!TIP]
> **Die Metapher:** Das ist wie die **Abnahme beim TÜV**. Wir prüfen Bremsen, Licht und Abgase, um sicherzugehen, dass dein Heimnetz-Auto sicher auf der digitalen Autobahn unterwegs ist.

---

## 📊 Die Test-Werkzeuge im Vergleich

Nutze diese Tools nacheinander, um ein vollständiges Bild zu erhalten.

| Tool | Schwerpunkt | Zielwert / Fokus |
| :--- | :--- | :--- |
| [**d3ward Adblock Test**](https://d3ward.github.io/toolz/adblock.html) | DNS-Filter & Browser-Blocker | **Ziel: > 90 %** (Schnelltest) |
| [**Can You Block It?**](https://canyoublockit.com/) | Extreme Werbeformate | Prüft Popups & Video-Ads |
| [**Cover Your Tracks (EFF)**](https://coveryourtracks.eff.org/) | Tracking & Fingerprinting | Schützt mein Browser meine Identität? |
| [**DNS Leak Test**](https://www.dnsleaktest.com/) | DNS-Leakage | Erscheint mein Provider? (Soll: Nein) |
| [**Tenta DNS Test**](https://tenta.com/test/) | DNS-Verschlüsselung | Ist DoT/DoH wirklich aktiv? |

---

## 🛠️ Manueller Check via Kommandozeile

Für die Profis: So prüfst du direkt im Terminal, welcher Server antwortet.

### Windows (CMD / PowerShell)
```powershell
nslookup google.de
```
*   **Ergebnis:** Unter „Server“ sollte die IP deiner Fritz!Box (`192.168.178.1`) oder deines eigenen DNS-Servers stehen.

### Mac / Linux / Android (Termux)
```bash
dig google.de
```
*   **Ergebnis:** Suche nach `SERVER: 192.168.178.1#53`. Steht dort eine fremde IP? Dann umgeht ein Gerät deinen Filter.

---

## 🚨 Was tun, wenn der Test fehlschlägt?

1.  **Cache leeren:** Dein Browser merkt sich DNS-Einträge. Starte den Browser neu oder leere den DNS-Cache (`ipconfig /flushdns` unter Windows).
2.  **IPv6 prüfen:** Oft ist IPv4 sicher, aber Anfragen „schlüpfen“ über IPv6 am Filter vorbei. Deaktiviere IPv6 testweise oder konfiguriere es ebenfalls.
3.  **Hardcoded DNS:** Manche Apps (z. B. YouTube, Netflix) nutzen eigene DNS-Server. Hier hilft nur ein [Pförtner auf Stufe 5](05-selfhosting.md), der diese Anfragen abfängt.

---
<p align="center">
  <a href="00-vanilla-dns.md">🍦 Stufe 0</a> | <a href="01-alternative-dns.md">⚡ Stufe 1</a> | <a href="02-dns-verschluesselt.md">💊 Stufe 2</a> | <a href="03-dns-verschluesselt-adblock.md">🛡️ Stufe 3</a> | <a href="04-cloud-adblocker.md">☁️ Stufe 4</a> | <a href="05-selfhosting.md">🏠 Stufe 5</a> | 🧪 Stufe 6 | <a href="07-sources.md">📚 Stufe 7</a>
</p>
<p align="center">
  <a href="../README.md">🏠 Zurück zur Übersicht</a>
</p>
