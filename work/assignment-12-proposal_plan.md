# Assignment 12: Proposal Plan

## Working Title
**USDA SBIR Phase I Proposal Plan for Fruitful Network Development**  
**Topic 8.6 — Rural and Community Development**

---

## Purpose of This Plan

This document is a planning guide for drafting the USDA SBIR Phase I proposal. Its purpose is not to function as the proposal itself, but to organize the reasoning, source hierarchy, section logic, and drafting priorities needed to create a proposal that is coherent, logically sound, and aligned with the actual position developed across the repo.

The central drafting rule is:

**Do not draft from the most polished prose first.  
Draft from the strongest reasoning chain first.**

That means the proposal should be built from the source stack in the correct order:
1. structure source
2. reasoning source
3. current narrative extraction source
4. business/system source
5. mechanism source
6. comparative/example source
7. evidence support source

---

## Core Proposal Logic

The proposal should preserve the following argumentative sequence:

1. **Rural problem:** increasingly, it is inequitable to work with and in local agriculture.
2. **Operational axis:** farm income volatility.
3. **Primary driver:** coordination failure, not simple absence of demand.
4. **Mechanism:** fragmented supply visibility, unstable sourcing, perishability, buyer-side overhead, and disconnected operational data.
5. **Observed partial solutions:** food hubs, co-ops, aggregation models, processing, retail shelf-access, shared infrastructure, auctions, and hybrid delivery networks.
6. **Proposed response:** a local-first, network-later coordination platform that begins with internal farm operations and extends into external coordination.
7. **Phase I question:** does a bounded two-sided feasibility window exist in which both farms and buyers are non-worse-off under coordinated local sourcing conditions?
8. **Phase II implication:** if yes, operationalize live workflows, commitments, and broader deployment.

This logic must remain visible across the proposal and should not be replaced by broader philosophical claims about information systems.

---

## Source Hierarchy

### Tier 1 — Structural guide
#### `past-writtings/sbir_fnd_proposal_considerations.md`
Use this as the proposal’s **section architecture source**.

Use it for:
- USDA SBIR section order
- section purpose
- formal topic fit
- standard expectations for objectives, work plan, market, team, and budget

Do not use it as the main reasoning source.  
It is the **proposal skeleton**, not the argument’s origin.

---

### Tier 2 — Reasoning spine
#### `past-writtings/sbir_discussion_evolution.md`
Use this as the **primary reasoning source**.

This is the most important internal source because it contains:
- the narrowing from broad vision to bounded Phase I feasibility
- the selection of **income volatility** as the operational axis
- the identification of **coordination failure** as the risk-driven constraint
- the distinction between:
  - business-development activity vs technical feasibility
  - full agronomic optimization vs capacity-banded coordination feasibility
  - abstract theory vs Phase I evaluable claims
- the evolution of the reinforcing loop and feasibility-window framing

This file should guide:
- the proposal’s core claim
- the Phase I technical question
- the feasibility framing
- what to exclude from the main narrative

---

### Tier 3 — Current extracted proposal material
#### `work/assignment-13-proposal.md`
Use this as the **section answer bank**.

This file is useful because it already maps:
- proposal questions
- current excerpts that attempt to answer them
- section-by-section content placement

Use it when drafting after the reasoning has been validated against the discussion record.

#### `past-writtings/SBIR/proposal-content.md`
Use this as the **closest current full narrative scaffold**.

Use it for:
- narrative tone
- section names
- transition ideas
- existing proposal-like prose

Do not let it override the more disciplined logic found in `sbir_discussion_evolution.md`.

---

### Tier 4 — Stable company and system positioning
#### `past-writtings/SBIR/FND_notes.txt`
Use this as the **business and platform positioning source**.

Use it for:
- what FND does
- how to describe the company modestly
- what producers use the platform for
- the internal/external operations distinction
- what not to claim
- the company/team/resource framing
- budget-justification direction

This source is especially important for:
- company overview
- innovation section wording
- resources/team section
- safe language for capabilities and prior work

---

### Tier 5 — Mechanism and feasibility framing
#### `past-writtings/articles/agronomic_micro_structure.md`
Use this as the **mechanism source**.

Use it for:
- coordination failure framing
- reinforcing loops
- feasibility window logic
- adjacency and product-variety constraints
- the transition from current state to bounded coordinated scenarios

This source should shape:
- problem significance
- technical objectives
- work plan rationale
- Phase I / Phase II relationship

---

### Tier 6 — Real-world comparison layer
#### `past-writtings/articles/modern_models_in_local_agriculture.md`
Use this as the **comparative examples source**.

Use it for:
- examples of coordination mechanisms already in the field
- food hubs
- cooperative models
- shelf-access models
- shared-use processing
- hybrid CSA/grocery models
- logistics and auction references

This source should support:
- background and rationale
- related research / competition
- commercialization framing
- proof that coordination burden is a real operational problem

---

### Tier 7 — Economic and external support source
#### `past-writtings/articles/market-research-report.md`
Use this as the **tertiary evidence support source**.

Use it for reviewer-safe external support such as:
- concentration of produce sales
- produce loss and shrink
- transport-cost framing
- careful claims about local versus industrial systems
- limits of national data
- parameterized examples
- avoid-overclaim guidance

This source should support claims made elsewhere.  
It should **not** be the source that determines the proposal’s logic.

---

### Tier 8 — Controlled support on diversity/regeneration
#### `past-writtings/articles/regenerative_farming.md`
Use this as the **discipline source** for claims about diversity, health, ecological value, and regenerative incentives.

Use it for:
- careful definitions
- systems-oriented treatment of regenerative practice
- avoiding overclaiming
- explaining why incentive structure matters

This source should support:
- problem significance
- broader impacts
- background and rationale

Use cautiously.  
Do not make the proposal dependent on proving regenerative superiority everywhere.

---

## Central Drafting Guardrails

### 1. Keep the proposal agricultural and evaluable
The proposal should read as an **agricultural coordination feasibility proposal**, not as a universal information-theory manifesto.

### 2. Keep Phase I bounded
Phase I is not:
- full agronomic optimization
- a complete live brokerage deployment
- a proof of universal semantic architecture
- a nationwide market rollout

Phase I is:
- a bounded feasibility study
- grounded in a regional context
- using farm interview data, current-output bands, and capacity bands
- testing whether a nontrivial two-sided feasibility window exists

### 3. Keep the technical novelty narrow enough to evaluate
The innovation should be described as:
- local-first, network-later operational tooling
- schema-based interoperability across decentralized participants
- reduced coordination burden without requiring centralized lock-in

Avoid letting the innovation section become dominated by:
- abstract semantic claims
- universal language assertions
- general anti-centralization philosophy
- unbounded blockchain comparisons

### 4. Keep the proposal tied to one governing Phase I claim
The proposal should revolve around one testable feasibility claim:
- whether bounded coordination and transparency can reduce farm-side instability while keeping buyer-side procurement within acceptable cost and service thresholds

### 5. Keep the logic two-sided
The proposal is strongest when it shows:
- farms must be non-worse-off
- buyers/grocers/food hubs must be non-worse-off
- feasibility exists only where these conditions overlap

---

## Section-by-Section Proposal Matrix

## 1. Project Summary / Abstract

### Purpose
Provide a public-facing summary of:
- the problem
- the innovation
- the Phase I objective
- the approach
- the expected outcome

### Primary sources
- `past-writtings/sbir_discussion_evolution.md`
- `past-writtings/sbir_fnd_proposal_considerations.md`

### Secondary sources
- `work/assignment-13-proposal.md`
- `past-writtings/SBIR/proposal-content.md`
- `past-writtings/articles/market-research-report.md`

### Main claim to establish
There is a meaningful rural coordination problem affecting local agriculture, and Phase I will test whether a bounded coordination-first platform is technically feasible under defined regional conditions.

### What to emphasize
- local agriculture is underused because coordination is hard
- Phase I is a feasibility study
- the approach is bounded and testable
- the innovation is local-first and interoperability-oriented

### What to avoid
- oversized philosophical claims
- unclear metaphors
- too many benefits in one sentence
- vague words like “revolutionize,” “decontamination,” or undefined “transparency”

---

## 2. Responsiveness to USDA NIFA SBIR Program Priorities

### Purpose
Show clear fit with Topic 8.6 and rural/community development goals.

### Primary sources
- `past-writtings/sbir_fnd_proposal_considerations.md`
- `past-writtings/SBIR/proposal-content.md`

### Secondary sources
- `past-writtings/SBIR/FND_notes.txt`
- `past-writtings/articles/agronomic_micro_structure.md`

### Main claim to establish
The project addresses a rural coordination and market-access problem that affects small and mid-size agricultural operations and rural economic resilience.

### What to emphasize
- rural/community development
- improved local coordination
- reduced waste and fragmentation
- preservation of farm autonomy
- support for local food networks and rural viability

### What to avoid
- making the proposal sound like a general software pitch
- treating climate or health benefits as the primary project objective instead of secondary benefits

---

## 3. Identification and Significance of the Problem or Opportunity

### Purpose
Define the problem precisely and make it matter.

### Primary sources
- `past-writtings/sbir_discussion_evolution.md`
- `past-writtings/articles/agronomic_micro_structure.md`

### Secondary sources
- `past-writtings/articles/market-research-report.md`
- `past-writtings/articles/regenerative_farming.md`
- `past-writtings/SBIR/FND_notes.txt`

### Main claim to establish
The core problem is that local agriculture is increasingly inequitable to work with and in because coordination failures create farm-side instability and buyer-side friction.

### What to emphasize
- income volatility as the operating axis
- demand is not absent; coordination is weak
- fragmented supply visibility and sourcing instability
- perishability and timing pressure
- buyer procurement complexity
- local value not becoming market advantage

### What to avoid
- unsupported claims that small farms dominate produce markets
- unsupported productivity claims
- making “inequitable” a rhetorical term without explaining for whom and how

---

## 4. Background and Rationale

### Purpose
Show command of existing models, end-user needs, and why current approaches are inadequate.

### Primary sources
- `past-writtings/articles/modern_models_in_local_agriculture.md`
- `past-writtings/SBIR/FND_notes.txt`

### Secondary sources
- `past-writtings/SBIR/proposal-content.md`
- `work/assignment-13-proposal.md`
- `past-writtings/articles/regenerative_farming.md`

### Main claim to establish
Current models solve fragments of the coordination problem, but local producers still face fragmented tools, centralized dependencies, and interoperability limitations.

### What to emphasize
- food hubs, aggregation, processing, shelf access, shared infrastructure, and delivery networks as partial coordination solutions
- end-user reality: multiple disconnected tools and workflows
- why a new approach is needed: interoperable coordination without forced central lock-in

### What to avoid
- dismissing existing models as failures
- overstating “no one else does anything similar”
- drifting into overly abstract architecture exposition

---

## 5. Relationship to Research and Phase II

### Purpose
Show how Phase I leads to a larger effort without overpromising.

### Primary sources
- `past-writtings/articles/agronomic_micro_structure.md`
- `past-writtings/sbir_discussion_evolution.md`

### Secondary sources
- `past-writtings/SBIR/proposal-content.md`
- `work/assignment-13-proposal.md`

### Main claim to establish
Phase I determines whether a two-sided feasibility window exists; Phase II would operationalize the commitments, workflows, and scaled deployment implied by that window.

### What to emphasize
- Phase I = bounded feasibility
- Phase II = implementation and scaling
- transition pathway rather than instant transformation
- link from simulation and pilot structure to later deployment

### What to avoid
- making Phase II sound guaranteed
- making Phase I sound like a full market launch
- collapsing feasibility study and operational deployment into one phase

---

## 6. Technical Objectives

### Purpose
State clear, testable objectives tied to technical uncertainty.

### Primary sources
- `past-writtings/sbir_discussion_evolution.md`
- `past-writtings/articles/agronomic_micro_structure.md`

### Secondary sources
- `past-writtings/SBIR/proposal-content.md`
- `work/assignment-13-proposal.md`
- `past-writtings/SBIR/FND_notes.txt`

### Main claim to establish
The project has a finite set of technical objectives that directly answer the Phase I feasibility question.

### Likely objective pattern
1. Define the data structure and minimum interoperable schema needed for participating farms and buyers.
2. Build a prototype that supports internal operations and external coordination-relevant outputs.
3. Collect bounded farm and buyer data needed to parameterize the regional feasibility study.
4. Evaluate whether a feasible overlap exists between farm-side and buyer-side conditions.

### What to emphasize
- technical uncertainty
- measurable outputs
- bounded scope
- feasibility, not platform maximalism

### What to avoid
- objective lists that are just broad company ambitions
- conflating business growth tasks with technical objectives
- hidden agronomic-optimization promises

---

## 7. Work Plan

### Purpose
Show exactly how Phase I will be executed.

### Primary sources
- `past-writtings/sbir_discussion_evolution.md`
- `past-writtings/articles/agronomic_micro_structure.md`

### Secondary sources
- `past-writtings/SBIR/proposal-content.md`
- `past-writtings/SBIR/FND_notes.txt`
- `work/assignment-13-proposal.md`

### Main claim to establish
The proposed tasks, timeline, and methods are sufficient to answer the Phase I feasibility question within the time and budget limits.

### What to emphasize
- interviews and data collection as inputs to a technical study
- current output + capacity bands, not full yield prediction
- bounded regional demand profile
- scenario-based feasibility testing
- pass/fail logic
- measured outputs tied to objectives

### What to avoid
- vague “build software, test it, analyze it”
- overextending into full brokerage operations
- implying full agronomic modeling or complete market deployment

---

## 8. Related Research and Competition

### Purpose
Show awareness of external solutions and explain differentiation.

### Primary sources
- `past-writtings/articles/modern_models_in_local_agriculture.md`
- `past-writtings/SBIR/proposal-content.md`

### Secondary sources
- `past-writtings/SBIR/FND_notes.txt`
- `work/assignment-13-proposal.md`

### Main claim to establish
Existing solutions address portions of the problem, but FND’s approach differs in combining local-first operational value with decentralized interoperable coordination.

### What to emphasize
- competition by category and operating model
- how current models depend on centralized ownership, proprietary structure, or single-channel success
- how FND differs: schema-first, open, local-first, not all-or-nothing

### What to avoid
- saying there are no competitors
- using blockchain comparisons as the main differentiator
- exaggerated claims about universal uniqueness

---

## 9. Market Opportunity and Commercialization Plan

### Purpose
Show who benefits, who may pay, and how the project can move toward use.

### Primary sources
- `past-writtings/articles/modern_models_in_local_agriculture.md`
- `past-writtings/articles/market-research-report.md`

### Secondary sources
- `past-writtings/SBIR/proposal-content.md`
- `past-writtings/SBIR/FND_notes.txt`

### Main claim to establish
There is a real market opportunity in reducing coordination friction across local food networks, and FND has a plausible path to serve that market without requiring central ownership of the whole system.

### What to emphasize
- target network: small and mid-size farms, food hubs, grocers, cooperatives, regional buyers
- use cases: visibility, planning, coordination, reduced fragmentation
- business model tension: open-source core plus viable service/business layer
- why coordination itself creates value

### What to avoid
- vague total-addressable-market claims without context
- making commercialization depend only on ideology
- unresolved contradiction between software wedge and brokerage/business model

---

## 10. Resources, Facilities, and Team

### Purpose
Demonstrate execution capability.

### Primary sources
- `past-writtings/SBIR/FND_notes.txt`
- `past-writtings/SBIR/proposal-content.md`

### Secondary sources
- `past-writtings/sbir_fnd_proposal_considerations.md`

### Main claim to establish
FND has the technical capability, organizational readiness, and access to the resources needed to execute Phase I.

### What to emphasize
- modest but credible capability
- relevant prior work with farms and digital infrastructure
- PI role clarity
- consultants/advisors only where justified
- access to cloud, development environment, and pilot participants
- ability to manage federal funds responsibly

### What to avoid
- overstating company scale
- mixing future ambitions with present capability
- underexplained consultant roles

---

## 11. Budget and Budget Justification

### Purpose
Tie requested funds directly to feasibility work.

### Primary sources
- `past-writtings/SBIR/FND_notes.txt`
- `past-writtings/SBIR/proposal-content.md`

### Secondary sources
- `past-writtings/sbir_fnd_proposal_considerations.md`

### Main claim to establish
Every requested cost supports a specific technical objective or Phase I task.

### What to emphasize
- personnel effort tied to task structure
- cloud/dev costs tied to prototype and analysis
- consultants tied to discrete gaps
- modest equipment only if essential
- disciplined scope

### What to avoid
- generic software/startup operating expenses with no objective tie
- budget items that imply Phase II scale
- “nice to have” costs

---

## 12. Biographical Sketches and References

### Purpose
Support credibility and compliance.

### Primary sources
- `past-writtings/SBIR/proposal-content.md`
- `past-writtings/SBIR/FND_notes.txt`

### Secondary sources
- all externally cited support sources

### Main claim to establish
The proposal is professionally documented, ethically sourced, and supported by relevant qualifications.

### What to emphasize
- relevance of experience
- technical and entrepreneurial fit
- proper references

### What to avoid
- overlong biographies
- references that do not support the claim they are attached to
- undocumented strong claims

---

## Drafting Order

The proposal should be drafted in this order:

1. **Phase I feasibility claim and pass/fail logic**
2. **Technical objectives**
3. **Work plan**
4. **Problem/significance**
5. **Background/rationale**
6. **Phase I / Phase II relationship**
7. **Innovation**
8. **Market/commercialization**
9. **Resources/team**
10. **Abstract**
11. **Budget alignment check**

This order forces the proposal to be built from evaluable logic rather than top-down persuasion.

---

## Proposal-Wide Questions That Must Stay Stable

Before the final proposal is drafted, the following questions must remain consistently answered across all sections:

1. What exact problem is being solved?
2. For whom is it a problem?
3. What is the chosen operating axis?
4. What is the technical uncertainty being tested in Phase I?
5. What is the minimum bounded demonstration?
6. What counts as success?
7. What counts as failure?
8. What is deferred to Phase II?
9. Why is the proposed response meaningfully different from current approaches?
10. Why is this a USDA-worthy rural/community development problem?

---

## Most Important Exclusions

The following material should remain secondary, bounded, or appendix-like unless directly translated into Phase I testable claims:

- broad information-ownership philosophy
- universal-language-of-information claims at full scale
- deep MSS bitstream mechanics
- generalized anti-centralization argument
- overly broad blockchain comparison
- claims of singular universal uniqueness
- full agronomic optimization implications

These ideas may still matter internally, but they should not dominate the sponsor-facing narrative.

---

## Deliverable Use

This proposal plan should support two later deliverables:

1. **The proposal writing itself**
   - by giving each section a source hierarchy and logic target

2. **Future revisions**
   - by making it easier to check whether any section drifted away from the actual reasoning developed in the repo

The proposal should be strongest when it reads as:
- disciplined
- bounded
- realistic
- evidence-supported
- technically specific
- and clearly rooted in the problem of coordination failure in local agriculture
