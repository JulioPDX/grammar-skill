---
name: docs-grammar-review
description: Review and correct grammar, clarity, and technical-writing style in documentation for open-source software projects. Use for prose in guides, tutorials, references, READMEs, release notes, and similar contributor- or user-facing documentation. In pull requests and feature branches, review only changed content; do not use to rewrite source code or machine-generated output.
---

# Documentation Grammar Review

Polish documentation without changing its technical meaning or the project's voice.

## Editorial basis

Read [references/style-guides.md](references/style-guides.md) before reviewing text. Apply the shared principles of the Google developer documentation style guide and the Microsoft Writing Style Guide rather than inventing a house style.

Use this precedence when guidance conflicts:

1. The user's explicit request.
2. The repository's documented conventions, terminology, and audience needs.
3. Technical accuracy and established product or API names.
4. The Google and Microsoft guidance summarized in the reference.

Mention a genuine style-guide conflict when it affects a correction; otherwise, choose the clearest wording without burdening the user with editorial mechanics.

## Review requirements

- Correct grammar, punctuation, spelling, agreement, sentence structure, and ambiguous modifiers.
- Improve clarity, concision, scannability, accessibility, and consistency when the request includes general correction or style review.
- Preserve meaning, technical accuracy, Markdown structure, links, code spans, identifiers, commands, paths, configuration keys, placeholders, and examples.
- Do not edit text inside code blocks, command output, logs, or literal UI strings unless the user explicitly asks.
- Prefer active voice, present tense, direct instructions, second person where appropriate, familiar words, and inclusive language.
- Avoid unnecessary rewrites. Do not present a style preference as a grammatical error.
- If context is insufficient to resolve a technically meaningful ambiguity, preserve the wording and flag the issue briefly.

## Change-scoped reviews

When the documentation is being reviewed in a pull request or feature branch, limit the review to content changed by that work:

- Use the pull request's target branch as the comparison base when PR metadata is available. Otherwise, compare the feature branch with the merge base of its intended target or the repository's default branch.
- Review added or modified documentation lines and files. If a documentation file is newly added, review the entire new file.
- Read unchanged lines around a diff hunk only to understand the changed text. Do not report or correct pre-existing issues outside the change set.
- Do not broaden the review to every documentation file or the full page containing a change unless the user explicitly requests a full review.
- If a correction to changed text requires a small adjustment to adjacent unchanged text for grammatical coherence, identify that dependency before proposing the adjustment.
- State the comparison base or supplied diff used to determine the review scope. If the base cannot be determined reliably, ask for the target branch or PR diff instead of reviewing the entire document.

## Response format

For a short passage, provide:

1. **Corrected text:** A clean, copy-ready version.
2. **Reasons:** Brief explanations of every substantive change. Distinguish required grammar corrections from optional style improvements.

If the original is already grammatically correct, say so explicitly. Offer a polished alternative only when it materially improves the documentation, and label it as optional.

For a long document, return the revised content in the format requested by the user and summarize recurring or significant edits. Do not enumerate every repeated mechanical correction unless asked.
