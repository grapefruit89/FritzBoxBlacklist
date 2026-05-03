# Design: Navigation Cleanup in FritzBoxBlacklist Docs

## Purpose
The documentation files in the `FritzBoxBlacklist` repository contain a redundant "Back to Overview" link (`[⬅️ Zurück zur Übersicht](../README.md)`) at the top, typically on line 3. This link is being removed to streamline the documentation and improve readability, especially since breadcrumb or other navigation systems might be in place.

## Goals
- Remove the exact string `[⬅️ Zurück zur Übersicht](../README.md)` from target files.
- Clean up adjacent redundant empty lines to ensure a single blank line between the H1 header and the following content.
- Verify the changes across all 9 specified files.
- Commit and push the changes to the remote repository.

## Target Files
1. `docs/00-vanilla-dns.md`
2. `docs/01-alternative-dns.md`
3. `docs/02-dns-verschluesselt.md`
4. `docs/03-dns-verschluesselt-adblock.md`
5. `docs/04-cloud-adblocker.md`
6. `docs/05-selfhosting.md`
7. `docs/06-testing.md`
8. `docs/07-sources.md`
9. `legacy/README.md`

## Proposed Approach
A Python script will be used to process each file. The script will:
1. Identify the H1 header (line 1).
2. Look for the target link string.
3. Remove the link and any extra whitespace, ensuring exactly one newline exists between the header and the subsequent text/block.
4. Save the files.

## Success Criteria
- Files no longer contain the "Zurück zur Übersicht" link.
- Documentation structure remains valid (H1 -> empty line -> content).
- No excessive blank lines are introduced.
- Git repository is updated and pushed.
