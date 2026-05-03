# Update Global Breadcrumb Navigation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Update breadcrumb navigation in all "Stufe" docs to the new format with bold text and proper links.

**Architecture:** Surgical text replacement in 8 Markdown files.

**Tech Stack:** Markdown, HTML.

---

### Task 1: Update docs/00-vanilla-dns.md (Stufe 0)

- [ ] **Step 1: Replace nav bar**

Old:
```html
<p align="center">
  **0** | <a href="01-alternative-dns.md">1</a> | <a href="02-dns-verschluesselt.md">2</a> | <a href="03-dns-verschluesselt-adblock.md">3</a> | <a href="04-cloud-adblocker.md">4</a> | <a href="05-selfhosting.md">5</a> | <a href="06-testing.md">6</a> | <a href="07-sources.md">7</a>
</p>
```

New:
```html
<p align="center">
  **Stufe 0** | <a href="01-alternative-dns.md">**Stufe 1**</a> | <a href="02-dns-verschluesselt.md">**Stufe 2**</a> | <a href="03-dns-verschluesselt-adblock.md">**Stufe 3**</a> | <a href="04-cloud-adblocker.md">**Stufe 4**</a> | <a href="05-selfhosting.md">**Stufe 5**</a> | <a href="06-testing.md">**Stufe 6**</a> | <a href="07-sources.md">**Stufe 7**</a>
</p>
```

### Task 2: Update docs/01-alternative-dns.md (Stufe 1)

- [ ] **Step 1: Replace nav bar**

New:
```html
<p align="center">
  <a href="00-vanilla-dns.md">**Stufe 0**</a> | **Stufe 1** | <a href="02-dns-verschluesselt.md">**Stufe 2**</a> | <a href="03-dns-verschluesselt-adblock.md">**Stufe 3**</a> | <a href="04-cloud-adblocker.md">**Stufe 4**</a> | <a href="05-selfhosting.md">**Stufe 5**</a> | <a href="06-testing.md">**Stufe 6**</a> | <a href="07-sources.md">**Stufe 7**</a>
</p>
```

### Task 3: Update docs/02-dns-verschluesselt.md (Stufe 2)

- [ ] **Step 1: Replace nav bar**

New:
```html
<p align="center">
  <a href="00-vanilla-dns.md">**Stufe 0**</a> | <a href="01-alternative-dns.md">**Stufe 1**</a> | **Stufe 2** | <a href="03-dns-verschluesselt-adblock.md">**Stufe 3**</a> | <a href="04-cloud-adblocker.md">**Stufe 4**</a> | <a href="05-selfhosting.md">**Stufe 5**</a> | <a href="06-testing.md">**Stufe 6**</a> | <a href="07-sources.md">**Stufe 7**</a>
</p>
```

### Task 4: Update docs/03-dns-verschluesselt-adblock.md (Stufe 3)

- [ ] **Step 1: Replace nav bar**

New:
```html
<p align="center">
  <a href="00-vanilla-dns.md">**Stufe 0**</a> | <a href="01-alternative-dns.md">**Stufe 1**</a> | <a href="02-dns-verschluesselt.md">**Stufe 2**</a> | **Stufe 3** | <a href="04-cloud-adblocker.md">**Stufe 4**</a> | <a href="05-selfhosting.md">**Stufe 5**</a> | <a href="06-testing.md">**Stufe 6**</a> | <a href="07-sources.md">**Stufe 7**</a>
</p>
```

### Task 5: Update docs/04-cloud-adblocker.md (Stufe 4)

- [ ] **Step 1: Replace nav bar**

New:
```html
<p align="center">
  <a href="00-vanilla-dns.md">**Stufe 0**</a> | <a href="01-alternative-dns.md">**Stufe 1**</a> | <a href="02-dns-verschluesselt.md">**Stufe 2**</a> | <a href="03-dns-verschluesselt-adblock.md">**Stufe 3**</a> | **Stufe 4** | <a href="05-selfhosting.md">**Stufe 5**</a> | <a href="06-testing.md">**Stufe 6**</a> | <a href="07-sources.md">**Stufe 7**</a>
</p>
```

### Task 6: Update docs/05-selfhosting.md (Stufe 5)

- [ ] **Step 1: Replace nav bar**

New:
```html
<p align="center">
  <a href="00-vanilla-dns.md">**Stufe 0**</a> | <a href="01-alternative-dns.md">**Stufe 1**</a> | <a href="02-dns-verschluesselt.md">**Stufe 2**</a> | <a href="03-dns-verschluesselt-adblock.md">**Stufe 3**</a> | <a href="04-cloud-adblocker.md">**Stufe 4**</a> | **Stufe 5** | <a href="06-testing.md">**Stufe 6**</a> | <a href="07-sources.md">**Stufe 7**</a>
</p>
```

### Task 7: Update docs/06-testing.md (Stufe 6)

- [ ] **Step 1: Replace nav bar**

New:
```html
<p align="center">
  <a href="00-vanilla-dns.md">**Stufe 0**</a> | <a href="01-alternative-dns.md">**Stufe 1**</a> | <a href="02-dns-verschluesselt.md">**Stufe 2**</a> | <a href="03-dns-verschluesselt-adblock.md">**Stufe 3**</a> | <a href="04-cloud-adblocker.md">**Stufe 4**</a> | <a href="05-selfhosting.md">**Stufe 5**</a> | **Stufe 6** | <a href="07-sources.md">**Stufe 7**</a>
</p>
```

### Task 8: Update docs/07-sources.md (Stufe 7)

- [ ] **Step 1: Replace nav bar**

New:
```html
<p align="center">
  <a href="00-vanilla-dns.md">**Stufe 0**</a> | <a href="01-alternative-dns.md">**Stufe 1**</a> | <a href="02-dns-verschluesselt.md">**Stufe 2**</a> | <a href="03-dns-verschluesselt-adblock.md">**Stufe 3**</a> | <a href="04-cloud-adblocker.md">**Stufe 4**</a> | <a href="05-selfhosting.md">**Stufe 5**</a> | <a href="06-testing.md">**Stufe 6**</a> | **Stufe 7**
</p>
```

### Task 9: Verification

- [ ] **Step 1: Check all files for correct breadcrumbs**
- [ ] **Step 2: Check "Zurück zur Übersicht" link exists**

### Task 10: Commit

- [ ] **Step 1: Commit changes locally**
