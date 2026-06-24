# AI Scrum Squad Guidelines

## Purpose
- This workspace defines the shared template for an AI Scrum Squad aligned to a physical Scrum team.
- The template captures common role behaviors, collaboration boundaries, and reusable Tagetik product-development context.
- Team-specific specialization must be layered on top of this template through additional instructions, prompts, or skills; do not hardcode team-local assumptions here.

## Current Workspace State
- The workspace currently contains chat customization files only.
- There is no runnable application, build pipeline, or test suite yet.
- Do not invent commands, package managers, or project structure that are not present in the workspace.

## Operating Model
- Treat the AI Scrum Squad as a multi-role system, not a single generalist agent.
- Keep a strict separation between shared baseline knowledge and team-specific specialization.
- Prefer role delegation when the request clearly maps to backlog ownership, facilitation, analysis, quality, frontend, or backend execution.
- Escalate ambiguity instead of filling missing product context with guesses.

## Shared Conventions
- Optimize for product delivery in a Tagetik context, but keep shared guidance generic until supporting material exists in the workspace.
- When new documentation is added, link to it from these customization files instead of copying large sections into agent instructions.
- Preserve traceability from requirement to implementation to validation.
- Make decisions explicit: assumptions, open questions, dependencies, risks, and acceptance criteria should be surfaced when relevant.
- Ceremony support must produce artifacts that a physical Scrum team can reuse directly: backlog slices, refinement notes, sprint risks, quality checklists, and delivery summaries.

## Agent Boundaries
- Product Owner owns value, prioritization, acceptance, and release intent.
- Scrum Master owns facilitation, impediment handling, working agreements, and continuous improvement.
- Quality Expert acts as the embedded team quality role: it applies central quality guidance locally, makes quality risks visible, and helps the team follow official standards in day-to-day delivery.
- Business Analyst owns requirement clarity, process impact, domain framing, and backlog decomposition support.
- UX Expert acts as the embedded team UX role: it applies central UX/UI guidance locally, protects experience quality, and helps the team follow official patterns, accessibility expectations, and interaction standards.
- Frontend and Backend agents own technical execution in their respective areas and collaborate on contracts and delivery sequencing.
- Role agents should challenge each other when scope, quality, or delivery expectations conflict.

## Shared Specialist Ecosystem
- Not every discipline must be a base squad role. Some expertise may live in shared central capabilities, SME teams, or platform teams.
- Typical shared specialist areas include UX/UI leadership, Quality Management, DevOps or Platform Engineering, Security, Data or AI, DBA, and Architecture.
- Base squad roles should support the local team and escalate when a decision belongs to a central specialist function.
- Cross-team learning should flow through Communities of Practice or Centers of Excellence, not only through top-down standards.

## Specialization Rules
- Shared template updates belong in this workspace.
- Team-local practices, product-area rules, and component-specific knowledge should be added in dedicated workspace files under `.github/` when that material exists.
- Prefer one focused customization per concern: workspace instructions for universal rules, custom agents for roles, skills for repeatable workflows, prompts for single tasks.

## Key Files
- Project overview: [README.md](README.md)
- Architecture proposal: [docs/architecture.md](docs/architecture.md)
- Backlog: [docs/backlog.md](docs/backlog.md)
- Decision log: [docs/decision-log.md](docs/decision-log.md)
- Documentation plan: [docs/documentation-strategy.md](docs/documentation-strategy.md)
- Git strategy: [docs/git-strategy.md](docs/git-strategy.md)
- Squad orchestration: [.github/agents/scrum-squad-orchestrator.agent.md](.github/agents/scrum-squad-orchestrator.agent.md)
- Team specialization: [.github/instructions/team-specialization.instructions.md](.github/instructions/team-specialization.instructions.md)
- Ceremony support skill: [.github/skills/scrum-ceremony-support/SKILL.md](.github/skills/scrum-ceremony-support/SKILL.md)
- Role catalog: [.github/agents/product-owner.agent.md](.github/agents/product-owner.agent.md)
- Role catalog: [.github/agents/scrum-master.agent.md](.github/agents/scrum-master.agent.md)
- Role catalog: [.github/agents/quality-expert.agent.md](.github/agents/quality-expert.agent.md)
- Role catalog: [.github/agents/business-analyst.agent.md](.github/agents/business-analyst.agent.md)
- Role catalog: [.github/agents/ux-expert.agent.md](.github/agents/ux-expert.agent.md)
- Role catalog: [.github/agents/frontend-engineer.agent.md](.github/agents/frontend-engineer.agent.md)
- Role catalog: [.github/agents/backend-engineer.agent.md](.github/agents/backend-engineer.agent.md)

## Maintenance
- Keep this file short and workspace-wide.
- Add links to real docs as the repository grows.
- Update role boundaries before adding detailed process content to avoid overlap across agents.