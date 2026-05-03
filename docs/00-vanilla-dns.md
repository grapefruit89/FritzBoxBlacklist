# 🍦 Stufe 0: Standard-DNS vom Anbieter (Vanilla)

[⬅️ Zurück zur Übersicht](../README.md)

Willkommen! Ohne Änderungen nutzt du das **Standard-DNS deines Providers** (Telekom, Vodafone, o2). Setup: „Vanilla“ – Standard-Geschmack. Funktioniert, aber wenig Privatsphäre.

---

## 📖 Was passiert hier?

Internet = Telefonbuch. `google.de` → DNS-Anfrage → IP-Adresse (`142.250.185.163`).

1. Gerät fragt **FritzBox**: „Wo wohnt `google.de`?“
2. FritzBox fragt **Provider-DNS**: „IP von `google.de` bitte.“
3. Provider antwortet → Browser lädt Seite.

> [!IMPORTANT]
> Problem: Wer das Telefonbuch kontrolliert, sieht **wen du wann angerufen hast**.

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
  <a href="01-alternative-dns.md">Stufe 1 ➡️</a>
</p>

[⬅️ Zurück zur Übersicht](../README.md)

