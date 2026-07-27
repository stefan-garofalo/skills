---
name: technical-writing
description: Plan technical articles, draft technical explanations and tutorials, revise technical prose, and package publication-ready writing for readers.
---

# Technical Writing

Build every artifact around **reader + gap + claim + evidence + payoff**.

## Governing composition rule

Apply `$human-writing` before drafting or revision, then rerun its necessity audit after the technical content is final. Let semantic progression and the deletion test override every outline, stage, template, and checklist in this skill. Adapt, merge, reorder, or omit elements so every remaining part advances the reader's understanding.

Make technical explanations plain and connected:

- Introduce each technical component at first use through its responsibility and effect; use familiar words, and define any exact term the reader must recognize by explaining what it does.
- **Term alignment:** Keep exact terms stable across diagrams, examples, and prose.
- Support claims about behavior with inspected code, documentation, data, or observed output. Bound uncertain claims and name the check that would settle them.

## Diagnostic workflow

Use these passes as defaults, not as a mandatory article shape. Start where the artifact is weak, and preserve approved material unless it conflicts with the claim or evidence.

### Reader and claim

- Identify the reader, relevant prior knowledge, unresolved gap, claim, and payoff.
- Bound the claim by the people, conditions, and systems to which it applies.
- Introduce a foundational premise or scope boundary at the first point where the reader needs it to interpret what follows.
- Identify what evidence would support the claim and what evidence could change it.

### Structure

- Arrange sections by conceptual dependency, so each section answers the question created by the preceding one.
- Use `promise -> context -> mechanism -> example -> tradeoff -> takeaway` only as a diagnostic sequence. Reorder, combine, or omit moves according to the genre and argument.
- Give each section one reader-facing job, while allowing that job to require several connected paragraphs.
- For revisions, preserve the intended meaning unless the evidence or user explicitly requires a change.

### Mechanism

- Explain the starting state, the relevant parts, what each part owns, how the parts interact, and the resulting state or capability.
- For a multi-part mechanism, map every part to its responsibility, inputs, operation, and outputs, then make the causal links between parts explicit.
- Distinguish concepts that can vary independently, such as execution state, domain outcome, evidence, and route, instead of overloading one term.
- **Artifact invariant:** Introduce each structured artifact through its role in the mechanism. Explain the purpose, relationship, or invariant that its visible fields cannot show alone; let field names and values carry their literal meaning, and group the minimum references needed to prove the explanation.

### Evidence and examples

- Use the minimum examples needed to resolve the reader's gap, and attach each example to the claim it demonstrates.
- **Scenario:** Write each hypothetical example as an ordinary scenario. Make its status unambiguous with a concrete setup such as `Suppose`, then move from the relevant starting state through the mechanism to its consequence. Apply `$human-writing`'s Demonstration audit to the finished scenario, and reserve `observation` for a result that was executed, measured, or recorded.
- Use baseline/change/prediction/observation structure only for a real comparison or experiment.
- When the article generalizes, establish transfer by showing how another case exercises the same mechanism; support that link with evidence or narrow the claim.
- Keep an example only when it changes the demonstrated outcome or adds evidence for the mechanism.

### Decisions and endings

- Include benefits, costs, exceptions, decision rules, questions, exercises, and next actions only when they serve the reader's decision and the available evidence supports them.
- **Ending:** Conclude with the strongest bounded implication the evidence supports, stated once; use it to resolve the opening gap or identify a genuine next decision.

## Completion gate

Finish only when:

- the reader, gap, claim, evidence, and payoff agree
- the claim's scope and foundational premises appear before dependent reasoning
- each mechanism part has a clear responsibility and causal relationship, and every structured artifact passes the Artifact invariant check
- evidence supports the claims made, and uncertainty in non-example claims is bounded
- examples are necessary and attached to the claims they clarify, and every hypothetical example passes the Scenario check
- technical distinctions remain precise, and the Term alignment check passes
- every section and paragraph passes `$human-writing`'s semantic progression and necessity audits
- the Ending check passes
