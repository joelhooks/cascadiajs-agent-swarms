# Narrative Seeds

## Possible talk enemy

Bad model: “agent swarms are just a bunch of chatbots calling tools in parallel.”

Replacement model: “agent swarms are distributed systems with identity, memory, protocols, work queues, and durable coordination.”

## Possible thesis

The interesting future of agent swarms is not smarter prompts. It is boring distributed systems primitives becoming agent-native.

## Cloudflare angle

Cloudflare’s platform is becoming a credible agent substrate because it already has the primitives swarms need:

- code everywhere: Workers
- durable per-entity state: Durable Objects
- task durability: Workflows / Dynamic Workflows
- backpressure: Queues
- memory/artifacts: Vectorize, R2, D1, KV
- model routing/governance: AI Gateway
- web-use: Browser Rendering

## ATProto angle

AT Protocol gives agents a public-ish substrate for identity and records. Instead of agents being hidden sessions inside a vendor tool, they become network participants with repos, records, and inspectable state.

## Swarm-tools / Koko angle

The local/OTP/tooling side shows the same idea from the other direction: coordination needs supervision, lifecycle, backpressure, and explicit handoff.

## Candidate punchline

Agent swarms are not a new kind of AI app. They are distributed systems with language-model-shaped workers.

## Open questions

- Is the talk primarily about Cloudflare as substrate, ATProto as protocol, or the synthesis?
- What is the demo that makes the audience feel “oh, I can build this Monday”?
- How much of joelclaw should appear as proof vs distraction?
- Where does “game loop” fit now that ATProto/Cloudflare is becoming central?
