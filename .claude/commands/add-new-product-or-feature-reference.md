---
name: add-new-product-or-feature-reference
description: Workflow command scaffold for add-new-product-or-feature-reference in skills.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /add-new-product-or-feature-reference

Use this workflow when working on **add-new-product-or-feature-reference** in `skills`.

## Goal

Adds documentation for a new Cloudflare product or feature, including API, configuration, patterns, gotchas, and README files, and updates the main SKILL.md index.

## Common Files

- `skills/cloudflare/SKILL.md`
- `skills/cloudflare/references/*/README.md`
- `skills/cloudflare/references/*/api.md`
- `skills/cloudflare/references/*/configuration.md`
- `skills/cloudflare/references/*/patterns.md`
- `skills/cloudflare/references/*/gotchas.md`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Create a new directory under skills/cloudflare/references/{product}/
- Add or update the following files: README.md, api.md, configuration.md, patterns.md, gotchas.md (sometimes not all, but at least 3-5 of these)
- Update skills/cloudflare/SKILL.md to reference the new product/feature

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.