# Product Context

A shared, durable context layer for PM workflows and stakeholder-facing product knowledge.

## Purpose

Maintain a compact, living representation of a product so other capabilities do not have to repeatedly reconstruct the same background from scattered documents.

Product Context is not a decision-making skill and is not a replacement for source documents. It records what the organization currently believes, what is supported by evidence, what has changed, what is planned, and what remains uncertain.

## Core principle

> A document is evidence of what was documented, not automatic proof that the underlying statement is true.

A PRD may describe intended behavior. A Figma file may describe proposed UX. A roadmap may describe an intention. A launch document may describe what was shipped. Production telemetry may show what actually happened. Keep these distinct.

## Context contents

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
- Historical decisions and rationale when documented

### Future state
Always distinguish:
- **Committed** — approved/planned work the organization has committed to
- **Targeted** — intended timing/outcome, but not fully committed
- **Proposed** — recommendation or idea under consideration
- **Exploratory** — being investigated
- **Deprecated** — intended for removal/replacement

Never present proposed, targeted, or exploratory work as committed behavior.

## Evidence and epistemic status

For material claims, distinguish:
- **Observed fact** — directly measured or observed with clear provenance.
- **Derived fact** — transparent calculation from observed data.
- **Authoritative external fact** — supported by an authoritative external source.
- **Reported observation** — reported by a user, operator, researcher, or other source and potentially requiring corroboration.
- **Company/vendor claim** — statement made by a company or vendor.
- **Documented assumption** — assertion embedded in a PRD, design, plan, or prior analysis without sufficient evidence.
- **PM belief / hypothesis** — current interpretation or proposed explanation.
- **Inference** — conclusion derived from evidence but not directly observed.
- **Unknown / unverified** — insufficient evidence.

Never silently upgrade an assumption or hypothesis into a fact because it appears in a formal document or has been repeated over time.

## Source hierarchy by question

### What is live today?
Prefer production/implementation evidence, current support/operations material, launch/release documentation, then current approved requirements/designs.

### What was intended?
Prefer approved requirements, approved design, then roadmap/planning material.

### What actually happened historically?
Prefer dated launch/release records, production evidence, retrospectives/change logs, then historical requirements/designs.

### What is planned?
Prefer current approved roadmap/planning decisions, then approved project plans, targeted plans, proposals, and exploratory documents.

When sources disagree, surface the conflict and explain which source is stronger for the particular claim.

## Context operations

### SETUP
Establish product context for the first time. The PM may provide a lightweight profile or simply dump material. All fields are optional.

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

### INGEST
Add one or more artifacts. Extract relevant claims, facts, decisions, assumptions, hypotheses, dates, populations, and limitations.

### REFRESH
Add new information and reconcile it with existing context. Identify new facts, superseded information, contradictions, updated current/future state, changed hypotheses, decisions needing review, and stale information.

### CHECK
Inspect the current context: what is well established, uncertain, stale, conflicting, planned, or missing.

## Artifact ingestion

Accept unstructured inputs such as PRDs, RFCs, Figma/design links, DS analyses, dashboards, spreadsheets, launch retrospectives, support materials, case reviews, vendor information, legal/policy documents, roadmaps, decision records, and PM/engineering/operations notes.

The PM does not need to classify them beforehand.

If a linked artifact cannot be accessed, state that clearly and do not invent its contents.

## Change ledger

Maintain a logical history when evidence permits:

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

Do not infer causality merely because a product change preceded a metric, CSAT, or support-volume change.

## Current-state synthesis

When answering “how does it work today?”, reconstruct current behavior from the strongest available evidence and effective dates. Distinguish intended, shipped, observed, and planned behavior.

If evidence does not establish current behavior confidently, say so.

## Freshness

Classify information as Current, Aging, Stale, or Historical. Recency alone does not establish truth; consider recency, source strength, and relevance.

## Stakeholder/access considerations

Context may contain sensitive internal information. Only expose information appropriate for the audience and available authorization. When authorization is unclear, err toward a higher-level answer.

## Relationship to other capabilities

Product Context is the universal foundation.

- **Product Q&A** uses it for stakeholder-facing product knowledge.
- **Product Opportunity Engine** uses it for product state, evidence, assumptions, constraints, and decisions.
- **Specialist Intelligence** can consume it to understand why external developments matter to the product. External intelligence remains distinguishable from internal product facts.
