# Addy Osmani: The Factory Model

Source: https://addyosmani.com/blog/factory-model/

## Core thesis

> Software engineering is not about writing code anymore. It is about building the factory that builds your software.

Addy's frame: coding has changed dramatically, but core software engineering has not. The craft moves up the abstraction stack from writing code to orchestrating systems that write code.

## Three generations of AI coding tools

1. **Accelerated autocomplete** — AI saves keystrokes inside the same workflow.
2. **Synchronous agents** — human describes a task and iterates with agent in real time.
3. **Autonomous agents** — agent runs for tens of minutes/hours/days, produces artifacts for review.

Talk mapping:

This gives a clean on-ramp for audience members who have experienced Copilot/Cursor but not swarms. Swarms are not “better autocomplete.” They are the third-generation shift plus distributed coordination.

## Factory mental model

A factory has:

- fleets of workers
- precise inputs/specifications
- tools and environments
- process documentation
- quality control
- feedback loops
- reliable production lines

Agentic software work maps cleanly:

- agents = workers
- specs = work orders
- repos/tests/docs = toolbelt
- CI/preview/logs = quality control
- humans = factory designers/operators/reviewers

## Onboarding parallel

Agents behave like new engineers:

- receive a spec
- break it into subtasks
- explore the codebase
- inspect git history/blame
- escalate through Slack/email/humans
- iterate until acceptance criteria are met

Talk relevance:

This supports the human-in-the-swarm frame. Slack/email/git are no longer just human collaboration tools; they become interfaces between humans and agents.

## Spec as leverage

Addy's sharpest line:

> The spec is not a prompt anymore. The spec is the product thinking made explicit.

With fleets of agents, vague thinking multiplies. Ambiguous requirements propagate through many autonomous runs and fail in different directions.

Talk mapping:

In game terms, the spec is the quest. Bad quest text produces bad play. A good mission defines goal, constraints, rules, resources, and done condition.

## What still matters

Traditional engineering skills are amplified, not deprecated:

- clear requirements
- strong abstractions
- reliable tests
- careful tradeoffs
- human oversight
- systems thinking
- problem decomposition
- architectural judgment
- output evaluation
- orchestration skill

Talk mapping:

This is the antidote to “AI replaces engineers” slop. The agentic era raises the value of judgment because mechanical implementation gets cheaper.

## Verification is the bottleneck

Generation is no longer scarce. Verification is.

Agents can generate impressive output; the hard part is knowing if it is correct. Tests, artifact validation, environment reliability, guardrails, and human review become the factory safety system.

Talk mapping:

This reinforces the “judge/referee/DM” role in swarms. A swarm without verification is just parallelized slop.

## Strong phrase candidates

- “The factory model is useful, but incomplete: games explain why the factory has rules, roles, resources, and consequences.”
- “A mission is a spec with stakes.”
- “The spec is the quest text. If it is vague, every worker goes on a different adventure.”
- “Agentic work does not remove engineering judgment; it multiplies the cost of missing judgment.”
- “Verification is the referee.”
- “The human moves from builder to factory designer, party leader, referee, and patron.”

## How this shifts the CascadiaJS talk

The factory model is a strong adjacent metaphor, but it risks being too industrial and sterile. The game/cartridge frame can absorb it:

- Factory explains production leverage.
- Game explains exploration, coordination, motivation, rules, and learning.
- Cartridge explains packaging the factory/game into a repeatable domain-specific work system.

Possible bridge:

> If Addy's factory is the system that builds software, the cartridge is the system that makes the factory playable.

## Caution

Do not over-index on “factory.” Joel's talk has a stronger, weirder angle with play. Factory is useful for economic framing; games are better for explaining why agents/humans can coordinate inside a designed world.
