# Addy Osmani: Long-running Agents + Agent Harness Engineering

Sources:

- https://addyosmani.com/blog/long-running-agents/
- https://addyosmani.com/blog/agent-harness-engineering/

## Why this matters for CascadiaJS

Addy's two posts are unusually aligned with the talk's current thesis. They supply mainstream vocabulary for what the CascadiaJS talk is circling:

> agents stop being chat windows and start becoming durable, observable, multiplayer work systems.

The posts are useful as external validation, but the talk should not become a summary of them. Use them to sharpen terms.

## Long-running agents: useful distinctions

Addy splits “long-running” into three different meanings:

1. **Long-horizon reasoning** — the model can plan and execute across many dependent steps.
2. **Long-running execution** — the agent process runs for hours/days across many model calls.
3. **Persistent agency** — the agent has identity and memory beyond one task.

For this talk, the strongest link is #2 and #3. The game/cartridge frame is about durable execution plus persistent identity inside a designed rulespace.

## Three walls

Every long-running agent hits:

- **Finite context** — context rot and hard limits.
- **No persistent state** — new sessions wake up blank unless state lives outside the model.
- **No self-verification** — models say “done” too early and grade themselves too generously.

Talk mapping:

- Finite context → why “session” is not enough.
- Persistent state → why agents need workspaces/inventory/logs.
- Self-verification → why swarms need judges, reviewers, tests, and consequence.

## The important architecture convergence

Addy's read: Google, Anthropic, and Cursor are converging on the same shape:

- separate model loop from execution sandbox from durable session log
- split planning from generation from evaluation
- bake in compaction, hooks, context resets
- expose memory as a managed service

This maps directly onto the talk's phrase:

> multiplayer agentic distributed systems for accomplishing units of work asynchronously.

A swarm is not “many LLMs talking.” It is a system with roles, logs, sandboxes, verification, identity, memory, and handoff.

## Anthropic frame

Key phrase from Addy summarizing Anthropic:

> Brain / Hands / Session

- Brain: model + loop
- Hands: sandbox/tool execution
- Session: append-only event log

Talk mapping:

- Brain = player/character intent
- Hands = moves/actions in the rulespace
- Session = campaign log / continuity

The session-as-event-log idea is load-bearing. It makes an agent recoverable, auditable, and handoff-able. Without it, “long-running” is just a process that might still be alive.

## Cursor frame

Cursor landed on:

- Planners
- Workers
- Judges

Talk mapping:

- Planner = quest-giver / party leader
- Worker = character/class specialist
- Judge = referee / test harness / DM consequence

This is close to games: roles exist because the system needs different failure modes separated.

## Google frame

Google productizes the same stack as named services:

- Agent Runtime
- Agent Sessions
- Agent Memory Bank
- Agent Sandbox
- Agent Identity
- Agent Gateway
- Agent Observability
- Agent Simulation

Talk mapping:

Cloudflare/ATProto are not the only possible substrate. Google is enterprise-packaging the same primitives. That helps avoid making the Cascadia talk sound like Cloudflare fanfic. The underlying structure matters more than vendor.

## Five production patterns

From Addy + Shubham Saboo:

1. Checkpoint-and-resume
2. Delegated approval / human-in-the-loop
3. Memory-layered context
4. Ambient processing
5. Fleet orchestration

Talk mapping:

- checkpoint = save point
- approval = DM/player choice/review gate
- layered memory = inventory + lore + campaign state
- ambient processing = NPC/background simulation
- fleet orchestration = party / raid / guild

This strengthens the game-pattern-language angle.

## Harness engineering: useful thesis

> Agent = Model + Harness. If you’re not the model, you’re the harness.

Harness includes:

- prompts / AGENTS.md / skills
- tools / MCP
- filesystem / sandbox / browser
- orchestration / subagents / model routing
- hooks / middleware / compaction
- observability / logs / traces / cost

Talk mapping:

A cartridge is a domain-specific harness. It defines the game/work rules, available actions, tools, resources, memory, and win conditions.

## Harness ratchet

Addy’s strongest operational rule:

> Every mistake becomes a rule.

The harness gets tighter every time the agent slips. This is exactly how game rules evolve too: exploit found → patch rule → new strategy emerges.

Talk use:

This explains why “play” is not frivolous. Play stress-tests the rules. A good agentic structure emerges from observing failures and ratcheting the harness.

## Hooks as enforcement

Hooks turn “I told the agent” into “the system enforces.”

Examples:

- block destructive commands
- run typecheck/lint/tests
- require approval before publish/push
- inject verbose failure, stay silent on success

Talk mapping:

Hooks are rules with teeth. In game terms, they are mechanics, not lore.

## AGENTS.md discipline

Addy repeats the pilot-checklist point:

- keep it short
- every line earned by a real failure
- ratchet, don’t brainstorm

This matches the talk prep resource doctrine too: do not turn the repo into a museum or the prompt into a constitution.

## Strongest new phrasing for the talk

Potential lines:

- “A swarm is not many chatbots. It is a harness with roles.”
- “A cartridge is a domain-specific harness: rules, tools, state, win conditions, and failure modes.”
- “The model is the player. The harness is the game.”
- “Play is how you discover which harness rules need to exist.”
- “Hooks are mechanics, not suggestions.”
- “The session log is the campaign log.”
- “Long-running agents need save points, inventories, roles, and referees. Games already gave us the language.”

## Caution

Do not let Addy’s terms flatten Joel’s frame into generic enterprise agent architecture.

The unique angle is not “long-running agents exist.” The unique angle is:

> Games are compressed laboratories for discovering the coordination patterns long-running agent swarms need.

Addy's posts provide engineering vocabulary for the back half of that claim.
