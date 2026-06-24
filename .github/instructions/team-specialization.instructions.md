---
name: "Team AI Specialization"
description: "Use when instantiating the shared AI Scrum Squad template inside a real Scrum team, or when adding team-specific context, product-area knowledge, local ceremonies, component boundaries, business rules, or delivery conventions. Covers how to specialize without polluting the shared template."
---
# Team AI Specialization Guidelines

- Use this instruction only for team-local specialization of the shared AI Scrum Squad template.
- Keep reusable role definitions and shared Tagetik-wide guidance in [AGENTS.md](../../AGENTS.md) and the role agents under [.github/agents](../agents/product-owner.agent.md).
- Add local product context in new focused files under `.github/` instead of editing the shared template unless the rule truly applies to every future team.

## What Belongs To Team Specialization

- Product-area scope, bounded context, owned modules, and interfaces handled by the physical team.
- Team-specific business vocabulary, rules, workflows, and recurring edge cases.
- Local ceremony variants, stakeholder map, decision cadence, and escalation paths.
- Development conventions tied to the team's codebase, architecture, or release process.
- Links to real documentation sources that the instantiated team maintains.

## What Must Stay Out Of The Shared Template

- Rules that are valid only for one product area or one codebase.
- Temporary sprint decisions, one-off incidents, or unstable local workarounds.
- Deep product details copied from other documentation when a link is enough.
- Role-specific procedures that belong in a focused instruction, prompt, or skill instead.

## Specialization Workflow

1. Identify what is truly team-local versus reusable across all teams.
2. Create one focused customization per concern: instructions for always-relevant team rules, prompts for repeatable single tasks, skills for multi-step workflows.
3. Link to source documentation instead of embedding large process or domain text.
4. Record assumptions explicitly when source material is incomplete.
5. Revisit local customizations when team scope or architecture changes.

## Recommended Specialization Artifacts

- A team-context instruction for product area, ownership boundaries, and domain vocabulary.
- A ceremony support skill if the team wants standardized outputs for refinement, planning, daily, or retro.
- Focused prompts for recurring tasks such as story drafting, defect triage, or release notes.
- Additional role instructions only when one team needs behavior that the shared role agent should not own globally.

## Quality Bar

- Every local customization should improve signal, not duplicate obvious context.
- Prefer concise constraints, explicit ownership, and direct links to maintained documentation.
- If a rule is likely to matter for multiple teams, propose moving it back into the shared template after validation.