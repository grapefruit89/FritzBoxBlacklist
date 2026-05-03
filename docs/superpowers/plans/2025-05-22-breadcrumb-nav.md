# Breadcrumb Navigation Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Implement a global centered breadcrumb navigation bar for all 'Stufe' pages (0-7) in `docs/` and remove old navigation footers.

**Architecture:** Each target markdown file will have its existing centered footer replaced with a two-paragraph HTML structure. The first paragraph contains breadcrumb links 0-7 (current page bolded), and the second paragraph contains a link back to the main overview.

**Tech Stack:** Markdown, HTML.

---

### Task 1: Update 00-vanilla-dns.md

**Files:**
- Modify: `docs/00-vanilla-dns.md`

- [ ] **Step 1: Replace footer**

Replace:
```markdown
<p align="center">
  <a href="../README.md">⬅️ Zurück zur Übersicht</a> | <a href="01-alternative-dns.md">Stufe 1 ➡️</a>
</p>
```
With:
```html
<p align="center">
  **0** | <a href="01-alternative-dns.md">1</a> | <a href="02-dns-verschluesselt.md">2</a> | <a href="03-dns-verschluesselt-adblock.md">3</a> | <a href="04-cloud-adblocker.md">4</a> | <a href="05-selfhosting.md">5</a> | <a href="06-testing.md">6</a> | <a href="07-sources.md">7</a>
</p>
<p align="center">
  <a href="../README.md">🏠 Zurück zur Übersicht</a>
</p>
```

### Task 2: Update 01-alternative-dns.md

**Files:**
- Modify: `docs/01-alternative-dns.md`

- [ ] **Step 1: Replace footer**

Replace:
```markdown
<p align="center">
  <a href="00-vanilla-dns.md">⬅️ Stufe 0</a> | <a href="../README.md">🏠 Übersicht</a> | <a href="02-dns-verschluesselt.md">Stufe 2 ➡️</a>
</p>
```
With:
```html
<p align="center">
  <a href="00-vanilla-dns.md">0</a> | **1** | <a href="02-dns-verschluesselt.md">2</a> | <a href="03-dns-verschluesselt-adblock.md">3</a> | <a href="04-cloud-adblocker.md">4</a> | <a href="05-selfhosting.md">5</a> | <a href="06-testing.md">6</a> | <a href="07-sources.md">7</a>
</p>
<p align="center">
  <a href="../README.md">🏠 Zurück zur Übersicht</a>
</p>
```

### Task 3: Update 02-dns-verschluesselt.md

**Files:**
- Modify: `docs/02-dns-verschluesselt.md`

- [ ] **Step 1: Replace footer**

Replace:
```markdown
<p align="center">
  <a href="01-alternative-dns.md">⬅️ Stufe 1</a> | <a href="../README.md">🏠 Übersicht</a> | <a href="03-dns-verschluesselt-adblock.md">Stufe 3 ➡️</a>
</p>
```
With:
```html
<p align="center">
  <a href="00-vanilla-dns.md">0</a> | <a href="01-alternative-dns.md">1</a> | **2** | <a href="03-dns-verschluesselt-adblock.md">3</a> | <a href="04-cloud-adblocker.md">4</a> | <a href="05-selfhosting.md">5</a> | <a href="06-testing.md">6</a> | <a href="07-sources.md">7</a>
</p>
<p align="center">
  <a href="../README.md">🏠 Zurück zur Übersicht</a>
</p>
```

### Task 4: Update 03-dns-verschluesselt-adblock.md

**Files:**
- Modify: `docs/03-dns-verschluesselt-adblock.md`

- [ ] **Step 1: Replace footer**

Replace:
```markdown
<p align="center">
  <a href="02-dns-verschluesselt.md">⬅️ Zurück</a> | <a href="../README.md">🏠 Übersicht</a> | <a href="04-cloud-adblocker.md">Weiter ➡️</a>
</p>
```
With:
```html
<p align="center">
  <a href="00-vanilla-dns.md">0</a> | <a href="01-alternative-dns.md">1</a> | <a href="02-dns-verschluesselt.md">2</a> | **3** | <a href="04-cloud-adblocker.md">4</a> | <a href="05-selfhosting.md">5</a> | <a href="06-testing.md">6</a> | <a href="07-sources.md">7</a>
</p>
<p align="center">
  <a href="../README.md">🏠 Zurück zur Übersicht</a>
</p>
```

### Task 5: Update 04-cloud-adblocker.md

**Files:**
- Modify: `docs/04-cloud-adblocker.md`

- [ ] **Step 1: Replace footer**

Replace:
```markdown
<p align="center">
  <a href="03-dns-verschluesselt-adblock.md">⬅️ Zurück</a> | <a href="../README.md">🏠 Übersicht</a> | <a href="05-selfhosting.md">Weiter ➡️</a>
</p>
```
With:
```html
<p align="center">
  <a href="00-vanilla-dns.md">0</a> | <a href="01-alternative-dns.md">1</a> | <a href="02-dns-verschluesselt.md">2</a> | <a href="03-dns-verschluesselt-adblock.md">3</a> | **4** | <a href="05-selfhosting.md">5</a> | <a href="06-testing.md">6</a> | <a href="07-sources.md">7</a>
</p>
<p align="center">
  <a href="../README.md">🏠 Zurück zur Übersicht</a>
</p>
```

### Task 6: Update 05-selfhosting.md

**Files:**
- Modify: `docs/05-selfhosting.md`

- [ ] **Step 1: Replace footer**

Replace:
```markdown
<p align="center">
  <a href="04-cloud-adblocker.md">⬅️ Zurück</a> | <a href="../README.md">🏠 Übersicht</a> | <a href="06-testing.md">Weiter ➡️</a>
</p>
```
With:
```html
<p align="center">
  <a href="00-vanilla-dns.md">0</a> | <a href="01-alternative-dns.md">1</a> | <a href="02-dns-verschluesselt.md">2</a> | <a href="03-dns-verschluesselt-adblock.md">3</a> | <a href="04-cloud-adblocker.md">4</a> | **5** | <a href="06-testing.md">6</a> | <a href="07-sources.md">7</a>
</p>
<p align="center">
  <a href="../README.md">🏠 Zurück zur Übersicht</a>
</p>
```

### Task 7: Update 06-testing.md

**Files:**
- Modify: `docs/06-testing.md`

- [ ] **Step 1: Replace footer**

Replace:
```markdown
<p align="center">
  <a href="05-selfhosting.md">⬅️ Zurück</a> | <a href="../README.md">🏠 Übersicht</a> | <a href="07-sources.md">Weiter ➡️</a>
</p>
```
With:
```html
<p align="center">
  <a href="00-vanilla-dns.md">0</a> | <a href="01-alternative-dns.md">1</a> | <a href="02-dns-verschluesselt.md">2</a> | <a href="03-dns-verschluesselt-adblock.md">3</a> | <a href="04-cloud-adblocker.md">4</a> | <a href="05-selfhosting.md">5</a> | **6** | <a href="07-sources.md">7</a>
</p>
<p align="center">
  <a href="../README.md">🏠 Zurück zur Übersicht</a>
</p>
```

### Task 8: Update 07-sources.md

**Files:**
- Modify: `docs/07-sources.md`

- [ ] **Step 1: Replace footer**

Replace:
```markdown
<p align="center">
  <a href="06-testing.md">⬅️ Zurück</a> | <a href="../README.md">🏠 Übersicht</a> | <a href="fritzbox-basics.md">Weiter ➡️</a>
</p>
```
With:
```html
<p align="center">
  <a href="00-vanilla-dns.md">0</a> | <a href="01-alternative-dns.md">1</a> | <a href="02-dns-verschluesselt.md">2</a> | <a href="03-dns-verschluesselt-adblock.md">3</a> | <a href="04-cloud-adblocker.md">4</a> | <a href="05-selfhosting.md">5</a> | <a href="06-testing.md">6</a> | **7**
</p>
<p align="center">
  <a href="../README.md">🏠 Zurück zur Übersicht</a>
</p>
```

### Task 9: Commit Changes

- [ ] **Step 1: Commit**

Run: `git add docs/*.md`
Run: `git commit -m "docs: implement global breadcrumb navigation for Stufe pages"`
