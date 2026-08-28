---
name: code-comments
description: Review, write, or rewrite code comments so they preserve information the code itself cannot reliably express, such as reasons, constraints, invariants, contracts, risks, and non-obvious intent. Use for inline comments, block comments, docstrings, Javadoc, XML documentation, TSDoc, TODOs, FIXMEs, or when deciding whether comments should be kept, rewritten, removed, or replaced by clearer code.
---

# Code Comments

Use comments to preserve important information that the code itself cannot express clearly enough.

The goal is not to maximize or minimize comments. The goal is to keep comments that carry durable information a reader needs and cannot get reliably from the code alone.

## Before adding a comment

Ask whether clearer code can express the same information better.

Prefer a better name, type, function boundary, data structure, or control flow when the comment only compensates for confusing code.

Add or keep a comment when the information remains important even after the code is clear.

## Information worth commenting

Comments are useful for information such as:

- why a non-obvious choice was made;
- a business rule or external constraint that is not visible from the syntax;
- an invariant or correctness condition that a future edit must preserve;
- a trade-off where the apparently simpler implementation is intentionally not used;
- a compatibility workaround or external-system behavior;
- a non-obvious algorithmic idea needed to understand or safely modify the implementation;
- a public API contract, including behavior, preconditions, side effects, errors, lifecycle, or ownership that the signature alone does not communicate;
- a TODO or FIXME that states the concrete gap and the condition for considering it resolved.

A comment may explain **what** when the code cannot make an important contract or behavior visible. "Explain why, not what" is a useful default for implementation comments, not an absolute rule for every form of code documentation.

## Comments to remove or rewrite

Do not keep comments that only:

- translate the next line into prose;
- repeat a function, variable, type, or method name;
- label a section that is already obvious from the code structure;
- describe implementation details that will predictably become false when the code changes;
- say that something is "important", "special", "optimized", or "temporary" without explaining the actual condition;
- speculate about historical intent;
- apologize for code instead of explaining a real constraint.

## Never invent rationale

Do not guess why code exists.

Never invent:

- business reasons;
- performance claims;
- bug or incident history;
- issue or ticket numbers;
- owners;
- deadlines;
- removal dates;
- compatibility requirements.

If the reason is not known, either omit the comment or state only the verified constraint.

## Public API documentation

For docstrings, Javadoc, XML documentation, TSDoc, and similar public documentation, describe the contract from the caller's perspective.

Include what a caller needs to use the API safely. Avoid narrating internal implementation unless it affects observable behavior or compatibility.

Do not omit useful contract information merely because it describes "what" the API does.

## TODO and FIXME

A useful TODO or FIXME should make the unfinished state understandable without inventing process metadata.

Prefer:

```text
TODO: Remove this fallback after all stored records have a non-null timezone.
```

Avoid:

```text
TODO: Clean this up later.
```

Add an owner, date, or ticket only when it is already known from the repository or provided context.

## Review existing comments

When the task is to audit comments, classify each meaningful case as one of:

- **keep**: the comment adds durable information the code cannot express clearly;
- **rewrite**: the information matters, but the wording is vague, stale, or misleading;
- **delete**: the comment only repeats the code or adds no useful information;
- **refactor code**: clearer code would remove the need for the comment;
- **move to documentation**: the information belongs in an ADR, issue, README, API guide, or other broader document rather than beside the code.

Explain the reason for the classification. Do not demand comments everywhere simply because a function is complex.

## Language and style

- Follow the repository's established comment and documentation language when one exists.
- Otherwise, follow the user's language.
- Preserve established documentation conventions for the language or framework.
- Keep comments close to the code or contract they explain.
- Prefer a short precise comment over a long narrative when both preserve the same necessary information.
