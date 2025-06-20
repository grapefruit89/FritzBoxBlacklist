# 🚫 Fritz!Box Blockliste – Werbefrei im Heimnetz

> ✨ Ein minimalistischer Ansatz, um die Top 500 Werbe- und Tracking-Domains mit der Fritz!Box zu blockieren – ganz ohne Informatikstudium.

[![Project Status: Semi-Active](https://img.shields.io/badge/status-semi--active-yellow)](#)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](#lizenz)
[![PRs welcome](https://img.shields.io/badge/contributions-welcome-yellow.svg)](#mitwirken)

---

## 🔍 Projektübersicht

Diese Blockliste ermöglicht es dir, mit deiner Fritz!Box einen effektiven AdBlocker zu betreiben – ohne zusätzliche Hardware oder komplizierte Setups.

Aufgrund der Fritz!Box-Beschränkung auf 500 Einträge wurde eine kompakte und effiziente Liste der meistgeblockten Webseiten erstellt, um maximale Wirkung bei minimalem Aufwand zu erzielen.

> 🧠 _Inspiriert von [fboes/fritzbox-blacklist](https://github.com/fboes/fritzbox-blacklist)_  
> 📚 _Lesetipp: [Fritz!Box als AdBlocker – Blogbeitrag](http://service.avm.de/help/de/FRITZ-Box-Fon-WLAN-7490/014/hilfe_internet_filter_blacklist)_

---

## 🚀 Schnellstart: Filterliste in der Fritz!Box einrichten

1. 📖 Lies die Anleitung: [FritzBox-Kindersicherung einrichten (heise.de)](https://www.heise.de/tipps-tricks/FritzBox-Kindersicherung-so-funktioniert-die-Einrichtung-4048867.html)
2. 📥 Kopiere den Inhalt der aktuellen Blockliste:  
   [🔗 Fritz 500 Blacklist (Stand: 23.11.2020)](https://github.com/grapefruit89/FritzBoxBlacklist/blob/master/Fritz%20500%202020-11-23.txt)
3. 📋 Füge die Domains unter **fritz.box › Internet › Filter › Listen › Gesperrte Webseiten** ein
4. ✅ Fertig! Keine Werbung mehr beim Surfen 🚀

> 💡 Auch weitere Quellen aus dem Abschnitt [Weiterführende Links](#weiterführende-links) sind nutzbar.

---

## 🛜 DNS-Server mit integriertem Werbeblocker

Alternativ oder ergänzend zur Fritz!Box-Blockliste kannst du einen DNS-Dienst mit Werbeblock-Funktion nutzen.

🧾 **Was ist ein DNS?**  
Ein DNS-Server funktioniert wie ein Telefonbuch: Er übersetzt Domainnamen in IP-Adressen. Wenn du einen DNS-Anbieter nutzt, der Werbung herausfiltert, wirst du zu weniger unerwünschtem Inhalt weitergeleitet.

### 🔐 Empfehlenswerte DNS-Provider (nach Filterstärke & Overblocking-Risiko)

| Anbieter | IPv4 | Kategorie 🧠 | Filterstärke 🔥 | Overblocking 🚫 | Beschreibung |
|----------|------|-------------------|------------------|--------------------|----------------|
| [Quad9](https://www.quad9.net/) | `9.9.9.9` | 🟢 Anfänger | 🟢 Niedrig | 🔓 Kein Overblocking | Blockiert nur Malware, DSGVO-konform, hohe Zuverlässigkeit |
| [UncensoredDNS](https://blog.uncensoreddns.org/) | `91.239.100.100` | 🟢 Anfänger | ⚪ Neutral | 🔓 Kein Filter | Zensurfrei, keinerlei Blockierung – ideal mit lokalem Pi-hole |
| [Mullvad DNS](https://mullvad.net/de/help/dns-over-https-and-dns-over-tls/) | `193.138.218.74` | 🟢 Anfänger | 🟡 Mittel | 🔓 Gering | Blockiert Tracker & Malware, keine Werbung, keine Logs |
| [LibreDNS](https://libredns.gr/) | `116.202.176.26` | 🟡 Fortgeschritten | 🟡 Mittel | 🔓 Gering | Werbe-/Malwarefrei, von Privacy-Community betrieben |
| [Dismail (fdns2)](https://dismail.de/) | `159.69.114.157` | 🟡 Fortgeschritten | 🟠 Mittel–Hoch | 🟠 Mäßig | Blockt u. a. `googleadservices`, solide Privat-DNS |
| [DNS.SB](https://dns.sb/) | `185.222.222.222` | 🟡 Fortgeschritten | 🔴 Hoch | 🔴 Mäßig–Hoch | Starke Blockliste, schnell, datenschutzorientiert |
| [pi-dns.com](https://pi-dns.com/) | – | 🔴 Power-User | 🔴 Hoch | 🔴 Hoch | Aggressive Blockierung – manche Webseiten oder Scripte brechen |
| [AH DNS](https://ahadns.com/) | – | 🔴 Power-User | 🔴 Sehr hoch | 🔴 Hoch | Blockiert massiv Werbung, Tracker & Telemetrie |
| [NextDNS](https://nextdns.io/) | – | 🔵 Individuell | 🧩 Konfigurierbar | 💡 Optional | Feingranular konfigurierbar – von „sanft“ bis „radikal“ |
| Weitere Empfehlungen | – | 📚 | – | – | [Kuketz](https://www.kuketz-blog.de/empfehlungsecke/#dns), [AvoidTheHack](https://avoidthehack.com/best-dns-privacy#ataglance) |



---

## 🧪 Tests & Tools

| Funktion | Tool | Link |
|---------|------|------|
| Funktion der Liste prüfen | Adblock-Test | [ads-blocker.com](https://ads-blocker.com/testing/) |
| DNS richtig konfiguriert? | DNS Leak Test | [dnsleaktest.com](https://www.dnsleaktest.com/) |
| DNS Geschwindigkeit | Benchmark | [GRC DNS Benchmark](https://www.grc.com/dns/benchmark.htm) |

🔄 Nutze die erweiterte `DNS Liste.ini`:  
[🔗 DNS Liste.ini](https://github.com/grapefruit89/FritzBoxBlacklist/blob/master/DNS%20Liste.ini)

![DNS Einstellungen](https://github.com/grapefruit89/FritzBoxBlacklist/blob/master/rect875.jpg)  
![DNS Benchmark Ergebnis](https://github.com/grapefruit89/FritzBoxBlacklist/blob/master/servertest.png)

---

## 🔗 Weiterführende Links

### 🧱 Blacklist-Quellen & Projekte

- [Pi-Hole auf Google Cloud](https://github.com/rajannpatel/Pi-Hole-PiVPN-on-Google-Compute-Engine-Free-Tier-with-Full-Tunnel-and-Split-Tunnel-OpenVPN-Configs)
- [The Firebog](https://firebog.net/)
- [StevenBlack/hosts](https://github.com/StevenBlack/hosts)
- [fboes/fritzbox-blacklist](https://github.com/fboes/fritzbox-blacklist)
- [xobit.de Blacklist](https://www.xobit.de/fritzbox-blacklist)

### 📓 Eigene Liste erstellen – Tools

- [Notepad++](https://notepad-plus-plus.org/)
- [Doppelte Zeilen entfernen](https://www.textfixer.de/tools/doppelte-zeilen-entfernen.php)
- [Domain Extractor](https://de.rakko.tools/tools/62/)
- [Top 10 TLDs mit Missbrauch](https://www.spamhaus.org/statistics/tlds/)
- [AM-Deadlink – Linkcheck-Tool](https://www.aignes.com/deadlink.htm)

---

## 🙋 FAQ

**Was passiert, wenn eine Domain blockiert wird, die ich benötige?**  
➡ Entferne sie einfach manuell aus der Liste in der Fritz!Box.

**Funktioniert das auch mit älteren Fritz!Box-Modellen?**  
➡ Ja, die Kindersicherung ist in vielen Modellen seit Jahren verfügbar.

---

## 🤝 Mitwirken

Pull Requests, Verbesserungsvorschläge und neue Quellen sind herzlich willkommen!  
Bitte beachte dabei:

- Die Liste darf **max. 500 Einträge** enthalten
- Domains sollten regelmäßig überprüft werden (z. B. mit AM-Deadlink)
- Nutze **Pull Requests mit kurzer Erklärung**

---

## 📜 Lizenz

[MIT License](https://opensource.org/licenses/MIT) – freie Nutzung mit Namensnennung

> Originalkonzept: [Frank Boës](http://3960.org) und weitere

---

## 🎯 Unterstütze dieses Projekt

Du findest die Blockliste nützlich? Dann gib dem Projekt ein ⭐️ oder teile es mit anderen Fritz!Box-Nutzer:innen!

