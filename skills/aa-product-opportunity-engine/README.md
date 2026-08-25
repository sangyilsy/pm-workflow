# AA Product Opportunity Engine

A persistent product discovery, hypothesis-testing, and prioritization skill for an Age Assurance PM.

## Goal

Maintain a living product evidence base and turn messy internal information into:

**evidence → signals → problems → hypotheses → opportunities → prioritized solutions → validation / decision**

The skill is intentionally broader than failure-rate analysis. It considers prevention, UX, communication, policy, assurance, fraud detection, cost optimization, operations, experiments, and reusable platform capabilities as potential intervention points.

## Operating modes

- **BUILD CONTEXT** — ingest a messy set of internal artifacts and establish product context.
- **REFRESH** — add new information to the existing evidence base and update affected hypotheses/decisions.
- **SPAR** — challenge the PM's thinking rather than simply agreeing with it.
- **DECIDE / PLAN** — prioritize opportunities, solutions, experiments, and planning recommendations such as OKRs.

## Supported inputs

The PM can simply throw in:

- Data-science analyses, dashboards, spreadsheets, CSVs, SQL outputs
- Case reviews and examples
- CSAT, surveys, support summaries
- PRDs, RFCs, launch retrospectives
- Figma/design links and user journeys
- Vendor pricing and operating constraints
- PM, engineering, legal, policy, and operations notes
- Existing hypotheses and decisions
- Relevant external links

The PM does not need to pre-structure the information.

## Evidence model

The skill maintains logical records for:

- Evidence items
- Hypotheses
- Problems
- Opportunities / solutions
- Decisions

It tracks source, time period, evidence quality, freshness, related hypotheses, contradictions, and limitations. New data can strengthen, weaken, reject, or create hypotheses.

## Why this is different from simple analysis

A failure does **not** automatically equal a product defect, but every failure category can still reveal product opportunities.

The skill looks for opportunities in:

- Legitimate users with avoidable failures
- Legitimate users who are policy-ineligible or misunderstand the threshold
- Fraud/spoof submissions that create avoidable cost or operational load
- Ambiguous evidence that requires better instrumentation or research
- System/vendor/operational failures

It also searches across prevention, clarification, early detection, simplification, assurance, fallback/recovery, policy, routing, cost optimization, operations, and platform architecture.

## Cost-aware prioritization

The PM can provide fixed and variable cost structures for AA methods. The skill considers:

- Cost per attempt
- Cost per successful legitimate outcome
- Manual-review cost
- Avoided vendor calls
- Contract/volume economics
- Fallback/waterfall costs
- Fraud/abuse cost implications

Cost is considered alongside user impact, evidence confidence, safety/privacy/regulatory risk, and effort rather than as a standalone optimization target.

## PM sparring

The skill is explicitly designed to challenge the PM. It should test:

- Unsupported assumptions
- Solution-first thinking
- Missing segmentation
- Base-rate errors
- Correlation vs causation
- Counter-evidence
- Safety/fraud implications
- Privacy/accessibility implications
- Economic assumptions
- Regulatory/competitor assumptions
- Better alternative explanations

When evidence is insufficient, it should ask for specific supplemental data or propose concrete analyses/experiments and explain how each result would change the recommendation.

## Strategic Intelligence integration

When a product question involves regulation, competitor precedent, AA technology, accepted evidence, youth-safety policy, or market trends, the skill can cross-check against the **Age Assurance Strategic Intelligence** skill.

This makes the two skills complementary:

**Strategic Intelligence:** external world → strategy / product implications

**Product Opportunity Engine:** internal evidence → problems / opportunities / decisions

Together:

**internal evidence + external intelligence → stronger product decisions**

See [`SKILL.md`](./SKILL.md) for the full workflow and output specification.
