# ⚡ Stufe 1: Öffentliche alternative DNS-Server

[⬅️ Zurück zur Übersicht](../README.md)

Standard-DNS deines Providers hat oft Lücken – durch Fehler oder bewusste Sperren.

> [!IMPORTANT]
> **Zensurfreiheit:** Alternative DNS-Server umgehen Netzsperren (wie CUII) effektiv. Freier Zugang zu Informationen.

---

## Warum wechseln? (Speed & Freedom)

1.  **Speed:** Globale Netzwerke (z. B. Cloudflare) antworten oft in Millisekunden. Surfen wird flüssiger.
2.  **Freiheit:** Ignoriert DNS-Sperrlisten der Provider (z. B. CUII).
3.  **Privacy:** Viele Anbieter löschen Logs schnell. Schutz vor neugierigen Provider-Blicken.

---

## Der Vergleich: Top DNS-Anbieter

Fokus wählen, DNS eintragen.

| Anbieter | Herkunft | DoT-Hostname oder IP-Adresse | Besonderheit |
| :--- | :---: | :--- | :--- |
| [**Cloudflare**](https://1.1.1.1/) | ![US](https://flagcdn.com/w20/us.png) | `1.1.1.1` / `one.one.one.one` | Extrem schnell, globaler Standard |
| [**Google**](https://developers.google.com/speed/public-dns) | ![US](https://flagcdn.com/w20/us.png) | `8.8.8.8` / `dns.google` | Höchste Verfügbarkeit, Big-Tech |
| [**Quad9**](https://www.quad9.net/) | ![CH](https://flagcdn.com/w20/ch.png) | `9.9.9.9` / `dns.quad9.net` | Security (Malware-Block), Non-Profit |
| [**dnsforge.de**](https://dnsforge.de/) | ![DE](https://flagcdn.com/w20/de.png) | `176.9.93.198` / `dnsforge.de` | **Kuketz-Empfehlung**, werbefrei, keine Logs |
| [**Mullvad**](https://mullvad.net/de/help/dns-over-tls-and-dns-over-https) | ![SE](https://flagcdn.com/w20/se.png) | `194.242.2.2` / `base.dns.mullvad.net` | Fokus Privacy, schwedischer Anbieter |
| [**Digitalcourage**](https://digitalcourage.de/support/zensurfreier-dns-server) | ![DE](https://flagcdn.com/w20/de.png) | `5.9.164.112` / `dns3.digitalcourage.de` | Datenschutz-Verein, keine Logs |
| [**Digitale Gesellschaft**](https://www.digitale-gesellschaft.ch/dns/) | ![CH](https://flagcdn.com/w20/ch.png) | `185.95.218.42` / `dns.digitale-gesellschaft.ch` | Schweizer Bürgerrechte, keine Vorratsdaten |
| [**DNS4EU**](https://joindns4.eu/) | ![EU](https://flagcdn.com/w20/eu.png) | `protective.joindns4.eu` | EU-Souveränität, DSGVO, Security-Filter |

---

## Big Tech vs. Community

*   **Big Tech (Google/Cloudflare):** Maximale Performance. Preis: Datenanalyse (anonymisiert), unterliegt CLOUD Act.
*   **Community (Digitalcourage/Quad9):** Fokus Datenschutz & Bürgerrechte. Geschwindigkeit meist exzellent.

> [!TIP]
> **Empfehlung:** Wert auf Privatsphäre + Werbefilter? [**dnsforge.de**](https://dnsforge.de) ist der Favorit vieler Experten (u.a. Mike Kuketz) für den Betrieb in Deutschland.

---

## Quellen & Links
- [Kuketz IT-Security Blog – DNS](https://www.kuketz-blog.de/empfehlungsecke/#dns)
- [Tarnkappe.info – DoH Einrichtung](https://tarnkappe.info/artikel/it-sicherheit/dns-sperren-der-cuii-umgehen-dns-over-https-fuer-windows-firefox-und-chrome-einrichten-252197.html)
- [Privacy-Handbuch – DNS-Suche](https://www.privacy-handbuch.de/handbuch_93d.htm)
- [Netzpolitik.org – Kritik an Netzsperren](https://netzpolitik.org/2021/cuii-kritik-an-netzsperren-ohne-richterbeschluss/)

---

<p align="center">
  <a href="00-vanilla-dns.md">Stufe 0</a> | Stufe 1 | <a href="02-dns-verschluesselt.md">Stufe 2</a> | <a href="03-dns-verschluesselt-adblock.md">Stufe 3</a> | <a href="04-cloud-adblocker.md">Stufe 4</a> | <a href="05-selfhosting.md">Stufe 5</a> | <a href="06-testing.md">Stufe 6</a> | <a href="07-sources.md">Stufe 7</a>
</p>
<p align="center">
  <a href="../README.md">🏠 Zurück zur Übersicht</a>
</p>


