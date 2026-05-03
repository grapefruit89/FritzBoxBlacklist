# 🍦 Stufe 0: Standard-DNS vom Anbieter (Vanilla)

Willkommen am Anfang deiner Reise! Wenn du bisher nichts an deinem Router oder deinen Geräten geändert hast, nutzt du mit an Sicherheit grenzender Wahrscheinlichkeit das **Standard-DNS deines Internetproviders** (z. B. Deutsche Telekom, Vodafone, o2).

Man nennt dieses Setup auch „Vanilla“, weil es der Standard-Geschmack ist: Es funktioniert einfach, aber es ist weder besonders sicher noch privat.

---

## 📖 Was passiert hier eigentlich?

Stell dir vor, das Internet ist ein riesiges Telefonbuch. Wenn du `google.de` eingibst, muss dein Computer wissen, unter welcher IP-Adresse (z. B. `142.250.185.163`) der Server erreichbar ist.

1. Dein Gerät fragt die **FritzBox**: „Wo wohnt `google.de`?“
2. Die FritzBox fragt den **Provider-DNS**: „Sag mir die IP von `google.de`.“
3. Der Provider antwortet – und dein Browser lädt die Seite.

> [!IMPORTANT]
> Das Problem: Wer das Telefonbuch kontrolliert, bestimmt nicht nur, wo du landest, sondern weiß auch ganz genau, **wen du wann angerufen hast**.

---

## 🚩 Die 5 größten Nachteile von Vanilla-DNS

### 1. Dein Provider sieht ALLES (Tracking)
Jede Domain, die du aufrufst – egal ob per Browser, App oder Smart-TV – wird über den DNS-Server deines Providers aufgelöst. 
- Dein Provider weiß, wann du Online-Banking machst.
- Dein Provider weiß, welche Gesundheits-Apps du nutzt.
- Dein Provider weiß, wann du Pornos schaust oder politische Foren besuchst.

> [!WARNING]
> Diese Daten sind Gold wert. Auch wenn Provider behaupten, sie nur für den Betrieb zu nutzen, bilden sie ein extrem präzises Profil deines digitalen Lebens.

### 2. Zensur „von oben“ (CUII-Sperren)
In Deutschland gibt es die **CUII** (Clearingstelle Urheberrecht im Internet). Große Provider haben sich verpflichtet, bestimmte Webseiten auf DNS-Ebene zu sperren.

Wenn du eine gesperrte Seite aufrufst, sagt dein Provider einfach: „Diese Adresse gibt es nicht“ oder leitet dich auf eine Warnseite um.
- **Beispiele für Sperren:** Streaming-Seiten (kinox.to), E-Book-Archive (Sci-Hub, Annas Archive) oder Gaming-Seiten.

### 3. DNS-Hijacking & Manipulation
Kennst du das, wenn du dich vertippst (z. B. `google.dee`) und statt einer Fehlermeldung auf einer Suchseite deines Providers mit viel Werbung landest? Das ist **DNS-Hijacking**.

> [!CAUTION]
> Die Telekom nennt das „Navigationshilfe“. In Wahrheit fälscht der Provider die DNS-Antwort, um dir Werbung anzuzeigen und dein Suchverhalten zu tracken. Das hebelt technische Standards aus und stört Programme, die eine echte Fehlermeldung erwarten.

### 4. Fehlende Verschlüsselung
Standard-DNS nutzt meist den Port **53 (UDP)**. Dieser Verkehr ist **komplett unverschlüsselt**. Jeder in deinem lokalen Netzwerk (oder dein Chef im Firmen-WLAN) kann theoretisch mitlesen, welche Seiten du anfragst.

### 5. Performance-Löcher
Provider-DNS-Server sind oft „gut genug“, aber selten die schnellsten. Bei großen Lastspitzen oder Störungen im Netz deines Anbieters kann es zu Verzögerungen kommen – das Internet fühlt sich „zäh“ an, obwohl die Leitung eigentlich schnell ist.

---

## 🛠️ Selbsttest: Was nutzt du gerade?

Möchtest du wissen, wer aktuell dein „Telefonbuch“ verwaltet?

<details>
<summary>👉 Klick hier für den Schnelltest (Windows/Mac/Linux)</summary>

1. Öffne dein Terminal (CMD oder PowerShell bei Windows).
2. Gib folgenden Befehl ein:
   ```bash
   nslookup google.com
   ```
3. Schau dir die Zeile **„Server“** an. Wenn dort etwas wie `fritz.box` oder die IP deines Routers steht, nutzt du das, was der Router vom Provider bekommen hat.
4. Besuche **[DNSLeakTest.com](https://www.dnsleaktest.com)** und mache einen „Standard Test“. Erscheint dort der Name deines Internetanbieters (z. B. AS3320 Deutsche Telekom)? Dann bist du auf Stufe 0.

</details>

---

## 📊 Vergleich: Vanilla vs. Custom DNS

| Feature | Vanilla (Stufe 0) | Custom (ab Stufe 1) |
| :--- | :---: | :---: |
| **Privatsphäre** | ❌ Niedrig | ✅ Hoch |
| **Werbefrei** | ❌ Nein | ✅ Ja (ab Stufe 3) |
| **Zensurfrei** | ❌ Nein | ✅ Ja |
| **Verschlüsselung** | ❌ Keine | ✅ Ja (DoT/DoH) |

---

> [!TIP]
> **Bereit für den nächsten Schritt?**  
> In [Stufe 1: Alternative DNS-Anbieter](01-alternative-dns.md) zeige ich dir, wie du mit nur zwei Klicks die Kontrolle über deine Anfragen zurückgewinnst.

---
[Zurück zur Übersicht](../README.md)
