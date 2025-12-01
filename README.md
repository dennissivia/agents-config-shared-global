# Shared `.agents/` (global rules)

This repository holds the **global `.agents/` package (01–09 range) plus a dispatcher copy**. It was extracted from a larger workflow bundle so teams can drop just the global rules into their repo’s `.agents/` (or `.agents/shared/global/`) folder. The structure follows `AGENTS_CODING_SPEC.md`.

## What Lives Here
- Global rules for communication, scope, safety, and context (`01–09` files).
- `00_index.md` as a dispatcher (kept here for convenience even though it typically sits at the root `.agents/`).
- `AGENTS_CODING_SPEC.md` as the reference for folder layout and numbering.

## Files
- `00_index.md` — dispatcher describing load order and precedence.
- `01_global_01_purpose-and-scope.md` — defines the `.agents/` mission and scope.
- `01_global_02_foundational-rules.md` — absolute rules and required workflow sequence.
- `01_global_03_communication-guidelines.md` — tone, clarity, pause/feedback expectations.
- `01_global_04_ai-context-maintenance.md` — how to keep instructions current and prioritized.

## Numbering Guide
- `00`: dispatcher only (always loaded first).
- `01–09`: global rules (communication, safety, boundaries, context).
- `10–69`: reserved for workflow packages not included in this repo.
- `70–79`: experimental / WIP.
- `80–99`: reserved.

## Precedence and Layering
- Read files in lexical order by prefix; `00_index.md` defines load order, then globals (`01–09`).
- In host repos with multiple scopes (e.g., `shared/`, `vendor/`, `local/`), the closest `.agents/` folder to the code wins; use `00_index.md` to declare load order.
- Keep `.agents/` tracked in git and avoid renaming/renumbering unless the structure changes; prefer adding new topic files.
- Do not use custom names like `.aicontract`; `.agents/` is the canonical location for AI guidance.
