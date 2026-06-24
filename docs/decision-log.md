# Decision Log

## D-001 Shared Template First

- Date: 2026-05-13
- Status: accepted

Decision:

Start from a shared AI Scrum Squad template before modeling any single product team.

Rationale:

- It keeps common behavior reusable.
- It separates baseline role design from team-local specialization.
- It allows multiple teams to instantiate a consistent AI operating model.

Consequences:

- Team-specific context must be added later through specialization assets.
- Shared files must stay generic and stable.

## D-002 Role-Based Multi-Agent Model

- Date: 2026-05-13
- Status: accepted

Decision:

Use a role-based multi-agent system with one orchestrator and specialist agents for Product Owner, Scrum Master, Quality Expert, Business Analyst, Frontend Engineer, and Backend Engineer.

Rationale:

- It preserves ownership boundaries.
- It enables better delegation than a single generic assistant.
- It aligns the AI operating model with the physical Scrum team structure.

Consequences:

- Cross-role requests must be routed deliberately.
- Orchestration becomes a first-class concern.

## D-003 Local-First Documentation

- Date: 2026-05-13
- Status: accepted

Decision:

Document the project locally in the workspace first, then publish to Confluence when a dedicated space is available.

Rationale:

- Documentation can start immediately without external dependencies.
- The local workspace becomes the source draft for later publication.
- Early decisions remain versionable together with the customization assets.

Consequences:

- The project needs a lightweight local documentation structure now.
- A later synchronization or publishing path to Confluence must be defined.

## D-004 Defer Repository Split Decision

- Date: 2026-05-13
- Status: accepted

Decision:

Do not initialize a nested Git repository inside this folder yet.

Rationale:

- The folder already sits inside a larger Git repository.
- Adding nested version control is possible but should be an explicit repository strategy decision.
- Documentation and customization work can continue safely before that choice is made.

Consequences:

- Current work should be preserved either by committing in the parent repository or by explicitly creating a separate repository later.
- Repository strategy remains an open structural decision rather than an accidental setup.

## D-005 Federated Evolution Path

- Date: 2026-05-13
- Status: proposed

Decision:

Evolve from shared template to team-local AI Squads and then to a federated model with communities of practice across squads.

Rationale:

- It allows incremental adoption.
- It supports both local productivity and cross-team learning.
- It avoids over-designing federation before local squads exist.

Consequences:

- The architecture must model local and federated boundaries explicitly.
- Communities of practice should be added only after the first local team instance is defined.

## D-006 Dedicated Repository Target

- Date: 2026-05-13
- Status: accepted

Decision:

Use a dedicated repository as the target versioning model for AI Scrum Squad, while allowing a temporary safeguard through the current parent repository only if immediate backup is required.

Rationale:

- The current parent repository root is a multi-project container rather than a focused product repository.
- The Scrum Squad project has its own documentation, customization assets, lifecycle, and future Confluence publication path.
- A dedicated repository keeps history, ownership, review flow, and release of shared AI Squad assets isolated from unrelated work.

Consequences:

- Short-term protection may happen through the parent repository if needed immediately.
- The preferred medium-term move is to place this folder in its own repository.
- Nested repository setup inside the current folder remains discouraged unless explicitly chosen for submodule or subtree workflows.

## D-007 UX Expert In Base Squad

- Date: 2026-05-16
- Status: accepted

Decision:

Add UX Expert to the base AI Scrum Squad composition as a first-class role in the shared template.

Rationale:

- Frontend execution alone does not cover user-flow quality, usability, accessibility, or experience tradeoffs.
- Refinement and backlog readiness benefit from an explicit user-experience perspective before implementation starts.
- UX concerns are common enough across product teams to justify inclusion in the shared baseline.

Consequences:

- The orchestrator must consider UX Expert as a standard routing target.
- Team instances can specialize UX practices locally, but the role itself is now part of the shared core.
- DevOps, Security, Data/AI, DBA, and Architecture expertise remain candidates for shared specialist layers rather than automatic base roles.

## D-008 Embedded Specialist Model For UX And Quality

- Date: 2026-05-16
- Status: accepted

Decision:

Model UX Expert and Quality Expert as embedded team roles aligned to central specialist capabilities, rather than as fully autonomous discipline owners inside each Scrum team.

Rationale:

- In the target organization, UX and Quality standards are defined centrally and applied locally.
- Team-level specialists provide day-to-day enablement, governance, and escalation support rather than replacing the central function.
- This model better reflects enterprise operating reality and avoids duplicating full specialist authority in every squad.

Consequences:

- UX Expert and Quality Expert profiles must distinguish local decision scope from central escalation scope.
- The architecture must represent both central capabilities and embedded team roles.
- Future specialist roles such as platform, security, data, DBA, or architecture can follow the same pattern where appropriate.

## D-009 Communities Of Practice And Centers Of Excellence

- Date: 2026-05-16
- Status: accepted

Decision:

Use Communities of Practice and Centers of Excellence as the federated mechanism through which embedded specialists share experience and contribute back to central guidance.

Rationale:

- Team specialists need a structured way to share practices and lessons learned across squads.
- Central guidance improves when it is informed by operational feedback from delivery teams.
- A federated learning model is more effective than either pure top-down governance or isolated team-level learning.

Consequences:

- Federation is not only cross-team coordination; it also becomes a knowledge and standards feedback loop.
- The architecture should explicitly connect team embedded roles, CoPs or CoEs, and central specialist capabilities.