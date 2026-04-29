---
use_case: AI-Enabled Complaint Intake
source: 4/28/2026 Ortho JR PCMH Deep Dive (raw/4282026 Ortho JR PCMH Deep Dive.pdf, reference/PMCH_Phase_2.pptx)
date_generated: 2026-04-28
---

---

### AI-Enabled Complaint Intake

An AI layer embedded at the point of complaint submission validates field rep MS Form responses against required TrackWise fields, surfaces data quality issues in real time, and performs early failure mode pre-classification before the complaint enters the specialist review queue. The solution directly targets the 40–50% of ~40K annual JR & MET complaints that require manual follow-up due to incomplete or ambiguous intake data, reducing rework, compressing the 90-day closure cycle, and lowering regulatory audit exposure. The current flow—MS Forms → Power Automate → SharePoint list → manual specialist review → TrackWise—contains no automated validation; any Phase 2 solution must preserve a human-in-the-loop review gate, and the UIPath RPA migration replacing Power Automate is still being scoped.

| Bucket | Weight | Score (1–5) | Descriptor |
|--------|--------|-------------|------------|
| **VALUE** | 5 | 4 | Reduces rework, audit risk, and 90-day closure delays across high-volume complaint pipeline |
| **COST** | 2 | 3 | Moderate cost; requires AI validation layer, TrackWise API integration, and RPA coordination |
| **EFFORT** | 3 | 2 | High effort; regulated environment, multi-system integration, and HITL architecture add complexity |
| **REACH** | 4 | 5 | Intake process is universal; JR & MET prototype (40K/yr) is scalable to 131K complaints across all Stryker divisions |

> **Composite Score: 52 / 70**

---

## Scoring Assumptions & Flags

- **VALUE (4)**: Scored conservatively vs. 5 because Phase 1 already addressed failure mode classification for straightforward cases; Phase 2 is incremental improvement on an established foundation.
- **COST (3)**: Architecture for RPA replacement (UIPath) is undefined; if the intake application is net-new rather than a forms enhancement, cost pressures up toward 2. *Revisit after architecture session.*
- **EFFORT (2)**: Low score reflects the regulated medical device context (TrackWise validation, 21 CFR Part 820 traceability requirements), multi-system touchpoints, and the dependency on IT to own the automation long-term.
- **REACH (5)**: Stryker explicitly noted complaint intake "applies across Stryker" — the 40K JR & MET volume is the prototype; 131K enterprise-wide is the ceiling.

---

## Key Details from Deep Dive (4/28/2026)

**Problem framing**
- Front-end intake is fragmented: MS Forms → Power Automate email → SharePoint list → manual review → TrackWise
- No automated data validation; specialists manually vet form content for typos and missing fields before TrackWise entry
- 40K complaints/year (JR & MET); 131K across all Stryker divisions
- Metric: close within 90 days; current delays create poor customer experience and regulatory audit risk
- 40–50 FTE working on complaints today

**Phase 1 context**
- Built in-house AI to classify failure mode against the Master File
- Runs on a scheduled basis (Mon/Fri); AI handles straightforward cases, team reviews and provides feedback
- Categorization happens at the complaint (child) level, not the PI (parent) level

**Phase 2 focus**
- Make the intake "front door" smarter, cleaner, faster, and more compliant
- Standardize intake channel (MS Forms or equivalent; eliminate phone/email intake)
- Add failure mode pre-classification earlier — at the point of form submission
- Key goal: **completeness and data quality at intake**
- Replacing Power Automate with UIPath (rationale and scope TBD — follow-up needed)

**Architecture constraints**
- A new solution cannot go directly from user submission to TrackWise — a manual review gate must remain
- Expectation that automation will move to IT ownership, not remain in the business
- Language of record in TrackWise is English; high US volume means English-first is appropriate

**Open questions (from session)**
- Inputs & outputs for the current failure mode classification model
- Full architecture of the Phase 1 solution
- Rationale for the current Power Platform–only build (skillset gap vs. deliberate choice)
- What the "master file" is and how it's maintained
- Where exactly the human review step fits in a redesigned flow
- What a prototype application would look like and own

---
