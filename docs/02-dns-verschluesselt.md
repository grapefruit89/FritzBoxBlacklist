# 💊 Stufe 2: DNS verschlüsseln

Standard-DNS-Anfragen sind wie eine Postkarte: Jeder auf dem Weg kann mitlesen, wen du besuchst. Jetzt schicken wir stattdessen einen **versiegelten Brief**.

> [!TIP]
> **Die Metapher:** Das ist die **rote Pille**. Du entscheidest dich dafür, den Tunnel der Überwachung zu verlassen. Deine Anfragen werden in einen unknackbaren Safe gelegt, bevor sie dein Haus verlassen.

---

## 🔒 Warum Verschlüsselung?

Ohne Verschlüsselung (Port 53) kann dein Internetanbieter, der WLAN-Betreiber im Café oder ein Angreifer im Netzwerk genau sehen, welche Domains du aufrufst.

1.  **DoT (DNS over TLS):** Der Standard für Router wie die Fritz!Box. Nutzt Port 853.
2.  **DoH (DNS over HTTPS):** Der Standard für Browser. Versteckt DNS-Anfragen im normalen Web-Traffic.

---

## 📊 Anbieter mit nativer Verschlüsselung

Diese Anbieter unterstützen den DoT-Standard der Fritz!Box perfekt.

| Anbieter | DoT-Hostname | Besonderheiten | Herkunft |
| :--- | :--- | :--- | :---: |
| ![CH](https://flagcdn.com/w20/ch.png) [**Quad9**](https://www.quad9.net/) | `dns.quad9.net` | Fokus auf Malware-Schutz. | ![CH](https://flagcdn.com/w20/ch.png) CH |
| ![DE](https://flagcdn.com/w20/de.png) [**dnsforge.de**](https://dnsforge.de/) | `dnsforge.de` | Werbefrei & keine Logs (Kuketz-Favorit). | ![DE](https://flagcdn.com/w20/de.png) DE |
| ![SE](https://flagcdn.com/w20/se.png) [**Mullvad**](https://mullvad.net/) | `base.dns.mullvad.net` | Maximale Anonymität aus Schweden. | ![SE](https://flagcdn.com/w20/se.png) SE |
| ![US](https://flagcdn.com/w20/us.png) [**Cloudflare**](https://1.1.1.1/) | `one.one.one.one` | Schnellster globaler Resolver. | ![US](https://flagcdn.com/w20/us.png) US |


---

<p align="center">
  <a href="00-vanilla-dns.md">🍦 Stufe 0</a> | <a href="01-alternative-dns.md">⚡ Stufe 1</a> | 💊 Stufe 2 | <a href="03-dns-verschluesselt-adblock.md">🛡️ Stufe 3</a> | <a href="04-cloud-adblocker.md">☁️ Stufe 4</a> | <a href="05-selfhosting.md">🏠 Stufe 5</a> | <a href="06-testing.md">🧪 Stufe 6</a> | <a href="07-sources.md">📚 Stufe 7</a>
</p>
<p align="center">
  <a href="../README.md">🏠 Zurück zur Übersicht</a>
</p>
