# 🍦 Stufe 0: Standard-DNS vom Anbieter (Vanilla)

[⬅️ Zurück zur Übersicht](../README.md)

Willkommen! Ohne Änderungen nutzt du das **Standard-DNS deines Providers** (Telekom, Vodafone, o2). Setup: „Vanilla“ – Standard-Geschmack. Funktioniert, aber wenig Privatsphäre.

> [!TIP]
> **Die Metapher:** Das ist der **Standard-Kiosk** deines Internet-Anbieters. Er kennt dich, er weiß genau, wen du besuchen willst, und er führt Buch über jede deiner Anfragen.

---

## 📖 Was passiert eigentlich, wenn du `google.de` in den Browser tippst?

Stell dir vor, du willst deine Oma besuchen, kennst aber ihre Hausnummer nicht. Du gehst zu einem Kiosk, der ein dickes Telefonbuch hat, und fragst den Besitzer:

> 🧒 „Wo wohnt Oma Müller?“  
> 👴 Der Kioskbesitzer blättert in seinem dicken Buch und sagt: **„Blumenstraße 42.“**  
> 🧒 Du bedankst dich und gehst direkt dorthin.

**Genauso funktioniert das Internet – nur mit deinem Computer und einem DNS-Server.**

| Person / Gegenstand | Deine Internet-Welt |
| :--- | :--- |
| 🧒 **Du** | Dein Computer, Tablet oder Handy |
| 🏠 **Oma** | Die Webseite, die du besuchen willst (z. B. `google.de`) |
| 📕 **Das dicke Adressbuch** | Die riesige Liste aller Webseiten-Namen und ihrer Nummern |
| 👴 **Der Kioskbesitzer** | Der **DNS-Server**, der dir die richtige Nummer nennt |
| 🔢 **Hausnummer 42** | Die **IP-Adresse**, z. B. `142.250.185.163` |

### 📡 Schritt für Schritt – so läuft es technisch

1. Du tippst `google.de` in deinen Browser und drückst Enter.  
2. Dein Gerät (z. B. Laptop) fragt die **Fritz!Box** (`http://fritz.box`):  
   *„Welche IP-Adresse hat `google.de`?“*  
3. Die Fritz!Box leitet die Frage an den **DNS-Server** weiter, der beim Internetanbieter (z. B. Telekom, Vodafone) voreingestellt ist.  
4. Der DNS-Server schaut in seine riesige Liste und antwortet:  
   *`142.250.185.163`*  
5. Dein Browser holt sich jetzt von dieser Nummer die Webseite – und zeigt sie an.

> [!IMPORTANT]
> **Das Problem:** Wenn du nichts änderst, gehört der „Kiosk“ deinem Internet-Anbieter. Der Anbieter schreibt sich genau auf, wen du wann „besuchen“ wolltest. So weiß er sehr viel über dein Privatleben.

---

### 💡 Warum heißen die Nummern IP-Adressen?

Jedes Gerät im Internet bekommt eine eigene Nummer, die sogenannte **IP-Adresse** (Internet Protocol).  
Webseiten liegen auf Computern, die eine **feste IP** haben. Damit du nicht die kryptischen Nummern auswendig lernen musst, gibt es die **DNS-Server** – sie übersetzen Namen in Nummern.  
Beispiel: `google.de` → `142.250.185.163`

---

## 🚩 5 Nachteile von Vanilla-DNS

> [!WARNING]
> **1. Tracking (Provider sieht ALLES):** Jede aufgerufene Domain geht über Provider-DNS. Banking, Gesundheit, Vorlieben: Der Provider weiß Bescheid.

> [!CAUTION]
> **2. Zensur (CUII-Sperren):** Provider sperren Webseiten via DNS (z. B. Streaming, E-Book-Archive). Ergebnis: „Adresse existiert nicht“.

> [!WARNING]
> **3. DNS-Hijacking & Manipulation:** Tippfehler werden oft für Werbung oder Tracking-Umleitungen („Navigationshilfe“) missbraucht.

> [!CAUTION]
> **4. Keine Verschlüsselung:** Standard-DNS ist wie eine Postkarte: Jeder auf dem Weg kann mitlesen, was du anfragst.

> [!WARNING]
> **5. Performance:** Provider-Server sind oft langsamer als moderne, globale DNS-Netzwerke, was den Seitenaufbau verzögert.

---

## 📊 Vergleich: Vanilla vs. Custom DNS

| Feature | Vanilla (Stufe 0) | Custom [(ab Stufe 1)](01-alternative-dns.md) |
| :--- | :---: | :---: |
| **Privatsphäre** | ❌ Niedrig | ✅ Hoch |
| **Werbefrei** | ❌ Nein | ✅ Ja [(ab Stufe 3)](03-dns-verschluesselt-adblock.md) |
| **Zensurfrei** | ❌ Nein | ✅ Ja |
| **Verschlüsselung** | ❌ Keine | ✅ Ja (DoT/DoH) |

---

<p align="center">
  🌱 Stufe 0 | <a href="01-alternative-dns.md">Stufe 1</a> | <a href="02-dns-verschluesselt.md">Stufe 2</a> | <a href="03-dns-verschluesselt-adblock.md">Stufe 3</a> | <a href="04-cloud-adblocker.md">Stufe 4</a> | <a href="05-selfhosting.md">Stufe 5</a> | <a href="06-testing.md">Stufe 6</a> | <a href="07-sources.md">Stufe 7</a>
</p>
<p align="center">
  <a href="../README.md">🏠 Zurück zur Übersicht</a>
</p>
