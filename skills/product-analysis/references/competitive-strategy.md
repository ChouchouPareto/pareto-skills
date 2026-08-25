# Competitive Strategy and Replication

Read this reference when the user treats the analyzed product as a competitor, asks why it was designed a certain way, wants to reproduce it, or wants implications for their own product.

## Evidence Boundary for “Why”

The product team’s actual internal motive is unknown unless an official interview, product note, or documentation states it. Derive possible motives only after observable behavior is established.

Classify each statement separately:

- **Confirmed behavior** — the UI, runtime result, official material, pricing, or state transition is visible.
- **Reasonable motive** — a product/business objective plausibly explains several confirmed behaviors.
- **Recommended action** — what the user should build, test, or avoid.
- **Unknown** — causality, effectiveness, metrics, ownership, or implementation cannot be verified.

Avoid phrases such as “they did this because” when motive is inferred. Prefer “a plausible product objective is” or “this design likely helps.”

## Behavior-to-Strategy Translation

For every strategically important behavior, answer:

| Question | Required output |
|---|---|
| What is visible? | Exact behavior, state, control, asset, pricing rule, or official claim with evidence ID |
| What objective might it serve? | Acquisition, activation, trust, retention, monetization, cost, safety, or operational efficiency; classify as inference |
| Why might it work? | User friction reduced, uncertainty managed, value made legible, or business constraint enforced |
| What is the reproducible mechanism? | Workflow, deterministic service, Agent role, data dependency, UI gate, or governance rule—not the surface copy alone |
| What should the user copy? | The mechanism and success condition |
| What should the user not copy? | State conflict, dark pattern, opaque claim, unsafe dependence, or unnecessary complexity |
| How can the user differentiate? | Evidence transparency, user control, reliability, privacy, speed, cost, domain depth, or feedback loop |
| What evidence is missing? | Metrics or failure-state observations needed to validate effectiveness |

Do not infer that a visible feature is successful merely because it exists. Separate design intent from measured outcome.

## Replication Architecture

Translate the competitor’s experience into the smallest reliable architecture:

1. **Deterministic business/tool layer** for calculations, IDs, links, permissions, billing, submission, and validated state.
2. **Agent layer** for language understanding, clarification, synthesis, and explanation.
3. **Workflow/state layer** for confirmations, asynchronous execution, retries, cancellation, dependency invalidation, and completion gates.
4. **Knowledge/data layer** for versioned rules, private context, public knowledge, and evidence references.
5. **Evaluation/governance layer** for factual consistency, output quality, safety, cost, and traceability.

Recommend single Agent + tools for bounded linear tasks. Recommend a deterministic workflow plus Writer/Reviewer for production reliability. Recommend Supervisor multi-Agent only when tasks have genuinely different expertise, permissions, context scopes, or independently recoverable branches. Never describe this recommendation as the competitor’s confirmed implementation.

## Build Priority

Organize recommendations by dependency, not visual appeal:

- **P0 — Correct and true:** deterministic domain engine, versioned data, state truth, authorization, safety, idempotency, cancellation, evidence chain.
- **P1 — Easy and valuable:** task routing, templates, progress, structured outputs, history, preflight cost/entitlement, local recomputation.
- **P2 — Differentiated and scalable:** premium artifacts, advanced routing, multi-Agent supervision, human service, cross-project learning.

For each priority, state the user outcome, system capability, acceptance test, and evidence or design reason.

## Required Competitive Deliverables

When the user requests competitive implications, include:

1. One-sentence explanation of the competitor’s core mechanism.
2. A “why this design may exist” section with explicit inference labels.
3. A table: competitor behavior → likely objective → why it works → what to copy → differentiation → evidence.
4. A “do not copy” list grounded in observed conflicts or known risks.
5. P0/P1/P2 build priorities for the user’s product.
6. The smallest viable Agent + tool + workflow replication pattern.
7. Validation questions or metrics needed before treating the inferred strategy as effective.

## Comprehension Standard

For long HTML or architecture reports:

- Put a one-sentence product explanation in the hero or executive summary.
- Add one “一句话理解 / One-sentence takeaway” after every major section heading.
- Make the sentence answer “so what?” in plain language; do not restate the section title.
- Use explicit labels and text, not color alone, for confirmed, inferred, recommended, and unknown claims.
- Keep the competitive section close to the user journey so strategy follows observable behavior before architecture detail.
