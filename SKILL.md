---
name: docs-grammar-review
description: Proofread, copyedit, or improve grammar, clarity, and technical-writing style in Markdown and open-source documentation. Use for guides, tutorials, API references, READMEs, release notes, pull-request documentation changes, and similar user- or contributor-facing prose. Preserve technical meaning and project voice; do not use to rewrite source code, generated files, logs, or command output.
---

# Documentation Grammar Review

Polish documentation without changing its technical meaning or the project's voice.

## Set the review contract

Infer the narrowest mode that satisfies the request:

- **Proofread:** Correct objective errors in grammar, spelling, punctuation, agreement, and sentence structure. Do not make optional stylistic rewrites.
- **Copyedit:** Also improve clarity, concision, consistency, accessibility, and scannability while preserving voice.
- **Rewrite:** Restructure or substantially rephrase only when the user explicitly asks.

Treat “review,” “check,” or “suggest” as a request for findings or corrected text. Modify files only when the user asks to edit, fix, apply, or update them.

## Editorial basis

For copyediting or rewriting, read [references/style-guides.md](references/style-guides.md) before reviewing. For proofreading, load it only when a disputed choice depends on style rather than grammar.

Use this precedence when guidance conflicts:

1. The user's explicit request.
2. The repository's documented conventions, terminology, and audience needs.
3. Technical accuracy and established product or API names.
4. The Google and Microsoft guidance summarized in the reference.

Mention a genuine style-guide conflict when it affects a correction; otherwise, choose the clearest wording without burdening the user with editorial mechanics.

## Protect technical meaning

Before accepting a smoother sentence, compare its technical claims with the original. Preserve:

- conditions, exceptions, prerequisites, sequence, causality, scope, and degree of certainty;
- normative force in words such as **must**, **should**, **may**, **required**, and **optional**;
- product names, established terminology, API and UI names, identifiers, commands, paths, configuration keys, placeholders, literal values, and examples;
- Markdown structure, link destinations, code spans, and formatting that conveys meaning.

Do not turn a conditional statement into an unconditional one, a recommendation into a requirement, or a possibility into a guarantee. If a technically meaningful ambiguity cannot be resolved from nearby context, preserve it and flag it instead of guessing.

Headings, labels, table cells, and list items may intentionally be fragments. Do not “correct” them into sentences unless grammar or parallelism actually requires it.

## Review documentation-aware prose

- Review headings, paragraphs, link text, image alt text, admonitions, tables, and list items as prose while preserving their markup.
- Do not edit fenced or indented code blocks, command output, logs, generated content, literal UI strings, or embedded source code unless explicitly asked.
- In mixed prose and code, change only the prose. Never silently change a token because it resembles a misspelling.
- Check parallel structure across sibling headings, steps, and list items. Preserve fragments when the whole set uses fragments consistently.
- Prefer active voice, present tense, direct instructions, second person where natural, familiar words, and inclusive language during copyediting—not as inflexible grammar rules.
- Avoid unnecessary rewrites and distinguish objective corrections from optional style choices.

## Change-scoped reviews

When reviewing a pull request, supplied diff, or feature branch, limit findings and edits to content changed by that work:

- Use the pull request's target branch as the comparison base when PR metadata is available. Otherwise, compare the feature branch with the merge base of its intended target or the repository's default branch.
- Review the changed logical prose unit—not an isolated line—when a modified line belongs to a sentence, list, table row, or paragraph. If a documentation file is newly added, review the entire file.
- Read adjacent unchanged content for grammar, referents, terminology, and technical context. Do not report or correct unrelated pre-existing issues outside the change set.
- Do not broaden the review to every documentation file or the full page containing a change unless the user explicitly requests a full review.
- If correcting changed text requires a small edit to adjacent unchanged text for grammatical coherence, identify the dependency and keep the expansion minimal.
- State the comparison base or supplied diff used to determine the review scope. If the base cannot be determined reliably, ask for the target branch or PR diff instead of reviewing the entire document.

## Response format

Unless the user requests another format, provide for a short passage:

1. **Corrected text:** A clean, copy-ready version.
2. **Reasons:** Brief explanations of substantive changes, distinguishing required corrections from optional style improvements.

If the original is already grammatically correct, say so explicitly. Offer a polished alternative only when it materially improves the documentation, and label it as optional.

For a long document or applied file edit, return or modify the content as requested and summarize recurring or significant changes. Do not enumerate every repeated mechanical correction unless asked.

For a review-only diff, report each issue with its location, original wording, proposed wording, and reason. Return no findings when the changed prose needs no correction.
