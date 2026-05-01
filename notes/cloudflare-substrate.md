# Cloudflare as Agent Swarm Substrate

Joel wants to highlight Cloudflare’s awesome shit, not as a sponsor reel, but as a coherent substrate for agent systems.

## Core angle

Cloudflare’s primitives are starting to look like the missing runtime layer for practical agent swarms:

- close to users and external systems
- cheap enough for many small agents
- durable enough for workflows and state
- globally reachable by default
- increasingly AI-native without forcing everything into a single provider

## Primitives to map

| Cloudflare primitive | Agent-system role |
| --- | --- |
| Workers | agent handlers, protocol adapters, webhook surfaces |
| Durable Objects | per-agent or per-room state, coordination locks, inboxes |
| Workflows | durable multi-step agent tasks |
| Dynamic Workflows | runtime-defined task graphs / agent-composed workflows |
| Queues | async handoff and backpressure |
| D1 | relational state / audit tables |
| R2 | raw blobs, transcripts, generated files, model outputs |
| Artifacts | versioned file trees, Git-compatible agent workspaces, branch/fork/diff/merge handoff |
| KV | config, caches, lightweight lookup |
| Vectorize | memory / retrieval |
| AI Gateway | model routing, metering, governance |
| Browser Rendering | web-using agents |
| Realtime / Calls / WebRTC surfaces | human-agent and agent-agent live coordination |

## Dynamic Workflows source

https://blog.cloudflare.com/dynamic-workflows/?utm_campaign=cf_blog&utm_content=20260501&utm_medium=organic_social&utm_source=twitter

Initial read hypothesis: Dynamic Workflows matters because agent systems rarely know the whole DAG upfront. If agents can define or extend workflow shape at runtime without abandoning durability, that’s a major step toward swarms that are less toy-demo and more operational fabric.

## Artifacts source

https://developers.cloudflare.com/artifacts/

Artifacts stores versioned file trees behind a Git-compatible interface. That matters for agent swarms because file trees are the native shape of software work. One repo per agent, user, branch, or task gives a clean isolation boundary; Git clients and Git-aware tools already know how to diff, merge, fork, and hand off that work.

This is stronger than treating generated output as blobs in R2. R2 is storage. Artifacts is a collaboration surface.

Potential talk line:

> Agents do not just need memory. They need workspaces they can fork, mutate, diff, and merge.

## Narrative caution

Do not make this “Cloudflare has products.” Boring.

Make it: “These primitives collapse the distance between distributed systems architecture and agent architecture.”

The audience should leave seeing Workers/DO/Workflows/Queues as agent coordination nouns.
