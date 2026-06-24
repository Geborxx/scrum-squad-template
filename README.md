# AI Scrum Squad

This workspace hosts the shared template for an AI Scrum Squad aligned to a physical Scrum team.

The goal is to define a reusable multi-agent operating model for product delivery in a Tagetik context, then let each real Scrum team instantiate and specialize its own local AI Squad.

## Current Scope

- Shared role model for Product Owner, Scrum Master, Quality Expert, Business Analyst, UX Expert, Frontend Engineer, and Backend Engineer.
- An orchestrator that routes requests to the right role or combination of roles.
- A reusable ceremony support skill for refinement, sprint planning, daily, and retrospective outputs.
- A specialization model for turning the shared template into a team-local AI Squad.

## Documentation

- Architecture proposal: [docs/architecture.md](docs/architecture.md)
- Backlog: [docs/backlog.md](docs/backlog.md)
- Decision log: [docs/decision-log.md](docs/decision-log.md)
- Documentation strategy: [docs/documentation-strategy.md](docs/documentation-strategy.md)
- Git strategy: [docs/git-strategy.md](docs/git-strategy.md)

## Core Workspace Files

- Shared workspace guidance: [AGENTS.md](AGENTS.md)
- Orchestrator agent: [.github/agents/scrum-squad-orchestrator.agent.md](.github/agents/scrum-squad-orchestrator.agent.md)
- Team specialization guidance: [.github/instructions/team-specialization.instructions.md](.github/instructions/team-specialization.instructions.md)
- Ceremony support skill: [.github/skills/scrum-ceremony-support/SKILL.md](.github/skills/scrum-ceremony-support/SKILL.md)

## Current Status

- The workspace contains customization and documentation assets only.
- It does not yet include runnable application code, team-local product knowledge, or Confluence integration.
- The folder currently lives inside a larger Git repository; repository strategy for this subproject must be chosen deliberately before adding nested version control.

## Next Evolution

- Add a first real team instance with local context, owned scope, and working agreements.
- Model cross-team communities of practice for federated learning across AI Squads.
- Model the central capability layer and its specialist escalation boundaries.
- Add an explicit structure for Communities of Practice and Centers of Excellence.
- Connect documentation and workflow artifacts to Jira and Confluence when the integration path is ready.