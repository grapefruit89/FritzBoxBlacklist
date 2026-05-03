# ⚡ Stufe 1: Öffentliche alternative DNS-Server

DNS ist das Telefonbuch des Internets. Standardmäßig nutzt du das Telefonbuch deines Internetanbieters (Telekom, Vodafone, etc.). Doch dieses Buch hat oft Lücken – entweder aus Versehen oder durch bewusste Sperren.

> [!IMPORTANT]
> **Zensurfreiheit als Grundrecht:** Die Nutzung alternativer DNS-Server ist einer der effektivsten Wege, um Netzsperren (wie die der CUII) zu umgehen und den uneingeschränkten Zugang zu Informationen zu sichern.

---

## Warum wechseln? (Speed & Freedom)

1.  **Geschwindigkeit:** Große Anbieter wie Cloudflare betreiben globale Netzwerke, die DNS-Anfragen oft in Millisekunden beantworten. Das macht das Surfen spürbar flüssiger.
2.  **Freiheit von Netzsperren:** In Deutschland setzen Provider oft DNS-Sperren für bestimmte Webseiten um (z. B. durch die Clearingstelle Urheberrecht im Internet - CUII). Alternative DNS-Resolver ignorieren diese Sperrlisten meist komplett.
3.  **Privatsphäre:** Viele alternative Anbieter protokollieren keine IP-Adressen oder löschen diese nach kurzer Zeit, was dein Surfverhalten vor den neugierigen Blicken deines Providers schützt.

---

## Der Vergleich: Top DNS-Anbieter

Hier findest du eine Auswahl der besten DNS-Resolver, unterteilt nach ihrem Fokus.

| Anbieter | Herkunft | DoT-Hostname oder IP-Adresse | Besonderheit |
| :--- | :---: | :--- | :--- |
| [**Cloudflare**](https://1.1.1.1/) | <img src="https://flagcdn.com/w20/us.png" width="20"> | `1.1.1.1` / `one.one.one.one` | Extrem schnell, globaler Standard |
| [**Google**](https://developers.google.com/speed/public-dns) | <img src="https://flagcdn.com/w20/us.png" width="20"> | `8.8.8.8` / `dns.google` | Höchste Verfügbarkeit, Big-Tech-Hintergrund |
| [**Quad9**](https://www.quad9.net/) | <img src="https://flagcdn.com/w20/ch.png" width="20"> | `9.9.9.9` / `dns.quad9.net` | Fokus auf Security (Malware-Block), Non-Profit |
| [**Digitalcourage**](https://digitalcourage.de/support/zensurfreier-dns-server) | <img src="https://flagcdn.com/w20/de.png" width="20"> | `5.9.164.112` / `dns3.digitalcourage.de` | Datenschutz-Verein, zensurfrei, keine Logs |
| [**Digitale Gesellschaft**](https://www.digitale-gesellschaft.ch/dns/) | <img src="https://flagcdn.com/w20/ch.png" width="20"> | `185.95.218.42` / `dns.digitale-gesellschaft.ch` | Schweizer Bürgerrechtsverein, keine EU-Vorratshaltung |
| [**DNS4EU**](https://joindns4.eu/) | <img src="https://flagcdn.com/w20/eu.png" width="20"> | `protective.joindns4.eu` | EU-Souveränität, DSGVO-konform, Security-Filter |

---

## "Big Tech" vs. Community – Wo ist der Haken?

*   **Big Tech (Google/Cloudflare):** Du bekommst maximale Performance und Ausfallsicherheit. Der "Preis" ist jedoch, dass deine (anonymisierten) Daten zur Analyse von Internet-Trends genutzt werden könnten. Zudem unterliegen US-Anbieter dem CLOUD Act.
*   **Community & Non-Profit (Digitalcourage/Quad9):** Hier steht der Datenschutz an erster Stelle. Diese Dienste werden oft von Vereinen oder Stiftungen betrieben, die sich für digitale Bürgerrechte einsetzen. Die Geschwindigkeit ist meist exzellent, erreicht aber in entlegenen Regionen nicht immer das Niveau der Hyperscaler.

> [!TIP]
> **Kuketz-Empfehlung:** Wenn du Wert auf maximale Privatsphäre und Werbefilter legst, schau dir auch Projekte wie [dnsforge.de](https://dnsforge.de) an, die oft in der Empfehlungsecke von Mike Kuketz auftauchen.

---

## Quellen & Weiterführende Links
- [Kuketz IT-Security Blog – Empfehlungsecke DNS](https://www.kuketz-blog.de/empfehlungsecke/#dns)
- [Tarnkappe.info – DoH Einrichtung für Browser & Windows](https://tarnkappe.info/artikel/it-sicherheit/dns-sperren-der-cuii-umgehen-dns-over-https-fuer-windows-firefox-und-chrome-einrichten-252197.html)
- [Privacy-Handbuch – Die Suche nach dem passenden DNS-Server](https://www.privacy-handbuch.de/handbuch_93d.htm)
- [Netzpolitik.org – CUII und die Privatisierung der Rechtsdurchsetzung](https://netzpolitik.org/2021/cuii-kritik-an-netzsperren-ohne-richterbeschluss/)
- [DNS4EU Projektseite](https://joindns4.eu)

---
[Zurück zur Übersicht](../README.md)
