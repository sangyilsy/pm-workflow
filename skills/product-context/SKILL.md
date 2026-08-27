# Product Context

A shared, durable context layer for PM workflows and stakeholder-facing product knowledge.

## Purpose

Maintain a compact, living representation of a product so other capabilities do not have to repeatedly reconstruct the same background from scattered documents.

Product Context is **not** a decision-making skill and is not a replacement for source documents. It is a structured knowledge layer that records what the organization currently believes, what is supported by evidence, what has changed, what is planned, and what remains uncertain.

## Core principle

> **A document is evidence of what was documented, not automatic proof that the underlying statement is true.**

A PRD may describe intended behavior. A Figma file may describe proposed UX. A roadmap may describe an intention. A launch document may describe what was shipped. Production telemetry may show what actually happened. Keep these distinct.

## What belongs in Product Context

### Stable context

- Product / service description
- Target users and important segments
- Core user problems / jobs to be done
- Product surfaces and important journeys
- Markets / geographies
- Important terminology
- Known dependencies and constraints
- Ownership / organizational context where appropriate

### Current state

- What is currently live
- Current product behavior / user flow
- Current policies / rules
- Current integrations / adopters
- Current goals / OKRs
- Current roadmap priorities
- Current metrics where appropriate
- Current experiments
- Current vendors / partners where relevant
- Current decisions and known limitations

### Historical state

- Previous product behavior
- Launches / rollouts / rollbacks
- Material changes and effective dates
- Superseded requirements/designs
- Historical decisions and their rationale when documented

### Future state

Always distinguish:

- **Committed** — approved/planned work the organization has committed to
- **Targeted** — intended timing/outcome, but not fully committed
- **Proposed** — recommendation or idea under consideration
- **Exploratory** — being investigated
- **Deprecated** — intended for removal/replacement

Never present proposed, targeted, or exploratory work as committed behavior.

### Evidence

- Quantitative analysis
- Qualitative research
- User feedback / support / CSAT
- Case reviews
- PRDs / RFCs / requirements
- Design / Figma / prototypes
- Launch / rollout / retrospective material
- Engineering / implementation documentation
- Vendor information and economics
- Legal / policy / compliance documentation
- PM / operations notes
- External intelligence intentionally attached as context

## Evidence and epistemic status

For material claims, distinguish at least:

- **Observed fact** — directly measured or observed with clear provenance.
- **Derived fact** — transparent calculation from observed data.
- **Authoritative external fact** — supported by an authoritative external source.
- **Reported observation** — reported by a user, operator, researcher, or other source and potentially requiring corroboration.
- **Company/vendor claim** — statement made by a company or vendor about its product or performance.
- **Documented assumption** — assertion embedded in a PRD, design, plan, or previous analysis without sufficient evidence.
- **PM belief / hypothesis** — current interpretation or proposed explanation.
- **Inference** — conclusion derived from available evidence but not directly observed.
- **Unknown / unverified** — insufficient evidence.

Never silently upgrade an assumption or hypothesis into a fact because it appears in a formal document or has been repeated over time.

## Source hierarchy by question

Use the source best suited to answering the specific question.

### What is live today?

Prefer:

1. Current production / implementation evidence
2. Current support / operations material that reflects actual behavior
3. Launch / release documentation
4. Current approved requirements/designs
5. Older documentation

### What was intended?

Prefer:

1. Approved requirements
2. Approved design
3. Roadmap / planning material

### What actually happened historically?

Prefer:

1. Dated launch/release records
2. Production evidence
3. Retrospectives / change logs
4. Historical requirements/designs

### What is planned?

Prefer:

1. Current approved roadmap / planning decisions
2. Explicitly approved project plans
3. Targeted plans
4. Proposals / exploratory documents

Always state commitment level when material.

## Context operations

### SETUP

Use when establishing product context for the first time.

A PM can provide a lightweight profile or simply dump material:

```text
Product / service:
Target users:
Primary goals:
Important journeys / surfaces:
Markets:
Current priorities / OKRs:
Key metrics:
Known constraints:
Relevant specialist intelligence:
Artifacts / links:
```

All fields are optional. Infer only what is supported by the supplied material and explicitly mark unknowns.

### INGEST

Add one or more new artifacts to the context.

The PM does not need to pre-structure the data. Extract relevant claims, facts, decisions, assumptions, and hypotheses and record provenance.

### REFRESH

Use whenever new information arrives.

Reconcile it with existing context. Identify:

- New facts
- Superseded information
- Contradictions
- Updated current state
- Updated future state
- Strengthened / weakened hypotheses
- Decisions that may need review
- Information that has become stale

### CHECK

Use to inspect the current context.

Examples:

- “What do we currently know about this product?”
- “What is actually live today?”
- “What changed since June?”
- “What is planned versus merely proposed?”
- “Which important claims are still unverified?”
- “Where do our sources conflict?”

## Change ledger

Maintain a logical change history when evidence permits:

- Change ID
- Date / effective date
- Product area
- Previous state
- New state
- Reason, if documented
- Source
- Rollout status
- Impacted stakeholders
- Superseded-by information

Do not infer causality merely because a product change preceded a metric, CSAT, or support-volume change. Record temporal association separately from causal evidence.

## Current-state synthesis

When answering “how does it work today?” do not simply retrieve the newest document.

Reconstruct the current state by reconciling the strongest available evidence and effective dates. Clearly distinguish:

- Intended behavior
- Shipped behavior
- Observed behavior
- Planned behavior

If the evidence does not establish current behavior confidently, say so and identify the source of uncertainty.

## Context freshness

Classify information as:

- **Current** — likely representative now
- **Aging** — still potentially useful but should be refreshed
- **Stale** — should not materially drive a current decision/answer without validation
- **Historical** — useful for history, not current state

Freshness matters especially for metrics, user behavior, model performance, vendor information, roadmap, policies, and operational procedures.

Recency does not by itself establish truth. Consider **recency + source strength + relevance to the claim**.

## Stakeholder and access considerations

Product Context may contain sensitive or internal-only information. Only expose information appropriate for the requesting audience and available authorization.

When audience or authorization is unclear, avoid disclosing sensitive details and provide a higher-level answer.

## Relationship to other capabilities

Product Context is the universal foundation.

- **Product Q&A** uses it to provide stakeholder-facing product knowledge.
- **Product Opportunity Engine** uses it to understand product state, evidence, assumptions, and decisions before reasoning about opportunities.
- **Specialist Intelligence** can consume Product Context to understand why external developments matter to the product. External intelligence should remain distinguishable from internal product facts.
