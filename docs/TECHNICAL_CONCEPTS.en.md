# ITHERLA Public Technical Concepts

Updated: 2026-11-25 · [繁體中文](TECHNICAL_CONCEPTS.zh-TW.md) · [Product and progress](PRODUCT_PROGRESS.en.md)

This page describes design directions without publishing source code, internal contracts, algorithms, or restricted data. See the progress page for current maturity.

ITHERLA aims to be an Agent that can play alongside you within the boundaries you set. Changing the model should not mean changing your teammate. Remembering how you played together does not grant permission to keep playing on your behalf.

## Conceptual architecture

```text
Game Screen / Audio / Action Feedback
                  |
                  v
          Perception System
      Separate Sources and Align Cues
                  |
                  v
        Context Resolver (CXR)
          Interpret the Situation
                  |
                  +<--- Governed Memory
                  |
                  v
          Model: Propose an Action
                  |
                  v
          Permission Check <--- Player: Authorize / Revoke
                  |
                  +-- Eligible ------> Game Action Path
                  +-- Not Eligible --> Do Not Execute

Player: Stop / Take Over ------------> Game Action Path
```

This diagram shows responsibilities, not implementation wiring. Perception organizes current signals and CXR interprets the situation. Memory informs judgment; it is neither fresh observation nor permission. Players do not need the model's approval to stop or take over.

## Permissions: the model can propose, but it cannot authorize itself

A system outside the model determines action eligibility based on the player's active authorization, the current task, and the permitted scope. Model confidence, past experience, and switching engines cannot broaden permission. After a stop or revocation, queued or late model proposals cannot justify continuing an action.

**Validated in isolation:** Core eligibility checks are connected to an isolated data store. If a required record is missing or changes during a read, the eligibility check does not pass. **Still to validate:** Live game input, player takeover, and stopping actions after revocation in an end-to-end workflow.

## Same Send button, different context

- **In a game:** You ask the Agent to send a rally point to your teammates. If you have authorized team messaging for that match, it can help within that scope without asking before every message.
- **Outside the game:** The game is still open, but you switch to a work chat. The same Send button does not carry over your game authorization. The Agent can help draft a message, but cannot send it under that permission.

CXR helps distinguish the situation. A separate permission check determines whether an action is eligible. These examples describe intended behavior, not live product features.

## Perception and scene understanding

Visuals, sound, action feedback, and other inputs are separated by source and context before being interpreted together. A background video may play alongside a game without its audio belonging to the same event. An Agent sending a control input does not prove that the game performed the expected action.

We plan to compare an algorithm-only baseline with the same approach assisted by a replaceable lightweight multimodal model, such as EmbeddingGemma 2, to see whether it helps organize current sensory signals. Adoption depends on a meaningful improvement in association quality or efficiency and acceptable impact on gameplay. This is a perception candidate, not a second memory retrieval system or a selected product model.

## Local-first inference and cloud support

Agent identity and governed memory do not belong to any one model. Routine inference defaults to local execution. Task needs and device load determine when to use authorized hybrid inference; cloud-only inference is reserved for cases where it is necessary and approved. Cloud usage and data disclosure are separate decisions: approved routine calls need no repeated prompts, and sensitive data is minimized locally before any necessary disclosure is confirmed separately.

Late results should not continue to affect a stopped task or one whose authorization was revoked. Stopping locally does not imply that data already received by a provider can be recalled. Cloud models can answer questions, help with research, or supplement local capabilities, but are not used to generate training data for model distillation.

## Memory, skills, and authority

Raw records, perception, facts, affect, Agent memory, skills, and media serve different purposes and have separate lifecycles. A user being able to review a transcript does not mean the Agent can automatically recall it. Knowing how to do something does not confer permission to do it. Sharing and migration retain source and use restrictions, and export does not make protected material portable. Capacity management should also prevent one Agent from displacing another's protected allocation.

## Age context and chat continuity

Where age eligibility matters, we plan to rely on trusted third-party proof with minimal disclosure rather than guessing a user's age or collecting identity documents ourselves. Eligibility can update within the same chat without replacing the Agent or starting a new conversation. Ordinary interactions are separate from restricted features, and eligibility changes do not automatically enable cross-session memory or restore conversations that were not available for recall. No verifier has been selected or qualified.
