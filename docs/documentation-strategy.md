# Documentation Strategy

## Objective

Keep the project explainable, versionable, and ready for later publication into a dedicated Confluence space.

## Local-First Approach

For now, documentation lives in this workspace.

Recommended local structure:

- [README.md](../README.md) for project overview and entry points.
- [architecture.md](./architecture.md) for system structure, levels, and interaction flows.
- [decision-log.md](./decision-log.md) for explicit architectural and operating decisions.
- [git-strategy.md](./git-strategy.md) for repository boundary, backup, and migration guidance.
- Additional focused documents later for team instances, community-of-practice models, and integration patterns.

## What To Document Locally Now

- Project purpose and target operating model.
- Shared architecture and role boundaries.
- Major decisions with rationale and consequences.
- Next-step roadmap.
- Template versus team-local versus federated responsibilities.

## What To Add When Team Instances Exist

- Team-specific context documents.
- Ownership boundaries and stakeholder maps.
- Local ceremony conventions.
- Tooling integration notes for Jira and Confluence.
- Codebase-specific delivery and validation rules.

## Confluence Publishing Goal

When the space is available, publish at least these pages:

- Overview of AI Scrum Squad.
- Architecture and operating model.
- Decision log or ADR summary.
- Team instance handbook for each real team.
- Community of practice guidelines.

## Suggested Confluence Space Structure

- Home
- Architecture
- Decisions
- Team Instances
- Communities of Practice
- Integrations

## Versioning Recommendation

The current recommendation is documented in [git-strategy.md](./git-strategy.md).

In short:

1. Use the parent repository only as a temporary safety net if an immediate commit is needed.
2. Move the project to a dedicated repository as the target operating model.
3. Avoid nested repositories unless submodule or subtree behavior is explicitly required.

## Publishing Principle

Treat local Markdown as the draft source and Confluence as the published collaboration surface.

That keeps early work lightweight while preserving a clear migration path toward shared organizational documentation.