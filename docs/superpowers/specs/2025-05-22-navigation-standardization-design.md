# Design Specification: Documentation Bottom Navigation Standardization

**Date:** 2025-05-22 (Simulated)
**Topic:** Standardization of footer navigation across documentation files.

## 1. Problem Statement
The documentation files in the `docs/` directory have inconsistent bottom navigation styles. Some files have simple links, while others have centered HTML bars. Additionally, there is a redundant "Zurück zur Übersicht" link at the bottom of every file that is better integrated into the navigation bar.

## 2. Goals
- Standardize the bottom navigation bar across all 10 documentation files.
- Integrate the "Zurück zur Übersicht" link into the centered navigation bar.
- Remove redundant standalone links at the bottom.
- Ensure logical "Previous", "Home", and "Next" links for every stage.

## 3. Proposed Design

### 3.1. Navigation Patterns

#### Pattern A: Initial Stage (00-vanilla-dns.md)
```html
<p align="center">
  <a href="../README.md">⬅️ Zurück zur Übersicht</a> | <a href="01-alternative-dns.md">Stufe 1 ➡️</a>
</p>
```

#### Pattern B: Intermediate Stages (01 to 06)
```html
<p align="center">
  <a href="prev.md">⬅️ Stufe X</a> | <a href="../README.md">🏠 Übersicht</a> | <a href="next.md">Stufe Y ➡️</a>
</p>
```

#### Pattern C: Final/Extra Stages (07, basics, manual-setup)
```html
<p align="center">
  <a href="prev.md">⬅️ Zurück</a> | <a href="../README.md">🏠 Übersicht</a> | <a href="next.md">Weiter ➡️</a>
</p>
```

### 3.2. Detailed Mapping

| File | Previous Link | Home Link | Next Link |
| :--- | :--- | :--- | :--- |
| `00-vanilla-dns.md` | - | `../README.md` | `01-alternative-dns.md` |
| `01-alternative-dns.md` | `00-vanilla-dns.md` | `../README.md` | `02-dns-verschluesselt.md` |
| `02-dns-verschluesselt.md` | `01-alternative-dns.md` | `../README.md` | `03-dns-verschluesselt-adblock.md` |
| `03-dns-verschluesselt-adblock.md` | `02-dns-verschluesselt.md` | `../README.md` | `04-cloud-adblocker.md` |
| `04-cloud-adblocker.md` | `03-dns-verschluesselt-adblock.md` | `../README.md` | `05-selfhosting.md` |
| `05-selfhosting.md` | `04-cloud-adblocker.md` | `../README.md` | `06-testing.md` |
| `06-testing.md` | `05-selfhosting.md` | `../README.md` | `07-sources.md` |
| `07-sources.md` | `06-testing.md` | `../README.md` | `fritzbox-basics.md` |
| `fritzbox-basics.md` | `07-sources.md` | `../README.md` | `manual-client-setup.md` |
| `manual-client-setup.md` | `fritzbox-basics.md` | `../README.md` | - |

## 4. Implementation Strategy
1.  Verify the bottom of each file for existing navigation blocks.
2.  Apply the `replace` tool to swap the old footer for the new standardized one.
3.  Remove the redundant `[⬅️ Zurück zur Übersicht](../README.md)` at the bottom.
4.  Confirm changes by reading the updated files.
5.  Commit the changes locally.

## 5. Verification
- All files should have a centered `<p>` tag at the bottom.
- Links must be valid and point to the correct relative paths.
- No redundant standalone links at the very end of files.
- The top navigation (under H1) remains unchanged.
