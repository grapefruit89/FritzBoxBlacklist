# Etappe 1: Öffentliche alternative DNS-Server

Wenn du dich entscheidest, den DNS deines Anbieters zu verlassen, sind große öffentliche Anbieter oft die erste Anlaufstelle. Sie sind meist sehr schnell und zuverlässig.

## Bekannte Anbieter

| Anbieter | IP-Adressen | Fokus |
| :--- | :--- | :--- |
| **Cloudflare** | `1.1.1.1`, `1.0.0.1` | Maximale Geschwindigkeit & grundlegender Datenschutz. |
| **Google** | `8.8.8.8`, `8.8.4.4` | Hohe Verfügbarkeit, aber Teil des Google-Ökosystems. |

## Geschwindigkeit vs. Privatsphäre

*   **Vorteil Geschwindigkeit:** Dienste wie Cloudflare (1.1.1.1) sind oft die schnellsten DNS-Resolver weltweit. Das macht das Surfen gefühlt flüssiger.
*   **Privatsphäre-Check:** Diese Anbieter versprechen zwar, keine Logs dauerhaft zu speichern, aber es bleiben US-Unternehmen. Für viele Nutzer ist das dennoch ein riesiger Sprung nach vorne im Vergleich zum lokalen Internetanbieter.

## Wie trägt man das ein? (Klassisch)

In der FritzBox unter:
`Internet` -> `Zugangsdaten` -> `DNS-Server`

Hier kannst du die oben genannten IPs unter "Andere DNSv4-Server verwenden" eintragen. Das ist die "klassische" Methode ohne Verschlüsselung.

---
[⬅️ Zurück zur Übersicht](../README.md)
