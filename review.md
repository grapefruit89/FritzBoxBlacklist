# Review — FritzBoxBlacklist

**Repo:** [grapefruit89/FritzBoxBlacklist](https://github.com/grapefruit89/FritzBoxBlacklist)  
**Branch dieses Dokuments:** `master`  
**Begleitdateien:** [`README.md`](README.md), [`README.alternative.md`](README.alternative.md)

## Was in diesem Chat zusammengetragen wurde

1. Code-/Doku-Review der acht Stufen (`docs/00`–`07`, `fritzbox-basics.md`, `manual-client-setup.md`, `legacy/`).
2. ChatGPT-Zweitmeinung: Kontrollebenen-These, Fallback/Zertifikat, Testschichten, Threat-Model — uebernommen wo sie schaerfer waren.
3. Kuketz-Empfehlungsecke und Privacy-Handbuch 93d als Massstab (Stufe 7 verlinkt sie, Stufe 1 folgt ihnen nicht).
4. Alternatives Root-README plus zweite Datei `README.alternative.md` mit GFM/Advanced-Formatting, **ohne** `<details>`.
5. Kein weiterer Feature-Branch. Arbeit liegt auf `master`.

---

## Executive Assessment

Nuetzliches Curriculum, mittlere Reife. Die Doku behandelt IPv4, IPv6, Router-DNS, Client-DNS, DoT, DoH und Filter als **eine** Kontrollebene. Das sind sie nicht.

| Ebene | Repo heute | Was den Pfad steuert |
| --- | --- | --- |
| IPv4 DHCP | Stufe 1, Stufe 5 Weg B | DHCPv4 Option 6 |
| IPv6 DNS | Ein Satz in `fritzbox-basics.md` | RA RDNSS, DHCPv6, ULA |
| WAN-DoT | Hostname, drei Klicks | DoT plus Fallback-Haken |
| Client-DNS | `manual-client-setup.md` | Browser-/OS-DoH |
| Filter | Cloud-Hostname oder Pi-hole | Wer die Query wirklich bekommt |

Filter ≠ Encryption ≠ Logging ≠ DNSSEC.

---

## 1. Critical Weaknesses

### 1.1 IPv6-Neglect — high

Stufe-1-Tabelle nur IPv4. Stufe 5 nur **IPv4-Konfiguration** / `192.168.178.X`. SLAAC-Clients gehen ueber RA am Filter vorbei.

### 1.2 IPv6-Disable-Fallacy — high

Stufe 6: *Deaktiviere IPv6 testweise oder konfiguriere es ebenfalls.* Isolation ja (60 s). Dauerloesung nein. Danach IPv6 konfigurieren.

### 1.3 DoT nicht operationalisiert — high

DoT ist WAN-seitig. LAN bleibt Port 53. DoH im Client ist Bypass.

Fehlt: v4+v6-Felder plus Aufloesungsname, Semikolon, Fallback-Klartext, Zertifikat=Hostname, Online-Monitor fuer beide Familien, eine Policy-Ebene.

### 1.4 Keine Validierung — high

`dig` / `nslookup` beweisen kein TLS und keinen IPv6-Pfad.

Noetig: Monitor `(DoT verschluesselt)`, `dig -6`, `kdig +tls-ca +tls-host=`, optional `tcpdump 53/853`, Firefox-DoH an/aus.

### 1.5 Weitere Luecken

Gastnetz/Mesh, kein Port-53-Intercept, Marketing statt Logging-Matrix, 500-Limit gilt nur fuer Kindersicherung.

### 1.6 Eigene Quellen ignoriert — high

| Stufe 1 | Kuketz / Privacy-Handbuch |
| --- | --- |
| Digitalcourage = `5.1.66.255` | **ffmuc** / `dot.ffmuc.net`. Digitalcourage = `dns3.digitalcourage.de` `5.9.164.112` `2a01:4f8:251:554::2`, nur DoT |
| dnsforge = `94.16.114.222` | `176.9.93.198` / `176.9.1.117` + IPv6, extra `hard.dnsforge.de` |
| Mullvad nur `194.242.2.2` | Hostnamen sind Produkte (`dns.` `base.` `adblock.`) |
| Cloudflare Privacy-first | Speed, Logs ~25 h |
| Google in der Haupttabelle | Logging-Beispiel |

https://www.kuketz-blog.de/empfehlungsecke/#dns  
https://www.privacy-handbuch.de/handbuch_93d.htm

---

## 2. Roadmap nach ROI

Sortiert: Wirkung geteilt durch Aufwand. Nicht nach Attraktivitaet.

| Rang | Aufgabe | ROI | Aufwand | Warum zuerst / spaeter |
| :---: | :--- | :---: | :---: | :--- |
| 1 | Stufe-1-Tabelle: IPv4 + IPv6 + DoT + DoH, sourced Kuketz/PH. Digitalcourage ≠ ffmuc, dnsforge-Anycast, Mullvad-Hostnamen | hoechstes | niedrig | Jeder kopiert diese Seite |
| 2 | Stufe 6: sechs Testschichten. IPv6-aus nur Isolation | hoechstes | niedrig | Fehlerfall ist der einzige Moment fuer extra Kommandos |
| 3 | Kapitel Advanced DoT: Fallback, Zertifikat, Semikolon, Gastnetz, Blacklist vs. Resolver | hoch | mittel | AVM-spezifischer Mehrwert |
| 4 | Logging-/Filter-Matrix, datiert, Jurisdiktion | hoch | mittel | Privacy-Claims belegbar machen |
| 5 | `manual-client-setup.md`: eine Policy-Ebene, DoH-Bypass | mittel-hoch | niedrig | Windows 11 / Firefox Default-DoH |
| 6 | Stufe 5 dual-stack: ULA, DNSv6 im Heimnetz, RA, Docker-v6, Fail-open/closed | mittel | hoch | Minderheit der Leser, hoher Schreibaufwand |
| 7 | Firewall 53/853, DoT-Cert-Lint, Screenshots, DoH3-Notiz | niedrig | variabel | Haertung, nicht Einstieg |

**Woche 1:** Rang 1, 2, 5.  
**Woche 2:** Rang 3, 4.  
**Danach:** Rang 6, 7.

Nicht auf Rang 6 warten, bevor die Tabelle stimmt.

---

## Markdown-Regeln fuer Folge-Edits

Nutzen: GFM-Tabellen, Tasklisten, Strike, Alerts, Fenced Code inkl. `diff`/`mermaid`/`bash`, Math, Footnotes, `<kbd>`.

Nicht nutzen: `<details>` / `<summary>`.

Doku:

- https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax
- https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting
- https://github.github.com/gfm/
