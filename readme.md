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
> 📚 _Lesetipp: [tarnkappe.info – Blogbeitrag](https://tarnkappe.info/artikel/it-sicherheit/datenschutz/dns-resolver-adguard-dns-control-d-nextdns-und-rethink-dns-im-vergleichstest-312812.html)_


---

## 🚀 Schnellstart: Filterliste in der Fritz!Box einrichten

1. 📖 Lies die Anleitung: [FritzBox-Kindersicherung einrichten (heise.de)](https://www.heise.de/tipps-tricks/FritzBox-Kindersicherung-so-funktioniert-die-Einrichtung-4048867.html)
2. 📥 Kopiere den Inhalt der aktuellen Blockliste:  
   [🔗 Fritz 500 Blacklist (Stand: 23.11.2020)](https://github.com/grapefruit89/FritzBoxBlacklist/blob/master/Fritz%20500%202020-11-23.txt)
3. 📋 Füge die Domains unter **fritz.box › Internet › Filter › Listen › Gesperrte Webseiten** ein
4. ✅ Fertig!  🚀

> 💡 Auch weitere Quellen aus dem Abschnitt [Weiterführende Links](#weiterführende-links) sind nutzbar.

---

## 🛜 DNS-Server mit integriertem Werbeblocker

Alternativ oder ergänzend zur Fritz!Box-Blockliste kannst du einen DNS-Dienst mit Werbeblock-Funktion nutzen.

🧾 **Was ist ein DNS?**  
Ein DNS-Server funktioniert wie ein Telefonbuch: Er übersetzt Domainnamen in IP-Adressen. Wenn du einen DNS-Anbieter nutzt, der Werbung herausfiltert, wirst du zu weniger unerwünschtem Inhalt weitergeleitet.

## 🧩 Teil 1: Set & Forget – DNS-Resolver ohne Konfigurationsaufwand unbedingt DoH nehmen 

| Anbieter                      | IPv4                                   | DoH-URL(s)                                                                                   | Nutzerlevel 🧠 | Filterstärke 🔥      | Overblocking 🚫 | Beschreibung                                                                       |
|-------------------------------|----------------------------------------|----------------------------------------------------------------------------------------------|---------------|---------------------|----------------|------------------------------------------------------------------------------------|
| **Quad9**                     | 9.9.9.9 / 149.112.112.112              | https://dns.quad9.net/dns-query                                                              | Einsteiger    | Hoch                | Mittel         | Malware-Block, DNSSEC, Schweizer Stiftung, Anycast weltweit                        |
| **Cloudflare Malware**        | 1.1.1.2 / 1.0.0.2                      | https://security.cloudflare-dns.com/dns-query                                                | Einsteiger    | Hoch                | Gering         | Blockiert Malware                                                                  |
| **Cloudflare Family**         | 1.1.1.3 / 1.0.0.3                      | https://family.cloudflare-dns.com/dns-query                                                  | Einsteiger    | Sehr hoch           | Hoch           | Blockiert Malware + Adult Content                                                  |
| **DNS0.eu Zero**              | 193.110.81.9 / 185.253.5.9             | https://zero.dns0.eu/                                                                        | Einsteiger    | Hoch                | Gering         | EU, starker Schutz vor bösartigen Domains, kein Werbe- oder Adult-Blocker           |
| **DNS4EU Protect**            | 86.54.11.1 / 86.54.11.201              | https://protective.joindns4.eu/dns-query                                                     | Einsteiger    | Hoch                | Gering         | EU-Projekt, blockiert Malware, Phishing                                            |
| **DNS4EU Child**              | 86.54.11.12 / 86.54.11.212             | https://child.joindns4.eu/dns-query                                                          | Einsteiger    | Sehr hoch           | Hoch           | + Kinderschutz (Adult, Gewalt, Drogen etc.)                                        |
| **DNS4EU NoAds**              | 86.54.11.13 / 86.54.11.213             | https://noads.joindns4.eu/dns-query                                                          | Einsteiger    | Hoch                | Mittel         | + Werbung/Tracker-Blocker                                                          |
| **LibreDNS**                  | 116.202.176.26                         | https://doh.libredns.gr/dns-query                                                            | Fortgeschr.   | Niedrig             | Gering         | Kein Logging, OpenNIC-basiert, Griechenland/EU                                     |
| **LibreDNS NoAds**            | 116.202.176.26                         | https://doh.libredns.gr/noads                                                                | Fortgeschr.   | Mittel              | Mittel         | Crowdsourced Ad-/Tracker-Blocklisten                                               |
| **UncensoredDNS (Anycast)**   | 91.239.100.100                         | https://anycast.uncensoreddns.org/dns-query                                                  | Fortgeschr.   | Keine Filter        | Keine          | Dänemark/EU, kompromisslos neutral, keine Filter                                   |
| **UncensoredDNS (Kopenhagen)**| 89.233.43.71                           | https://unicast.uncensoreddns.org/dns-query                                                  | Fortgeschr.   | Keine Filter        | Keine          | Kopenhagen, Single-Server, neutral                                                 |
| **DNS.SB Düsseldorf**         | 185.222.222.222 / 45.11.45.11          | https://de-dus.doh.sb/dns-query                                                              | Fortgeschr.   | Keine Filter        | Keine          | Standort Düsseldorf, DE, Unicast                                                   |
| **DNS.SB Frankfurt**          | –                                      | https://de-fra.doh.sb/dns-query                                                              | Fortgeschr.   | Keine Filter        | Keine          | Standort Frankfurt, DE, Unicast                                                    |
| **DNS.SB Berlin**             | –                                      | https://de-ber.doh.sb/dns-query                                                              | Fortgeschr.   | Keine Filter        | Keine          | Standort Berlin, DE, Unicast                                                       |
| **DNS.SB Amsterdam**          | –                                      | https://nl-ams.doh.sb/dns-query                                                              | Fortgeschr.   | Keine Filter        | Keine          | Standort Amsterdam, NL, Unicast                                                    |
| **DNS.SB London**             | –                                      | https://uk-lon.doh.sb/dns-query                                                              | Fortgeschr.   | Keine Filter        | Keine          | Standort London, UK, Unicast                                                       |
| **DNS.SB Tallinn**            | –                                      | https://ee-tll.doh.sb/dns-query                                                              | Fortgeschr.   | Keine Filter        | Keine          | Standort Tallinn, EE, Unicast                                                      |
| **DNS.SB Global Anycast (EU)**| 185.222.222.222 / 45.11.45.11          | https://doh.sb/dns-query<br>https://doh.dns.sb/dns-query<br>https://dns.sb/dns-query         | Fortgeschr.   | Keine Filter        | Keine          | EU-Anycast-fähig, weltweit erreichbar                                              |
| **Mullvad Anycast (ohne Filter)** | 194.242.2.2                      | https://dns.mullvad.net/dns-query                                                            | Fortgeschr.   | Keine Filter        | Keine          | Schweden/EU, hohe Privatsphäre                                                     |
| **Mullvad Anycast (Adblock)** | 194.242.2.3                            | https://adblock.dns.mullvad.net/dns-query                                                    | Fortgeschr.   | Hoch                | Mittel         | + Werbung/Tracker                                                                  |
| **Mullvad Anycast (Base)**    | 194.242.2.4                            | https://base.dns.mullvad.net/dns-query                                                       | Fortgeschr.   | Hoch                | Mittel         | + Werbung/Tracker/Malware                                                          |
| **Mullvad Anycast (Extended)**| 194.242.2.5                            | https://extended.dns.mullvad.net/dns-query                                                   | Fortgeschr.   | Sehr hoch           | Hoch           | + Werbung/Tracker/Malware/Social Media                                             |
| **Mullvad Anycast (Family)**  | 194.242.2.6                            | https://family.dns.mullvad.net/dns-query                                                     | Fortgeschr.   | Sehr hoch           | Hoch           | + Family Filter (inkl. Gambling, Adult, etc.)                                      |
| **Mullvad Anycast (All)**     | 194.242.2.9                            | https://all.dns.mullvad.net/dns-query                                                        | Fortgeschr.   | Maximale Sperre     | Hoch           | Blockiert alles: Ads, Malware, Tracker, Adult, Gambling, Social Media etc.          |
| **Mullvad DE (Frankfurt)**    | –                                      | https://de-fra-dns-001.mullvad.net/dns-query                                                 | Fortgeschr.   | Keine Filter        | Keine          | DE-Server, ohne Filter                                                             |
| **Mullvad UK (London)**       | –                                      | https://gb-lon-dns-001.mullvad.net/dns-query<br>https://gb-lon-dns-301.mullvad.net/dns-query | Fortgeschr.   | Keine Filter        | Keine          | UK-Server, ohne Filter                                                             |
| **Mullvad SE (Stockholm)**    | –                                      | https://se-sto-dns-001.mullvad.net/dns-query                                                 | Fortgeschr.   | Keine Filter        | Keine          | SE-Server, ohne Filter                                                             |
| **Mullvad SE (Göteborg)**     | –                                      | https://se-got-dns-001.mullvad.net/dns-query                                                 | Fortgeschr.   | Keine Filter        | Keine          | SE-Server, ohne Filter                                                             |
| **Mullvad SE (Malmö)**        | –                                      | https://se-mma-dns-001.mullvad.net/dns-query                                                 | Fortgeschr.   | Keine Filter        | Keine          | SE-Server, ohne Filter                                                             |


 



## 🧰 Teil 2: Fremdserver mit Web-GUI & Konfigurationsoptionen  
### Diese DNS-Anbieter bieten Online-Oberflächen zur Feinanpassung – ideal für technisch Interessierte ohne eigenes Hosting.  
| Anbieter | Hostname | Nutzerlevel 🧠 | Filterstärke 🔥 | Overblocking 🚫 | Beschreibung |
|----------|----------|----------------|------------------|------------------|--------------|
| [AdGuard DNS](https://adguard-dns.io/de/public-dns.html) | `dns.adguard-dns.com` | 🔵 Komfortnutzer | 🟠 Hoch | 🟠 Mäßig | Blocklisten, Malware, Tracking, Zeitsteuerung für Kinder – sehr einsteigerfreundlich |
| [NextDNS](https://nextdns.io/) | (Benutzerdefiniert) | 🔵 Komfortnutzer | 🧩 Konfigurierbar | 💡 Optional | Viele globale Blocklisten (auch China, Vietnam), Gerätetrennung & Logs |
| [Control D](https://controld.com/) | (Benutzerdefiniert) | 🔵 Fortgeschritten | 🧩 Konfigurierbar | 💡 Mittel | Schnell, flexible Profile – aber kostenpflichtig nach 30 Tagen |
| [Rethink DNS](https://rethinkdns.com/) | (Benutzerdefiniert) | 🔴 Nerds | 🧩 Extrem flexibel | 🔴 Hoch | Unzählige Listen & Optionen, kostenfrei – läuft über Cloudflare |




## 🏠 Teil 3: Selfhosting-Lösungen – maximale Kontrolle im Heimnetz  
### Diese Tools erfordern einen eigenen Mini-Server oder Raspberry Pi, bieten dafür aber maximale Kontrolle & Datenschutz.  
| Lösung | Hosting | Nutzerlevel 🧠 | Filterstärke 🔥 | Overblocking 🚫 | Beschreibung |
|--------|---------|----------------|------------------|------------------|--------------|
| [Pi-hole](https://pi-hole.net/) | Selbsthosted | 🔴 Power-User | 🔴 Hoch | 🔴 Hoch | Lokaler DNS-Filter, sehr bekannt, aber kein DoQ – dafür hochflexibel |
| [AdGuard Home](https://adguard.com/de/adguard-home/overview.html) | Selbsthosted | 🔵 Komfortnutzer | 🔴 Hoch | 🔴 Mittel | Benutzerfreundlich, unterstützt DoQ, gute Familienoption |
| [Technitium DNS](https://technitium.com/dns/) | Selbsthosted | 🔴 Nerds | 🧩 Extrem konfigurierbar | 🔴 Hoch | Leistungsfähiger DNS-Server für Nerds, auch als Resolver einsetzbar |
| [eBlocker](https://www.eblocker.com/) *(EOL)* | Box (früher HW) | ⚫️ Veraltet | 🟡 Mittel | 🟡 Mäßig | Eingestellt, aber nützlich zum Verständnis klassischer DNS-Blocker |
| [Blocky](https://github.com/0xERR0R/blocky) | Selbsthosted | 🔴 Power-User | 🔴 Hoch | 🔴 Hoch | Sehr schnell, mit DoH/DoT Support, konfigurierbar per YAML – wenig UI |








---

## 🧪 Tests & Tools – funktioniert dein DNS-Blocker?

> Hier findest du praktische Seiten, um zu prüfen, ob Werbung und Tracking wirklich blockiert werden – inklusive eines humorvollen Klassikers.

### 🔍 Adblock-Funktion testen

| Tool | Beschreibung | Link |
|------|--------------|------|
| **ads-blocker.com** | Klassiker zum Erkennen blockierter Werbeelemente | [🔗 ads-blocker.com/testing](https://ads-blocker.com/testing/) |
| **blockads.fivefilters.org** | Erkennt gängige Anzeigenanbieter | [🔗 fivefilters.org](https://blockads.fivefilters.org/?pihole) |
| **browserleaks.com/adblock** | Analyse, ob Adblocker aktiv ist | [🔗 browserleaks.com/adblock](https://browserleaks.com/adblock) |
| **whoisblocked.com** | Checkt, ob eine bestimmte Domain durch deinen DNS geblockt wird | [🔗 whoisblocked.com](https://whoisblocked.com/) |
| **💣 www.bild.de** | Wenn *diese Seite* nicht lädt, funktioniert dein DNS Server sehr gut 😉 | [🔗 bild.de](https://www.bild.de/) |

---

### 🌐 DNS-Konfiguration testen

| Tool | Funktion | Link |
|------|----------|------|
| **DNS Leak Test** | Prüft, ob dein DNS-Anbieter korrekt verwendet wird | [🔗 dnsleaktest.com](https://www.dnsleaktest.com/) |
| **GRC DNS Benchmark** *(nur Windows)* | Geschwindigkeitsvergleich lokaler & externer Resolver | [🔗 grc.com](https://www.grc.com/dns/benchmark.htm) |
| **1.1.1.1/help** *(Cloudflare)* | Check für DoH, DoT, IPv6 etc. | [🔗 1.1.1.1/help](https://1.1.1.1/help) |
| **TestDoH** | Testet DNS-over-HTTPS | [🔗 test.doh.watch](https://test.doh.watch/) |
| **Quad9 DNS Check** | Spezieller Diagnosetest für `9.9.9.9` | [🔗 quad9.net/test](https://www.quad9.net/test) |

---

### 🧪 Spezial: Blockiert dein DNS-Filter Tracking?

| Tool | Beschreibung | Link |
|------|--------------|------|
| **coveryourtracks.eff.org** | Erkennung von Tracking über Fingerprinting, Cookies etc. | [🔗 EFF Tool](https://coveryourtracks.eff.org/) |
| **amiunique.org** | Sieht dein Browser eindeutig aus? | [🔗 amiunique.org](https://amiunique.org/fp) |
| **privacytests.org** | Datenschutz-Browser-Vergleich | [🔗 privacytests.org](https://privacytests.org/) |


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

