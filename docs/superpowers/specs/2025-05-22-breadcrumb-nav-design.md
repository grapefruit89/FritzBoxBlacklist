# Design: Global Centered Breadcrumb Navigation

Implement a consistent navigation bar across all 'Stufe' pages (0-7) in `docs/`.

## Target Files
- `docs/00-vanilla-dns.md`
- `docs/01-alternative-dns.md`
- `docs/02-dns-verschluesselt.md`
- `docs/03-dns-verschluesselt-adblock.md`
- `docs/04-cloud-adblocker.md`
- `docs/05-selfhosting.md`
- `docs/06-testing.md`
- `docs/07-sources.md`

## Navigation Bar Structure
Two centered paragraphs:
1. Links to Stufe 0-7, with the current page bolded and unlinked.
2. A link back to the main README overview.

Example for Stufe 1:
```html
<p align="center">
  <a href="00-vanilla-dns.md">0</a> | **1** | <a href="02-dns-verschluesselt.md">2</a> | <a href="03-dns-verschluesselt-adblock.md">3</a> | <a href="04-cloud-adblocker.md">4</a> | <a href="05-selfhosting.md">5</a> | <a href="06-testing.md">6</a> | <a href="07-sources.md">7</a>
</p>
<p align="center">
  <a href="../README.md">🏠 Zurück zur Übersicht</a>
</p>
```

## Cleanup
Remove existing centered navigation footers at the end of each target file.

## Implementation Plan
1. Create a helper script or internal logic to generate the navigation bar for each page index.
2. Update each file sequentially using the `replace` tool.
3. Verify that the navigation bar looks correct in each file.
4. Commit the changes.
