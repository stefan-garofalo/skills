---
name: human-writing
description: Draft and revise human-facing prose through semantic progression. Use for articles, documentation, essays, posts, explanations, and public copy when the user wants high signal, coherent paragraph flow, natural human rhythm, or removal of repetitive AI-writing patterns such as antithesis and epanorthosis.
---

# Human Writing

Use **semantic progression** as the governing criterion: make every sentence add a distinct, necessary change to the reader's working model, then make that change follow logically from the preceding material.

## Build semantic progression

Give each paragraph one reader-facing job. Assign every sentence a concrete role:

- define a term or claim
- explain a cause or mechanism
- supply evidence or an example
- derive a consequence
- establish a boundary or tradeoff
- change the reader's next action

Keep stable terms for stable entities. Prefer verbs that expose operations, such as `selects`, `commits`, `derives`, `validates`, and `returns`.

Choose sentence length from the information being carried. Keep a complete relation together. Split at a genuine conceptual boundary.

Use prose for causality and judgment. Use lists, tables, diagrams, or code when repeated fields, sequence, hierarchy, or structure become easier to inspect through those forms.

## Draft

1. State the paragraph's intended reader change in one sentence.
2. Build a dependency chain from the available material.
3. Open with the operative claim, observation, or pressure point.
4. Make each following sentence answer one live question raised so far: what, how, why, what proves it, what follows, where it applies, or what to do.
5. Close when the paragraph's job is fulfilled.

Complete the draft pass when the paragraph job and every sentence's contribution can be named without inventing missing links.

## Revise

1. Name the existing paragraph's job.
2. Label every sentence by its concrete role.
3. Name the relationship between every adjacent pair: definition, elaboration, cause, mechanism, evidence, consequence, boundary, or action.
4. Run three tests:
   - **Deletion:** remove the sentence; keep it only when understanding, prediction, or action loses something material.
   - **Link:** require a defensible relationship with the preceding material; rewrite, reorder, or split when the relationship is unclear.
   - **Substitution:** replace the subject with an unrelated concept; rewrite generic language that still appears to work.
5. Attach evidence and examples to the claim they support.
6. Compress after the logic is sound.

Complete the revision pass when every sentence makes a unique contribution and every transition carries a visible semantic relationship.

## Control rhetorical repetition

Reserve antithesis and epanorthosis for isolated moments where the distinction or correction carries real information:

- **Antithesis** balances one idea against another.
- **Epanorthosis** stages a correction or sharper reformulation.

Treat recurring forms such as `not X, but Y`, `not only X, but also Y`, and `X did A; X did not do B` as failed progression. State the operative claim directly.

```text
Staged correction:
The workflow is not stateful because the model remembers;
it is stateful because the handoff is durable.

Direct claim:
Durable handoffs make the workflow stateful across transitions.
```

Build rhythm from the shape of the information. Replace repeated correction pivots, forced triads, generic emphasis, rhetorical recaps, and strings of short declarations with new substance. Use periods, commas, colons, or parentheses by default; use an em dash only when the interruption itself matters.

Use a rhetorical question only when the question opens necessary reasoning. Replace recap questions with the concrete consequence already established.

## Completion gate

Finish only when:

- each paragraph has one job
- every sentence has a unique, necessary role
- every adjacent sentence pair has a defensible relationship
- deleting any remaining sentence causes a material loss
- terminology remains stable
- evidence stays attached to its claim
- rhetorical patterns serve isolated ideas instead of carrying the whole argument
- the final sentence fulfills the paragraph's job
