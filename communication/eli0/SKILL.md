---
name: eli0
description: Make technical or professional content understandable to an intelligent reader with no prior context without losing accuracy or necessary detail. Use for explanations, rewrites, plans, documentation, review comments, summaries, or when the user wants clearer, plainer, newcomer-friendly language.
---

# ELI0

**Explain Like I Have Zero Context.**

Write for an intelligent reader who has not seen the earlier discussion, does not know unstated project history, and should not need to guess what the writer means.

Do not treat the reader like a child. Do not simplify by removing important meaning.

## Core rule

Make the minimum hidden context needed for understanding explicit while preserving the original facts, constraints, uncertainty, and technical meaning.

## How to write

1. Start with the actual answer, change, problem, or recommendation. Add background after the reader knows why it matters.
2. Name concrete actors, actions, and objects. Replace vague phrases with what is actually happening when the concrete information is known.
3. Keep established technical terms when they are the clearest words. Define a term or acronym on first use when a new reader cannot reasonably infer it from the surrounding text.
4. Explain the key connection between a premise and a conclusion. Do not jump from A to D when B or C is necessary to understand why D follows.
5. Use examples to support the real mechanism, not to replace it.
6. Remove abstract wording that adds no information. If a phrase such as "decouple", "unify", "capability", "pipeline", "governance", or "closure" is useful, say what it means in this case instead of relying on the label alone.
7. Do not explain basic knowledge merely because the reader has zero project context. Assume normal intelligence and relevant general competence unless the user says otherwise.
8. Keep caveats, exceptions, numbers, risks, and uncertainty. Clearer wording must not turn a qualified statement into a stronger claim.
9. Match the user's language and appropriate level of formality.
10. Keep code, identifiers, commands, API names, and quoted source text exact unless the task explicitly asks to change them.

## Choose the right operation

### Explain or write

Produce the clearest useful version directly. Give the reader enough context to understand the answer without reconstructing the previous conversation.

### Review

When asked to review clarity, do not rewrite everything by default. Identify the places where a new reader would get stuck.

For each meaningful problem, state:

- where the problem is;
- what the reader is missing or likely to misunderstand;
- what information or wording would fix it.

Focus on problems that change understanding or action. Do not report cosmetic preferences as comprehension failures.

### Rewrite

Preserve the original meaning. Rewrite structure and wording only as much as needed to make the content independently understandable.

Do not silently add facts. If required context is missing and cannot be inferred safely, mark the gap instead of inventing it.

## What to look for in a cold read

Check for:

- an undefined term, acronym, role, component, or identifier;
- a pronoun or vague noun whose referent is unclear;
- a conclusion whose reason is missing;
- a recommendation that does not say what should change;
- a sentence that uses an abstract label in place of a concrete explanation;
- a step that depends on knowledge introduced only later;
- a summary that drops an important condition or exception;
- repetition or formatting that makes the explanation look structured without making it easier to follow.

## Boundaries

- Do not turn every answer into a tutorial.
- Do not replace precise domain language with childish analogies.
- Do not add source-code comments merely to explain code. Code comments have their own quality rules.
- Do not use ELI0 to shorten content when shortening would remove information the reader needs.
- Do not manufacture background, intent, history, or rationale that was not provided or established.
