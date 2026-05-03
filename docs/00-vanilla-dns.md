# 🍦 Stufe 0: Standard-DNS vom Anbieter (Vanilla)

[⬅️ Zurück zur Übersicht](../README.md)

Willkommen! Ohne Änderungen nutzt du das **Standard-DNS deines Providers** (Telekom, Vodafone, o2). Setup: „Vanilla“ – Standard-Geschmack. Funktioniert, aber wenig Privatsphäre.

---

## 📖 Wie findet dein Computer eine Webseite? – Die Anfänger-Erklärung

Stell dir vor, du willst deine Oma besuchen, kennst aber ihre Hausnummer nicht. Du gehst zu einem Kiosk, der ein dickes Telefonbuch hat, und fragst: *„In welcher Hausnummer wohnt Oma Müller?“* Der Kioskbesitzer schaut nach und sagt: *„Blumenstraße 42“*. Jetzt kannst du hinfahren.

So ähnlich funktioniert das Internet:

- Du tippst **google.de** in dein Handy oder deinen Browser.
- Dein Router (die Fritz!Box) fragt einen **DNS-Server** (den „Kiosk“): *„Welche Nummer gehört zu google.de?“*
- Der DNS-Server antwortet mit einer Nummer (z. B. `142.250.185.163`), und dein Gerät holt die Seite ab.

> [!IMPORTANT]
> **Das Problem:** Wenn du nichts änderst, gehört der „Kiosk“ deinem Internet-Anbieter (z. B. Telekom oder Vodafone). Der Anbieter schreibt sich genau auf, wen du wann „besuchen“ wolltest. So weiß er sehr viel über dein Privatleben.

---

## 🚩 5 Nachteile von Vanilla-DNS

### 1. Tracking (Provider sieht ALLES)
Jede aufgerufene Domain geht über Provider-DNS.
- Banking, Gesundheit, Vorlieben: Provider weiß Bescheid.
- Datenprofile sind wertvoll für Tracking.

> [!WARNING]
> Profilbildung deines digitalen Lebens – oft ohne dein Wissen.

### 2. Zensur (CUII-Sperren)
Provider sperren Webseiten via DNS (z. B. Streaming, E-Book-Archive).
- Ergebnis: „Adresse existiert nicht“ oder Warnseite.
- Hintergründe in [Stufe 7: Quellen](07-sources.md).

### 3. DNS-Hijacking & Manipulation
Tippfehler (`google.dee`) → Provider leitet auf eigene Suchseite mit Werbung um.
- Telekom nennt es „Navigationshilfe“.
- Realität: DNS-Antwort gefälscht für Werbung/Tracking.

### 4. Keine Verschlüsselung
Standard: **Port 53 (UDP)**. Komplett unverschlüsselt.
- Mitlesbar im lokalen Netz oder durch den Provider.

### 5. Performance
Provider-Server oft langsam oder überlastet. Verzögert den Seitenaufbau spürbar.

---

## 🛠️ Selbsttest: Was nutzt du?

### 👉 Schnelltest (Windows/Mac/Linux)

1. Terminal öffnen.
2. Befehl: `nslookup google.com`
3. Zeile **„Server“**: `fritz.box` oder Router-IP = Provider-DNS aktiv.
4. Check auf **[DNSLeakTest.com](https://www.dnsleaktest.com)**. Erscheint dein Provider? Dann Stufe 0.


---

## 📊 Vergleich: Vanilla vs. Custom DNS

| Feature | Vanilla (Stufe 0) | Custom [(ab Stufe 1)](01-alternative-dns.md) |
| :--- | :---: | :---: |
| **Privatsphäre** | ❌ Niedrig | ✅ Hoch |
| **Werbefrei** | ❌ Nein | ✅ Ja [(ab Stufe 3)](03-dns-verschluesselt-adblock.md) |
| **Zensurfrei** | ❌ Nein | ✅ Ja |
| **Verschlüsselung** | ❌ Keine | ✅ Ja (DoT/DoH) |

---

> [!TIP]
> **Nächster Schritt:**  
> In [Stufe 1: Alternative DNS-Anbieter](01-alternative-dns.md) Kontrolle zurückgewinnen.

---

<p align="center">
  **0** | <a href="01-alternative-dns.md">1</a> | <a href="02-dns-verschluesselt.md">2</a> | <a href="03-dns-verschluesselt-adblock.md">3</a> | <a href="04-cloud-adblocker.md">4</a> | <a href="05-selfhosting.md">5</a> | <a href="06-testing.md">6</a> | <a href="07-sources.md">7</a>
</p>
<p align="center">
  <a href="../README.md">🏠 Zurück zur Übersicht</a>
</p>


