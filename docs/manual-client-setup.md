# Manuelles Client-Setup (Windows, Android, iOS)

Manchmal möchtest du DNS-Filter nur auf einem bestimmten Gerät nutzen (z.B. auf dem Arbeitslaptops) oder auch unterwegs im mobilen Datennetz geschützt sein. Hier erfährst du, wie du "Privates DNS" (DoH/DoT) direkt am Endgerät einrichtest.

## 📱 Android (ab Version 9)
Android unterstützt natives DNS-over-TLS (DoT).
1.  Gehe zu **Einstellungen** -> **Netzwerk & Internet** (oder Verbindungen).
2.  Wähle **Privates DNS**.
3.  Wähle **Hostname des privaten DNS-Anbieters**.
4.  Gib den Hostnamen ein (z.B. `dnsforge.de` oder `adblock.dns.mullvad.net`).
5.  Speichern.

## 🍎 iOS (iPhone / iPad)
iOS unterstützt verschlüsseltes DNS nativ, bietet aber keine direkte Eingabemaske in den Einstellungen an. Du benötigst ein "Konfigurationsprofil".
1.  Nutze Dienste wie **[dns.notjakob.com](https://dns.notjakob.com/)** oder das Tool von **NextDNS**, um ein Profil zu erstellen.
2.  Lade das Profil herunter.
3.  Gehe zu **Einstellungen** -> **Profil geladen** -> **Installieren**.
4.  Unter **Einstellungen** -> **Allgemein** -> **VPN, DNS und Geräteverwaltung** kannst du es später verwalten.

## 💻 Windows 11
Windows 11 unterstützt DNS-over-HTTPS (DoH) direkt in den Einstellungen.
1.  Gehe zu **Einstellungen** -> **Netzwerk und Internet** -> **Ethernet** (oder WLAN).
2.  Klicke auf **DNS-Serverzuweisung bearbeiten**.
3.  Stelle auf **Manuell** um und aktiviere IPv4 (und IPv6).
4.  Gib die IP des DNS-Servers ein (z.B. `176.9.93.198` für dnsforge).
5.  Wähle unter "DNS über HTTPS" die Option **Ein (automatischer Vorlagentest)**.

## 🌐 Browser-spezifisch (DoH)
Du kannst DNS-over-HTTPS auch nur im Browser aktivieren (unabhängig vom Betriebssystem):
*   **Chrome/Edge:** Einstellungen -> Datenschutz & Sicherheit -> Sicherheit -> "Sicheres DNS verwenden".
*   **Firefox:** Einstellungen -> Datenschutz & Sicherheit -> "DNS über HTTPS" (ganz unten).

---
[← Zurück zur Übersicht](../README.md)
