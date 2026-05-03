# Documentation Navigation Fix Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Fix centered navigation links in all documentation files by replacing Markdown links inside `<p align="center">` tags with HTML `<a>` tags and ensuring correct sequential logic.

**Architecture:** Surgical replacement of bottom navigation blocks in Markdown files.

**Tech Stack:** Markdown, HTML.

---

### Task 1: Update 00-vanilla-dns.md

**Files:**
- Modify: `docs/00-vanilla-dns.md`

- [ ] **Step 1: Replace bottom navigation**
Replace:
```markdown
<p align="center">
  [Stufe 1 ➡️](01-alternative-dns.md)
</p>

[⬅️ Zurück zur Übersicht](../README.md)
```
With:
```html
<p align="center">
  <a href="01-alternative-dns.md">Stufe 1 ➡️</a>
</p>

[⬅️ Zurück zur Übersicht](../README.md)
```

- [ ] **Step 2: Commit**
```bash
git add docs/00-vanilla-dns.md
git commit -m "docs: fix centered nav in 00-vanilla-dns.md"
```

### Task 2: Update 01-alternative-dns.md

**Files:**
- Modify: `docs/01-alternative-dns.md`

- [ ] **Step 1: Replace bottom navigation**
Replace:
```markdown
<p align="center">
  [⬅️ Stufe 0](00-vanilla-dns.md) | [Stufe 2 ➡️](02-dns-verschluesselt.md)
</p>

[⬅️ Zurück zur Übersicht](../README.md)
```
With:
```html
<p align="center">
  <a href="00-vanilla-dns.md">⬅️ Stufe 0</a> | <a href="02-dns-verschluesselt.md">Stufe 2 ➡️</a>
</p>

[⬅️ Zurück zur Übersicht](../README.md)
```

- [ ] **Step 2: Commit**
```bash
git add docs/01-alternative-dns.md
git commit -m "docs: fix centered nav in 01-alternative-dns.md"
```

### Task 3: Update 02-dns-verschluesselt.md

**Files:**
- Modify: `docs/02-dns-verschluesselt.md`

- [ ] **Step 1: Replace bottom navigation**
Replace:
```markdown
<p align="center">
  [⬅️ Stufe 1](01-alternative-dns.md) | [Stufe 3 ➡️](03-dns-verschluesselt-adblock.md)
</p>

[⬅️ Zurück zur Übersicht](../README.md)
```
With:
```html
<p align="center">
  <a href="01-alternative-dns.md">⬅️ Stufe 1</a> | <a href="03-dns-verschluesselt-adblock.md">Stufe 3 ➡️</a>
</p>

[⬅️ Zurück zur Übersicht](../README.md)
```

- [ ] **Step 2: Commit**
```bash
git add docs/02-dns-verschluesselt.md
git commit -m "docs: fix centered nav in 02-dns-verschluesselt.md"
```

### Task 4: Update 03-dns-verschluesselt-adblock.md

**Files:**
- Modify: `docs/03-dns-verschluesselt-adblock.md`

- [ ] **Step 1: Add bottom navigation**
Replace:
```markdown
[⬅️ Zurück zur Übersicht](../README.md)
```
With:
```html
<p align="center">
  <a href="02-dns-verschluesselt.md">⬅️ Stufe 2</a> | <a href="04-cloud-adblocker.md">Stufe 4 ➡️</a>
</p>

[⬅️ Zurück zur Übersicht](../README.md)
```

- [ ] **Step 2: Commit**
```bash
git add docs/03-dns-verschluesselt-adblock.md
git commit -m "docs: add centered nav in 03-dns-verschluesselt-adblock.md"
```

### Task 5: Update 04-cloud-adblocker.md

**Files:**
- Modify: `docs/04-cloud-adblocker.md`

- [ ] **Step 1: Add bottom navigation**
Replace:
```markdown
[← Zurück zur Übersicht](../README.md)
```
With:
```html
<p align="center">
  <a href="03-dns-verschluesselt-adblock.md">⬅️ Stufe 3</a> | <a href="05-selfhosting.md">Stufe 5 ➡️</a>
</p>

[⬅️ Zurück zur Übersicht](../README.md)
```

- [ ] **Step 2: Commit**
```bash
git add docs/04-cloud-adblocker.md
git commit -m "docs: add centered nav in 04-cloud-adblocker.md"
```

### Task 6: Update 05-selfhosting.md

**Files:**
- Modify: `docs/05-selfhosting.md`

- [ ] **Step 1: Add bottom navigation**
Replace:
```markdown
[← Zurück zur Übersicht](../README.md)
```
With:
```html
<p align="center">
  <a href="04-cloud-adblocker.md">⬅️ Stufe 4</a> | <a href="06-testing.md">Stufe 6 ➡️</a>
</p>

[⬅️ Zurück zur Übersicht](../README.md)
```

- [ ] **Step 2: Commit**
```bash
git add docs/05-selfhosting.md
git commit -m "docs: add centered nav in 05-selfhosting.md"
```

### Task 7: Update 06-testing.md

**Files:**
- Modify: `docs/06-testing.md`

- [ ] **Step 1: Add bottom navigation**
Replace:
```markdown
[← Zurück zur Übersicht](../README.md)
```
With:
```html
<p align="center">
  <a href="05-selfhosting.md">⬅️ Stufe 5</a> | <a href="07-sources.md">Stufe 7 ➡️</a>
</p>

[⬅️ Zurück zur Übersicht](../README.md)
```

- [ ] **Step 2: Commit**
```bash
git add docs/06-testing.md
git commit -m "docs: add centered nav in 06-testing.md"
```

### Task 8: Update 07-sources.md

**Files:**
- Modify: `docs/07-sources.md`

- [ ] **Step 1: Add bottom navigation**
Replace:
```markdown
[← Zurück zur Übersicht](../README.md)
```
With:
```html
<p align="center">
  <a href="06-testing.md">⬅️ Stufe 6</a> | <a href="fritzbox-basics.md">Stufe: Fritz!Box Basics ➡️</a>
</p>

[⬅️ Zurück zur Übersicht](../README.md)
```

- [ ] **Step 2: Commit**
```bash
git add docs/07-sources.md
git commit -m "docs: add centered nav in 07-sources.md"
```

### Task 9: Update fritzbox-basics.md

**Files:**
- Modify: `docs/fritzbox-basics.md`

- [ ] **Step 1: Replace bottom navigation**
Replace:
```markdown
<p align="center">[⬅️ Stufe 7 (Quellen)](07-sources.md) | [Manuelles Setup ➡️](manual-client-setup.md)</p>

[⬅️ Zurück zur Übersicht](../README.md)
```
With:
```html
<p align="center">
  <a href="07-sources.md">⬅️ Stufe 7 (Quellen)</a> | <a href="manual-client-setup.md">Manuelles Setup ➡️</a>
</p>

[⬅️ Zurück zur Übersicht](../README.md)
```

- [ ] **Step 2: Commit**
```bash
git add docs/fritzbox-basics.md
git commit -m "docs: fix centered nav in fritzbox-basics.md"
```

### Task 10: Update manual-client-setup.md

**Files:**
- Modify: `docs/manual-client-setup.md`

- [ ] **Step 1: Replace bottom navigation**
Replace:
```markdown
<p align="center">[⬅️ Stufe 7 (Quellen)](07-sources.md)</p>

[⬅️ Zurück zur Übersicht](../README.md)
```
With:
```html
<p align="center">
  <a href="07-sources.md">⬅️ Stufe 7 (Quellen)</a>
</p>

[⬅️ Zurück zur Übersicht](../README.md)
```

- [ ] **Step 2: Commit**
```bash
git add docs/manual-client-setup.md
git commit -m "docs: fix centered nav in manual-client-setup.md"
```
