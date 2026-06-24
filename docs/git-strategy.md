# Git Strategy

## Objective

Protect the current AI Scrum Squad work immediately without locking the project into the wrong repository boundary.

## Current Situation

- This workspace lives under `C:/Sviluppo/GHCP - GitHub Copilot/Scrum Squad`.
- The actual Git top-level repository is `C:/Sviluppo`.
- That parent repository contains multiple unrelated projects and already has unrelated local changes.
- `Scrum Squad` is therefore a subfolder inside a broad container repository, not a clean standalone repository.

## Recommendation

Adopt a two-step strategy.

### Step 1. Immediate Safety

Use the parent repository only as a temporary safeguard if you need to preserve work immediately.

This is the fastest path because:

- Git is already active.
- No structural move is required right now.
- The new files in `Scrum Squad` can be staged and committed without creating a nested repository.

Constraints:

- The parent repository is noisy and multi-purpose.
- History for Scrum Squad would be mixed with unrelated projects.
- Reviews and future ownership would be less clean.

### Step 2. Target State

Move `Scrum Squad` into a dedicated repository.

This is the preferred long-term model because:

- The project has its own architecture, documentation, and decision trail.
- It is intended to evolve as a reusable shared template across teams.
- It will likely need its own lifecycle, contribution flow, and publication path to Confluence.
- Repository boundaries will then match product boundaries.

## Option Assessment

### Option A. Keep Scrum Squad in the parent repository

Use when:

- You only need a quick backup.
- The parent repository is already the intended home for all AI enablement assets.

Pros:

- No migration effort.
- Fastest way to save current work.

Cons:

- Weak project isolation.
- Mixed history with unrelated work.
- Harder to manage ownership, pull requests, and future reuse.

Assessment:

- Acceptable as a short-term safety measure.
- Not recommended as the steady-state model.

### Option B. Move Scrum Squad to a dedicated repository

Use when:

- You want clean ownership and traceability.
- The project is expected to grow independently.
- Documentation, decisions, and customization assets should evolve as a coherent product.

Pros:

- Clean history.
- Clear project scope.
- Easier onboarding and publication.
- Better alignment with future Confluence space and federated governance.

Cons:

- Requires a conscious migration step.
- If other assets in the parent repository are tightly coupled, links may need adjustment.

Assessment:

- Recommended target state.

### Option C. Create a nested repository inside the current folder

Use when:

- You explicitly want submodule or subtree behavior.

Pros:

- Local isolation without moving files.

Cons:

- Easy to confuse contributors.
- Error-prone if the parent repository also tracks the same folder.
- Usually the worst compromise unless there is a strong Git workflow reason.

Assessment:

- Not recommended here.

## Practical Strategy

### Immediate action

1. Preserve the current work in the parent repository if you need protection today.
2. Keep the commit focused on the `GHCP - GitHub Copilot/Scrum Squad` folder only.
3. Avoid touching unrelated changes already present in `C:/Sviluppo`.

### Near-term follow-up

1. Create a dedicated remote repository for AI Scrum Squad.
2. Move or extract this folder into that repository.
3. Keep the existing Markdown docs as the initial seed history.
4. Continue local-first documentation there, then publish to Confluence from the dedicated repo artifacts.

## Suggested Commit Scopes

If using the parent repository temporarily, split commits by concern:

- initial squad template and role agents
- orchestration and specialization assets
- ceremony support skill
- architecture and documentation baseline
- git strategy and repository decision records

This keeps later migration easier.

## Recommendation Summary

- Immediate protection: parent repository is acceptable.
- Preferred destination: dedicated repository.
- Avoid: nested Git repository inside the current folder.