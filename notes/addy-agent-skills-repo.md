# Addy Osmani: agent-skills repo autopsy

Source: https://github.com/addyosmani/agent-skills
Local autopsy: `/Users/joel/.repo-autopsy/addyosmani/agent-skills`

## What it is

Production-grade engineering skills for AI coding agents. The repo packages senior-engineer workflows, quality gates, checklists, slash commands, and personas into portable Markdown skills.

Scale at inspection:

- 53 files
- ~10K lines
- 20 skills
- 7 lifecycle slash commands
- 3 specialist personas
- reference checklists
- hooks for session start and cache/ignore behavior

## Lifecycle model

The README centers a lifecycle:

```text
DEFINE → PLAN → BUILD → VERIFY → REVIEW → SHIP
/spec   /plan   /build   /test    /review   /ship
```

Talk relevance:

This is a concrete “factory operating manual.” It decomposes agentic work into named stages with skills and quality gates.

## Skill inventory

Define:

- idea-refine
- spec-driven-development

Plan:

- planning-and-task-breakdown

Build:

- incremental-implementation
- test-driven-development
- context-engineering
- source-driven-development
- frontend-ui-engineering
- api-and-interface-design

Verify:

- browser-testing-with-devtools
- debugging-and-error-recovery

Review:

- code-review-and-quality
- code-simplification
- security-and-hardening
- performance-optimization

Ship:

- git-workflow-and-versioning
- ci-cd-and-automation
- deprecation-and-migration
- documentation-and-adrs
- shipping-and-launch

Meta:

- using-agent-skills

## Personas

- `code-reviewer` — senior staff engineer lens
- `test-engineer` — QA/test strategy lens
- `security-auditor` — security/threat model lens

Talk mapping:

These are not just personalities. They are role cards. The repo is a practical example of a party/class system for engineering work.

## Orchestration patterns

The most relevant file is `references/orchestration-patterns.md`.

Governing rule:

> the user (or a slash command) is the orchestrator. Personas do not invoke other personas.

Endorsed patterns:

1. Direct invocation
2. Single-persona slash command
3. Parallel fan-out with merge
4. Sequential pipeline as user-driven slash commands
5. Research isolation

Important distinctions:

- `/ship` is a verdict pattern: fan out to reviewer/security/tester, merge reports, decide go/no-go.
- Agent Teams are for investigations where agents can challenge each other and rule out competing hypotheses.
- Research isolation preserves the main context by letting a subagent eat large input and return only a digest.

Talk relevance:

This is concrete evidence for “agent swarms need topology.” Many agents is not automatically better. The structure depends on the kind of work:

- verdict
- investigation
- pipeline
- isolated research
- direct task

## Anti-patterns implied

- personas invoking personas recursively
- deep agent trees
- orchestrating when direct invocation is enough
- slash commands whose only job is deciding which persona to call
- parallelism where tasks have ordering/shared-state dependencies

Talk mapping:

This is the “party composition” lesson. More characters is not the same as a better party. The dungeon/mission determines party shape.

## Why it matters for the talk

This repo is a working example of agentic structure as a reusable artifact:

- skills = moves / abilities
- commands = rituals / mission phases
- personas = roles/classes
- checklists = rulebooks
- hooks = mechanics with teeth
- orchestration patterns = party topology

It supports the cartridge thesis:

> A cartridge packages a domain’s rules, roles, tools, workflows, checks, and handoff patterns into something agents and humans can play/work inside.

## Useful phrases

- “Skills are moves; personas are classes; slash commands are rituals.”
- “Orchestration topology is a design choice, not a vibe.”
- “A party is only useful if the mission actually needs multiple roles.”
- “Parallel fan-out is a verdict pattern. Agent teams are an investigation pattern.”
- “This is what a cartridge starts to look like when the domain is software engineering.”

## Follow-up

Potentially compare `agent-skills` to joelclaw skills:

- Addy's skills are lifecycle/productivity packaged for general agents.
- joelclaw skills are operational memory for one living system.
- CascadiaJS cartridge might need both: general moves + local lore.
