# ⚡ Stufe 1: Alternative DNS

Standard-DNS deines Providers hat oft Lücken – durch technische Fehler oder bewusste Sperren.

> [!IMPORTANT]
> **Zensurfreiheit:** Alternative DNS-Server umgehen Netzsperren (wie CUII) effektiv. Freier Zugang zu Informationen ist ein Grundrecht.

---

## Warum wechseln? (Speed & Freedom)

1.  **Speed:** Globale Netzwerke antworten oft in Millisekunden. Surfen wird flüssiger.
2.  **Freiheit:** Ignoriert DNS-Sperrlisten der Provider (z. B. CUII).
3.  **Privacy:** Viele Anbieter löschen Logs schnell. Schutz vor neugierigen Provider-Blicken.

---

## 📊 Der Vergleich: Top DNS-Anbieter

Diese Tabelle ist schlank gehalten, um auf allen Geräten gut lesbar zu bleiben. Details zu Verschlüsselung (DoT) folgen in Stufe 2.

| Anbieter | Herkunft | IPv4-Adressen | Kurzcharakteristik |
| :--- | :---: | :--- | :--- |
| [**Cloudflare**](https://1.1.1.1/) | ![US](https://flagcdn.com/w20/us.png) | `1.1.1.1` / `1.0.0.1` | Maximaler Speed, Privacy-first |
| [**Google DNS**](https://developers.google.com/speed/public-dns) | ![US](https://flagcdn.com/w20/us.png) | `8.8.8.8` / `8.8.4.4` | Globaler Standard, sehr stabil |
| [**Quad9**](https://www.quad9.net/) | ![CH](https://flagcdn.com/w20/ch.png) | `9.9.9.9` / `149.112.112.112` | Malware-Schutz, Schweizer Stiftung |
| [**Mullvad**](https://mullvad.net/de/help/dns-over-https-and-dns-over-tls) | ![SE](https://flagcdn.com/w20/se.png) | `194.242.2.2` | Radikal anonym, keine Logs |
| [**dnsforge**](https://dnsforge.de/) | ![DE](https://flagcdn.com/w20/de.png) | `94.16.114.222` | Zensurfrei, DE-Verein, Adblock-Option |
| [**Digitale Ges.**](https://www.digitale-gesellschaft.ch/dns/) | ![CH](https://flagcdn.com/w20/ch.png) | `185.95.218.42` | Fokus Bürgerrechte & Neutralität |
| [**Digitalcourage**](https://digitalcourage.de/support/dns-server) | ![DE](https://flagcdn.com/w20/de.png) | `5.1.66.255` | Datenschutz-Pionier aus Deutschland |
| [**Control D**](https://controld.com/free-dns) | ![CA](https://flagcdn.com/w20/ca.png) | `76.76.2.0` / `76.76.10.0` | Hochgradig anpassbar, modern |
| [**AdGuard DNS**](https://adguard-dns.io/de/public-dns.html) | ![CY](https://flagcdn.com/w20/cy.png) | `94.140.14.14` | Spezialist für Werbe- & Tracking-Block |
| [**CleanBrowsing**](https://cleanbrowsing.org/) | ![US](https://flagcdn.com/w20/us.png) | `185.228.168.168` | Fokus Jugendschutz (Family Filter) |
| [**DNS4EU**](https://joindns4.eu/) | ![EU](https://flagcdn.com/w20/eu.png) | `86.54.11.100` | EU-Projekt für digitale Souveränität |
| [**OpenNIC**](https://www.opennic.org/) | 🌐 | *Je nach Region* | Community-Projekt, alternative TLDs |

---

<details>
<summary>📋 Vollständige Anbieter-Liste & Spezialdienste (Klick zum Ausklappen)</summary>

Hier findest du weitere bekannte oder historische Anbieter, die für spezielle Nischen interessant sein können.

| Anbieter | Herkunft | Fokus / Besonderheit |
| :--- | :---: | :--- |
| **Cisco OpenDNS** | ![US](https://flagcdn.com/w20/us.png) | Phishing-Schutz, Enterprise-Wurzeln |
| **Comodo Secure** | ![US](https://flagcdn.com/w20/us.png) | Fokus auf Malware-Blockierung |
| **Yandex.DNS** | ![RU](https://flagcdn.com/w20/ru.png) | Russische Alternative, verschiedene Filter-Profile |
| **Verisign** | ![US](https://flagcdn.com/w20/us.png) | Stabilität vom Root-Server-Betreiber |
| **DNS.WATCH** | ![DE](https://flagcdn.com/w20/de.png) | Deutsches Non-Profit-Projekt |
| **BlissDNS** | ![DE](https://flagcdn.com/w20/de.png) | Fokus auf Verschlüsselung & Privatsphäre |
| **BebasDNS** | ![ID](https://flagcdn.com/w20/id.png) | Neutraler Resolver aus Indonesien |
| **Level3** | ![US](https://flagcdn.com/w20/us.png) | Historischer Klassiker (jetzt CenturyLink) |
| **HaGeZi DNS** | ![DE](https://flagcdn.com/w20/de.png) | Hochwertige Filterlisten für Fortgeschrittene |

</details>

---

## Big Tech vs. Community

*   **Big Tech (Google/Cloudflare):** Maximale Performance. Preis: Datenanalyse (anonymisiert), unterliegt US-Recht (CLOUD Act).
*   **Community (Digitalcourage/dnsforge):** Fokus Datenschutz & Bürgerrechte. Oft von Vereinen oder Stiftungen betrieben.

> [!TIP]
> **Empfehlung:** Wert auf Privatsphäre + Werbefilter? Gehe direkt zu [**Stufe 3: Quick Start (Adblock)**](03-dns-verschluesselt-adblock.md).

---
<p align="center">
  <a href="00-vanilla-dns.md">🍦 Stufe 0</a> | ⚡ Stufe 1 | <a href="02-dns-verschluesselt.md">💊 Stufe 2</a> | <a href="03-dns-verschluesselt-adblock.md">🛡️ Stufe 3</a> | <a href="04-cloud-adblocker.md">☁️ Stufe 4</a> | <a href="05-selfhosting.md">🏠 Stufe 5</a> | <a href="06-testing.md">🧪 Stufe 6</a> | <a href="07-sources.md">📚 Stufe 7</a>
</p>
<p align="center">
  <a href="../README.md">🏠 Zurück zur Übersicht</a>
</p>
