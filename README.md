# PM Workflow

A modular PM workflow for turning product knowledge, internal evidence, and domain intelligence into better product decisions — and making product knowledge easier for stakeholders to access.

## Architecture

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
                              (optional/domain-specific)
```

### Product Context — universal foundation

The shared, living representation of the product: what it is, who uses it, what is live, what changed, what is planned, the evidence behind it, and what remains uncertain.

### Product Q&A — for stakeholders

Self-service product knowledge for Customer Support, Operations, Business, Legal, Policy, Government Relations, PR, Sales, Engineering, and other stakeholders.

Use it for questions such as:

- How does this feature work?
- What is live today?
- What changed recently?
- What is planned?
- Which teams use this service?
- How should Support troubleshoot this?
- Did we support this capability in 2024?

### Product Opportunity Engine — for PMs

The domain-general reasoning layer:

**evidence → signals → problems → hypotheses → opportunities → solutions → prioritization → decision**

Use it to challenge assumptions, find problems and root-cause hypotheses, explore non-obvious solutions, and prioritize using impact, evidence confidence, risk, economics, and effort.

### Specialist Intelligence — optional and domain-specific

External intelligence for domains where dedicated expertise materially matters.

Current example:

- **Age Assurance Strategic Intelligence** — regulation, competitors, technology, youth-safety policy, and AA-specific product implications.

Specialist Intelligence is not required for every product area and should remain distinct from internal product facts.

---

# The five core actions

| Action | Use it when | Example |
|---|---|---|
| **SETUP** | Establish or update the shared product context | `SETUP: Here are our PRDs, OKRs, metrics, designs and key constraints.` |
| **REFRESH** | New information arrives | `REFRESH: Here is the latest CSAT analysis. Tell me what changed.` |
| **SPAR** | You have an idea, hypothesis, or priority and want to be challenged | `SPAR: I think A/B should be our top priorities. Challenge this.` |
| **DECIDE** | You need a recommendation, prioritization, roadmap, or OKR decision | `DECIDE: Given everything we know, what should we prioritize next quarter?` |
| **MAJOR-EVENT SCAN** | A monitoring workflow checks for a material external development | Run automatically by a monitoring/automation layer; the PM can also request it manually. |

You do not need a separate command for every question. Ask naturally and use the relevant capability when needed.

## SETUP — establish context

Do this once at the beginning and update it when the product materially changes. You can also simply dump your existing product materials and ask the workflow to build context from them.

```text
SETUP
Product / service: ...
Target users: ...
Primary goals: ...
Important journeys / surfaces: ...
Markets: ...
Current priorities / OKRs: ...
Key metrics: ...
Known constraints: ...
Relevant specialist intelligence: ...
Artifacts / links: ...
```

Fields are optional. The system should infer only what is supported and label what remains unknown.

## REFRESH — keep context current

Use whenever a new document, analysis, design, metric, case review, decision, or external development arrives.

The PM can simply throw in messy material. The system should reconcile it with existing context, identify what changed, update hypotheses/decisions, and flag stale or conflicting information.

Examples:

> `REFRESH: Here is the latest monthly CSAT summary. Add it to context and tell me what changed.`

> `REFRESH: Here is a new launch doc and Figma. Reconcile them with the current product state.`

## SPAR — challenge my thinking

Use when you have a thesis or proposed direction.

> `SPAR: I think these three problems should be our Q4 priorities. Challenge this using the evidence.`

The workflow should distinguish facts from assumptions and hypotheses, look for alternative explanations, missing segmentation, stale evidence, counter-evidence, economics, and domain constraints. It should be willing to say that the evidence does not support the proposed priority.

## DECIDE — make a product decision

Use for product proposals, roadmap decisions, investments, experiments, or OKR planning.

> `DECIDE: Given the current evidence, should we adopt this proposal? Show alternatives, evidence, risks, economics, and unknowns.`

When relevant, explicitly ask it to cross-check external intelligence:

> `DECIDE: Should we accept this proposal? Use our internal product evidence and the latest relevant external intelligence.`

The output should normally include the recommendation, evidence and counter-evidence, key hypotheses, alternatives, risks/trade-offs, economics, remaining uncertainty, and next actions.

---

# External intelligence for fast-moving domains

Specialist Intelligence is optional and domain-specific. For Age Assurance, it monitors regulation, competitors, technology, youth-safety policy, and cross-market trends.

### Weekly intelligence

Weekly intelligence is a **cadence**, not a separate core action. Ask naturally:

> `Give me this week's AA intelligence and tell me which developments could affect my roadmap.`

A scheduled workflow can also run this automatically each week.

The brief should prioritize:

- Material regulatory developments
- Competitor / industry moves
- Technology developments
- Relevant policy or market drivers
- Cross-market trends
- Strategic hypotheses strengthened or weakened
- Product / roadmap implications
- PM questions and watchlist

It should not be a news dump. The brief should answer:

> **What changed? Why does it matter? What might this change for our product? What should I monitor next?**

### Major-event monitoring

The monitoring/automation layer can run a recurring scan of the external landscape. Specialist Intelligence evaluates candidate developments and surfaces only those that cross a materiality threshold.

A major event could be:

- a material new regulation or court decision
- major regulator guidance
- a major platform changing its approach
- a technology development that materially changes the cost/friction/assurance trade-off
- an event that materially strengthens or weakens a strategic hypothesis
- an event likely to require product, architecture, policy, compliance, or roadmap response

Most monitoring cycles should produce **no alert**. The goal is to interrupt the PM only when something is genuinely material.

> `MAJOR-EVENT SCAN: Check the latest development and tell me whether it is material for our product.`

A skill is reactive on its own; automatic monitoring requires an automation/scheduling layer to invoke it.

---

# Product Q&A — stakeholder use

Product Q&A is designed primarily for stakeholders, not for the PM's strategic reasoning.

Stakeholders can ask natural questions such as:

> `How does the latest flow work?`

> `A customer is stuck here. What should Support tell them?`

> `What changed in the last 30 days that could explain this increase in contacts?`

> `Which business teams are currently using this service?`

> `What changes are planned that Operations should prepare for?`

> `What is the current state of this product for Legal?`

> `Did we support this capability in 2024?`

The skill uses Product Context and prioritizes **accuracy, freshness, provenance, and audience usefulness**. It should distinguish current, historical, intended, observed, and planned states and should not invent missing information.

---

# Evidence discipline

Formal documents are not automatically truth.

A PRD may contain a hypothesis. A Figma file may describe intended UX. A roadmap may describe a plan. A launch record may describe what shipped. Production or support evidence may describe what actually happens.

For important answers and decisions, the workflow should distinguish:

- Observed facts
- Derived facts
- Authoritative external facts
- Reported observations
- Company/vendor claims
- Documented assumptions
- PM beliefs/hypotheses
- Inferences
- Unknowns

The core questions are:

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
- **Product Q&A** exposes that knowledge to stakeholders.
- **Product Opportunity Engine** provides universal PM reasoning.
- **Specialist Intelligence** adds domain-specific external intelligence where useful.
- **Monitoring/automation** invokes Specialist Intelligence on a schedule or external trigger.
