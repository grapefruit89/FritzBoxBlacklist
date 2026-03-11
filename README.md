<div align="center">
  <h1>🛡️ DNS-Blocker & Heimnetz-Sicherheit</h1>
  <p><b>Schluss mit Werbung, Tracking und Malware – für das ganze Netzwerk.</b></p>
  
  [![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](#lizenz)
  [![PRs welcome](https://img.shields.io/badge/contributions-welcome-green.svg)](#mitwirken)
</div>

---

## 📖 Wie funktioniert ein DNS-Adblocker?

Stell dir vor, das Internet ist eine riesige Stadt und der **DNS-Server ist das Telefonbuch**. 
Wenn du `bild.de` in deinen Browser eintippst, schaut dein Gerät im DNS-Telefonbuch nach, unter welcher Hausnummer (IP-Adresse) die Seite zu finden ist. 

Die Webseite lädt aber nicht nur den eigentlichen Artikel, sondern fragt im Hintergrund dutzende andere Adressen nach Werbebannern und unsichtbaren Trackern. 

**Was macht ein DNS-Adblocker?**  
Er ist ein zensiertes Telefonbuch. Wenn dein Gerät nach der Adresse für `werbung-nervt.com` fragt, sagt der DNS-Server einfach: *"Gibt's nicht!"* (oder er gibt eine falsche Adresse zurück). Die Werbung kann nicht geladen werden, die Lücken auf der Webseite bleiben leer – und dein Netz ist schneller und sicherer.

---

## 🚦 Das Overblocking-Ampelsystem

Wenn ein DNS-Server zu streng ist, reißt er aus Versehen "gute" Seiten aus dem Telefonbuch. Das nennt man **Overblocking**. Plötzlich laden bestimmte Webseiten nicht mehr richtig oder Links in Newslettern (die über Tracker laufen) führen ins Nichts. 

Damit du den passenden Server für deinen Haushalt (und deine Nerven) findest, nutzen wir dieses Ampelsystem:

*   🟢 **Gering:** Sehr behutsam. Blockt primär Malware und die schlimmsten Tracker. Keine Einschränkungen im Alltag zu erwarten. (WAF: Wife/Roommate Acceptance Factor = Hoch)
*   🟡 **Mittel:** Der beste Kompromiss. Blockt fast alle Werbung. Affiliate-Links (z.B. von Deal-Plattformen) könnten manchmal ins Leere laufen.
*   🔴 **Hoch:** Sehr aggressiv. Blockt auch Telemetrie von Smart-TVs oder Windows. Kann dazu führen, dass Apps streiken. Nur für Nutzer, die wissen, wie man Whitelists pflegt!

---

## 🛜 Die besten DNS-Server (Empfehlungen)

Hier findest du eine kuratierte Liste von DNS-Diensten, inspiriert durch Foren wie Kuketz-IT-Security. Alle hier gelisteten Server nehmen Datenschutz ernst (kein Logging).

> **🔒 Info zu DoT / DoH:** Trage in deinen Router oder dein Handy wenn möglich immer die verschlüsselten Adressen (DNS-over-TLS oder DNS-over-HTTPS) ein. So kann nicht einmal dein Internetanbieter (Telekom, Vodafone) mitlesen, welche Seiten du besuchst!

### 🧩 Teil 1: Set & Forget – Eintragen und vergessen
Keine Registrierung, keine Accounts. Einfach die IPs oder den DoT-Hostnamen im Router eintragen.

| Anbieter | Standort | Filterung | Logs | Overblocking | DoT / DoH Hostname | IPv4 (Fallback) |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Mullvad (Adblock)** | 🇸🇪 SE / Global | Werbung, Tracker, Malware | ❌ Nein | 🟡 Mittel | `adblock.dns.mullvad.net` | `194.242.2.3` |
| **Quad9 (Threat)** | 🇨🇭 CH / Global | Malware, Phishing (keine Ads!) | ❌ Nein | 🟢 Gering | `dns.quad9.net` | `9.9.9.9` |
| **DigiGes** | 🇨🇭 CH | Zensurfrei, ungefiltert | ❌ Nein | 🟢 Keine | `dns.digitale-gesellschaft.ch` | `5.1.66.255` |
| **DNS0.eu (Zero)** | 🇪🇺 EU | Malware, Phishing (EU-Fokus) | ❌ Nein | 🟢 Gering | `zero.dns0.eu` | `193.110.81.9` |
| **LibreDNS (NoAds)**| 🇩🇪 DE | Werbung, Tracker | ❌ Nein | 🟡 Mittel | `doh.libredns.gr` | `116.202.176.26` |
| **DNS.SB** | 🇪🇺 EU | Zensurfrei, ungefiltert | ❌ Nein | 🟢 Keine | `dns.sb` | `185.222.222.222` |

---

### 🧰 Teil 2: Cloud-Dienste mit Web-Oberfläche
Du willst sehen, was blockiert wird, und eigene Ausnahmen (Whitelists) hinzufügen? Diese Dienste bieten dir ein Dashboard in der Cloud.

| Anbieter | Datenschutz | Flexibilität | Schwierigkeit | Overblocking | Besonderheiten |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **[NextDNS](https://nextdns.io/)** | 🇺🇸 US (Server in EU) | Sehr Hoch | 🔵 Leicht | 🟡/🔴 Anpassbar | Kostenlos bis 300k Anfragen/Monat. Tolle UI, viele fertige Listen (OISD, etc.). |
| **[AdGuard DNS](https://adguard-dns.io/de/public-dns.html)**| 🇨🇾 CY / Global | Hoch | 🔵 Leicht | 🟡/🔴 Anpassbar | Sehr einsteigerfreundlich, gute Kindersicherungs-Optionen. |
| **[Control D](https://controld.com/)** | 🇨🇦 CA | Sehr Hoch | 🟠 Mittel | 🟡/🔴 Anpassbar | Bietet extrem feingranulare Filter und Geo-Unblocking (teilw. kostenpflichtig). |
| **[Rethink DNS](https://rethinkdns.com/)** | 🇺🇸 US (Cloudflare) | Hoch | 🔴 Nerd | 🔴 Anpassbar | Open-Source, kostenfrei, riesige Auswahl an Listen, erfordert Einarbeitung. |

---

### 🏠 Teil 3: Self-Hosting (Maximale Souveränität)
Du vertraust keiner Cloud? Dann hoste dein "Telefonbuch" selbst auf einem Raspberry Pi, NAS oder Mini-PC.

| Lösung | Benutzeroberfläche | Ressourcen-Bedarf | Schwierigkeit | Beschreibung |
| :--- | :--- | :--- | :--- | :--- |
| **[AdGuard Home](https://adguard.com/de/adguard-home/overview.html)** | 🟢 Sehr gut | Mittel | 🔵 Leicht | Der aktuelle Favorit. Modernes Interface, out-of-the-box Support für DoH/DoT und detaillierte Statistiken. |
| **[Pi-hole](https://pi-hole.net/)** | 🟡 Gut | Sehr gering | 🟠 Mittel | Der Klassiker. Enorme Community, aber benötigt Zusatz-Software (wie Unbound), um verschlüsseltes DNS (DoT/DoH) zu sprechen. |
| **[Blocky](https://0xerr0r.github.io/blocky/)** | ❌ Keine (YAML) | Minimal | 🔴 Nerd | Extrem leichtgewichtig und schnell. Konfiguration läuft rein über Textdateien. Perfekt für GitOps/NixOS. |
| **[Technitium](https://technitium.com/dns/)** | 🟢 Gut | Hoch (.NET) | 🔴 Nerd | Mächtiger, vollwertiger DNS-Server für fortgeschrittene Heimnetz-Administratoren. |

---

## 🧪 Tests & Tools: Kontrolliere dein Setup

Du hast alles eingestellt? Prüfe hier, ob es wirklich funktioniert:

### 1. Funktioniert der Werbeblocker?
*   **[d3ward Adblock Test](https://d3ward.github.io/toolz/adblock.html):** Ein exzellenter, moderner Test, der prüft, wie viel Prozent der gängigsten Werbe- und Tracking-Domains geblockt werden.
*   **[ads-blocker.com/testing](https://ads-blocker.com/testing/):** Ein visueller Test, der klassische Banner lädt (oder eben nicht).
*   **💣 [bild.de](https://www.bild.de):** Der Endgegner. Wenn BILD dich aussperrt und meckert, dass du einen Adblocker nutzt, funktioniert dein Setup hervorragend! 😉

### 2. Leckt dein DNS? (Privacy Check)
*   **[DNS Leak Test](https://www.dnsleaktest.com/):** Führe den "Extended Test" aus. Hier sollten nur noch Server deines gewählten Anbieters (z.B. Quad9 oder Mullvad) auftauchen, **nicht** mehr die von Telekom/Vodafone/O2.
*   **[1.1.1.1/help](https://1.1.1.1/help):** Zeigt dir direkt an, ob du über DoH (DNS over HTTPS) oder DoT (DNS over TLS) verschlüsselt unterwegs bist.

### 3. Wie einzigartig bist du noch?
*   **[Cover Your Tracks (EFF)](https://coveryourtracks.eff.org/):** Testet, wie stark dein Browser noch über Fingerprinting verfolgt werden kann.

---

## 🏛️ Historie: Die klassische Fritz!Box Blockliste

*Dieses Repository startete einst mit dem Ziel, die von AVM eingebauten Filter-Listen der Fritz!Box optimal auszureizen.*

Die Fritz!Box erlaubt in der Kindersicherung das Eintragen einer Blacklist – diese ist jedoch **hart auf 500 Einträge limitiert**. In einer Zeit, in der Blocklisten wie OISD oder StevenBlack hunderte von Tausenden Domains umfassen, ist dieses 500er-Limit schlichtweg nicht mehr zeitgemäß, um ein Heimnetz effektiv zu schützen.

**Warum wir von der Fritz!Box-Liste abraten:**
1. Es ist ein ständiges Katz-und-Maus-Spiel. Werbenetzwerke wechseln ihre Domains schneller, als man 500 Plätze manuell pflegen kann.
2. Es blockiert nur HTTP(S) auf rudimentärer Ebene, schützt aber nicht vor Tracking innerhalb von Apps oder Smart-TVs.

**Wer sie aus historischen oder infrastrukturellen Gründen (z.B. im Gastnetz) dennoch nutzen will:**
In den [Releases / alten Commits](https://github.com/grapefruit89/FritzBoxBlacklist/blob/master/Fritz%20500%202020-11-23.txt) findest du unsere alte, manuell kuratierte Top-500 Liste. *Hinweis: Diese wird nicht mehr aktiv gepflegt.*

---

## 🔗 Quellen & Weiterführende Links

*   **[Kuketz IT-Security Forum - DNS Vergleichstabelle](https://www.kuketz-forum.de/t/tabelle-dns-server-vergleichstabelle/9643):** Eine großartige, detaillierte Übersicht und Diskussion zu datenschutzfreundlichen DNS-Servern (die Inspiration für unsere Tabellen).
*   [The Firebog](https://firebog.net/): Die beste Anlaufstelle für Blocklisten (falls du AdGuard Home oder Pi-hole selbst hostest).
*   [StevenBlack/hosts](https://github.com/StevenBlack/hosts): Die wohl bekannteste kuratierte Host-Datei zur Filterung.
*   [Pi-hole Forum](https://discourse.pi-hole.net/): Unerschöpfliche Wissensquelle zu Regex-Filtern und DNS-Problemen.

---

## 📜 Lizenz

[MIT License](https://opensource.org/licenses/MIT) – freie Nutzung mit Namensnennung.
