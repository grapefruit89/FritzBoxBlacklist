# Documentation Navigation Standardization Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Standardize the bottom navigation bar across all 10 documentation files in the `docs/` folder.

**Architecture:** Surgical replacement of the footer in each markdown file with a consistent HTML structure.

**Tech Stack:** Markdown, HTML.

---

### Task 1: Update Stufe 0 (00-vanilla-dns.md)

**Files:**
- Modify: `docs/00-vanilla-dns.md`

- [ ] **Step 1: Replace footer with Pattern A**

```markdown
---

<p align="center">
  <a href="../README.md">⬅️ Zurück zur Übersicht</a> | <a href="01-alternative-dns.md">Stufe 1 ➡️</a>
</p>
```

- [ ] **Step 2: Remove redundant standalone link**

Ensure `[⬅️ Zurück zur Übersicht](../README.md)` at the bottom is gone.

- [ ] **Step 3: Commit**

```bash
git add docs/00-vanilla-dns.md
git commit -m "docs: standardize footer for Stufe 0"
```

### Task 2: Update Intermediate Stages (01-06)

**Files:**
- Modify: `docs/01-alternative-dns.md`
- Modify: `docs/02-dns-verschluesselt.md`
- Modify: `docs/03-dns-verschluesselt-adblock.md`
- Modify: `docs/04-cloud-adblocker.md`
- Modify: `docs/05-selfhosting.md`
- Modify: `docs/06-testing.md`

- [ ] **Step 1: Update docs/01-alternative-dns.md**

```html
<p align="center">
  <a href="00-vanilla-dns.md">⬅️ Stufe 0</a> | <a href="../README.md">🏠 Übersicht</a> | <a href="02-dns-verschluesselt.md">Stufe 2 ➡️</a>
</p>
```

- [ ] **Step 2: Update docs/02-dns-verschluesselt.md**

```html
<p align="center">
  <a href="01-alternative-dns.md">⬅️ Stufe 1</a> | <a href="../README.md">🏠 Übersicht</a> | <a href="03-dns-verschluesselt-adblock.md">Stufe 3 ➡️</a>
</p>
```

- [ ] **Step 3: Update docs/03-dns-verschluesselt-adblock.md**

```html
<p align="center">
  <a href="02-dns-verschluesselt.md">⬅️ Stufe 2</a> | <a href="../README.md">🏠 Übersicht</a> | <a href="04-cloud-adblocker.md">Stufe 4 ➡️</a>
</p>
```

- [ ] **Step 4: Update docs/04-cloud-adblocker.md**

```html
<p align="center">
  <a href="03-dns-verschluesselt-adblock.md">⬅️ Stufe 3</a> | <a href="../README.md">🏠 Übersicht</a> | <a href="05-selfhosting.md">Stufe 5 ➡️</a>
</p>
```

- [ ] **Step 5: Update docs/05-selfhosting.md**

```html
<p align="center">
  <a href="04-cloud-adblocker.md">⬅️ Stufe 4</a> | <a href="../README.md">🏠 Übersicht</a> | <a href="06-testing.md">Stufe 6 ➡️</a>
</p>
```

- [ ] **Step 6: Update docs/06-testing.md**

```html
<p align="center">
  <a href="05-selfhosting.md">⬅️ Stufe 5</a> | <a href="../README.md">🏠 Übersicht</a> | <a href="07-sources.md">Stufe 7 ➡️</a>
</p>
```

- [ ] **Step 7: Commit**

```bash
git add docs/01-alternative-dns.md docs/02-dns-verschluesselt.md docs/03-dns-verschluesselt-adblock.md docs/04-cloud-adblocker.md docs/05-selfhosting.md docs/06-testing.md
git commit -m "docs: standardize footers for Stufe 1-6"
```

### Task 3: Update Extra Stages (07, fritzbox-basics)

**Files:**
- Modify: `docs/07-sources.md`
- Modify: `docs/fritzbox-basics.md`

- [ ] **Step 1: Update docs/07-sources.md**

```html
<p align="center">
  <a href="06-testing.md">⬅️ Zurück</a> | <a href="../README.md">🏠 Übersicht</a> | <a href="fritzbox-basics.md">Weiter ➡️</a>
</p>
```

- [ ] **Step 2: Update docs/fritzbox-basics.md**

```html
<p align="center">
  <a href="07-sources.md">⬅️ Zurück</a> | <a href="../README.md">🏠 Übersicht</a> | <a href="manual-client-setup.md">Weiter ➡️</a>
</p>
```

- [ ] **Step 3: Commit**

```bash
git add docs/07-sources.md docs/fritzbox-basics.md
git commit -m "docs: standardize footers for extra stages"
```

### Task 4: Update Final Stage (manual-client-setup.md)

**Files:**
- Modify: `docs/manual-client-setup.md`

- [ ] **Step 1: Update docs/manual-client-setup.md**

```html
<p align="center">
  <a href="fritzbox-basics.md">⬅️ Zurück</a> | <a href="../README.md">🏠 Übersicht</a>
</p>
```

- [ ] **Step 2: Commit**

```bash
git add docs/manual-client-setup.md
git commit -m "docs: standardize footer for manual-client-setup"
```
