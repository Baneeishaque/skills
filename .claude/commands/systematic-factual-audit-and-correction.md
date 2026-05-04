---
name: systematic-factual-audit-and-correction
description: Workflow command scaffold for systematic-factual-audit-and-correction in skills.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /systematic-factual-audit-and-correction

Use this workflow when working on **systematic-factual-audit-and-correction** in `skills`.

## Goal

Performs a systematic audit to find and correct factual errors across multiple documentation files, ensuring alignment with live Cloudflare documentation.

## Common Files

- `skills/*/SKILL.md`
- `skills/*/references/*.md`
- `skills/cloudflare/references/**/*.md`
- `README.md`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Review multiple documentation files for factual errors (limits, pricing, API names, etc.)
- Correct errors and cite sources where appropriate
- Update all affected files in a single commit

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.