# ITHERLA Product Concept and Development Progress

Updated: 2026-11-17  
Current phase: cognitive-core integration  
Private source checkpoint: `2098fae`

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

## Development Progress

| Stage | Status | Public summary |
| --- | --- | --- |
| Cognitive-core baseline | Isolated validation complete | Domain-neutral context, fact, memory, affect, reasoning, and governance contracts exist; this does not mean the product Runtime is complete |
| Core integration path | In progress | Building one verifiable read/write path so components cannot bypass governance independently |
| Memory and skill lifecycle | Planned / not implemented | Consolidation, recall, skill extraction, fair capacity, backup, and portability |
| Rights and provenance governance | Planned / not implemented | Separate treatment for reading, abstraction, private experiments, adaptation, commercial use, and redistribution |
| Real models and managed runtime | Blocked by prerequisites | Local, cloud, hybrid, and managed-runtime compatibility and degradation will be qualified |
| Player desktop product | Not implemented | Conversation, voice, Agent management, game state, authorization, stop, diagnosis, and resource-governance UI remain incomplete |
| Game adapters and control | Not enabled | Deterministic harnesses and simulated games come before legally supported real-game scenarios |
| Public testing and commercial release | Not started | Installation, update, rollback, licensing, privacy, compatibility, security, and long-duration validation remain required |

## Recently Added Public Directions

1. System-wide and per-Agent memory-capacity governance designed to prevent stronger, louder, or
   more capable Agents from unfairly displacing others.
2. A Rights & Provenance Gate that separates source tracking, intended use, and commercial-output
   eligibility.
3. User-delegated Agent assistance without self-expanding authority, redelegation, or sacrificing
   another Agent's protected space.

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

## Maturity Notice

ITHERLA remains an active research and product-engineering project. It is not a finished download,
and real game control is not enabled. This document describes product direction, isolated baseline
work, and planned validation. It is not a guarantee of safety, legal compliance, commercial
readiness, or release timing.

