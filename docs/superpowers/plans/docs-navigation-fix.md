# Docs Navigation Fix Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Fix navigation links at the bottom of documentation files using HTML `<a>` tags for GitHub clickability.

**Architecture:** Replace Markdown/HTML-hybrid navigation with centered pure HTML structure.

**Tech Stack:** Markdown, HTML.

---

### Task 1: Fix `docs/07-sources.md`

**Files:**
- Modify: `docs/07-sources.md`

- [ ] **Step 1: Add centered navigation**

```markdown
---
<p align="center">
  <a href="06-testing.md">⬅️ Stufe 6</a> | <a href="fritzbox-basics.md">Fritz!Box Basics ➡️</a>
</p>

[⬅️ Zurück zur Übersicht](../README.md)
```

- [ ] **Step 2: Verify content**
Check that the navigation is at the bottom before the "Zurück zur Übersicht" link.

### Task 2: Fix `docs/fritzbox-basics.md`

**Files:**
- Modify: `docs/fritzbox-basics.md`

- [ ] **Step 1: Replace hybrid navigation with pure HTML**

```html
<p align="center">
  <a href="07-sources.md">⬅️ Stufe 7</a> | <a href="manual-client-setup.md">Manuelles Setup ➡️</a>
</p>
```

- [ ] **Step 2: Verify content**
Check that the link to Stufe 7 and Manual Setup works (relative paths).

### Task 3: Fix `docs/manual-client-setup.md`

**Files:**
- Modify: `docs/manual-client-setup.md`

- [ ] **Step 1: Replace hybrid navigation and fix backward link**

```html
<p align="center">
  <a href="fritzbox-basics.md">⬅️ Fritz!Box Basics</a>
</p>
```

- [ ] **Step 2: Verify content**
Check that it points back to `fritzbox-basics.md`.

### Task 4: Final Verification and Commit

- [ ] **Step 1: Verify all files**
Check `06-testing.md`, `07-sources.md`, `fritzbox-basics.md`, and `manual-client-setup.md` for consistent navigation style.

- [ ] **Step 2: Commit changes**
Use `caveman-commit` to generate a commit message and commit locally.
