# grammar-skill

A [Claude Code skill](https://docs.anthropic.com/en/docs/claude-code/skills) that reviews and corrects grammar, clarity, and technical-writing style in open-source documentation.

## What it does

Point the skill at any piece of documentation — a README, guide, tutorial, release notes, or API reference — and ask it to proofread, copyedit, or rewrite the prose. It preserves technical meaning and distinguishes required grammar fixes from optional style improvements.

Key behaviors:

- Follows the [Google developer documentation style guide](https://developers.google.com/style) and the [Microsoft Writing Style Guide](https://learn.microsoft.com/style-guide/welcome/) as its editorial baseline.
- Respects your project's existing voice, terminology, and conventions over generic style rules.
- Preserves conditions, exceptions, and normative terms such as `must`, `should`, and `may`.
- Preserves Markdown structure, links, code spans, commands, and examples — it won't touch anything inside code blocks unless you ask.
- In pull requests and feature branches, reviews only changed content rather than the entire document.
- Flags ambiguities it can't resolve instead of guessing.

## Installation

Install the skill into your Claude Code environment:

```bash
claude install-skill https://github.com/JulioPDX/grammar-skill
```

## Usage

Invoke the skill by name when asking Claude Code to review documentation:

```text
Review the grammar in README.md
```

```text
Use $docs-grammar-review to review this open-source documentation and explain every correction.
```

For pull request reviews, the skill scopes findings to changed content while reading the surrounding logical prose unit for context. It uses the PR's target branch as the comparison base.

## Project structure

```text
SKILL.md                   # Skill definition and instructions
references/style-guides.md # Editorial reference (Google + Microsoft guidance)
agents/openai.yaml         # OpenAI agent interface config
```

## License

[MIT](LICENSE)
