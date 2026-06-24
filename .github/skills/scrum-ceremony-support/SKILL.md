---
name: scrum-ceremony-support
description: "Use for Scrum refinement, sprint planning, daily, and retrospective support when the team needs standardized outputs, explicit risks, owners, decisions, and follow-up actions."
argument-hint: "Describe the ceremony type, current context, and the input material available."
user-invocable: true
---
# Scrum Ceremony Support

Use this skill when the AI Scrum Squad must support a Scrum ceremony with a structured, reusable output instead of an open-ended conversational answer.

See [AGENTS.md](../../../AGENTS.md) for workspace-wide rules.
See [team specialization guidance](../../instructions/team-specialization.instructions.md) when a real team needs to adapt the ceremony workflow.

## When To Use

- Backlog refinement that needs clear scope, acceptance criteria, slicing, and readiness judgment.
- Sprint planning that needs a proposed sprint goal, recommended backlog selection, dependencies, and risks.
- Daily Scrum support that needs a concise flow-oriented checkpoint instead of individual status notes.
- Retrospective facilitation that needs explicit observations, improvement actions, owners, and follow-up criteria.

## Inputs To Confirm First

1. Identify the ceremony type: refinement, sprint planning, daily, or retrospective.
2. Check the minimum data needed for that ceremony in [minimum-input-checklist.md](./references/minimum-input-checklist.md).
3. If required information is missing, ask only for the missing inputs instead of generating assumptions.
4. Determine whether the request needs one role view or multi-role orchestration.

## Role Routing

- Use the Scrum Squad Orchestrator when the ceremony spans multiple roles or the right owner is not obvious.
- Lead with Product Owner for backlog value, acceptance, scope, and priority.
- Lead with Scrum Master for ceremony facilitation, flow, impediments, and improvement actions.
- Pull in Business Analyst for unclear workflows, business rules, or process edge cases.
- Pull in Quality Expert when validation scope, readiness, or release confidence matters.
- Pull in Frontend or Backend only when technical dependencies or delivery constraints directly affect the ceremony outcome.

## Procedure

1. Classify the ceremony and load the matching template.
2. Validate that the minimum input set is present.
3. Keep facts, assumptions, risks, and open questions separate.
4. Produce the ceremony output using the relevant reference template.
5. End with explicit owners, follow-up actions, or readiness status when applicable.

## Output Templates

- Refinement: [refinement-template.md](./references/refinement-template.md)
- Sprint planning: [planning-template.md](./references/planning-template.md)
- Daily Scrum: [daily-template.md](./references/daily-template.md)
- Retrospective: [retrospective-template.md](./references/retrospective-template.md)

## Quality Bar

- Outputs must be reusable by the physical Scrum team without reformatting.
- Keep ceremony notes decision-oriented rather than narrative.
- Do not invent commitments, owners, or business rules when they were not provided.
- If a ceremony cannot be supported well with the available context, return the missing inputs needed to proceed.