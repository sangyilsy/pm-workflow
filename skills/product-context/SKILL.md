# Product Context

A shared context layer for PM workflows and specialist skills.

## Purpose

Maintain the durable context needed to reason about a product without forcing every specialist skill to ingest the same background repeatedly.

Product Context is a **shared context capability, not a standalone analysis skill**. It stores product facts, current state, evidence, hypotheses, assumptions, decisions, and constraints so other workflows can consume the same source of truth.

## What belongs here

### Stable context

- Product/domain description
- Target users and key segments
- Core user problems
- Product surfaces/journeys
- Markets/geographies
- Important terminology
- Known constraints

### Current state

- Current goals / OKRs
- Current roadmap priorities
- Current product metrics
- Current experiments
- Current vendors/partners where relevant
- Current decisions

### Evidence base

- Quantitative analyses
- Qualitative research
- Case reviews
- User feedback / support / CSAT
- Product and design artifacts
- Cost/economic information
- External evidence when intentionally added

### Epistemic state

- Observed facts
- Derived facts
- External authoritative facts
- Reported observations
- Company/vendor claims
- Documented assumptions
- PM beliefs/hypotheses
- Model inferences
- Unknown/unverified claims
- Open questions

## Evidence discipline

A source tells us what was written or observed; it does not automatically establish truth.

A PRD, design, previous analysis, vendor proposal, or PM note may state a hypothesis as though it were a fact. Preserve the claim, but independently classify its epistemic status.

Never silently upgrade a hypothesis because it appears in a formal, old, or authoritative-looking document.

When claims conflict, surface the conflict and prefer better-supported evidence.

## Context operations

### SETUP

Use when establishing product context for the first time.

The PM can provide a lightweight profile such as:

```text
Product / domain:
Target users:
Primary product goal:
Key user journeys / surfaces:
Markets:
Current priorities / OKRs:
Key metrics:
Known constraints:
Relevant specialist skills:
Initial artifacts / links:
```

All fields are optional. The system should infer what it safely can from supplied material and explicitly flag what remains unknown.

### INGEST

Use when adding a substantial body of artifacts.

Accept messy inputs without requiring the PM to pre-structure them. Record source, date/time period, type, scope, freshness, epistemic status, and limitations.

### REFRESH

Use whenever new information arrives.

Identify what is new, what it updates or supersedes, which hypotheses/decisions are strengthened or weakened, and which prior assumptions may now be stale.

### CHECK

Use to inspect the current context.

Examples:

- What do we currently know about this product?
- What are our strongest hypotheses?
- Which assumptions are unverified?
- What evidence is stale?
- What decisions are currently open?

## How other skills consume Product Context

### Product Opportunity Engine

Consumes Product Context to understand the product, current state, evidence, hypotheses, constraints, and decisions before analyzing opportunities or challenging PM thinking.

### Specialist intelligence skills

Consume Product Context to understand why external developments matter to the product. They should not overwrite internal evidence with external assumptions.

Example: Age Assurance Strategic Intelligence can use Product Context to map a new regulation to the relevant product surfaces, age cohorts, user journeys, and current roadmap.

## Context lifecycle

Do not treat the context as an unlimited transcript. Maintain a compact current-state representation plus linked evidence.

Track freshness for information that changes frequently, including metrics, user behavior, vendor performance/pricing, market conditions, regulatory status, and competitor behavior.

Historical artifacts remain useful for understanding decisions and trends but should not automatically be treated as current state.
