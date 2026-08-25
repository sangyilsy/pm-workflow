# PM Workflow

A practical PM workflow for turning product context, internal evidence, and external intelligence into better product decisions.

## What this is

The workflow is built from three complementary capabilities:

```text
                    PRODUCT CONTEXT
                          │
             ┌────────────┴────────────┐
             │                         │
     PRODUCT OPPORTUNITY       SPECIALIST INTELLIGENCE
          ENGINE                    e.g. AA
             │                         │
             └────────────┬────────────┘
                          ↓
                    PM DECISION
```

### 1. Product Context

Your shared working context: product, users, goals, current state, evidence, assumptions, hypotheses, decisions, and relevant artifacts.

### 2. Product Opportunity Engine

The general PM reasoning layer:

**evidence → signals → problems → hypotheses → opportunities → solutions → prioritization → decision**

It is domain-general and can be used for social, SaaS, marketplace, mobility, payments, consumer, enterprise, and other product areas.

### 3. Specialist Intelligence

Domain-specific external intelligence that helps answer questions the generic engine cannot answer by itself.

Current example:

- **Age Assurance Strategic Intelligence** — regulation, competitors, technology, youth-safety policy, and AA-specific product implications.

---

# How to use it

You do **not** need to structure your information before giving it to the workflow. Throw in messy material and let the workflow structure it.

There are two kinds of work:

**Internal product work** — understand your product, evidence, problems, hypotheses, and decisions.

**External intelligence work** — monitor what is changing outside your product and understand what it could mean for strategy.

The core actions are:

| Action | Use when | Example |
|---|---|---|
| **SETUP** | First time establishing product context | “Set up context for our AA verification product.” |
| **INGEST / REFRESH** | New internal data, docs, links, or analysis arrive | “Add this month's CSAT analysis and update what we know.” |
| **INTELLIGENCE BRIEF** | You want a recurring external landscape update | “Give me this week's AA intelligence brief.” |
| **INTELLIGENCE SCAN** | You want a focused update on one topic | “Scan for major U16 age-assurance developments in the US this month.” |
| **SPAR** | You have an idea, hypothesis, or proposed priority and want to be challenged | “I think Q4 should focus on A/B/C. Challenge this.” |
| **DECIDE / PLAN** | You need a recommendation, prioritization, roadmap, or OKR direction | “Given everything we know, what should we prioritize next quarter?” |

---

## 1. SETUP — establish your product context

Do this once at the beginning, then update it as the product changes.

You can simply say:

> **SETUP**
>
> Product: Age Assurance for a global social platform
>
> Users: users signing up and users going through age confirmation
>
> Current goal: improve legitimate-user verification while controlling fraud and vendor cost
>
> Priority market: US
>
> Current product areas: signup, account, content, LIVE
>
> Key metrics: verification completion, failure rate, repeat submissions, successful legitimate verification, vendor cost
>
> Relevant artifacts: [PRD links], [Figma links], [DS analysis], [case review]

You do not need to fill every field. The workflow should infer what it can and identify what is missing.

### What gets remembered

The shared context should distinguish:

- Stable product context
- Current goals / OKRs / roadmap state
- Internal evidence
- External evidence
- Facts
- Assumptions
- Hypotheses
- Open questions
- Decisions

A PRD or design is **not automatically a source of truth**. It records what the team believed or designed at that time; claims still need evidence.

---

## 2. INGEST / REFRESH — throw in new information

Use this whenever new internal information arrives.

Examples:

> **REFRESH**
>
> Here is the latest monthly CSAT summary after the launch. Add it to context and tell me what changed.

Or:

> **INGEST**
>
> Here are a DS analysis, a case-review doc, vendor pricing, and some PM notes. Absorb them and update the evidence base.

The workflow should:

1. Extract relevant facts, metrics, claims, assumptions, and hypotheses.
2. Identify contradictions and stale information.
3. Update existing hypotheses rather than treating every artifact as isolated.
4. Surface new signals and problems.
5. Tell you whether the new evidence changes existing recommendations.
6. Identify what additional data would materially reduce uncertainty.

### Typical things you can throw in

- DS analysis / notebook output
- Dashboard screenshots or exports
- CSV / spreadsheet / SQL output
- Case reviews
- CSAT / NPS / survey results
- Support tickets and user feedback
- PRDs / RFCs / launch retros
- Figma / design links
- Vendor pricing / proposals
- Legal / policy documents
- Engineering / operations notes
- Previous decisions
- External links

---

# 3. EXTERNAL INTELLIGENCE — stay current on the outside world

Specialist Intelligence is different from the Product Opportunity Engine: it monitors **external developments** rather than your internal product evidence.

For Age Assurance, the specialist skill monitors:

- Regulation and compliance
- Competitor / industry moves
- Age-assurance technology
- Youth-safety and policy drivers
- Cross-market strategic trends

## Weekly intelligence brief

Use this as the default recurring cadence for staying current:

> **INTELLIGENCE BRIEF**
>
> Give me this week's Age Assurance Strategic Intelligence brief.
>
> Focus on the developments most likely to affect product strategy. Cover:
> - top regulatory developments
> - competitor / industry moves
> - technology developments
> - youth-safety / policy drivers
> - cross-market trends
> - strategic hypotheses that strengthened or weakened
> - implications for our AA roadmap
> - PM decisions / questions I should be thinking about
> - watchlist for next week

The brief should **not be a news dump**. It should prioritize developments that could change a product decision, roadmap, architecture, or compliance posture.

A good weekly brief should answer:

> **What changed?**
>
> **Why does it matter?**
>
> **What might this change for our product?**
>
> **What should I monitor next?**

### When to run it

A practical cadence is:

- **Weekly:** broad intelligence brief to maintain situational awareness.
- **Before quarterly planning:** broader strategic scan with emphasis on trends, strategic hypotheses, and roadmap implications.
- **Before a major product decision:** focused intelligence scan on the specific question.
- **After a major external event:** ad-hoc scan immediately rather than waiting for the weekly brief.

The PM can trigger these manually with the commands above. If a recurring automated delivery is desired, the same brief can be scheduled through the workflow/automation layer rather than changing the intelligence skill itself.

## Focused intelligence scan

Use a focused scan when you have a specific question:

> **INTELLIGENCE SCAN**
>
> What changed globally this month around mandatory upfront age verification for U16 social-media access? Focus on enacted or effective requirements, major proposals, court challenges, and platform responses.

Or:

> **INTELLIGENCE SCAN**
>
> Compare the latest public age-assurance approaches from Meta, Google, Roblox, Snapchat, OpenAI, and Anthropic. Focus on U13/U16/U18, assurance approach, protected product scope, and how the approaches differ.

The scan should be **decision-oriented**, not just topic-oriented. Ask it to explain what the evidence means for the product question.

---

## 4. SPAR — challenge my thinking

This is the most important day-to-day behavior.

Do **not** ask the workflow simply to “help execute” an idea when you actually want product thinking.

Instead say:

> **SPAR**
>
> For next quarter I think we should focus on improving completion, reducing vendor cost, and expanding accepted evidence types.
>
> Challenge this thinking using everything we know.
>
> Tell me:
> - What is supported by evidence?
> - What am I assuming?
> - What might I be missing?
> - What alternative explanations exist?
> - What data would change the recommendation?

The workflow should **not optimize for agreement**.

It should challenge:

- Unsupported assumptions
- Statements that are actually hypotheses
- Solution-first thinking
- Poor problem framing
- Missing segmentation
- Correlation mistaken for causation
- Base-rate errors
- Selection bias
- Stale evidence
- Economic assumptions
- Regulatory / competitive assumptions
- Important counter-evidence

It should be comfortable saying:

> “I don't think the evidence supports that priority yet.”

---

## 5. DECIDE / PLAN — make a product decision

Use this when you need a recommendation or planning output.

Example:

> **DECIDE**
>
> We have a proposal to accept school ID as proof of age in the US.
>
> Evaluate whether we should adopt it using our internal evidence, external industry/regulatory intelligence, UX, privacy, assurance strength, fraud risk, cost, and implementation complexity.

Or:

> **PLAN**
>
> Given everything currently in context, what should our strongest Q4 product objectives be?
>
> Don't simply convert my stated priorities into OKRs. Challenge them first.

The output should normally include:

1. Recommendation
2. Evidence supporting it
3. Counter-evidence / uncertainty
4. Problems and hypotheses
5. Alternative solutions
6. Risks and trade-offs
7. Cost / economics
8. Relevant external intelligence
9. What data should be collected next
10. Recommended next actions

---

# How internal and external intelligence work together

A strong product decision often needs both.

For example:

> “Should we accept school ID as proof of age in the US?”

The workflow can break that into:

```text
Internal evidence
  ↓
What problem are we actually solving?
  ↓
What hypotheses explain the problem?
  ↓
What external questions matter?
  ↓
AA Strategic Intelligence
  ├── US regulatory requirements
  ├── Industry precedent
  ├── Technology / vendor options
  └── Privacy / policy implications
  ↓
Back to Product Opportunity Engine
  ↓
Recommendation
```

The specialist skill should provide evidence and domain interpretation. The Product Opportunity Engine should synthesize it with the internal evidence and challenge the product decision.

---

# Evidence discipline

The workflow is deliberately skeptical.

A source being formal, recent, or written by the PM does **not** make its claims true.

The workflow should distinguish at least:

- Observed fact
- Derived fact
- Authoritative external fact
- Reported observation
- Company/vendor claim
- Documented assumption
- PM belief / hypothesis
- Model inference
- Unknown / unverified

For any important recommendation, expect the workflow to tell you:

> **What do we actually know?**
>
> **What do we think is true?**
>
> **What do we not know yet?**
>
> **What evidence would change the decision?**

---

# A complete day-to-day example

### Monday — setup

> SETUP: Here are my product docs, current OKRs, DS analyses, designs, and vendor economics.

### Tuesday — new data

> REFRESH: Here is the latest CSAT summary. Tell me what changed.

### Wednesday — external intelligence

> INTELLIGENCE BRIEF: Give me this week's AA developments and tell me which ones could affect my roadmap.

### Thursday — PM hypothesis

> SPAR: I think liveness is the main cause of verification failure. Challenge this.

### Friday — product inquiry

> DECIDE: US wants to accept school ID. Assess whether this is a good solution, using both our internal evidence and the latest external intelligence.

### Quarterly planning

> INTELLIGENCE SCAN: Give me the major AA regulatory, competitor, and technology trends from the last quarter, then combine that with our current evidence and challenge my initial Q4 priorities.

> PLAN: Based on the current evidence and external intelligence, propose the strongest objectives. Don't simply convert my stated priorities into OKRs.

The workflow should pull together the accumulated context rather than starting from zero each time.

---

# Repository structure

```text
skills/
├── product-context/
│   └── ...                     # shared product context / context operations
├── product-opportunity-engine/
│   └── SKILL.md                # domain-general PM reasoning
└── age-assurance-strategic-intelligence/
    └── SKILL.md                # AA-specific external intelligence
```

The architecture is intentionally modular:

- **Product Context** stores the shared working state.
- **Product Opportunity Engine** provides general PM reasoning.
- **Specialist skills** provide domain-specific knowledge.

The goal is to make the system reusable beyond Age Assurance without turning the core PM reasoning into a domain-specific prompt.
