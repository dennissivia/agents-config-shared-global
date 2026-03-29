# Foundational Rules (Global)

These rules are absolute.  
They use **pattern references**, not file references, to avoid fragility.  
If a rule appears to conflict with project-specific guidance, follow the stricter one.

## 1. Security First
- Never expose secrets.
- Assume all inputs are untrusted.
- Avoid injection, validate all external data.
- Prefer secure defaults.

## 2. Follow the Workflow Package
- Use the ordered phases defined by the repository’s workflow package (`10_*` index and its `20–69` stage rules). Do not reorder or skip phases.
- If multiple packages exist (e.g., dev, tech review), follow the one selected by `00_index.md` or the task scope; ask for clarification if unclear.
- If the workflow package is missing or underspecified, pause and ask for guidance before proceeding.

## 3. Maintain Quality
- Always format before committing.  
- Always run all tests before any git action.  
- Never generate or propose code that knowingly breaks the build.

## 4. Git Safety
- Never perform git actions without confirmation.  
- Use feature branches.  
- Make atomic commits with clear messages.  
- Treat PRs as a final safety review.

## 5. Maintain the `.agents/` Rules
- Re-read these rules before tasks that modify design, behavior, or conventions.  
- Update them when new preferences or shared decisions emerge.  
- Treat them as the primary context anchor whenever session memory is lost.

## 6. Never Commit `.agents/` Changes
- The `.agents/` directory is a **shared remote repository**.
- AI agents must **never commit changes** to `.agents/` files.
- Committing `.agents/` changes will cause git repository confusion around submodules and sync issues.
- Rules updates will be committed by a human or an agent with explicit instructions to do so.
- You may modify `.agents/` files locally during a session, but never stage, commit, or push them.
