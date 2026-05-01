# Context — CascadiaJS Agent Swarms Talk

## Purpose

This repo is a thinking space for the CascadiaJS 2026 talk. It is not an implementation repo yet. Its job is to collect sources, sharpen language, define the narrative, and eventually host demo scaffolding.

## Glossary

### Agent swarm

A group of agents coordinating around shared work. The important part is not “many agents”; it is coordination under partial knowledge, bounded autonomy, and observable handoff.

### Agent network

A protocol-level substrate where agents can discover each other, publish state, exchange work, and maintain identity across tools. AT Protocol is the current candidate substrate.

### Durable identity

A stable identity for an agent that survives process restarts, tool changes, and host boundaries. Without durable identity, “swarm” is just parallel subprocesses in a trench coat.

### Coordination primitive

A boring, reliable mechanism for agent handoff: queue, workflow, durable object, repo record, event, mailbox, or protocol record.

### Cloudflare substrate

The set of Cloudflare primitives that can host agent coordination close to the edge: Workers, Durable Objects, Workflows, Queues, D1/R2/KV, Browser Rendering, AI Gateway, Vectorize, Realtime, and Dynamic Workflows.

### ATProto agent network

A candidate architecture where agent identity, records, and communication live on AT Protocol, making agents portable and inspectable instead of trapped inside one chat app or one vendor’s dashboard.

### Flue

Astro’s repo/project that may contribute ideas about content/workflow glue. Needs source review before claiming more.

### Project Think

Placeholder term for the broader thinking/tooling cluster Joel wants included. Needs concrete source links and definition.
