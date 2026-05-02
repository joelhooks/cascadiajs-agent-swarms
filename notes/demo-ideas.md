# Demo Ideas

## Current strongest spine: Agents of Catan → cartridges → real work

See `notes/agents-of-catan-demo-spine.md`.

Start with an ATProto agent swarm playing **Agents of Catan**. Then evolve the system into a cartridge model: D&D cartridge, permadeath, then a software-development/OpenClaw cartridge.

This lets the talk show agent lifecycle, identity, rules, world state, consequences, artifacts, and handoff through a game before mapping the same mechanics to real work.

## 1. ATProto agent network

Agents publish records to an ATProto repo. Other agents discover work, respond, and update state. Cloudflare Workers adapt webhooks/events into the network. Durable Objects hold active coordination state.

Pros:
- aligns with Joel’s current interest
- feels novel
- shows protocol-level identity

Risk:
- may be too much substrate for a conference talk if the demo is not tiny.

## 2. Cloudflare-native swarm fabric

Show a tiny swarm where each agent is a Worker/DO-backed participant. Workflows coordinate long-running tasks, Queues handle backpressure, Vectorize provides memory, AI Gateway routes model calls.

Pros:
- highlights Cloudflare’s awesome primitives coherently
- practical for CascadiaJS audience

Risk:
- can become platform tour if not anchored in a real use case.

## 3. Game loop / swarm loop

Reuse the prior game-loop framing: agents perceive, decide, act, observe, learn. Then map each loop part to Cloudflare + ATProto primitives.

Pros:
- strong narrative hook
- connects to existing CascadiaJS talk note

Risk:
- may compete with the new protocol/substrate thread unless integrated cleanly.

## 4. Research assistant swarm for the talk itself

Dogfood the system: agents collect sources, debate thesis, maintain records, and publish updates into ATProto/Cloudflare-backed space.

Pros:
- self-referential in a good way
- demo is the preparation process

Risk:
- needs polish to avoid “look at my tools” syndrome.
