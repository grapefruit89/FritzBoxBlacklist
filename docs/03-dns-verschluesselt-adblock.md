# 🛡️ Stufe 3: Quick Start (Adblock)

Du willst keine Theorie, sondern **Ergebnisse**? Dann ist Stufe 3 dein Ziel. Wir nutzen einen kostenlosen, bewährten Cloud-Filter, den du direkt in deine Fritz!Box einträgst.

> [!TIP]
> **Die Metapher:** Das ist wie ein **bewachter Wohnpark**. Du engagierst einen professionellen Pförtner (den DNS-Server), der eine schwarze Liste führt. Werbefirmen und Tracker kommen gar nicht erst durch das Tor.

---

## 🚀 Empfohlene Anbieter (mit Werbefilter)

Hier sind die besten "Rundum-Sorglos"-Pakete für die Fritz!Box.

| Anbieter | DoT-Hostname | Besonderheiten & Modell | Herkunft |
| :--- | :--- | :--- | :---: |
| ![DE](https://flagcdn.com/w20/de.png) [**dnsforge.de**](https://dnsforge.de/) | `dnsforge.de` | **Top-Empfehlung.** Keine Logs, sehr sauberer Filter. | ![DE](https://flagcdn.com/w20/de.png) DE |
| ![CH](https://flagcdn.com/w20/ch.png) [**Digital Society**](https://www.digitale-gesellschaft.ch/dns/) | `dns.digitale-gesellschaft.ch` | Hoher Datenschutz, Schweizer Neutralität. | ![CH](https://flagcdn.com/w20/ch.png) CH |
| ![US](https://flagcdn.com/w20/us.png) [**AdGuard DNS**](https://adguard-dns.io/de/public-dns.html) | `dns.adguard-dns.com` | Mächtiger Filter, blockt fast alles an Werbung. | ![CY](https://flagcdn.com/w20/cy.png) CY |
| ![US](https://flagcdn.com/w20/us.png) [**CleanBrowsing**](https://cleanbrowsing.org/) | `family-filter-dns.cleanbrowsing.org` | Fokus auf Jugendschutz (Pornografie-Filter). | ![US](https://flagcdn.com/w20/us.png) US |

---

## 🛠️ Einrichtung in 3 Schritten

1.  Öffne deine Fritz!Box Oberfläche (`http://fritz.box`).
2.  Navigiere zu **Internet -> Zugangsdaten -> DNS-Server**.
3.  Aktiviere **DNS-over-TLS (DoT)** und trage einen der Hostnames von oben ein.

> [!IMPORTANT]
> Achte darauf, dass du **nur den Hostnamen** (z. B. `dnsforge.de`) einträgst – keine `https://`, keine IPs und keine Schrägstriche!

---

<p align="center">
  <a href="00-vanilla-dns.md">🍦 Stufe 0</a> | <a href="01-alternative-dns.md">⚡ Stufe 1</a> | <a href="02-dns-verschluesselt.md">💊 Stufe 2</a> | 🛡️ Stufe 3 | <a href="04-cloud-adblocker.md">☁️ Stufe 4</a> | <a href="05-selfhosting.md">🏠 Stufe 5</a> | <a href="06-testing.md">🧪 Stufe 6</a> | <a href="07-sources.md">📚 Stufe 7</a>
</p>
<p align="center">
  <a href="../README.md">🏠 Zurück zur Übersicht</a>
</p>
