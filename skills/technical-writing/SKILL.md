---
name: technical-writing
description: Plan technical articles, draft technical explanations and tutorials, revise technical prose, and package publication-ready writing for readers.
---

# Technical Writing

Build every artifact around **reader + gap + claim + evidence + payoff**.

## Governing composition rule

Apply `$human-writing` before drafting or revision, then rerun its necessity audit after the technical content is final. Let semantic progression and the deletion test override every outline, stage, template, and checklist in this skill. Adapt, merge, reorder, or omit any element that does not advance the reader's understanding; never retain prose merely to satisfy a form.

Make technical explanations plain and connected:

- Name the concrete thing, its responsibility, and what changes.
- Use familiar words, and define an exact technical term at first use by explaining what it does.
- Give each sentence or clause one coherent explanatory move. Join related moves when conjunctions expose cause, condition, consequence, sequence, contrast, or qualification; split them when the explanation changes subject or job.
- Keep terms stable for stable subjects, especially across diagrams, examples, and prose.
- Support claims about behavior with inspected code, documentation, data, or observed output. Bound uncertain claims and name the check that would settle them.

## Diagnostic workflow

Use these passes as defaults, not as a mandatory article shape. Start where the artifact is weak, preserve approved material unless it conflicts with the claim or evidence, and stop when the requested deliverable is ready.

### Reader and claim

- Identify the reader, relevant prior knowledge, unresolved gap, claim, and payoff.
- Bound the claim by the people, conditions, and systems to which it applies.
- Introduce a foundational premise or scope boundary when the reader first needs it to interpret what follows; do not defer it to a generic boundary section.
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
- Include only the before-and-after detail needed to establish why the result follows.

### Evidence and examples

- Use the minimum examples needed to resolve the reader's gap, and attach each example to the claim it demonstrates.
- Distinguish observed evidence from a hypothetical derivation. Call a result an observation only when it was executed, measured, or recorded; otherwise label it as a prediction, trace, or scenario.
- Use baseline/change/prediction/observation structure only for a real comparison or experiment.
- Add a transfer case only when the article makes a generalization claim, and either support that transfer with evidence or narrow the claim.
- Remove examples that merely restate the mechanism or leave the demonstrated outcome unchanged.

### Decisions and endings

- Include benefits, costs, exceptions, decision rules, questions, exercises, and next actions only when the reader's decision or the requested genre requires them and the available evidence supports them.
- Never invent a cost, exception, timing heuristic, rhetorical question, exercise, or call to action to fill a template.
- Let the conclusion fulfill the argument: resolve the opening gap, state the bounded implication, or identify a genuine next decision. Do not require an action paragraph.

## Completion gate

Finish only when:

- the reader, gap, claim, evidence, and payoff agree
- the claim's scope and foundational premises appear before dependent reasoning
- each mechanism part has a clear responsibility and causal relationship
- evidence supports the claims made, while uncertainty and hypothetical material are labeled
- examples are necessary, honest about their status, and attached to the claims they clarify
- terminology remains stable and distinctions remain precise
- every section and paragraph passes `$human-writing`'s semantic progression and necessity audits
- the ending completes the argument without adding a new premise or a template-driven action
