---
name: technical-writing
description: Plan technical articles, draft technical explanations and tutorials, revise technical prose, and package publication-ready writing for readers.
---

# Technical Writing

Governing model: **reader + gap + claim + evidence + payoff**.
Execution order: **promise -> context -> mechanism -> example -> tradeoff -> takeaway**.

## Composition

Apply `$human-writing` to every artifact containing clauses, sentences, or paragraphs. Invoke it before drafting or revision, then rerun its necessity audit after technical edits.

Composition Gate
- Pass only if every prose artifact passes `$human-writing`'s completion gate after its technical content is final.

## Compact workflow

Start from the earliest missing artifact required. Preserve approved artifacts unless inconsistent.
Stop when the user-requested deliverable is ready.
Each stage has an `Artifact` and a `Gate`. Advance only after that Gate and the Composition Gate pass.

## Stage 1 - Reader contract

Artifact
- Reader clause: define reader role and decision horizon.
- Prior actions: list what the reader already did and already knows.
- Exactly one confusion: include one unanswered confusion sentence only.
- Changed understanding/action: one concrete action the reader can now take.
- Promise: resolve the gap without stating mechanism.

Gate
- Pass only if all five bullets exist, only one confusion sentence is present, and the promise resolves that one gap without naming the mechanism.

## Stage 2 - Claim card

Artifact
- Topic.
- Contestable position-taking claim.
- Testable `when` + `who` boundary.
- Decision payoff.
- Title that encodes claim and tension.
- Dissenter path: one type of persuasive evidence a skeptic would require.

Gate
- Pass only if claim is testable, bounded, and directly tied to a decision.
- Pass only if the title expresses both claim and tension.
- Pass only if the dissenter path names evidence that would change the claim.

## Stage 3 - Problem frame (120-170 words)

Artifact moves
- Neutral opening on familiar practice.
- Why this practice is reasonable.
- First observable failure.
- One concrete cost question.
- No solution language.

Gate
- Pass only if moves are exactly in this order and no solution language exists:
  1) familiar practice, 2) reason it is reasonable, 3) first observable failure, 4) one concrete cost question.
- Pass only if word count is between 120 and 170.

## Stage 4 - Spine

Artifact
- Context.
- Tension.
- Mechanism.
- Example.
- Boundary.
- Decision/takeaway.
- One job sentence each, all explicitly supporting the claim.

Gate
- Pass only if all six elements are present and exactly in order.
- Pass only if each heading carries one job that answers a new reader question and directly supports the claim.

## Stage 5 - Mechanism (150-250 words)

Artifact
- Familiar anchor.
- Preserved behavior.
- Exactly one changed operation.
- Capability gained.
- Boundary statement.
- Causal before/after explanation with stable terms.

Gate
- Pass only if stable terminology is used throughout.
- Pass only if exactly one changed operation is defined.
- Pass only if causal capability is explicit from before to after.
- Pass only if boundary is explicit.
- Pass only if mechanism length is between 150 and 250 words.

## Stage 6 - Three progressive examples

Artifact
- Build exactly three examples.
- For each example:
  - Baseline.
  - one change.
  - prediction made before observation.
  - observation.
  - explanation tied to the changed variable.
- Change one variable from that example's baseline.
- In the third example, use a neutral second variable for transfer.
- Record whether transfer holds or fails.

Gate
- Pass only if exactly three examples exist.
- Pass only if every example has all five slots in order.
- Pass only if each example changes exactly one variable from its baseline.
- Pass only if each example makes prediction before observation.
- Pass only if each explanation is explicitly tied to that example's changed variable.
- Pass only if the third example uses a neutral second variable transfer check and records hold/fail explicitly.

## Stage 7 - Tradeoffs

Artifact
- For each recommendation: trigger, benefit, cost, exception, sub-minute rule.
- Benefit+cost must be present per recommendation.

Gate
- Pass only if each recommendation has trigger, benefit, cost, concrete exception, and sub-minute decision rule.
- Temporary uncertainty markers must be resolved before publication.
- Genuine uncertainty is allowed when explicitly stated with scope and test.
- Pass only if exception and rule are concrete and bounded.

## Stage 8 - Clarity

Artifact
- Assign exactly one job to each section; split any section carrying two jobs.
- Add temporary confidence labels to sentences during the edit.
- Delete sentences that do not advance their section job.
- Keep each concrete example attached to the claim it clarifies.
- Compare old and new wording to preserve meaning.
- Remove all temporary confidence labels.

Gate
- Pass only if every section has one job.
- Pass only if every remaining sentence advances that section's job.
- Require at least one justified deletion unless every sentence independently passed the job test.
- Pass only if examples remain attached, meaning is preserved, and temporary labels are gone.

## Stage 9 - Publish packet

Artifact
- Title with claim/tension.
- One-line pitch tied to reader relevance.
- Final compress-and-transfer paragraph with action.
- Checklist: reader need, claim consistency, bounded evidence, explicit boundary.

Decision rule
- If evidence/boundary fails, keep as draft and do not claim completion.

Gate
- Pass only if publish packet is self-consistent and all checklist items pass.
