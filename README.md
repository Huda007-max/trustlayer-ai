# TrustLayer AI

**An agentic GRC layer for financial institutions that turns regulatory requirements into structured, auditable compliance decisions, with human oversight.**

> Compliance teams don't need more documents. They need to know what to do next.

![Status](https://img.shields.io/badge/status-prototype-blue) ![Category](https://img.shields.io/badge/category-RegTech-purple) ![Market](https://img.shields.io/badge/market-Jordan%20%E2%86%92%20MENA%20%E2%86%92%20Global-green)

---

## Overview

TrustLayer AI helps fintechs, payment companies and banks turn complex regulations into actionable controls, find compliance gaps, assess risk and keep audit-ready evidence in one place.

Specialized AI agents return **typed decisions with confidence scores**. Confident, low-impact decisions move automatically. Uncertain or high-impact decisions go to a qualified human. Every step is logged.

```
REGULATION → REQUIREMENTS → CONTROLS → RISKS → GAPS → ACTIONS → EVIDENCE → TRUST SCORE
```

## The problem

- Financial companies receive hundreds of pages of regulation (KYC/KYB, AML/CFT, monitoring, reporting, third-party risk).
- Compliance teams map requirements to controls by hand and track evidence in spreadsheets.
- Gaps are often found during audits, when they are already costly.
- Leaders lack a clear answer to: *"Are we covered, and what do we fix first?"*

## The solution

| Agent | Decision |
|---|---|
| Regulation Agent | Extracts and classifies requirements, with source page and section |
| Control Mapping Agent | Maps each requirement to a control, owner and required evidence |
| Risk Agent | Scores likelihood × impact |
| Gap Detection Agent | Coverage = `FULL` / `PARTIAL` / `MISSING` / `UNKNOWN` + confidence |
| Remediation Agent | Next action, priority, owner and deadline; decides when a human must review |
| Evidence Agent | Checks whether evidence supports a control |
| Orchestrator | Coordinates agents and routes decisions to automation or human review |

**Human-in-the-loop routing (example):**

```
if confidence >= 0.90 and impact != "high":
    create_remediation_action()
else:
    request_human_review()
```

> TrustLayer AI provides decision support. It never makes a legal determination of compliance. Final decisions remain with qualified professionals.

## Features (MVP)

- 📄 Regulatory intake (PDF, DOCX, text)
- 🔎 AI requirement extraction with source traceability
- 🔗 Requirement → control mapping with Accept / Edit / Reject
- ⚠️ Risk register (likelihood × impact)
- 🧩 Gap analysis with "why it matters" and a recommended fix
- ✅ Action center (owner, priority, due date, status)
- 📁 Evidence center and audit trail
- 💬 Ask TrustLayer copilot (answers cite requirements, controls and evidence)
- 📊 GRC dashboard, Trust Score and executive view

**Not in scope yet:** payment processing, wallets, banking integrations, real-time transaction monitoring, mobile app, automated regulatory filing.

## Architecture (planned)

```
User
 └─ Web app (Next.js / React)
     └─ API (Python / FastAPI)
         ├─ Agent orchestrator → specialized agents (typed decisions + confidence)
         ├─ RAG layer over approved regulatory sources
         ├─ GRC rules & risk engine
         ├─ PostgreSQL (companies, regulations, requirements, controls, risks, gaps, actions, evidence)
         └─ Document storage (e.g., AWS S3)
```

**Core data model:** Company → Regulations → Requirements → Controls → Risks → Gaps → Actions → Evidence

The design is model-agnostic. We are evaluating decision-focused models (e.g., TypeSafe Jev) for the typed decision layer.

## Demo

A clickable front-end prototype with **sample data** for a fictional fintech, *JordanPay*.

- ▶️ Live demo: https://huda007-max.github.io/trustlayer-ai/
- Suggested flow: Dashboard → Regulatory Intake → Requirements → Controls → Risk → Gaps → Actions → Executive View

> The demo is a front-end simulation. It has no backend, real AI calls or real customer data.

## Roadmap

| Phase | Focus |
|---|---|
| 1 | Product spec, agent architecture and clickable prototype ✅ |
| 2 | Working MVP + Jordan pilots (fintechs, SME platforms, compliance consultants) |
| 3 | MENA regulatory packs (KSA, UAE, Qatar, Bahrain, Oman) |
| 4 | United States regulatory pack |
| 5 | Global multi-jurisdiction GRC intelligence |

## Status

🟡 **Early stage:** product defined, agent architecture designed, clickable prototype built. Pre-revenue. Looking for a **technical co-founder** and **design partners**.

## Team

- **Huda Ahmad**: Founder & CEO (Product & Operations)
- **Omar Nofal**: Co-Founder (Business & Customer Experience)
- **CTO / AI Engineer**: we're hiring. Get in touch!

## Contact

- LinkedIn: [linkedin.com/in/hudaahmad1](https://www.linkedin.com/in/hudaahmad1)
- Email: huda.trustlayerai@gmail.com
- Location: Amman, Jordan

---

*TrustLayer AI: AI agents turn regulation into action. Humans stay in charge of the decisions that matter.*
