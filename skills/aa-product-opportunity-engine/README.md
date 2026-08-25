# Product Opportunity Engine

A domain-general product discovery, hypothesis-testing, and prioritization skill for Product Managers.

## Goal

Maintain a living product evidence base and turn messy internal information into:

**evidence → signals → problems → hypotheses → opportunities → prioritized solutions → validation / decision**

The engine is intentionally domain-general. Domain-specific taxonomies, risks, metrics, terminology, and specialist intelligence can be supplied through a **Domain Context**.

## Operating modes

- **BUILD CONTEXT** — ingest messy internal artifacts and establish product context.
- **REFRESH** — add new information and update affected evidence, hypotheses, opportunities, and decisions.
- **SPAR** — challenge the PM's thinking rather than simply agreeing with it.
- **DECIDE / PLAN** — prioritize opportunities, solutions, experiments, and planning recommendations such as OKRs.

## Supported inputs

The PM can simply throw in:

- Data-science analyses, dashboards, spreadsheets, CSVs, SQL outputs
- Case reviews and examples
- CSAT, surveys, interviews, support summaries
- PRDs, RFCs, launch retrospectives
- Figma/design links and user journeys
- Vendor pricing and operating constraints
- PM, engineering, legal, policy, and operations notes
- Existing hypotheses and decision logs
- Relevant external links

The PM does not need to pre-structure the information.

## Evidence discipline

A document is evidence of **what someone wrote or believed**, not automatic proof that the underlying statement is true.

The engine independently distinguishes:

- Observed fact
- Derived fact
- Authoritative external fact
- Reported observation
- Company/vendor claim
- Documented assumption
- PM belief/hypothesis
- Model inference
- Unknown/unverified

This prevents PRDs, designs, old analyses, or notes from silently turning hypotheses into facts.

## Product Evidence Base

The engine maintains logical records for:

- Evidence items
- Hypotheses
- Problems
- Opportunities / solutions
- Decisions

It tracks provenance, time period, evidence quality, epistemic status, freshness, contradictions, limitations, and relationships between evidence and hypotheses/decisions.

## Why this is different from simple analysis

The engine does not stop at identifying a failure or funnel drop-off. It explores the full opportunity space:

- Prevention
- Clarification
- Early detection
- Simplification
- Capability improvement
- Recovery/fallback
- Policy or decisioning changes
- Routing
- Cost optimization
- Operations
- Experiments/research
- Reusable platform capabilities

A population can be invalid, ineligible, abusive, or fraudulent and still reveal an intervention opportunity.

## Cost-aware prioritization

The engine treats economics as first-class evidence when supplied:

- Fixed and variable cost
- Cost per attempt
- Cost per successful outcome
- Vendor/operations cost
- Avoided cost
- Contract/volume economics
- Downstream loss or support cost
- Opportunity cost

Cost is evaluated alongside user/business impact, evidence confidence, domain-specific risk, and effort.

## PM sparring

The engine is designed to challenge the PM. It tests:

- Unsupported assumptions
- Claims that are actually hypotheses
- Solution-first thinking
- Missing segmentation
- Base-rate and selection errors
- Correlation vs causation
- Counter-evidence
- Stale evidence
- Economic assumptions
- Domain-specific risk/constraints
- Better alternative explanations

When evidence is insufficient, it asks for specific supplemental data or proposes concrete analyses/experiments and explains how each result would change the recommendation.

## Domain Context

A specialist domain context can provide:

- Product/domain taxonomy
- Lifecycle/journey model
- Domain-specific metrics
- Non-negotiable risks and constraints
- Domain terminology
- Regulatory/industry considerations
- Specialist intelligence skills

For Age Assurance, the intended specialist companion is **Age Assurance Strategic Intelligence**. The same Product Opportunity Engine can be reused with other domain contexts without rewriting its core reasoning.

## Architecture

**Product Opportunity Engine:** internal evidence → problems / hypotheses / opportunities / decisions

**Specialist Intelligence:** external evidence → domain implications

Together:

**internal evidence + external intelligence → stronger product decisions**

See [`SKILL.md`](./SKILL.md) for the full workflow and output specification.
