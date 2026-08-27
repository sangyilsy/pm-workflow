# PM Workflow

A modular PM workflow for turning product knowledge, internal evidence, and domain intelligence into better product decisions — and making product knowledge easier for stakeholders to access.

## The architecture

```text
                         PRODUCT KNOWLEDGE
                               │
                        Product Context
                         /            \
                        ↓              ↓
                Product Q&A      PM Reasoning
                  (XFN)                │
                                     ↕
                           Specialist Intelligence
                              (domain-specific)
```

### Product Context — universal foundation

The shared, living representation of the product:

- What the product is and who uses it
- What is live today
- What changed historically
- What is planned and how committed it is
- Evidence, assumptions, hypotheses, decisions, and constraints

### Product Q&A — for stakeholders

Self-service product knowledge for Customer Support, Operations, Business, Legal, Policy, Government Relations, PR, Sales, Engineering, and other stakeholders.

It answers questions such as:

- How does this feature work?
- What is live today?
- What changed recently?
- What is planned?
- Who is already using the service?
- How should Support troubleshoot this?
- Did we support this capability in 2024?

### Product Opportunity Engine — for PMs

The domain-general reasoning layer:

**evidence → signals → problems → hypotheses → opportunities → solutions → prioritization → decision**

It is designed to challenge PM thinking, identify missing evidence, explore multiple intervention types, and prioritize based on impact, confidence, risk, economics, and effort.

### Specialist Intelligence — optional, domain-specific

External intelligence for domains where dedicated expertise is useful.

Current example:

- **Age Assurance Strategic Intelligence** — regulation, competitors, technology, youth-safety policy, and AA-specific product implications.

Specialist intelligence is optional; it is not a required layer for every product area.

---

# How a PM uses the workflow

You do not need to pre-structure your information. Throw in the documents, links, numbers, notes, or hypotheses you have and let the workflow organize them.

There are four core actions:

| Action | Use it when | Example |
|---|---|---|
| **SETUP** | Establishing the shared product context | `SETUP: Here are our PRDs, OKRs, metrics, designs and key constraints.` |
| **REFRESH** | New information arrives | `REFRESH: Here is the latest CSAT analysis. Tell me what changed.` |
| **SPAR** | You have a hypothesis, idea, or priority and want challenge | `SPAR: I think A/B should be our top priorities. Challenge this.` |
| **DECIDE** | You need a recommendation, prioritization, roadmap or OKR decision | `DECIDE: Given everything we know, what should we prioritize next quarter?` |

### Keeping external intelligence current

For domains with a specialist intelligence skill, use the same workflow when external context matters.

- **Weekly:** run a broad intelligence brief to maintain situational awareness.
- **Before a major decision:** request a focused intelligence check on the relevant question.
- **After a major external event:** run a major-event scan immediately rather than waiting for the weekly brief.

For Age Assurance, the specialist skill can be invoked explicitly in a request such as:

> `DECIDE: Should we accept school ID as proof of age in the US? Use our internal evidence and the latest AA regulatory, competitor and technology intelligence.`

Major-event monitoring can also be automated through a scheduled workflow. The intelligence skill determines whether a development is material enough to surface to the PM; the PM does not have to remember to check every day.

---

# Working with messy product information

Typical inputs include:

- PRDs / RFCs
- Figma / design links
- Data-science analyses
- Dashboards / spreadsheets / SQL outputs
- Case reviews
- CSAT / survey / support data
- Launch retrospectives
- Vendor information and pricing
- Engineering / operations notes
- Roadmaps and decision records
- PM notes and hypotheses

A formal document is not automatically a source of truth. The workflow distinguishes actual facts from documented assumptions, PM beliefs, vendor claims, and inferences.

For important answers or decisions, expect it to tell you:

> **What do we actually know?**
>
> **What do we think is true?**
>
> **What do we not know yet?**
>
> **What evidence would change the conclusion?**

---

# Repository structure

```text
skills/
├── product-context/
│   └── SKILL.md
├── product-qna/
│   ├── SKILL.md
│   └── README.md
├── product-opportunity-engine/
│   └── SKILL.md
└── age-assurance-strategic-intelligence/
    └── SKILL.md
```

The architecture is intentionally modular:

- **Product Context** is the universal knowledge foundation.
- **Product Q&A** makes that knowledge self-service for stakeholders.
- **Product Opportunity Engine** provides general PM reasoning.
- **Specialist Intelligence** adds domain-specific external intelligence when useful.
