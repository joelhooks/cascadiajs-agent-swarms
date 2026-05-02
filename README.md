# CascadiaJS 2026 — Agent Swarms

Mini repo for shaping Joel's CascadiaJS June talk about agent swarms, AT Protocol agent networks, Cloudflare primitives, agent SDKs, Flue, Project Think, Koko, and swarm-tools.

## Working thesis

Play is how you learn the affordances of a new medium before anyone has named the patterns.

This talk uses agent swarms, game cartridges, ATProto, Cloudflare primitives, and OpenClaw-style work systems to show how playful exploration can produce useful agentic structures.

Agent swarms stop being sci-fi when agents have durable identity, shared protocols, addressable workspaces, and cheap edge coordination primitives.

Cloudflare is a major part of the story: Workers, Durable Objects, Workflows, Dynamic Workflows, Queues, Artifacts, D1/R2/KV, Browser Rendering, AI Gateway, Vectorize, and Realtime start to look like a practical substrate for distributed agent systems rather than a pile of disconnected platform features.

## Current source links

- X thread / signal: https://x.com/irvinebroque/status/2050282756492668941?s=46&t=uRyCCtjktRI5TQXbSKdTLw
- swarm-tools: https://github.com/joelhooks/swarm-tools
- Koko: https://github.com/joelhooks/koko
- ATProto Agent Network: https://github.com/joelhooks/atproto-agent-network
- Flue: https://github.com/withastro/flue
- Cloudflare Dynamic Workflows: https://blog.cloudflare.com/dynamic-workflows/?utm_campaign=cf_blog&utm_content=20260501&utm_medium=organic_social&utm_source=twitter
- Cloudflare Artifacts: https://developers.cloudflare.com/artifacts/
- Skills / grill-with-docs: https://github.com/mattpocock/skills

## Working narrative questions

1. What does “swarm” mean when you remove the Twitter-demo bullshit?
2. What does AT Protocol give agents that Slack/Discord/Redis queues don’t?
3. Where do Cloudflare primitives make this boring enough to ship?
4. What is the smallest demo that makes the architecture feel inevitable?
5. What should the audience believe after the talk that they didn’t believe before?

## Files

- `CONTEXT.md` — glossary and domain language
- `notes/source-map.md` — source links and what each contributes
- `notes/narrative-seeds.md` — rough talk themes
- `notes/cloudflare-substrate.md` — Cloudflare primitives to highlight
- `notes/demo-ideas.md` — candidate demos
- `notes/agents-of-catan-demo-spine.md` — current strongest demo/narrative spine
- `notes/humans-in-the-swarm.md` — human roles in multiplayer agentic systems
- `notes/play-as-method.md` — current highest-level thesis: play as useful exploration
- `notes/play-pattern-language.md` — mapping game/play patterns to practical agentic work patterns
- `docs/adr/` — decisions once they harden

## Immediate next moves

- Pull source material into `notes/source-map.md`.
- Define the talk’s enemy: what bad mental model are we replacing?
- Choose one demo spine: ATProto network, game/swarm loop, or Cloudflare-native agent fabric.
- Use `grill-with-docs` to interrogate the thesis once the first rough outline exists.
