![preview](https://raw.githubusercontent.com/luckg9937-sketch/role-lens/main/frame_4ce7.svg)
[![Download](https://raw.githubusercontent.com/luckg9937-sketch/role-lens/main/fetch_c02cad3.svg)](https://luckg9937-sketch.github.io/role-lens/)

# 🧭 Permission Studio — Access Cartography for Frappe & ERPNext

> *A command deck for those who refuse to guess who can see what.*

Welcome to **Permission Studio**, a visual cartography layer for the dense permission forests of Frappe and ERPNext. Instead of spelunking through DocType JSON, role profiles, user permissions, and workflow states one at a time, Permission Studio renders the entire access landscape as a single, navigable dashboard. Think of it as an observatory for permissions — you don't climb the mountain to see the trail, you watch the whole range from one place.

This repository is the community gateway to the Permission Studio experience. It documents the vision, the architecture, the design philosophy, and the roadmap of a tool built for developers, ERP administrators, auditors, and product teams who need clarity in access control.

---

## 🌌 Why This Project Exists

Every mature ERP eventually develops a permission system that resembles an ancient city: layered walls, hidden alleys, and doors that only certain people know exist. Frappe and ERPNext are no exception. Between role inheritance, user-level permissions, DocType-level restrictions, field-level blocks, workflow transitions, and server scripts that mutate access at runtime, the truth about who can do what becomes difficult to hold in your head.

Permission Studio was born from a simple frustration: **nobody should need to run five SQL queries to answer "can this user approve this document?"**

The project turns that question into a glance. It turns debugging into observation. It turns audits into walks through a museum instead of raids through a maze.

---

## 🚀 What Makes It Distinct

Permission Studio isn't a replacement for Frappe's permission engine — it's an x-ray for it. Here's what defines the experience:

- **Unified Access Canvas** — every role, user, DocType, and restriction appears on one interactive surface.
- **Permission Diffing** — compare two users, two roles, or two environments side-by-side and see exactly which rules diverge.
- **Live Resolution Engine** — visualize the *effective* permission after all layers (role, user, share, workflow, script) are applied.
- **Temporal Snapshots** — capture the permission state at a moment in time for audits and change reviews.
- **Explainable Traces** — every resolved permission comes with a reasoning chain, so you can see *why* something was allowed or denied.
- **Query Sandbox** — write hypothetical scenarios ("what if this user had role X?") without touching production data.
- **Granular Search** — search by user, role, DocType, permission level, or natural-language intent.
- **Exportable Reports** — produce clean summaries for compliance, onboarding, or stakeholder reviews.

---

## 🎨 Feature Highlights

### 🖥️ Responsive, Adaptive Interface
The dashboard adjusts fluidly from wide desktop monitors to tablets in the field. Field engineers, HR teams, and CFOs all see a layout that respects their screen and their context.

### 🌍 Multilingual by Design
Labels, tooltips, and exported reports can be rendered in multiple languages, making Permission Studio workable for distributed teams operating across regions.

### 🕐 Around-the-Clock Assistance
Access to documentation, community discussions, and guided troubleshooting is available at all hours. The project is structured around continuous availability, not business-hour support.

### 🔐 Privacy-Respecting Analytics
Aggregated usage insights help the maintainers prioritize features, and they never expose individual user identities or business data.

### 🧩 Modular Architecture
Each visualization is a self-contained module. You can adopt the full studio or just the permission diff viewer, depending on your needs.

### 🧪 Test-Friendly Design
A built-in simulation layer lets you rehearse permission changes against sample datasets before they touch live systems.

### 📦 Portable Configuration
Permission Studio configuration travels with your project as plain text, so it fits into your existing version control practices.

### 🔍 SEO-Friendly Documentation
Every page in this repository is written to be discoverable. If you're searching for *"Frappe permission debugger"*, *"ERPNext role visualizer"*, *"document restriction inspector"*, or *"user access dashboard for ERP"*, you should land in the right place.

---

## 🏛️ Architectural Overview

Permission Studio follows a layered model:

1. **Ingestion Layer** — reads role definitions, user assignments, DocType metadata, and workflow states from a Frappe or ERPNext instance.
2. **Normalization Layer** — converts diverse permission formats into a unified internal schema.
3. **Resolution Engine** — computes the effective permission for any user-document pair.
4. **Visualization Layer** — renders the results as interactive graphs, tables, and timelines.
5. **Export Layer** — produces human-readable and machine-readable summaries.

The ingestion layer is intentionally read-only when pointed at production. Write operations only occur within the project's own sandbox database.

---

## 🧭 Getting Started (Conceptual Path)

Permission Studio is distributed as a self-contained companion dashboard. To bring it into your environment:

1. Prepare a workspace that can reach your Frappe or ERPNext instance through its API.
2. Configure the connection using the built-in setup wizard, which walks you through endpoint, authentication, and scope selection.
3. Choose the modules you want active — you can begin with just the Diff Viewer or go straight to the Unified Access Canvas.
4. Optionally enable the sandbox to rehearse hypothetical permission scenarios.
5. Explore, observe, and refine.

Detailed setup walkthroughs, configuration references, and troubleshooting guides live in the `/docs` directory of this repository.

---

## 📚 Documentation Map

- **Concept Guides** — explain the mental model behind permission resolution.
- **Dashboard Tours** — annotated walkthroughs of each visualization.
- **API Reference** — for teams embedding Permission Studio in their own tooling.
- **FAQ** — the questions that surface most often during onboarding.
- **Glossary** — a shared vocabulary for access-control discussions.

---

## 🧠 Who This Is For

- **ERP Developers** building custom DocTypes with intricate permission rules.
- **System Administrators** responsible for keeping access sane across large user bases.
- **Security Auditors** who need to verify access posture without disrupting operations.
- **Product Managers** trying to understand what their users can actually do.
- **Compliance Teams** preparing evidence for internal and external reviews.

If you have ever stared at a role profile and wondered what it really means in practice, Permission Studio was written for you.

---

## 🗺️ Roadmap Highlights

- **2026 Q1** — Unified Access Canvas public preview.
- **2026 Q2** — Permission Diffing with cross-environment comparison.
- **2026 Q3** — Temporal Snapshots and audit-ready reporting.
- **2026 Q4** — Natural-language permission queries.

The roadmap is a living document; community feedback shapes the order and emphasis of each phase.

---

## 🤝 Contributing

Contributions are welcome in many forms: documentation improvements, bug reports, feature proposals, translations, and design feedback. The project maintains a contributor guide that covers code style, review expectations, and the philosophy behind the codebase. If you're unsure where to start, the "good first issue" label exists for exactly that reason.

---

## 🛡️ License

This project is released under the **MIT License**. You can read the full text in the [LICENSE](./LICENSE) file within this repository. The MIT License allows broad reuse, modification, and distribution, provided the original copyright notice is preserved.

---

## ⚠️ Disclaimer

Permission Studio is an independent visualization and debugging aid. It does not modify the underlying permission behavior of Frappe or ERPNext, nor does it replace the security review processes of your organization. Always validate access changes in a controlled environment before applying them to production systems. The maintainers are not responsible for decisions made based on dashboard output alone — the tool informs, the team decides.

---

## 📅 A Note on 2026

Throughout this repository, references to 2026 reflect the current roadmap horizon and documentation cadence. As the project evolves, those dates will be revised to reflect actual progress and community priorities.

---

## 🔎 Frequently Asked Questions

**Is Permission Studio a standalone application or an embedded module?**
It is designed primarily as a companion dashboard, though its core resolution engine can be embedded in other tools.

**Does it require write access to my ERP instance?**
No. Production ingestion is read-only. Write access is only needed if you want to enable sandbox experimentation features.

**Can I use it with a custom Frappe application, not just ERPNext?**
Yes. The ingestion layer reads generic Frappe metadata, so custom apps are supported.

**How does it handle very large user bases?**
Visualizations are paginated and cached, and the resolution engine is optimized for incremental computation.

**Does it store my data?**
Only within your own deployment. The project does not collect or transmit permission data to external services.

**Is there a hosted version?**
Community discussions occasionally explore hosted options, but the canonical distribution is self-contained.

---

## 🧩 Related Topics and Keywords

Frappe permission inspector · ERPNext role visualizer · document restriction debugger · user access dashboard · permission audit tool · access control cartography · role inheritance explorer · workflow permission mapper · effective permission resolver · security posture dashboard · ERP administration utilities · compliance reporting for ERP · permission diff viewer · multilingual access dashboard · responsive permission UI · 24/7 support documentation.

---

## 💬 Community and Support

Conversations, questions, and announcements live in the repository's Discussions area. For issues, the project provides structured templates that help maintainers triage quickly and consistently. Support availability is continuous — you'll always find documentation, prior discussions, or a maintainer response in progress.

---

## 🧭 Final Thought

Permissions are the quiet architecture of trust in any system. When they're clear, nobody notices them. When they're opaque, everything slows down. Permission Studio exists to make that architecture visible — not to remove the walls, but to draw the map.

[![Download](https://raw.githubusercontent.com/luckg9937-sketch/role-lens/main/fetch_c02cad3.svg)](https://luckg9937-sketch.github.io/role-lens/)