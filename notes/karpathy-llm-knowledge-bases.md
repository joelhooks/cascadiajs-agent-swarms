# Karpathy: LLM Knowledge Bases

Source: https://x.com/karpathy/status/2039805659525644595
Author: Andrej Karpathy
Date: 2026-04-02

## Core idea

Karpathy describes using LLMs to build and maintain personal research knowledge bases. Token throughput shifts from manipulating code to manipulating knowledge stored as markdown and images.

## Workflow

### Raw ingest

- Collect source documents into `raw/`: articles, papers, repos, datasets, images.
- Use an LLM to incrementally compile a wiki from raw sources.
- Wiki is a directory of markdown files.
- LLM writes summaries, backlinks, concept pages, categories, and links.
- Uses Obsidian Web Clipper for web articles and local image capture.

### IDE / frontend

- Obsidian is the human-facing IDE.
- Human views raw data, compiled wiki, visualizations.
- LLM maintains the wiki; human rarely edits it directly.
- Plugins like Marp can render slides.

### Q&A

- Once the wiki reaches useful scale (~100 articles / ~400K words), ask an LLM complex questions against it.
- Fancy RAG may not be necessary at this scale if the LLM maintains index files and summaries.
- The agent can read summaries and related docs well enough.

### Output

- Agent renders answers as markdown files, slide decks, matplotlib images, etc.
- Outputs get filed back into the wiki so explorations add up.

### Linting / health checks

- Run LLM health checks over the wiki:
  - find inconsistent data
  - impute missing data with web searches
  - identify connections
  - suggest new article candidates
  - clean up data integrity
  - suggest further questions

### Extra tools

- Build small domain tools, e.g. search engine over the wiki.
- Tools have both human UI and CLI interface for LLM use.

### Further exploration

- As the repo grows, consider synthetic data generation and fine-tuning so the LLM knows the domain in weights, not just context.

## Talk relevance

This is almost exactly what the CascadiaJS talk repo is becoming:

- raw source archive
- compiled markdown wiki
- LLM-maintained notes
- derived synthesis artifacts
- local/CLI tools
- outputs filed back into the knowledge base

The strong link to the talk is “knowledge cartridge.” A cartridge is not only code + rules. It can be a knowledge base compiled by agents from sources, with tools and health checks around it.

## Mapping to current frame

- Raw data → source documents / repo autopsies / X archives
- Compiled wiki → `notes/` synthesis files
- Obsidian as IDE → repo + Vault + markdown frontend
- Q&A → agent asks against curated research base
- Outputs filed back → generated notes become new context
- Health checks → lint the knowledge base for drift, missing links, weak claims
- Extra tools → source search, timeline extraction, term graph, talk-outline generator

## Good phrase candidates

- “The agent doesn’t just write code. It compiles a working memory.”
- “A knowledge base becomes a cartridge when it has tools, rules, and feedback loops.”
- “The human stops editing the wiki directly and starts steering the compiler.”
- “Research becomes an executable substrate.”

## Caution

Karpathy's frame is individual/research oriented. The CascadiaJS talk is about multiplayer swarms. The bridge is: once the knowledge base has structured artifacts, tools, and health checks, multiple agents and humans can participate in it asynchronously.
