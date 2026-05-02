# Agents of Catan Demo Spine

Source: Joel voice note, 2026-05-01.

## Raw idea

The ATProto Agent Swarms demonstration starts with an agent swarm playing a version of Settlers of Catan called **Agents of Catan**.

That evolves into **game cartridges**: different playable worlds/rule systems agents can inhabit. One cartridge is Dungeons & Dragons, where agents play through a D&D-style scenario.

A key mechanic: **permadeath**. If an agent dies in the game, the agent is deleted.

This is interesting because it makes agent lifecycle concrete. Agents are not infinite chat sessions. They have identity, state, capabilities, consequences, and termination conditions.

## Expansion path

The question is how this translates from game worlds into software development and real work:

- Agents of Catan / D&D show coordination, role, resources, conflict, memory, and consequences.
- Software work has the same structure: units of work, claims, artifacts, review, handoff, failure, and retry.
- OpenClaw-style systems are the “real work” cartridge: the same swarm runtime, pointed at code, docs, support, research, or operations.

## Core metaphor

Game cartridges are domain modules for agent swarms.

Each cartridge defines:

- rules of play
- valid actions
- resources
- world state
- success conditions
- failure modes
- consequences
- lifecycle rules

In games, consequences are things like permadeath. In software work, consequences are failed tests, rejected PRs, stale branches, revoked credentials, degraded trust, or task reassignment.

## Why this works for the talk

The game makes the distributed-system concepts visible before the audience has to care about infrastructure.

Then the reveal:

> A game cartridge and a software-work cartridge need the same substrate: identity, state, tools, messages, artifacts, workflows, and review loops.

## Building blocks Joel wants connected

- Pi as an agent harness
- ATProto for identity / records / network substrate
- Cloudflare primitives as runtime substrate
- Artifacts as versioned agent workspaces
- Workflows / Dynamic Workflows for durable task progression
- Durable Objects for per-agent or per-world state
- Queues for async work handoff
- OpenClaw-style systems as the practical work surface

## Narrative seed

Using these building blocks, we can construct bespoke agent systems for the situation instead of pretending one generic chatbot workflow fits every problem.

The learning process matters: you play through the domain, discover the actual rules, then encode the rules into the cartridge/runtime until the system can produce the outcomes you want.

## Possible talk move

1. Show Agents of Catan.
2. Add D&D cartridge.
3. Introduce permadeath to make lifecycle/consequence visceral.
4. Ask: what is the “software development” cartridge?
5. Map game mechanics to real work mechanics.
6. Reveal the substrate: ATProto + Cloudflare + agent harness + artifacts.
