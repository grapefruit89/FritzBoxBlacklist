# Navigation Cleanup Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Remove redundant "Back to Overview" links and clean up whitespace in 9 markdown files.

**Architecture:** Scripted batch update using Python for precision and consistency across multiple files.

**Tech Stack:** Python, Git

---

### Task 1: Preparation and Scripting

**Files:**
- Create: `C:\Users\morit\FritzBoxBlacklist\cleanup_nav.py`

- [ ] **Step 1: Create the cleanup script**

```python
import os

files = [
    "docs/00-vanilla-dns.md",
    "docs/01-alternative-dns.md",
    "docs/02-dns-verschluesselt.md",
    "docs/03-dns-verschluesselt-adblock.md",
    "docs/04-cloud-adblocker.md",
    "docs/05-selfhosting.md",
    "docs/06-testing.md",
    "docs/07-sources.md",
    "legacy/README.md"
]

target_string = "[⬅️ Zurück zur Übersicht](../README.md)"

def cleanup_file(rel_path):
    abs_path = os.path.join(r"C:\Users\morit\FritzBoxBlacklist", rel_path)
    if not os.path.exists(abs_path):
        print(f"File not found: {abs_path}")
        return

    with open(abs_path, "r", encoding="utf-8") as f:
        content = f.read()

    if target_string not in content:
        print(f"String not found in {rel_path}")
        return

    # Split lines and find the target
    lines = content.splitlines()
    new_lines = []
    
    i = 0
    while i < len(lines):
        if target_string in lines[i]:
            # Found it. Now skip it and any adjacent empty lines
            # Check previous line for extra whitespace if it's the only thing between H1 and link
            if i > 0 and lines[i-1].strip() == "":
                # We'll handle whitespace after removing the link
                pass
            i += 1
            # Skip any immediately following empty lines
            while i < len(lines) and lines[i].strip() == "":
                i += 1
            continue
        
        new_lines.append(lines[i])
        i += 1

    # Ensure exactly one empty line after the H1 header (assuming it's line 0)
    # If the file starts with H1 and then we want one blank line
    final_lines = []
    if new_lines and new_lines[0].startswith("# "):
        final_lines.append(new_lines[0])
        final_lines.append("") # One blank line
        # Start adding the rest, skip any leading blank lines in the rest
        rest_idx = 1
        while rest_idx < len(new_lines) and new_lines[rest_idx].strip() == "":
            rest_idx += 1
        final_lines.extend(new_lines[rest_idx:])
    else:
        final_lines = new_lines

    with open(abs_path, "w", encoding="utf-8", newline="\n") as f:
        f.write("\n".join(final_lines) + "\n")
    print(f"Cleaned up {rel_path}")

for f in files:
    cleanup_file(f)
```

- [ ] **Step 2: Run the script**

Run: `python C:\Users\morit\FritzBoxBlacklist\cleanup_nav.py`
Expected: "Cleaned up ..." for all 9 files.

### Task 2: Verification

- [ ] **Step 1: Inspect modified files**

Run: `grep -r "Zurück zur Übersicht" C:\Users\morit\FritzBoxBlacklist\docs C:\Users\morit\FritzBoxBlacklist\legacy`
Expected: No matches in the target files.

- [ ] **Step 2: Check first few lines of a sample file**

Run: `Get-Content C:\Users\morit\FritzBoxBlacklist\docs\00-vanilla-dns.md -TotalCount 5`
Expected: H1 header, one blank line, then intro text.

### Task 3: Commit and Push

- [ ] **Step 1: Stage changes**

Run: `cd C:\Users\morit\FritzBoxBlacklist; git add .`

- [ ] **Step 2: Commit**

Run: `git commit -m "docs: remove redundant navigation links and clean up whitespace"`

- [ ] **Step 3: Push**

Run: `git push origin master`

- [ ] **Step 4: Cleanup**

Run: `Remove-Item C:\Users\morit\FritzBoxBlacklist\cleanup_nav.py`
