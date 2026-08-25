# Product Opportunity Engine

A domain-neutral product reasoning workflow for Product Managers.

## Goal

Turn messy information into:

**information → evidence → signals → problems → hypotheses → opportunities → options → prioritization → decision**

The engine is intentionally generic. It does not assume an industry-specific taxonomy, lifecycle, metric, or risk model. Those can be added through a lightweight **Domain Context** when useful.

## How a PM uses it

### 1. SETUP

Provide a minimal profile once:

> Product/area: B2B SaaS onboarding  
> Users: workspace admins  
> Goal: improve activation  
> Key metric: 7-day activation  
> Constraints: optional  
> Specialist context: optional

The PM does not need to create a taxonomy.

### 2. INGEST

Drop in whatever already exists: DS analyses, dashboards, case reviews, customer feedback, CSAT, PRDs, RFCs, launch retros, Figma, vendor information, notes, prior decisions, or links.

The PM does not need to pre-structure it.

### 3. REFRESH

Whenever new information arrives:

> “Add this month's CSAT. Tell me what changed in our evidence, hypotheses, and priorities.”

### 4. SPAR

> “I think our next-quarter priorities should be A, B, and C. Challenge my thinking based on everything we know.”

The engine should challenge unsupported assumptions rather than optimize for agreement.

### 5. DECIDE / PLAN

> “Given the current evidence, what should we prioritize? Show alternatives, risks, economics, unknowns, and what evidence would change the recommendation.”

### 6. CROSS-CHECK

Use a specialist skill when the decision depends on external or domain-specific knowledge. For example, an AA decision can cross-check **Age Assurance Strategic Intelligence**.

## Evidence discipline

A document proves that a claim was written; it does not prove the claim is true. The engine independently distinguishes observed facts, derived facts, authoritative external facts, reported observations, company/vendor claims, documented assumptions, PM hypotheses, model inference, and unknowns.

A formal PRD, previous analysis, or design can therefore be useful context while still being factually unverified.

## Living Product Evidence Base

The engine tracks evidence, hypotheses, problems, opportunities/solutions, and decisions, including provenance, freshness, contradictions, limitations, and relationships between them.

New information can strengthen, weaken, reject, or create hypotheses.

## Cost-aware prioritization

Economics are first-class evidence when supplied: fixed/variable cost, cost per successful outcome, vendor/operations cost, avoided cost, contract/volume economics, downstream loss, and opportunity cost.

Cost is evaluated alongside impact, evidence confidence, domain-specific risk, and effort.

## PM sparring + data discovery

When evidence is missing, the engine should tell the PM exactly:

- what question is unresolved;
- why it matters;
- what data/analysis/research would help;
- what result would strengthen or weaken each hypothesis; and
- how the recommendation would change.

## Specialist / Domain Context

A Domain Context may supply only what the generic engine cannot know, such as:

- domain vocabulary;
- important product entities or journeys;
- key metrics and denominators;
- non-negotiable risks/constraints;
- economic variables;
- regulatory/industry requirements;
- specialist intelligence or research.

The same engine can therefore be reused across SaaS, payments, mobility, creator products, marketplace, social, enterprise, or other areas without rewriting the core reasoning framework.

See [`SKILL.md`](./SKILL.md) for the full operating specification.