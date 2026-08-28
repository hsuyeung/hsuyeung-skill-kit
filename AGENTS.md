# Repository guidance

This repository contains independent, reusable Agent Skills.

## Structure

- Keep the hierarchy shallow: `<category>/<skill-name>/`.
- Group Skills by the primary problem they solve, not by model provider or agent product.
- Do not create empty category directories.
- Each Skill must work independently. Do not require sibling Skills unless a real dependency is unavoidable and documented.
- Every published Skill should contain `SKILL.md` and a human-readable `README.md`.
- Add `references/`, `scripts/`, or `assets/` only when the Skill genuinely needs them. Do not create empty supporting directories.

## Naming

- Use lowercase letters, numbers, and hyphens for directory names and frontmatter `name` values.
- Prefer names whose purpose is easy to discover from the repository listing.
- Memorable concept names are welcome when the concept itself is clear, such as `eli0`.
- Do not invent opaque abbreviations just to make a name look clever.

## SKILL.md

- Keep each Skill focused on one primary job.
- Write durable rules and decision boundaries rather than patches for individual bad cases.
- Prefer concrete instructions over vague abstractions, slogans, or long blacklists.
- Preserve important facts, constraints, uncertainty, edge cases, and user intent.
- Do not force a fixed output format unless the task actually needs one.
- Keep the main Skill concise. Move optional long material into supporting files only when useful.

## Descriptions

The frontmatter `description` is used for routing. It should say what the Skill does and when it applies.

Descriptions should:

- state the primary job directly;
- mention representative tasks or triggers;
- use ordinary, specific language;
- remain useful across projects and repositories;
- avoid temporary history, unexplained jargon, and model-specific wording unless required.

## Language

- Maintain one canonical version of each general-purpose `SKILL.md`.
- Use concise English for general-purpose Skill instructions.
- The Skill should respond in the language requested by the user or established by the task context.
- For source code, preserve the repository's established comment and documentation language unless asked otherwise.
- Create a language-specific Skill only when the behavior itself depends on that language.

## Portability

- Use the shared Agent Skills format as the baseline.
- Keep Skills platform-neutral unless platform-specific behavior is genuinely required.
- Do not add a repository-wide install-all workflow.
- A Skill directory should remain useful when copied by itself into another compatible Agent environment.

## Before committing a Skill

Check that:

1. the directory name matches the frontmatter `name`;
2. the description clearly says what the Skill does and when to use it;
3. the Skill has one primary job;
4. the instructions are general rather than tied to one previous example;
5. the Skill works independently;
6. the README explains the Skill to a human reader without duplicating the full instruction file;
7. optional files and dependencies exist only when they add real value.
