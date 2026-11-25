# ITHERLA Product Concept and Development Progress

Updated: 2026-11-25
Current phase: cognitive-core integration
Latest private source commit: `b0fd9d68e553adc3e548d1ffba17aeba35d5af68`

[Traditional Chinese version](PRODUCT_PROGRESS.zh-TW.md)

## What ITHERLA Is

ITHERLA is a player-centered, local-first game AI Agent system with replaceable model engines.

Its goal is not to build another game chatbot. It is intended to let the same Agent preserve
identity, governed memory, skills, and collaboration context across local, cloud, and hybrid
models, then safely observe, communicate, and participate in supported games under explicit
user authorization.

Models are replaceable reasoning engines. They do not own the Agent's memory, identity, or tool
authority. The user retains the ability to start, pause, correct, revoke, and stop Agent activity.

## Problems We Intend to Solve

### 1. Changing Models Should Not Mean Starting the Relationship Over

Cloud and local models have different strengths, but switching models often discards context,
preferences, and long-term collaboration experience. ITHERLA keeps Agent identity and governed
memory outside the model so the engine can change without resetting the Agent.

### 2. Remembering More Must Not Grant More Authority

Memory, emotion, familiarity, model confidence, and repeated interaction cannot create tool or
action authority. Observation, interpretation, memory, authorization, and execution are handled
as separate concerns. Knowing more about a user must not become permission to decide for them.

### 3. Multiple Agents Need Cooperation and Fair Resource Governance

Users may eventually work with several Agents. Private memory, competence, and experience remain
separate, while only suitable procedures enter shared skill spaces. A more assertive Agent, a
stronger model, or a closer relationship must not let one Agent silently displace another Agent's
protected memory. Final resource governance remains with the user.

### 4. Long-Term Memory Needs a Lifecycle, Not Endless Accumulation

Short-term context, durable memory, skills, evidence, and large media are planned as separate
data planes. Duplicate material can be consolidated and experience can become reusable concepts,
without erasing provenance, counterexamples, revision history, or rollback paths.

### 5. Learning from External Material Must Not Become Commercial Copying

An Agent may read, discuss, compare, and extract general concepts, but lawful access does not
automatically grant adaptation, redistribution, or commercial-use rights. ITHERLA plans to retain
source and rights state while distinguishing discussion, quotation, concept abstraction, private
experimentation, derivative creation, and commercial release. Unknown rights do not silently
become commercially usable.

### 6. Safety Cannot Depend Only on Model Self-Restraint

Model output is a candidate, not authority. Real capabilities must still pass identity, current
intent, user authorization, capability scope, managed execution, and pre-action validation.
Component failures should degrade locally. When a critical boundary cannot be proven, the related
capability should stop instead of silently bypassing governance.

## Public Design Principles

- **Local-first**: private memory and core data remain under user-controlled storage by default.
- **Replaceable models**: local, cloud, and hybrid inference should not bind an Agent to one provider.
- **Human-led operation**: consequential, irreversible, or cross-boundary actions require explicit,
  revocable user authorization.
- **Memory does not grant authority**: continuity, intimacy, capability, and confidence cannot
  bootstrap control.
- **Misalignment remains repairable**: mistaken interpretation retains correction and re-anchoring
  paths instead of hiding inconsistency by deleting history.
- **Portable without crossing boundaries**: users can carry legally portable memory and skills;
  organizational secrets, third-party restrictions, and private data retain their own boundaries.
- **Stoppable, recoverable, and reviewable**: the system must support safe pause, rollback,
  diagnosis, and clear disclosure of current limits.
- **Validation before claims**: support is claimed only after the relevant capability is tested.

## How We Approach AI Safety

Perception data, tool results, memories, and model outputs carry no authority by default.
Evidence can support or revise a judgment within its applicable scope, but it remains open
to correction. It is neither final truth nor authorization.

ITHERLA does not allow a single model to simultaneously control reasoning, Agent identity,
memory, authorization, execution, and the final review of its own behavior.

Explainability, event records, authorization validation, and review capability therefore do not
depend on one reasoning model. A model may be replaced, fail, or degrade while governance and
review boundaries remain effective.

This design is not based on assumptions about the motives of any particular model or provider.
It is intended to prevent any single component from forming a closed loop of authority that
cannot be independently verified by another component. ITHERLA also does not assume that any
model will always be correct or rely on model self-restraint as the primary safety boundary.

Observation, interpretation, memory, skills, authorization, and execution are handled as separate
layers. Model output begins as a candidate. Memory, familiarity, confidence, historical success,
and procedural knowledge cannot create tool or action authority. Before an external effect is
allowed, the system must re-evaluate Agent identity, current user intent, valid authorization,
capability scope, and execution boundaries.

The safety approach follows several principles:

- **Models do not own authority**: a model may reason and propose, but it cannot create or expand
  authorization.
- **Memory is separate from capability**: knowing how to perform an action does not mean the
  action is currently permitted.
- **Consequential actions require renewed validation**: irreversible, sensitive, or
  cross-boundary actions require matching user authorization.
- **Failures should degrade locally**: when one component becomes unreliable, the affected
  capability should stop without silently weakening the rest of the system.
- **The system must remain stoppable and recoverable**: diagnosis, pause, revocation, rollback,
  and human takeover are part of the design.
- **Safety is not treated as zero risk**: it is an ongoing engineering process involving
  validation, adversarial testing, review, and correction.

The goal is not to create an Agent that can never be wrong. The goal is to prevent an error from
automatically becoming authority, and to make drift visible, bounded, repairable, and safely
stoppable.

## How We Approach Employment Anxiety in the AI Era

Rapid improvements in AI have also created understandable concern that human experience,
employment, and learning speed may be left behind. ITHERLA does not promise to eliminate
unemployment, and it does not present AI as a complete answer to social or economic problems.

Our direction is to make AI understandable, governable, replaceable, and capable of long-term
collaboration without requiring users to surrender judgment.

Within the ITHERLA concept:

- Humans retain responsibility for goals, values, authorization, and consequential decisions.
- Agents help organize information, preserve experience, learn procedures, and reduce repetitive
  work.
- Model engines can be replaced without forcing legally portable memory and skills to disappear
  with one provider.
- Collaboration supports correction in both directions instead of training users to accept every
  AI conclusion.
- Games provide the first product setting because interest, cooperation, and low-pressure
  experimentation can be a healthier introduction to AI than requiring everyone to become a
  prompt engineer.

We believe the more sustainable response to AI-driven change is not to frame humans and AI only
as replacements for one another. It is to help more people combine their judgment and experience
with governed Agents as small, capable human-AI teams.

This cannot guarantee that anyone's work will remain unchanged. It aims to preserve something
more fundamental: after adopting AI, a person should still be able to think, choose, refuse, and
carry learned capabilities into the next stage of life and work.

## Development Progress

| Stage | Status | Public summary |
| --- | --- | --- |
| Cognitive-core baseline | Isolated validation complete | Domain-neutral context, fact, memory, affect, reasoning, and governance contracts exist; this does not mean the product Runtime is complete |
| Core integration path | In progress | Building one verifiable read/write path so components cannot bypass governance independently |
| Multimodal perception and context separation | Isolated data foundation complete | Authority-free source, event, context-revision, and action-feedback foundations exist; real perception and product wiring are not enabled |
| Memory and skill lifecycle | Planned / not implemented | Consolidation, recall, skill extraction, fair capacity, backup, and portability |
| Rights and provenance governance | Planned / not implemented | Separate treatment for reading, abstraction, private experiments, adaptation, commercial use, and redistribution |
| Real models and managed runtime | Blocked by prerequisites | Local, cloud, hybrid, and managed-runtime compatibility and degradation will be qualified |
| Player desktop product | Not implemented | Conversation, voice, Agent management, game state, authorization, stop, diagnosis, and resource-governance UI remain incomplete |
| Game adapters and control | Not enabled | Deterministic harnesses and simulated games come before legally supported real-game scenarios |
| Public testing and commercial release | Not started | Installation, update, rollback, licensing, privacy, compatibility, security, and long-duration validation remain required |

## Public Technical Concepts

See [Public Technical Concepts](TECHNICAL_CONCEPTS.en.md) for multimodal perception,
local-first inference, memory and skill boundaries, and age-context updates within the same chat.
This page tracks product direction, maturity, and dated progress.

## Next Steps

- Complete the formal memory-write and capability-entry integration path.
- Implement machine-readable lifecycle contracts for memory, skills, source rights, and capacity.
- Establish shared conformance tests before connecting real model engines.
- Complete stoppable, recoverable, and diagnosable foundations before product UI, game control,
  or public testing begins.

## Public Update History

Beginning on `2026-11-17`, material changes to product direction, maturity, or validation status
will be recorded here with explicit dates. Earlier development history will not be reconstructed
from guesswork; verifiable earlier milestones remain represented by Git and evidence records.

- **2026-11-17**: Published the bilingual product concept and progress pages; recorded the current
  cognitive-core integration phase and the public directions for fair memory capacity, Rights &
  Provenance, replaceable models, and later product qualification.
- **2026-11-17 22:43:53 UTC+08:00**: Added the public AI-safety approach and position on
  employment anxiety, including layered authority, stoppability and rollback, explicit rejection
  of zero-risk claims, and the direction of human judgment working with governed Agents as small
  collaborative teams.
- **2026-11-18 17:42:11 UTC+08:00**: Added an isolated multimodal-perception and context-separation
  data foundation. Sources, events, context revisions, and action feedback remain authority-free,
  while perception, safety, affect, facts, memory, skills, source archives, and media retain
  separate write domains. This checkpoint passed `544` isolated tests; it does not claim real
  perception models, cross-store recall, game control, or a completed product Runtime.
- **2026-11-18**: Clarified the public boundary that no single model may simultaneously control
  reasoning, Agent identity, memory, authorization, execution, and self-review; governance and
  review capability do not depend on any one reasoning model.
- **2026-11-24**: Added design notes on zero authority by default, multimodal scene
  interpretation, and local-first inference. Capability eligibility is now connected to an
  isolated data store; incomplete records and records that change during a read block
  eligibility. This private source commit corresponds to **564 passing tests and 70 passing
  subtests**. Tool execution, real models, live perception, and game control were not enabled.
- **2026-11-25**: Core integration added isolated validation for governed memory disposition records
  and read-only context packets. The latest confirmed isolated regression passed **571 tests and 75 subtests**.
  Technical concepts moved to a separate page covering perception model comparisons, cloud request and
  use boundaries, and in-chat age-context updates. These product directions still await implementation or validation.
- **2026-11-25**: Added a [public architecture overview and permission boundaries](TECHNICAL_CONCEPTS.en.md#conceptual-architecture),
  with written game and work-chat examples distinguishing context interpretation from action eligibility. Documentation update only.
- **2026-11-25**: Expanded [memory, skills, and authority](TECHNICAL_CONCEPTS.en.md#memory-skills-and-authority), explaining how experience guides new observations, how procedures can be shared, and how risk shapes checking and action. Documentation update only.

## Maturity Notice

ITHERLA remains an active research and product-engineering project. It is not a finished download,
and real game control is not enabled. This document describes product direction, isolated baseline
work, and planned validation. It is not a guarantee of safety, legal compliance, commercial
readiness, or release timing.

