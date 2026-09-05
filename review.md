# Code & Documentation Review

**Repository:** [grapefruit89/FritzBoxBlacklist](https://github.com/grapefruit89/FritzBoxBlacklist)  
**Scope:** Dokumentation, Dual-Stack, DoT/DoH, Self-Hosting, Tests  
**Basis:** `master` vor diesem Commit (`docs/`, `legacy/`)

## Executive Assessment

Nuetzliches Stufen-Curriculum, mittlere Reife. Die Dokumentation behandelt IPv4-DNS, IPv6-DNS, Router-DNS, Client-DNS, DoT, DoH und Filter so, als waeren sie **eine** Kontrollebene. Das sind sie nicht.

| Ebene | Was das Repo dokumentiert | Was den Pfad wirklich steuert |
| --- | --- | --- |
| IPv4 DHCP DNS | Ja (Stufe 1, 5 Weg B) | DHCPv4 Option 6 |
| IPv6 DNS | Ein Satz in `fritzbox-basics.md` | RA RDNSS, DHCPv6, ULA, WAN-DNSv6 |
| Router-Uplink | DoT-Hostname, drei Klicks | WAN-DoT plus Fallback |
| Client-DNS | `manual-client-setup.md` | Browser-DoH, Windows-11-DoH, Android Private DNS |
| Filter | Cloud-Hostname oder Pi-hole | Wer die Query tatsaechlich bekommt |

Filter ≠ Verschluesselung ≠ Logging-Politik ≠ DNSSEC.

---

## 1. Critical Weaknesses

### 1.1 IPv6 fehlt in der Haupttabelle — Severity: high

`docs/01-alternative-dns.md` listet nur IPv4. Stufe 5 Weg B geht nur in die **IPv4-Konfiguration** (`192.168.178.X`). SLAAC-Clients nutzen RA/RDNSS und laufen am Filter vorbei.

```
Client
 ├── IPv4 DNS → FRITZ!Box / Filter → gewollte Policy
 └── IPv6 DNS → ISP-Resolver          → unkontrolliert
```

### 1.2 "IPv6 deaktivieren" — Severity: high

Stufe 6: *Deaktiviere IPv6 testweise oder konfiguriere es ebenfalls.*

Isolationsprobe: erlaubt, 60 Sekunden. Dauerloesung: verboten. Danach IPv6 explizit konfigurieren.

### 1.3 DoT nicht operationalisiert — Severity: high

DoT auf der Box ist **WAN-seitig**. LAN bleibt Port 53. DoH im Browser umgeht Filter und Pi-hole.

Fehlt in der Anleitung:

- IPv4- **und** IPv6-Felder plus Aufloesungsnamen
- mehrere Namen mit Semikolon
- Fallback auf Klartext (Verfuegbarkeit vs. "immer TLS")
- Zertifikat = Hostname
- Online-Monitor `(DoT verschluesselt)` fuer beide Familien

### 1.4 Keine Validierung von Encryption und IPv6-Leak — Severity: high

`nslookup` / `dig` beweisen nur den Port-53-Responder.

| Schicht | Frage | Werkzeug |
| :---: | :--- | :--- |
| 1 | Wer antwortet im LAN? | `dig example.com` |
| 2 | IPv4-Pfad | `dig A example.com` |
| 3 | IPv6-Pfad | `dig -6 AAAA example.com` |
| 4 | Transport | Online-Monitor, `kdig +tls-ca +tls-host=...` |
| 5 | Zertifikat | dieselbe `kdig`-Zeile |
| 6 | Draht | `tcpdump ... port 53 or port 853` |

### 1.5 Weitere Luecken

- Gastnetz / Mesh / Weg A vs. Weg B nicht modelliert
- kein Hinweis, Port 53/853 von Clients ausser zum Resolver zu blocken
- Marketing-Labels statt Logging-Matrix

### 1.6 Kuketz und Privacy-Handbuch zitiert, nicht angewandt — Severity: high

Stufe 7 verlinkt beides. Stufe 1 folgt ihnen nicht.

| Repo Stufe 1 | Kuketz / Privacy-Handbuch |
| --- | --- |
| Digitalcourage = `5.1.66.255` | Das ist **ffmuc** (`dot.ffmuc.net`). Digitalcourage: `dns3.digitalcourage.de` / `5.9.164.112` / `2a01:4f8:251:554::2`, **nur DoT**. |
| dnsforge = `94.16.114.222` | `176.9.93.198` / `176.9.1.117` plus IPv6, extra `hard.dnsforge.de` |
| Mullvad = nur `194.242.2.2` | Hostnamen sind verschiedene Produkte (`dns.`, `base.`, `adblock.`, ...) |
| Cloudflare = Privacy-first | Speed-Option, Logs ~25 h, kein Privacy-Default |
| Google in der Haupttabelle | Logging-Beispiel, nicht fuer Datenschutz |

Quellen:

- https://www.kuketz-blog.de/empfehlungsecke/#dns
- https://www.privacy-handbuch.de/handbuch_93d.htm

---

## 2. Optimization Roadmap (ROI)

1. **Hoechstes ROI** — Stufe-1-Tabelle: IPv4 + IPv6 + DoT + DoH, sourced aus Kuketz/PH, Digitalcourage ≠ ffmuc zuerst korrigieren.
2. **Hoch** — Stufe 6: sechs Testschichten, IPv6-Disable nur als Isolation.
3. **Hoch** — Kapitel Advanced DoT (Fallback, Zertifikat, Semikolon, Gastnetz).
4. **Mittel-hoch** — Logging-/Filter-Matrix, datiert.
5. **Mittel-hoch** — eine Policy-Ebene in `manual-client-setup.md` (DoH-Bypass).
6. **Mittel** — Stufe 5 dual-stack: ULA, DNSv6 im Heimnetz, RA.
7. **Spaeter** — Firewall-Cookbook, DoT-Cert-Lint, Screenshots.

Reihenfolge: Tabelle und Tests vor Self-Hosting-Umbau.

---

## Schreibweise dieses Repos

Inspiration, keine Klappboxen:

- https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax
- https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting
- https://github.github.com/gfm/
