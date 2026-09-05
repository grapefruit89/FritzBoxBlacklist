# Code & Documentation Review

**Repository:** [grapefruit89/FritzBoxBlacklist](https://github.com/grapefruit89/FritzBoxBlacklist)

Vollstaendige Review liegt in diesem Branch. Die ausgearbeitete Fassung folgt direkt — siehe auch lokale Arbeitskopie.

## Kurzfassung

Die Dokumentation behandelt IPv4-DNS, IPv6-DNS, Router-DNS, Client-DNS, DoT, DoH und Filter so, als waeren sie eine Kontrollebene. Das sind sie nicht.

Kritisch:
- Stufe-1-Tabelle nur IPv4
- Digitalcourage `5.1.66.255` ist ffmuc (`dot.ffmuc.net`); Digitalcourage ist `dns3.digitalcourage.de` / `5.9.164.112`
- dnsforge-Anycast in Stufe 1 veraltet (`94.16.114.222` vs. `176.9.93.198`)
- Stufe 6 empfiehlt IPv6-Deaktivieren als Workaround
- DoT-Fallback und Zertifikatspruefung fehlen
- Kuketz und Privacy-Handbuch stehen in Stufe 7, steuern die Tabelle aber nicht

Die vollstaendige Review mit Roadmap steht in der Arbeitskopie und wird als vollstaendige `review.md` nachgezogen.
