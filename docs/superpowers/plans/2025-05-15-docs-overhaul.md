# Documentation Overhaul Stufe 5 & 7 Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Perform a "No-Lazy" overhaul of `docs/05-selfhosting.md` and `docs/07-sources.md` with expanded technical comparisons and comprehensive source lists.

**Architecture:** Systematic update of Markdown documentation files while preserving structure, navigation, and core instructional content.

**Tech Stack:** Markdown

---

### Task 1: Overhaul Stufe 5 (Self-Hosting)

**Files:**
- Modify: `docs/05-selfhosting.md`

- [ ] **Step 1: Replace Comparison Table**
    Expand the existing table to include 6 systems: AdGuard Home, Pi-hole, Technitium, Blocky, Gravity, CoreDNS.
    Add columns: System, Sprache, Stärken, Metapher, DoT/DoH nativ, Zielgruppe.
    Use provided data:
    - AdGuard Home: Go | All-in-One, schickes UI | Der moderne Allrounder | ✅ Ja | Einsteiger
    - Pi-hole: PHP/C | Riesige Community, sparsam | Der robuste Veteran | ❌ (via dnsproxy) | Bastler
    - Technitium: C#/.NET | Rekursiv & Autoritativ, Enterprise | Das Schweizer Taschenmesser | ✅ Ja | Profis & Sysadmins
    - Blocky: Go | Schlank, extrem schnell, Single-Binary | Der flinke Flitzer | ✅ Ja | Minimalisten & IaC-Fans
    - Gravity: Go | Voll replizierbar (etcd), DNS+DHCP+TFTP | Die Kommandozentrale | ⚠️ (via Blocky) | Homelabber
    - CoreDNS: Go | Plugin-basiert, Kubernetes-native | Der modulare Baukasten | ⚠️ (via Plugin) | DevOps-Experten

- [ ] **Step 2: Verify Footers**
    Ensure navigation footers are intact and NOT bolded.

### Task 2: Overhaul Stufe 7 (Sources)

**Files:**
- Modify: `docs/07-sources.md`

- [ ] **Step 1: Expand Metaphor and Header**
    Update the 'Die private Fachbibliothek' metaphor section.

- [ ] **Step 2: Implement Table 1 (Vertrauenswürdige Quellen DE)**
    Include Kuketz, Privacy-Handbuch, DNSforge, Tarnkappe.

- [ ] **Step 3: Implement Table 2 (Praxis-Tutorials)**
    Include FFMUC (FritzBox DoT), Tarnkappe (Windows/Browser DoH), Heise (DNS-Grundlagen).

- [ ] **Step 4: Implement Table 3 (Netzpolitik & Zensur)**
    Include Netzpolitik.org, Heise (CUII Analysen), CCC (39C3).

- [ ] **Step 5: Implement Table 4 (Tools & Blocklisten)**
    Include Kuketz Blocklists, OISD, Firebog, CaptainDNS Benchmarks.

- [ ] **Step 6: Add 'Warum diese Quellen?' Section**
    Detailing Independence, No-Ads, and Technical depth.

- [ ] **Step 7: Verify Footers**
    Ensure navigation footers are intact and NOT bolded.

### Task 3: Git Commit

- [ ] **Step 1: Stage and Commit**
    Stage `docs/05-selfhosting.md` and `docs/07-sources.md`.
    Commit with message: `docs: overhaul Stufe 5 comparison and Stufe 7 sources library`
