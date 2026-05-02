# Source Map

## Joel signal: CascadiaJS agent swarms

Prompt:

> i'm speaking at cascadiajs in june about agent swarms and need to start capturing my thoughts
>
> i'm really interested in the at proto agent network using cloudflare primitives, the agent sdk, flue, project think etc - let's bring this shit together into a single project space and knowledge base to start jamming on some thoughts for how to build the narrative for the talk

## X thread

URL: https://x.com/irvinebroque/status/2050282756492668941?s=46&t=uRyCCtjktRI5TQXbSKdTLw

Status: needs fetch via X API or browser because raw X scraping is unreliable.

## X API docs

URL: https://docs.x.com/x-api/introduction

Relevant docs confirmed via search:

- Full-Archive Search quickstart: https://docs.x.com/x-api/posts/search/quickstart/full-archive-search
- Full-Archive Counts quickstart: https://docs.x.com/x-api/posts/counts/quickstart/full-archive-tweet-counts

Operational note: bot credentials can access Full-Archive Search (`/2/tweets/search/all`) by deriving an app bearer token from `x_consumer_key` + `x_consumer_secret`. Do not use `/2/tweets/search/recent` for YTD account research; it will reject older `start_time` values.

## swarm-tools

URL: https://github.com/joelhooks/swarm-tools

Likely contribution: practical agent swarm coordination tooling. Needs repo read.

## Koko

URL: https://github.com/joelhooks/koko

Likely contribution: Elixir/OTP agent model, actor supervision, durable process thinking. Needs repo read.

## ATProto Agent Network

URL: https://github.com/joelhooks/atproto-agent-network

Likely contribution: protocol-native agent identity, records, and network coordination. This may be the strongest demo spine.

## Flue

URL: https://github.com/withastro/flue

Likely contribution: project/content/workflow glue. Needs repo read before using as pillar.

## Cloudflare Dynamic Workflows

URL: https://blog.cloudflare.com/dynamic-workflows/?utm_campaign=cf_blog&utm_content=20260501&utm_medium=organic_social&utm_source=twitter

Likely contribution: runtime-defined durable workflows; important for agents because plan shape changes as agents discover work.

## Cloudflare Artifacts

URL: https://developers.cloudflare.com/artifacts/

Extracted summary: Artifacts stores versioned file trees behind a Git-compatible interface. Repositories can be created programmatically, imported, and addressed from Workers, REST API, and Git clients. Cloudflare explicitly frames this as useful for Git-aware tools, agents, automation, isolated parallel execution, fork/diff/merge workflows, and one repo per agent/user/branch/task.

Likely contribution: agent workspaces. Swarms need isolated, versioned, mergeable file trees, not just blob storage. This connects directly to sub-agent handoff, review, and parallel work.

## workers-routes

URL: https://github.com/yusukebe/workers-routes

Likely contribution: Cloudflare Workers routing/composition patterns. Needs repo read before using as pillar.

## Deconstruct: How to Prepare a Talk

URL: https://www.deconstructconf.com/blog/how-to-prepare-a-talk

Likely contribution: preparation method. Talks are verbal performances, so prep should mostly be spoken rehearsal, not silent outline/slide polishing. Use repeated once-per-day spoken passes to discover the shape, then group/cut/design after the spoken talk starts stabilizing.

Captured notes: `notes/talk-prep-method.md`

## Addy Osmani: agent-skills repo

URL: https://github.com/addyosmani/agent-skills

Likely contribution: concrete skill/persona/orchestration package. The repo encodes engineering work as lifecycle commands, skills, personas, checklists, hooks, and orchestration patterns. Strong evidence for the cartridge frame: domain rules + roles + tools + workflows + verification gates packaged as reusable agent substrate.

Captured notes: `notes/addy-agent-skills-repo.md`

## Addy Osmani: The Factory Model

URL: https://addyosmani.com/blog/factory-model/

Likely contribution: economic/productivity frame for autonomous agent work. Addy argues engineering shifts from writing code to building the factory that builds software. Useful but slightly sterile; CascadiaJS can use it as contrast. Factory explains production leverage, games explain play/coordination/rules/consequence, cartridge packages both.

Captured notes: `notes/addy-factory-model.md`

## Karpathy: LLM Knowledge Bases

URL: https://x.com/karpathy/status/2039805659525644595

Likely contribution: knowledge-base-as-compiled-artifact frame. Karpathy describes collecting raw sources, having an LLM compile a markdown wiki, querying it, rendering outputs, filing outputs back into the wiki, and running LLM health checks. This maps directly to the CascadiaJS repo as a talk/research cartridge.

Captured notes: `notes/karpathy-llm-knowledge-bases.md`

## Addy Osmani: Long-running Agents / Harness Engineering

URLs:

- https://addyosmani.com/blog/long-running-agents/
- https://addyosmani.com/blog/agent-harness-engineering/

Likely contribution: mainstream engineering vocabulary for the talk's architecture frame. Long-running agents need durable state, session logs, sandboxes, planners/workers/judges, memory, hooks, and verification. Harness engineering maps cleanly to the cartridge idea: a cartridge is a domain-specific harness with rules, tools, state, win conditions, and failure modes.

Captured notes: `notes/addy-long-running-agents.md`

## Talk prep resource map

Captured notes: `notes/talk-prep-resource-map.md`

High-signal additions:

- Zach Holman / speaking.io: https://speaking.io/
- Practicing: https://speaking.io/prep/practicing-it/
- Recording: https://speaking.io/prep/recording-your-talk/
- Improving: https://speaking.io/react/improving/
- Slide Design for Developers: https://zachholman.com/posts/slide-design-for-developers/
- The Talk on Talks: https://zachholman.com/talk/the-talk-on-talks/

## grill-with-docs

Installed from:

```bash
npx skills add https://github.com/mattpocock/skills --skill grill-with-docs -g -y
```

Use it to interrogate the talk once `CONTEXT.md` and first outline exist.
