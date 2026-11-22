# Market and YC notes

Compiled 22 Nov 2026. Market-size figures come from commercial research firms and vary a lot. Quote them as "one estimate", never as fact.

## What YC says it wants (ycombinator.com/rfs)
- **Spring 2026: AI-Native Agencies** (Aaron Epstein). Agencies scale only by adding people, and AI changes that. In short: sell the finished work, not the tool.
- **Summer 2026: AI-native service companies.** Insurance brokerage, accounting, tax, audit, compliance and healthcare administration named as areas to replace outsourced services.
- **Fall 2026:** AI compliance infrastructure; software that lets AI operate in regulated industries (healthcare, finance, compliance); financial infrastructure for transactions made by agents.
- **Winter 2027 (current, 11 requests):** most relevant are "AI for the Air-Gapped Economy" (Brad Flora: on-prem frontier AI with deployment tooling and security accreditation for defense, banks, hospitals) and "The $15-an-Hour Expert" (AI doing specialist paperwork such as billing and claims). No request specifically covers logistics or India.

## AI governance / compliance (idea 01)
- **Demand:** 56% of enterprises take 6–18 months from GenAI idea to production; 55% manage AI use-case intake with spreadsheets and email (ModelOp / Corinium 2025).
- **Delays:** 82.9% of organisations had AI projects delayed by security or compliance reviews (EMA / Protegrity, April 2026).
- **Banks:** governance is their top barrier to AI performance; only 18% are fully confident in their AI controls (Grant Thornton 2026).
- **Manual effort:** 100+ hours of manual documentation per model (ValidMind, via SiliconANGLE).
- **Market size:** one estimate is $839M (2025) growing to $13.07B (2035) (GMI); other estimates differ widely.
- **Competitors:**
  - ValidMind: $8.1M seed, model risk management for banks.
  - ServiceNow AI Control Tower: governance dashboard, expanded May 2026.
  - Credo AI, Vanta and Drata: compliance platforms.
- **Cautionary tale:** Delve (YC) raised $32M at a $300M valuation, was accused of fabricating audit evidence and was dropped by YC in April 2026. Lesson: never generate evidence, only link to it.
- **India drivers:**
  - RBI FREE-AI framework (13 Aug 2025): board-approved AI policy, accountability, a suggested board-policy outline and an AI incident reporting form.
  - DPDP Rules: notified 13 Nov 2025; most obligations, including Significant Data Fiduciary assessments and audits, apply from **13 May 2027**.
- **ServiceNow automation:** the Change Management REST API (`/api/sn_chg_rest/change/normal`, `/change/standard/{template}`) creates and updates change requests, so there's no need to drive the UI. Free personal developer instances exist for demos.

## Freight audit and payment (idea 02)
- **Global market:** about $0.97B (2025) to $1.89B (2030) per Mordor Intelligence; other firms say $0.8–1.3B.
- **India:** logistics costs are 7.97% of GDP, ₹24.01 lakh crore (FY24, government study); road carries 65% of freight.
- **Leakage:** Fretron (an Indian vendor) says audits flag 5–8% of transporter invoices, ₹1–2 Cr a year on a ₹50 Cr freight budget. This is the vendor's own claim.
- **Comparables:** Lighthouz AI (YC S24, US freight-broker AP, AR and audit); Evos ($9M pre-seed, $1M+ ARR, auditing LTL invoices); Shipium Always On Audit.
- **India-specific rules:** Section 43B(h) requires paying registered micro and small enterprises within 15 days (no written contract) or 45 days (written contract).
- **Diesel price source:** PPAC publishes IOCL's Delhi diesel retail price (₹87.67/L on 20 Feb 2026).
- **Bank-detail fraud:** e.g. Yash Highvoltage lost ₹2.10 Cr to a payment diversion scam (Mar 2026).
- **Gotcha:** RazorpayX account validation (penny drop) is not supported in test mode.
