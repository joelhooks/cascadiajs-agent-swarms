# Concept Map: Agentic Work Systems

Purpose: map Joel's emerging talk concepts against Karpathy, Addy Osmani, Cloudflare/Sunil, Cursor/Anthropic/Google, and Addy's `agent-skills` repo without flattening everything into one person's vocabulary.

## Top-level taxonomy

```text
Agentic Work System
├── Substrate
│   ├── Runtime
│   ├── Sandbox
│   ├── Workspace
│   ├── Identity
│   └── Event/session log
├── Harness
│   ├── Prompt/rules
│   ├── Tools/skills
│   ├── Hooks/enforcement
│   ├── Context policy
│   └── Verification loop
├── Knowledge Base
│   ├── Raw sources
│   ├── Compiled wiki
│   ├── Indexes/summaries
│   ├── Derived artifacts
│   └── Health checks
├── Orchestration
│   ├── Planner
│   ├── Worker
│   ├── Judge/evaluator
│   ├── Human actor
│   └── Handoff protocol
├── Mission
│   ├── Goal/spec
│   ├── Constraints
│   ├── Resources
│   ├── Done condition
│   └── Consequence
└── Cartridge
    ├── Domain model
    ├── Rules
    ├── Roles/classes
    ├── Tools/moves
    ├── State/inventory
    ├── Missions
    └── Feedback loops
```

## Crosswalk

| Joel term | Karpathy | Addy: harness | Addy: long-running | Addy: factory | agent-skills | Cloudflare/Sunil | Game pattern |
|---|---|---|---|---|---|---|---|
| Cartridge | LLM-maintained wiki + tools | domain-specific harness | packaged durable agent workflow | factory cell / production line | skill pack + commands + personas | Workers + Artifacts + bindings | game cartridge / module |
| Mission | query/output request | task + done condition | feature list / checkpoint unit | work order/spec | `/spec` → `/plan` task | Dynamic Workflow | quest |
| Party | N/A; implicit agents over wiki | subagents | planners/workers/judges | fleet of agents | personas | sub-agents / Durable Objects | adventuring party |
| Human actor | steers compiler, views Obsidian | harness designer/operator | approval gate / reviewer | factory designer/reviewer | user orchestrator | operator/user | DM / player / patron |
| Inventory | sources, wiki, outputs | tools, files, context | memory, session, artifacts | toolbelt/docs/tests | skills/checklists | bindings, R2, D1, Artifacts | inventory/resources |
| Session log | wiki history / outputs filed back | observability/traces | append-only session | logs/previews/PRs | progress artifacts | Durable Object logs/traces | campaign log |
| Rules with teeth | health checks | hooks | judges/evaluators | quality control | quality gates | Workers constraints/policies | mechanics |
| Consequence | lint/health findings | failed hook/test | restart/checkpoint/fail | rejected output | go/no-go ship | deployment/runtime failure | permadeath / failure state |
| Knowledge substrate | raw/ + compiled wiki | context injection | memory-layered context | docs as training material | references/checklists | docs + Artifacts | lore/world state |

## Concept clusters

### 1. Cartridge

Definition candidate:

> A cartridge is a domain-specific agentic work system: a packaged set of rules, roles, tools, state, missions, and feedback loops that humans and agents can operate inside.

Related terms:

- Addy harness
- Addy factory cell
- Karpathy compiled knowledge base
- agent-skills plugin/skill pack
- Cloudflare Artifacts + Workers substrate
- tabletop RPG module / game cartridge

Distinction:

- A harness is mostly execution scaffolding.
- A knowledge base is mostly domain memory.
- A factory is mostly production flow.
- A cartridge combines execution, memory, production, and playability around a domain.

### 2. Harness

Definition candidate:

> A harness is everything around the model that turns it into an agent: rules, tools, context, execution, feedback, persistence, and observability.

Source alignment:

- Addy: `Agent = Model + Harness`
- Anthropic: brain/hands/session
- joelclaw: skills + CLI + Inngest + gateway + memory + OTEL
- agent-skills: skills + commands + personas + hooks

Talk role:

Harness is the technical bridge between vague “agents” and concrete systems.

### 3. Substrate

Definition candidate:

> Substrate is the runtime material the harness uses: compute, sandbox, storage, identity, logs, and network.

Source alignment:

- Cloudflare: Workers, Dynamic Workers, Durable Objects, Artifacts, bindings
- Google: Agent Runtime, Sessions, Memory Bank, Sandbox, Identity
- Anthropic: Hands + Session
- Cursor: cloud worktrees/background agents

Talk role:

Substrate explains why this is becoming possible now. Do not let it become the whole talk.

### 4. Knowledge base

Definition candidate:

> A knowledge base is compiled domain memory: raw sources transformed into linked, queryable, maintainable artifacts.

Source alignment:

- Karpathy: raw/ → LLM-compiled markdown wiki → Q&A → outputs filed back → health checks
- Cascadia repo: source map → notes → concept maps → outline → spoken talk
- joelclaw: Vault + skills + recall + docs

Talk role:

Knowledge bases are cartridges for thinking. They become multiplayer when they gain roles, tools, and handoff protocols.

### 5. Orchestration topology

Definition candidate:

> Orchestration topology is the shape of collaboration among agents and humans for a unit of work.

Source alignment:

- Cursor: planners/workers/judges
- agent-skills: direct invocation, slash command, parallel fan-out, sequential pipeline, research isolation
- Anthropic: initializer/coder/evaluator
- joelclaw: gateway/worker/loop/reviewer

Talk role:

This prevents “swarm” from meaning “more agents.” A swarm has topology. The mission determines the topology.

### 6. Mission

Definition candidate:

> A mission is a bounded unit of work with goal, constraints, resources, done condition, and consequence.

Source alignment:

- Addy factory: spec/work order
- Addy long-running: checkpoint unit
- agent-skills: task with acceptance criteria
- games: quest

Talk role:

Missions are how we stop agents from hallucinating direction. A vague prompt is not a mission.

### 7. Rules / mechanics / hooks

Definition candidate:

> Rules describe what should happen. Mechanics enforce what can happen.

Source alignment:

- Addy harness: hooks
- agent-skills: quality gates/checklists
- joelclaw: gateway relay gates, deploy checks, skill-loading requirements
- games: mechanics

Talk role:

This is where play becomes serious. The system learns by turning failures into rules with teeth.

## Tensions / useful disagreements

### Factory vs game

Factory frame:

- good for production, scale, QA, throughput
- bad for exploration, motivation, weirdness, human participation

Game frame:

- good for roles, rules, exploration, consequence, motivation
- risks sounding unserious unless tied to work systems

Synthesis:

> The factory explains leverage. The game explains why people and agents can coordinate inside the system. The cartridge packages both.

### Knowledge base vs harness

Karpathy's KB is about compiling knowledge. Addy's harness is about executing work.

Synthesis:

> A knowledge base becomes a cartridge when agents can act on it through tools, missions, rules, and feedback loops.

### Swarm vs workflow

Workflow implies predefined sequence. Swarm implies adaptive multi-actor coordination.

Synthesis:

> A workflow is a path through a cartridge. A swarm is the set of actors that can choose and execute paths.

### Human-in-the-loop vs human-in-the-system

Human-in-the-loop sounds like an approval interrupt. Joel's frame is broader: human as DM, party leader, patron, player, reviewer, operator.

Synthesis:

> Humans are not outside the swarm. They occupy high-context roles inside it.

## Candidate ontology

```text
Actor
├── HumanActor
│   ├── Operator
│   ├── Reviewer
│   ├── Patron
│   ├── Player
│   └── DungeonMaster
└── AgentActor
    ├── Planner
    ├── Worker
    ├── Judge
    ├── Researcher
    └── Toolsmith

Artifact
├── Source
├── Note
├── Spec
├── Plan
├── Code
├── Test
├── Trace
├── Summary
└── DecisionRecord

Capability
├── Skill
├── Tool
├── Hook
├── Binding
├── Memory
└── Sandbox

WorkUnit
├── Mission
├── Task
├── Checkpoint
├── Review
└── Handoff

SystemBoundary
├── Cartridge
├── Harness
├── Substrate
├── KnowledgeBase
└── Workflow
```

## Talk-safe distilled map

If this needs to fit on one slide:

```text
Karpathy: compile knowledge
Addy: build the harness/factory
Cursor/Anthropic/Google: split roles, sandbox, session, memory
Cloudflare/ATProto: provide substrate and identity
Joel: make it playable as a cartridge
```

Or shorter:

```text
Knowledge → Harness → Substrate → Orchestration → Cartridge
```

## What to stop doing in notes

- Stop saying “strong evidence” and “useful validation” unless naming the exact concept it validates.
- Prefer crosswalk tables, ontologies, term conflicts, and merge/split decisions.
- For every source, extract:
  - terms
  - primitives
  - roles
  - workflows
  - failure modes
  - what it clarifies in Joel's frame
  - what it conflicts with
