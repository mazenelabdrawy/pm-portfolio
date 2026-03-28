# Case Study: Multi-Agent Pre-Sales System

**Role:** AI Product Manager & Project Lead  
**Company:** Odoo Dubai  
**Domain:** AI Product · Internal Tooling · Sales Enablement

---

## Context

The pre-sales process at Odoo Dubai required consultants to manually build ROI analyses, scope assessments, and tailored proposals for each prospect. This took 2–4 hours per prospect, created inconsistency across the team, and created a bottleneck when multiple deals were in motion simultaneously.

---

## Problem Definition

**The problem wasn't effort — it was cognitive overhead on templated work.**

90% of what a consultant produced in pre-sales followed patterns: same structure, same metrics frameworks, same ROI calculation logic — just with different client inputs. The work felt bespoke but was largely systematic.

The real value a consultant added was in the 10%: judgment calls on feasibility, identifying red flags, and reading the prospect relationship. That was being crowded out by the templated 90%.

---

## Approach

I ran a discovery process with 5 pre-sales consultants:
- Shadow sessions on 3 live prospect analyses
- Time-tracking analysis across 8 engagements
- Template audit: mapped every repeating pattern across 15 previous proposals

Identified 4 discrete tasks that could be AI-automated end-to-end, and 3 that could be AI-assisted (human in the loop).

Designed a multi-agent architecture where each agent owned a specific task, with a coordinator agent managing sequencing and output assembly.

---

## Execution

**Agent Architecture**

| Agent | Responsibility |
|---|---|
| Intake Parser | Extracts structured data from prospect intake form |
| Industry Classifier | Tags vertical and sub-vertical; loads industry-specific templates |
| ROI Analyst | Calculates efficiency gains using Odoo benchmark data per module |
| Proposal Writer | Assembles final proposal document with client-specific framing |
| QA Reviewer | Flags missing data, low-confidence estimates, and edge cases for human review |

**Technical Approach**
- Built on top of Odoo's API and internal data
- LLM orchestration with structured output validation at each step
- Consultant review interface: shows agent outputs with confidence scores and flagged items
- Feedback loop: consultants mark changes → used to improve prompts over time

**Rollout**
- Piloted with 2 consultants for 3 weeks before full team rollout
- Ran parallel (manual + AI) for first 4 engagements to validate accuracy
- Trained team on where to trust the output and where to apply judgment

---

## Outcome

| Metric | Result |
|---|---|
| Pre-sales prep time | ↓ 60% (from ~3 hours to ~70 minutes) |
| Proposal consistency score | Significantly improved (from subjective to structured baseline) |
| Consultant capacity | Each consultant could handle 40% more simultaneous prospects |
| Deal velocity | Faster proposal turnaround → shorter sales cycles |

---

## What I'd Do Differently

- Build the feedback capture UI earlier — the first 6 weeks of corrections were tracked in a spreadsheet
- Add a "deal similarity" feature so consultants can instantly see the 3 closest past deals
- Make confidence scores more visible in the UI; consultants often didn't check them

---

## Skills Demonstrated

`AI Product Management` `Multi-Agent Systems` `LLM Orchestration` `Sales Enablement` `Process Automation` `Internal Tooling` `Prompt Engineering` `Stakeholder Training`
