# AI Scrum Squad Architecture

## Purpose

Define the target architecture for an AI-assisted delivery system in which each physical Scrum team works with its own AI Scrum Squad, while multiple squads can later collaborate across teams through shared practices and governance.

## Architectural Levels

### 1. Shared Template Layer

This layer defines the reusable baseline for every AI Scrum Squad.

- Shared role definitions and boundaries.
- A common orchestration model.
- Reusable ceremony workflows.
- Shared conventions for Tagetik product delivery.
- Rules for what belongs in the template versus what must remain team-local.

Current workspace assets for this layer:

- [AGENTS.md](../AGENTS.md)
- [.github/agents/scrum-squad-orchestrator.agent.md](../.github/agents/scrum-squad-orchestrator.agent.md)
- [.github/agents/product-owner.agent.md](../.github/agents/product-owner.agent.md)
- [.github/agents/scrum-master.agent.md](../.github/agents/scrum-master.agent.md)
- [.github/agents/quality-expert.agent.md](../.github/agents/quality-expert.agent.md)
- [.github/agents/business-analyst.agent.md](../.github/agents/business-analyst.agent.md)
- [.github/agents/ux-expert.agent.md](../.github/agents/ux-expert.agent.md)
- [.github/agents/frontend-engineer.agent.md](../.github/agents/frontend-engineer.agent.md)
- [.github/agents/backend-engineer.agent.md](../.github/agents/backend-engineer.agent.md)
- [.github/skills/scrum-ceremony-support/SKILL.md](../.github/skills/scrum-ceremony-support/SKILL.md)

### 2. Central Capability Layer

This layer represents shared specialist capabilities that operate across multiple teams.

Typical examples include:

- UX or UI leadership and design-system ownership.
- Quality management and release-quality governance.
- DevOps or platform engineering.
- Security, Data or AI, DBA, and architecture capabilities.

This layer provides:

- Official guidelines and standards.
- Shared frameworks, libraries, and design systems.
- Cross-team guardrails and escalation points.
- Reusable expertise that should not be duplicated independently in every team.

This layer should guide local teams without absorbing day-to-day execution that belongs inside each Scrum team.

### 3. Team Instance Layer

Each physical Scrum team creates a specialized AI Squad starting from the shared template.

This layer adds:

- Product area and bounded context.
- Owned modules and interfaces.
- Team-specific business vocabulary and business rules.
- Local ceremony variants and working agreements.
- Local Jira and Confluence conventions.
- Codebase-specific delivery, validation, and release practices.

Within this layer, some roles act as embedded local representatives of central capabilities rather than autonomous discipline owners.

Current examples:

- UX Expert as the local UX enablement and governance role.
- Quality Expert as the local quality enablement and governance role.

This layer must not rewrite the shared template unless the learning is broadly reusable.

### 4. Federation Layer

Multiple team-local AI Squads collaborate across product teams.

This layer exists to share:

- Validated practices.
- Decision patterns.
- Quality heuristics.
- Reusable backlog and refinement patterns.
- Common architectural concerns.
- Lessons learned that matter across teams.

This layer also hosts role-based Communities of Practice and Centers of Excellence that connect team-level experience with central capabilities.

Examples:

- UX Expert CoP feeding back into central UX or UI guidance.
- Quality Expert CoP feeding back into central quality standards and heuristics.
- Future CoPs for platform, security, data, architecture, or other shared disciplines.

This layer must preserve team autonomy. It should spread signal, not flatten domain differences.

## Role Model

### Orchestrator

Coordinates requests, selects the owning role, involves adjacent specialists only when required, and returns one coherent result.

### Product Owner

Owns value, prioritization, acceptance, and release intent.

### Scrum Master

Owns facilitation, flow, impediments, working agreements, and continuous improvement.

### Quality Expert

Acts as the embedded team quality role, applying central quality guidance locally and making team-level quality risks, validation scope, and release confidence explicit.

### Business Analyst

Owns requirement clarity, process framing, business rules, and decomposition support.

### UX Expert

Acts as the embedded team UX role, applying central UX or UI guidance locally and protecting interaction quality, accessibility expectations, and user-centered design tradeoffs.

### Frontend Engineer

Owns browser-facing implementation concerns, client integration, and user-facing behavior.

### Backend Engineer

Owns service logic, APIs, data flows, persistence impact, and integration boundaries.

## Interaction Flows

### Central-To-Team Guidance Flow

1. Central specialist capabilities publish standards, frameworks, patterns, and escalation rules.
2. Embedded team roles such as UX Expert and Quality Expert interpret those standards in the local delivery context.
3. The local squad applies them in refinement, implementation, validation, and release preparation.
4. When local decisions exceed delegated authority, the relevant central capability is engaged.

### Ceremony Flow

1. A ceremony request enters through the orchestrator or the ceremony support skill.
2. The ceremony type is classified.
3. Minimum inputs are checked.
4. The owning role is identified.
5. Supporting roles are involved only when there are cross-role dependencies or tradeoffs.
6. A standardized output is produced for the physical Scrum team.

### Sprint Execution Flow

1. A team member pairs with the most relevant AI role for the task at hand.
2. The role agent uses local team context and project assets.
3. If the task crosses boundaries, the orchestrator coordinates multiple roles.
4. Artifacts and decisions are written back to the team workflow tools when integration is available.

### Federated Learning Flow

1. Local squads identify reusable patterns, not just local details.
2. Candidate practices are reviewed across teams, Communities of Practice, or Centers of Excellence.
3. Validated patterns are promoted either to central capabilities, shared documentation, or to the template layer.
4. Team-local rules remain local unless there is evidence they should become shared defaults.

## External Systems

### Jira

Target usage:

- Prepare backlog items.
- Refine requirements.
- Track dependencies and sprint scope.
- Support daily coordination and retrospective follow-up.

### Confluence

Target usage:

- Store project documentation.
- Publish ceremony outputs when needed.
- Capture architecture decisions and shared practices.
- Expose team-local and federated knowledge in a searchable structure.

For now, documentation remains local in this workspace until the Confluence space is available.

## Information Boundaries

- Shared template knowledge belongs in the template layer.
- Central discipline standards belong in the central capability layer.
- Team-local knowledge belongs in specialized local instructions, prompts, skills, and docs.
- Federated knowledge must be curated before promotion into central guidance or shared template assets.
- Runtime ceremony data and sprint-specific noise should not pollute the shared template.

## Design Principles

- Keep role ownership explicit.
- Prefer orchestration over monolithic all-in-one behavior.
- Promote only validated cross-team practices into the template.
- Link to maintained sources instead of duplicating them.
- Optimize for reusable delivery artifacts, not conversational summaries.

## Near-Term Roadmap

1. Create the first concrete team instance model.
2. Define documentation artifacts for local team context.
3. Model central capability layers and their escalation boundaries.
4. Add a structure for Communities of Practice or Centers of Excellence.
5. Connect Jira and Confluence through the preferred central integration path.