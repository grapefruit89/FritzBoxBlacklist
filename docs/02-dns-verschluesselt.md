# 💊 Stufe 2: DNS verschlüsseln

[⬅️ Zurück zur Übersicht](../README.md)

DNS-Verschlüsselung ist dein Ticket aus der Matrix der Provider-Überwachung. Während Stufe 1 dir ein besseres Telefonbuch gegeben hat, sorgt Stufe 2 dafür, dass niemand mehr heimlich mitliest.

---

## 🕶️ DoT vs. DoH
Normale DNS-Anfragen sind wie Postkarten: Jeder kann sie mitlesen. Verschlüsselung schützt deine Privatsphäre.

1. **DoT (DNS over TLS):** Verschlüsselter Tunnel (Port 853). Ideal für Router wie die **Fritz!Box**.
2. **DoH (DNS over HTTPS):** Versteckt Anfragen im Web-Traffic (Port 443). Nutzen vor allem Browser und Smartphones.

---

## 🏛️ Die Anbieter (DoT Fokus)
Diese Anbieter bieten Sicherheit ohne aggressive Filter. Ideal zum Testen.

| Anbieter | Herkunft | DoT-Hostname / IP | Besonderheit |
| :--- | :---: | :--- | :--- |
| [**Quad9**](https://www.quad9.net/) | <img src="https://flagcdn.com/w20/ch.png" width="20"> | `dns9.quad9.net` | Fokus Security, Non-Profit |
| [**Digitalcourage**](https://digitalcourage.de/support/zensurfreier-dns-server) | <img src="https://flagcdn.com/w20/de.png" width="20"> | `dns3.digitalcourage.de` | Datenschutz-Verein, keine Logs |
| [**Digitale Gesellschaft**](https://www.digitale-gesellschaft.ch/dns/) | <img src="https://flagcdn.com/w20/ch.png" width="20"> | `dns.digitale-gesellschaft.ch` | CH-Bürgerrechtsverein |
| [**Cloudflare**](https://1.1.1.1/) | <img src="https://flagcdn.com/w20/us.png" width="20"> | `1.1.1.1` | Extrem schnell |
| [**Google**](https://developers.google.com/speed/public-dns) | <img src="https://flagcdn.com/w20/us.png" width="20"> | `dns.google` | Höchste Verfügbarkeit |
| [**DNS4EU**](https://joindns4.eu/) | <img src="https://flagcdn.com/w20/eu.png" width="20"> | `unfiltered.joindns4.eu` | EU-Souveränität, DSGVO |

---

## ⚙️ Fritz!Box Setup
1. `Internet` -> `Zugangsdaten` -> `DNS-Server`.
2. Bereich **DNS über TLS (DoT)** suchen.
3. **DNS über TLS (DoT) aktiv** anhaken.
4. Hostnamen (einer pro Zeile) eintragen (z.B. `dns9.quad9.net`).

> [!IMPORTANT]
> Nur den **Hostnamen** eintragen! Keine IPs, kein Port.

---

## 🧪 Testen
### Check-Tools

- [Quad9 Check](https://on.quad9.net/)
- [Cloudflare Check](https://www.cloudflare.com/ssl/cloudflarereader/)
- [Mullvad Check](https://mullvad.net/de/check)


---

<p align="center">
  <a href="01-alternative-dns.md">⬅️ Stufe 1</a> | <a href="03-dns-verschluesselt-adblock.md">Stufe 3 ➡️</a>
</p>

[⬅️ Zurück zur Übersicht](../README.md)
