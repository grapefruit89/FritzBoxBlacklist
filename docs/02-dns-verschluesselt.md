# 💊 Etappe 2: DNS verschlüsseln – Nimm die rote Pille

[⬅️ Zurück zur Übersicht](../README.md)

DNS-Verschlüsselung ist dein Ticket aus der Matrix der Provider-Überwachung. Während Etappe 1 dir ein besseres Telefonbuch gegeben hat, sorgt Etappe 2 dafür, dass niemand mehr heimlich mitliest, welche Nummern du wählst. Willkommen in der Realität.

---

## 🕶️ Was sind DoT und DoH?
[⬅️ Zurück zur Übersicht](../README.md)

Normale DNS-Anfragen sind wie Postkarten: Jeder (dein Internetanbieter, Hacker im öffentlichen WLAN, Geheimdienste) kann sie im Klartext lesen. Um das zu verhindern, nutzen wir moderne Verschlüsselungsverfahren.

1.  **DoT (DNS over TLS):** Packt deine DNS-Anfrage in einen dedizierten, verschlüsselten Tunnel (Port 853). Das ist der Goldstandard für Router wie die Fritz!Box.
2.  **DoH (DNS over HTTPS):** Versteckt die Anfrage im normalen Web-Traffic (Port 443). Das nutzen vor allem Browser (Chrome, Firefox) oder Smartphones direkt.

---

## 🔴 Warum Verschlüsselung? (Die rote Pille)
[⬅️ Zurück zur Übersicht](../README.md)

Selbst wenn du in [Etappe 1](./01-alternative-dns.md) einen privaten DNS-Anbieter gewählt hast, sieht dein Internetanbieter (ISP) weiterhin jede einzelne Anfrage, da sie standardmäßig unverschlüsselt übertragen wird. Er kann Profile über dein Surfverhalten erstellen, Anfragen manipulieren oder dich durch DNS-Sperren bevormunden.

> [!IMPORTANT]
> **Verschlüsselung ist Pflicht:** Ohne DoT/DoH ist die Wahl eines alternativen DNS-Servers nur die halbe Miete. Dein ISP bleibt der "Stille Beobachter" deiner digitalen Schritte. Mit DoT nimmst du die rote Pille und entziehst dich dieser Beobachtung.

---

## 🏛️ Die Anbieter (DoT Fokus)
[⬅️ Zurück zur Übersicht](../README.md)

Diese Anbieter bieten höchste Sicherheit und Privatsphäre ohne (vorerst) aggressive Werbefilter. Ideal, um die Infrastruktur zu testen.

| Anbieter | Herkunft | DoT-Hostname oder IP-Adresse | Besonderheit |
| :--- | :---: | :--- | :--- |
| [**Quad9**](https://www.quad9.net/) | <img src="https://flagcdn.com/w20/ch.png" width="20"> | `dns9.quad9.net` | Fokus auf Security (Malware-Block), Non-Profit |
| [**Digitalcourage**](https://digitalcourage.de/support/zensurfreier-dns-server) | <img src="https://flagcdn.com/w20/de.png" width="20"> | `dns3.digitalcourage.de` | Datenschutz-Verein, zensurfrei, keine Logs |
| [**Digitale Gesellschaft**](https://www.digitale-gesellschaft.ch/dns/) | <img src="https://flagcdn.com/w20/ch.png" width="20"> | `dns.digitale-gesellschaft.ch` | Schweizer Bürgerrechtsverein, keine EU-Vorratshaltung |
| [**Cloudflare**](https://1.1.1.1/) | <img src="https://flagcdn.com/w20/us.png" width="20"> | `1.1.1.1` / `one.one.one.one` | Extrem schnell, globaler Standard |
| [**Google**](https://developers.google.com/speed/public-dns) | <img src="https://flagcdn.com/w20/us.png" width="20"> | `dns.google` | Höchste Verfügbarkeit |
| [**DNS4EU**](https://joindns4.eu/) | <img src="https://flagcdn.com/w20/eu.png" width="20"> | `unfiltered.joindns4.eu` | EU-Souveränität, DSGVO-konform |

---

## ⚙️ Fritz!Box Setup Guide
[⬅️ Zurück zur Übersicht](../README.md)

So aktivierst du DoT in deiner Fritz!Box und machst dein Heimnetz sicher.

1.  Navigiere in der Benutzeroberfläche zu `Internet` -> `Zugangsdaten` -> `DNS-Server`.
2.  Scrolle zum Bereich **DNS über TLS (DoT)**.
3.  Setze den Haken bei **DNS über TLS (DoT) aktiv**.
4.  Unter **Auflösungsnamen der zu verwendenden DNS-Server** gibst du die Hostnamen deiner Wahl ein (einer pro Zeile).

> [!IMPORTANT]
> **Konfigurations-Falle:** In das Feld gehört **nur der Hostname** (z. B. `dns9.quad9.net`). Die Fritz!Box benötigt hier keine IP-Adressen und kein Feld für den Port (sie nutzt automatisch Port 853).

5.  **Empfehlung:** Deaktiviere "Fallback auf unverschlüsselte Namensauflösung im Internet zulassen", um sicherzustellen, dass keine einzige Anfrage unverschlüsselt "leakt".
6.  Klicke auf **Übernehmen**.

---

## 🧪 Testen
[⬅️ Zurück zur Übersicht](../README.md)

Nach der Einrichtung solltest du verifizieren, ob du wirklich verschlüsselt surfst.

<details>
<summary>Klicke hier, um die Test-Tools zu sehen</summary>

-   [Quad9 Check](https://on.quad9.net/) – Bestätigt sofort, ob du über Quad9 gesichert bist.
-   [Cloudflare Browsing Experience Check](https://www.cloudflare.com/ssl/cloudflarereader/) – Prüft "Secure DNS" (DoT/DoH).
-   [Mullvad DNS Check](https://mullvad.net/de/check) – Zeigt dir detailliert, welcher DNS-Server deine Anfragen aktuell beantwortet.
</details>

---

### 🚀 Nächste Schritte
[⬅️ Zurück zur Etappe 1: Alternative DNS](./01-alternative-dns.md) | [Weiter zu Etappe 3: DNS Verschlüsselt + Adblock ➡️](./03-dns-verschluesselt-adblock.md)

---
*Mit Liebe zum Detail für ein freieres Internet erstellt.*
