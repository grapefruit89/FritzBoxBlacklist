# 💊 Stufe 2: DNS verschlüsseln

[⬅️ Zurück zur Übersicht](../README.md)

DNS-Verschlüsselung ist dein Ticket aus der Matrix der Provider-Überwachung. Während Stufe 1 dir ein besseres Telefonbuch gegeben hat, sorgt Stufe 2 dafür, dass niemand mehr heimlich mitliest.

> [!TIP]
> **Die Wahl:** Du kannst die blaue Pille schlucken (Standard-DNS deines Providers) und in der gewohnten Überwachung bleiben – oder die rote Pille (verschlüsseltes DNS) und sehen, wie tief der Kaninchenbau der digitalen Freiheit reicht.

---

## 🕶️ DoT vs. DoH
Normale DNS-Anfragen sind wie Postkarten: Jeder kann sie mitlesen. Verschlüsselung schützt deine Privatsphäre.

1. **DoT (DNS over TLS):** Verschlüsselter Tunnel (Port 853). Ideal für Router wie die **Fritz!Box**.
2. **DoH (DNS over HTTPS):** Versteckt Anfragen im Web-Traffic (Port 443). Nutzen vor allem Browser und Smartphones.

---

## 🏛️ Die Anbieter (DoT Fokus)
Diese Anbieter bieten Sicherheit ohne aggressive Filter. Ideal zum Testen.

| Anbieter | Herkunft | DoT-Hostname | Besonderheit |
| :--- | :---: | :--- | :--- |
| [**Quad9**](https://www.quad9.net/) | ![CH](https://flagcdn.com/w20/ch.png) | `dns.quad9.net` | Fokus Security, Non-Profit |
| [**dnsforge.de**](https://dnsforge.de/) | ![DE](https://flagcdn.com/w20/de.png) | `dnsforge.de` | **Kuketz-Empfehlung**, werbefrei |
| [**Mullvad**](https://mullvad.net/de/help/dns-over-tls-and-dns-over-https) | ![SE](https://flagcdn.com/w20/se.png) | `base.dns.mullvad.net` | Fokus Privacy, schwedisch |
| [**Digitalcourage**](https://digitalcourage.de/support/zensurfreier-dns-server) | ![DE](https://flagcdn.com/w20/de.png) | `dns3.digitalcourage.de` | Datenschutz-Verein, keine Logs |
| [**Digitale Gesellschaft**](https://www.digitale-gesellschaft.ch/dns/) | ![CH](https://flagcdn.com/w20/ch.png) | `dns.digitale-gesellschaft.ch` | CH-Bürgerrechtsverein |
| [**Cloudflare**](https://1.1.1.1/) | ![US](https://flagcdn.com/w20/us.png) | `one.one.one.one` | Extrem schnell |
| [**Google**](https://developers.google.com/speed/public-dns) | ![US](https://flagcdn.com/w20/us.png) | `dns.google` | Höchste Verfügbarkeit |
| [**DNS4EU**](https://joindns4.eu/) | ![EU](https://flagcdn.com/w20/eu.png) | `unfiltered.joindns4.eu` | EU-Souveränität, DSGVO |

---

## ⚙️ Fritz!Box Setup
1. `Internet` -> `Zugangsdaten` -> `DNS-Server`.
2. Bereich **DNS über TLS (DoT)** suchen.
3. **DNS über TLS (DoT) aktiv** anhaken.
4. Hostnamen (einer pro Zeile) eintragen (z.B. `dns.quad9.net`).

> [!IMPORTANT]
> Nur den **Hostnamen** eintragen! Keine IPs, keine Schrägstriche, kein Port. IPs gehören in die Felder darüber (Stufe 1).

---

## 🧪 Testen
### Check-Tools

- **[Quad9 Check](https://on.quad9.net/):** Bestätigt sofort, ob du Quad9 nutzt und ob die Verbindung gesichert ist.
- **[DNS-Leak-Test](https://www.dnsleaktest.com/):** Zeigt an, welche DNS-Server dein System tatsächlich kontaktiert. Erscheint hier dein Internetprovider (z.B. Telekom, Vodafone), "leakt" dein DNS.
- **[Cloudflare Check](https://www.cloudflare.com/ssl/cloudflarereader/):** Überprüft auf verschlüsseltes SNI und DoT/DoH.
- **[Mullvad Check](https://mullvad.net/de/check):** Ein schneller Rundum-Check für DNS und Privacy.


---

<p align="center">
  <a href="00-vanilla-dns.md">Stufe 0</a> | <a href="01-alternative-dns.md">Stufe 1</a> | Stufe 2 | <a href="03-dns-verschluesselt-adblock.md">Stufe 3</a> | <a href="04-cloud-adblocker.md">Stufe 4</a> | <a href="05-selfhosting.md">Stufe 5</a> | <a href="06-testing.md">Stufe 6</a> | <a href="07-sources.md">Stufe 7</a>
</p>
<p align="center">
  <a href="../README.md">🏠 Zurück zur Übersicht</a>
</p>

