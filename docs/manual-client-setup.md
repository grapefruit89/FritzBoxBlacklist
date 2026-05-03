# Manuelles Client-Setup (Sicheres DNS & Adblocking)
[⬅️ Zurück zur Übersicht](../README.md)

Nutze DNS-Filter unterwegs (Mobilfunk/öffentliches WLAN) oder gezielt für einzelne Geräte.

> [!TIP]
> Client-seitiges Setup ist ideal für Schutz außerhalb des Heimnetzes (z.B. unterwegs).

---

## 📱 Android (ab Version 9)
Natives DNS-over-TLS (DoT).
1. **Einstellungen** → **Netzwerk & Internet** → **Privates DNS**.
2. **Hostname des privaten DNS-Anbieters** wählen.
3. Hostname eingeben (z.B. `dnsforge.de` oder `adblock.dns.mullvad.net`).
4. **Speichern**.

## 🍎 iOS & iPadOS
Natives DoH/DoT via Konfigurationsprofil.
1. Profil erstellen: **[dns.notjakob.com](https://dns.notjakob.com/)** oder NextDNS.
2. Profil laden, dann **Einstellungen** → **Profil geladen** → **Installieren**.
3. Verwaltung: **Einstellungen** → **Allgemein** → **VPN, DNS und Geräteverwaltung**.

## 💻 macOS
1. **Systemeinstellungen** → **Netzwerk**.
2. Verbindung wählen → **Details...** → **DNS**.
3. Über `+` DNS-Server-IPs hinzufügen.

> [!NOTE]
> macOS unterstützt DoH/DoT nativ am besten via Konfigurationsprofil (analog zu iOS).

---

## 🪟 Windows 11 & 10

### Windows 11 (Natives DoH)
1. **Einstellungen** → **Netzwerk & Internet** → **WLAN/Ethernet**.
2. **DNS-Serverzuweisung** → **Bearbeiten**.
3. **Manuell**, IPv4/IPv6 aktivieren.
4. IPs eintragen. **DNS über HTTPS** auf **Ein (automatischer Vorlagentest)**.

### Windows 10
1. **Systemsteuerung** → **Netzwerkcenter** → **Adaptereinstellungen**.
2. Rechtsklick Adapter → **Eigenschaften** → **IPv4** → **Eigenschaften**.
3. DNS-IPs eintragen.

> [!NOTE]
> Windows 10 unterstützt natives DoH nur eingeschränkt (Insider-Builds). Nutze Browser-Einstellungen oder Tools wie YogaDNS.

---

## 🐧 Linux (systemd-resolved)
1. `/etc/systemd/resolved.conf` editieren:
   ```ini
   DNS=9.9.9.9
   DNSOverTLS=yes
   ```
2. `systemctl restart systemd-resolved`.

---

## 🌐 Browser (Secure DNS)
Unabhängig vom Betriebssystem (DoH).
- **Firefox:** Einstellungen → Datenschutz & Sicherheit → **DNS über HTTPS**.
- **Chrome/Edge:** Einstellungen → Datenschutz & Sicherheit → Sicherheit → **Sicheres DNS**.

---

<p align="center">[⬅️ Stufe 7 (Quellen)](07-sources.md)</p>

[⬅️ Zurück zur Übersicht](../README.md)
