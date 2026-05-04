```markdown
# skills Development Patterns

> Auto-generated skill from repository analysis

## Overview

This skill documents the development patterns, coding conventions, and key workflows for the `skills` repository. The codebase is written in TypeScript and focuses on maintaining high-quality, modular documentation for Cloudflare products and related SDKs. It emphasizes systematic documentation, factual accuracy, and consistency across all reference materials.

## Coding Conventions

- **File Naming:**  
  Use camelCase for file names.  
  _Example:_  
  ```
  productReference.md
  apiDocumentation.md
  ```
- **Import Style:**  
  Use relative imports for TypeScript modules.  
  _Example:_  
  ```typescript
  import { fetchData } from './utils/fetchData';
  ```
- **Export Style:**  
  Use named exports.  
  _Example:_  
  ```typescript
  export function getProductInfo() { ... }
  export const PRODUCT_LIMIT = 100;
  ```
- **Commit Message Patterns:**  
  - Mixed types, with prefixes like `fix`, `[workflows]`, `ci`
  - Average commit message length: ~58 characters

## Workflows

### Add New Product or Feature Reference
**Trigger:** When adding documentation for a new Cloudflare product or feature  
**Command:** `/add-feature-reference`

1. Create a new directory:  
   ```
   skills/cloudflare/references/{product}/
   ```
2. Add or update at least 3-5 of the following files:  
   - `README.md`
   - `api.md`
   - `configuration.md`
   - `patterns.md`
   - `gotchas.md`
3. Update the main index:  
   - Edit `skills/cloudflare/SKILL.md` to reference the new product or feature.

_Example directory structure:_
```
skills/cloudflare/references/flagship/
  ├─ README.md
  ├─ api.md
  ├─ configuration.md
  ├─ patterns.md
  └─ gotchas.md
```

---

### Systematic Factual Audit and Correction
**Trigger:** When ensuring documentation is accurate and up-to-date with official sources  
**Command:** `/audit-docs`

1. Review multiple documentation files for factual errors (e.g., limits, pricing, API names).
2. Correct any errors found and cite sources where appropriate.
3. Update all affected files in a single commit.

_Example:_
> Update API limits in `api.md` and reference the official Cloudflare docs.

---

### Consolidate and Revamp Skill Documentation
**Trigger:** When centralizing documentation for a product or SDK and removing deprecated guides  
**Command:** `/consolidate-skill`

1. Create or expand a consolidated skill directory (e.g., `skills/agents-sdk/`).
2. Add or update `SKILL.md` and reference files in the new directory.
3. Update related command documentation to reference the new skill.
4. Remove or deprecate legacy skill files.

_Example:_
```
skills/agents-sdk/
  ├─ SKILL.md
  ├─ references/
  │    ├─ api.md
  │    └─ patterns.md
commands/
  └─ agents-sdk.md
```

---

### Update Import Paths or APIs in References
**Trigger:** When fixing inconsistencies in import paths or API usage across documentation  
**Command:** `/update-import-paths`

1. Identify inconsistent import paths or API usage in reference files.
2. Update all affected files to use the standardized path or API.
3. Reference official documentation for correctness.

_Example:_
```diff
- import { Agent } from 'cf-agents';
+ import { Agent } from '@cloudflare/agents-sdk';
```

---

## Testing Patterns

- **Framework:** Unknown (not explicitly detected)
- **Test File Pattern:** Files are named with `.test.` in the filename.
  _Example:_  
  ```
  utils.test.ts
  productReference.test.ts
  ```
- **Test Placement:** Tests are located alongside source files or in dedicated test directories.

## Commands

| Command                | Purpose                                                                 |
|------------------------|-------------------------------------------------------------------------|
| /add-feature-reference | Add documentation for a new product or feature                          |
| /audit-docs            | Systematic factual audit and correction across documentation            |
| /consolidate-skill     | Consolidate and revamp skill documentation, removing deprecated guides  |
| /update-import-paths   | Standardize import paths or API usage in reference documentation        |
```