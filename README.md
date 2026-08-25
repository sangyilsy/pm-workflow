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

## The five core actions

| Action | Use when | Example |
|---|---|---|
| **SETUP** | Establish or update shared product context | “Set up context for our AA verification product.” |
| **REFRESH** | New internal or external information arrives | “Add this month's CSAT analysis and update what we know.” |
| **SPAR** | You have an idea, hypothesis, or proposed priority and want to be challenged | “I think Q4 should focus on A/B/C. Challenge this.” |
| **DECIDE** | You need a recommendation, prioritization, roadmap, or OKR direction | “Given everything we know, what should we prioritize next quarter?” |
| **MAJOR-EVENT SCAN** | A monitoring workflow checks for material external developments | Automatically run by the monitoring/automation layer; the PM can also request one manually. |

You do not need separate commands for every kind of intelligence task. Ask naturally, and the relevant specialist intelligence capability should be used when needed.

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

## 2. REFRESH — throw in new information

Use this whenever new information arrives, whether it is internal product evidence or a new external development you want incorporated into the context.

Examples:

> **REFRESH**
>
> Here is the latest monthly CSAT summary after the launch. Add it to context and tell me what changed.

Or:

> **REFRESH**
>
> Here is a new regulatory development. Add it to the AA context, explain which strategic hypotheses it affects, and tell me whether any open product decisions should be revisited.

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

# External intelligence and monitoring

Specialist Intelligence monitors **what is changing outside your product**. For Age Assurance, this includes:

- Regulation and compliance
- Competitor / industry moves
- Age-assurance technology
- Youth-safety and policy drivers
- Cross-market strategic trends

The PM should not need to remember to manually check the world every day. The long-term design is:

```text
External world
      ↓
Monitoring / scheduled trigger
      ↓
Specialist Intelligence
      ↓
Materiality filter
      ↓
Major event?
   ↙       ↘
 No         Yes
 ↓           ↓
Keep       Alert PM
as context    +
             update context
```

A skill is reactive by itself; **automatic Major-Event Scan requires a monitoring/automation layer to invoke the skill on a schedule or from an external trigger**.

### Weekly intelligence

Weekly intelligence is a **cadence**, not a separate core command.

The PM can request it naturally:

> “Give me this week's AA intelligence and tell me which developments could affect my roadmap.”

A scheduled workflow can also run it automatically each week.

The brief should prioritize:

- Top regulatory developments
- Competitor / industry moves
- Technology developments
- Youth-safety / policy drivers
- Cross-market trends
- Strategic hypotheses strengthened or weakened
- Product / roadmap implications
- PM decisions or questions worth considering
- Watchlist

It should **not be a news dump**. The brief should answer:

> **What changed?**
>
> **Why does it matter?**
>
> **What might this change for our product?**
>
> **What should I monitor next?**

### Major-event monitoring

The monitoring workflow should evaluate recent developments against a materiality threshold. Examples of potential major events include:

- A law or regulation that materially changes platform obligations
- A significant court decision
- Major regulator guidance
- A major platform changing its age-assurance approach
- A meaningful technology development that changes the assurance/friction/cost trade-off
- A development that materially strengthens or weakens a strategic hypothesis
- An event likely to require product, architecture, policy, or roadmap response

Most monitoring cycles should produce **no alert**. The goal is to interrupt the PM only when something is genuinely material.

The PM can also request an ad-hoc scan after hearing about something important:

> “MAJOR-EVENT SCAN: Check what happened with the new France age-assurance development and tell me whether it is material for our roadmap.”

---

## 3. SPAR — challenge my thinking

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

## 4. DECIDE — make a product decision

Use this when you need a recommendation or planning output.

Example:

> **DECIDE**
>
> We have a proposal to accept school ID as proof of age in the US.
>
> Evaluate whether we should adopt it using our internal evidence, external industry/regulatory intelligence, UX, privacy, assurance strength, fraud risk, cost, and implementation complexity.

Or:

> **DECIDE**
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

### Wednesday — monitoring

> The monitoring workflow checks for major AA developments. If one crosses the materiality threshold, it alerts the PM and updates the shared context.

### Thursday — PM hypothesis

> SPAR: I think liveness is the main cause of verification failure. Challenge this.

### Friday — product inquiry

> DECIDE: US wants to accept school ID. Assess whether this is a good solution, using both our internal evidence and the latest external intelligence.

### Weekly

> “Give me this week's AA intelligence and tell me which developments could affect my roadmap.”

### Quarterly planning

> “Review the last quarter of AA developments, combine them with our current evidence, and challenge my initial Q4 priorities.”

> “DECIDE: Based on the current evidence and external intelligence, propose the strongest objectives. Don't simply convert my stated priorities into OKRs.”

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
- **Monitoring/automation** invokes specialist intelligence on a schedule or when an external trigger is available.

The goal is to make the system reusable beyond Age Assurance without turning the core PM reasoning into a domain-specific prompt.
