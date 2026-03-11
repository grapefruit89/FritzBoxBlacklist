<div align="center">
  <h1>🛡️ DNS-Blocker & Heimnetz-Sicherheit</h1>
  <p><b>Schluss mit Werbung, Tracking und Malware – für das ganze Netzwerk.</b></p>
  
  [![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](#lizenz)
  [![PRs welcome](https://img.shields.io/badge/contributions-welcome-green.svg)](#mitwirken)
</div>

---

## 📖 Wie funktioniert ein DNS-Adblocker?

Stell dir vor, das Internet ist eine riesige Stadt und der **DNS-Server ist das Telefonbuch**. 
Wenn du eine Adresse wie 'bild.de' suchst, schaut dein Browser im DNS-Telefonbuch nach der Hausnummer (IP).

**Der Adblocker-Trick:**  
Ein DNS-Server, der Werbung filtert, ist wie ein Telefonbuch, aus dem jemand die **Seiten von Werbefirmen und Trackern einfach herausgerissen hat**. Wenn dein Handy nach der Nummer von 'werbung-nervt.com' fragt, sagt das Telefonbuch: 'Gibt es nicht!'. Die Werbung wird gar nicht erst geladen – dein Internet wird schneller und privater.

---

## 🚦 Das Overblocking-Ampelsystem

Manchmal reißt ein DNS-Filter aus Versehen eine 'gute' Seite raus. Das nennt man **Overblocking**. 

*   🟢 **Gering:** Blockt nur Malware/Phishing. Keine Störungen im Alltag. (WAF: Hoch)
*   🟡 **Mittel:** Der beste Kompromiss. Blockt fast alle Werbung. Affiliate-Links könnten streiken.
*   🔴 **Hoch:** Sehr aggressiv. Blockt auch Telemetrie (Smart-TV). Nur für Profis mit Whitelist!

---

## 🛜 Die besten DNS-Server (Empfehlungen 2026)

### 🧩 Teil 1: Set & Forget (Eintragen und vergessen)
Keine Anmeldung nötig. Einfach IPs oder DoT-Hostnamen im Router/Handy eintragen.

| Anbieter | Standort | Filterung | Overblocking | DoT / DoH Hostname |
| :--- | :--- | :--- | :--- | :--- |
| **Mullvad (Ads)** | 🇸🇪 SE / Global | Werbung, Tracker | 🟡 Mittel | `adblock.dns.mullvad.net` |
| **dnsforge.de** | 🇩🇪 DE | Werbung, Tracker | 🟡 Mittel | `dnsforge.de` |
| **HaGeZi DNS** | 🇪🇺 EU | Multi-Pro Filter | 🟡 Mittel | `dns.hagezi.com` |
| **Quad9 (Threat)**| 🇨🇭 CH / Global | Malware (Keine Ads) | 🟢 Gering | `dns.quad9.net` |
| **DNS4EU** | 🇪🇺 EU | Malware, Phishing | 🟢 Gering | `protective.joindns4.eu` |
| **DigiGes** | 🇨🇭 CH | Ungefiltert | 🟢 Keine | `dns.digitale-gesellschaft.ch` |

---

### 🧰 Teil 2: Cloud-Dashboards (Mit Web-Oberfläche)
Für Nutzer, die sehen wollen, was blockiert wird und eigene Ausnahmen pflegen möchten.

| Anbieter | Datenschutz | Schwierigkeit | Besonderheiten |
| :--- | :--- | :--- | :--- |
| **[NextDNS](https://nextdns.io/)** | 🇪🇺 EU Server | 🔵 Leicht | Perfekte UI, extrem viele fertige Listen. |
| **[AdGuard DNS](https://adguard-dns.io/de/public-dns.html)**| 🇨🇾 CY / Global | 🔵 Leicht | Sehr familienfreundlich, gute Kindersicherung. |
| **[Control D](https://controld.com/)** | 🇨🇦 CA | 🟠 Mittel | Fokus auf Produktivität und Geo-Steuerung. |
| **[Rethink DNS](https://rethinkdns.com/)** | 🇺🇸 US / Global | 🔴 Nerd | Unzählige Listen kombinierbar, Open-Source. |

---

### 🏠 Teil 3: Self-Hosting (Maximale Kontrolle)
Hoste dein eigenes 'Telefonbuch' auf deinem Server (z.B. NixOS, Pi, NAS).

| Lösung | UI | Ressourcen | Beschreibung |
| :--- | :--- | :--- | :--- |
| **[AdGuard Home](https://adguard.com/)** | 🟢 Top | Mittel | Modern, einfach, unterstützt DoT/DoH nativ. |
| **[Pi-hole](https://pi-hole.net/)** | 🟡 Gut | Minimal | Der Klassiker. Riesige Community. |
| **[Blocky](https://0xerr0r.github.io/blocky/)**| ❌ Keine| Minimal | Rein deklarativ (YAML). Perfekt für NixOS. |
| **[Technitium](https://technitium.com/)**| 🟢 Gut | Hoch | Mächtiger DNS-Server für Netzwerk-Experten. |

---

## 🧪 Tests & Tools: Kontrolliere dein Setup

1.  **[d3ward Adblock Test](https://d3ward.github.io/toolz/adblock.html):** Wie viel % Werbung wird wirklich geblockt?
2.  **[DNS Leak Test](https://www.dnsleaktest.com/):** Tauchen nur noch deine gewählten Anbieter auf (z.B. Mullvad)?
3.  **[1.1.1.1/help](https://1.1.1.1/help):** Prüfe, ob Verschlüsselung (DoH/DoT) aktiv ist.
4.  **💣 [bild.de](https://www.bild.de):** Der 'Endgegner'. Wenn die Seite meckert, ist dein Filter scharf! 😉

---

## 🏛️ Historie & Quellen
*   **Fritz!Box 500:** Aus historischen Gründen findest du in den Releases noch die alte Top-500 Liste für die Fritz!Box-Kindersicherung. Aufgrund des 500er-Limits raten wir heute jedoch zu DoT/DoH oder lokalen Filtern (Teil 1-3).
*   Inspiriert durch das **[Kuketz IT-Security Forum](https://www.kuketz-forum.de/t/tabelle-dns-server-vergleichstabelle/9643)**.

---

## 📜 Lizenz
[MIT License](https://opensource.org/licenses/MIT) – freie Nutzung mit Namensnennung.