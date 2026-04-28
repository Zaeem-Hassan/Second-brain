# Second-brain

A markdown-based second brain for researching `AI agents` with `Codex` and `Obsidian`.

This repo is built around an  idea:

- `raw/` stores your source material
- `wiki/` stores the structured knowledge base the agent maintains
- `reports/` stores saved answers and research outputs

Instead of asking an LLM the same questions from scratch every time, you keep a persistent wiki that compounds as you add more sources and more analysis.

## What This Repo Is

This is a starter vault for building a personal research system around AI agents.

It is designed to work like this:

1. You collect articles, PDFs, and notes in `raw/`
2. Codex reads those sources and writes summaries plus linked concept pages in `wiki/`
3. You browse the results in Obsidian using backlinks and graph view
4. When you ask a research question, Codex answers by reading your wiki and saves the result in `reports/`
5. Over time the vault becomes a durable, queryable knowledge base instead of disposable chat history

## Folder Structure

```text
.
├── AGENTS.md
├── Memory.md
├── index.md
├── log.md
├── raw/
├── reports/
├── assets/
└── wiki/
    ├── concepts/
    ├── entities/
    ├── maps/
    └── summaries/
```

## Core Files

- `AGENTS.md`
  The operating rules for Codex. This is the main schema file that tells the agent how to maintain the vault.

- `Memory.md`
  Stable context about the topic, goals, research priorities, and open questions.

- `index.md`
  The main navigation page for the vault. Codex should read this first before broad queries.

- `log.md`
  A chronological record of ingests, reports, and lint passes.

## How The System Works

### 1. Raw Sources

Put source material in `raw/`.

Examples:

- clipped web articles
- PDFs
- exported notes
- transcripts

These files should be treated as immutable source material. The agent reads from them but should not rewrite them.

### 2. Wiki

The `wiki/` folder contains the structured knowledge base.

Subfolders:

- `wiki/concepts/` for ideas like planning, tool use, memory, evals, orchestration
- `wiki/entities/` for companies, frameworks, researchers, and products
- `wiki/maps/` for overview pages that organize a whole area
- `wiki/summaries/` for source-by-source summaries

This is the layer that compounds over time.

### 3. Reports

The `reports/` folder stores saved outputs such as:

- research briefs
- comparisons
- Q&A outputs
- synthesis notes
- lint reports

Important rule: good answers should be saved here instead of disappearing in chat.

## How To Use This Repo

### Option 1: Use With Obsidian

1. Install Obsidian: `https://obsidian.md/`
2. Open `E:\second brain` as a vault
3. Enable backlinks and graph view
4. Optionally install Obsidian Web Clipper to save articles into `raw/`

Obsidian is mainly the browsing interface. Codex does the writing and maintenance.

### Option 2: Use From The Terminal

You can also work directly from the repo with Codex and skip Obsidian during writing. Obsidian is not required for the actual file updates.

## Recommended Workflow

### Ingest

Add a source file to `raw/`, then ask Codex:

```text
Read the new file in /raw. Create or update relevant pages in /wiki.
Write a summary in /wiki/summaries if needed. Update /index.md.
Append what changed to /log.md. Show me every file you touched.
```

### Query

Ask a question against the wiki:

```text
Using only my wiki and linked source summaries, answer this question:
[your question here]

Save the answer as a markdown report in /reports and cite the relevant wiki pages.
```

### Lint

Run a periodic health check:

```text
Review /wiki and find contradictions, weak cross-links, stale claims,
orphan pages, and concepts that should have their own page.
Write the results to a markdown report in /reports and summarize the fixes.
```

## Initial Topic Scope

This vault is currently seeded for `AI agents`, including:

- agent architectures
- memory systems
- planning
- tool use
- orchestration
- model/tool interfaces
- evaluation and reliability
- product and market implications

You can keep this repo AI-agent-specific, or evolve it into a broader research vault later.

## Existing Seed Pages

The repo already includes these starter pages:

- `wiki/maps/AI Agents Overview.md`
- `wiki/concepts/Agent Memory.md`
- `wiki/concepts/Planning.md`
- `wiki/concepts/Tool Use.md`
- `wiki/entities/OpenAI.md`
- `wiki/entities/Anthropic.md`

These are starter nodes, not final knowledge. Their purpose is to give the wiki an initial shape before real sources are ingested.

## First Run Checklist

1. Open the repo in Obsidian
2. Read `AGENTS.md`
3. Add 3-5 articles or PDFs to `raw/`
4. Run your first ingest
5. Check `index.md`, `log.md`, and the affected wiki pages
6. Ask one real research question and save the result to `reports/`

## Conventions

- Keep raw sources in `raw/`
- Save durable knowledge in `wiki/`
- Save outputs in `reports/`
- Update `index.md` when new pages are added
- Append all meaningful work to `log.md`
- Prefer updating existing pages over creating duplicates

## Who This Is For

This setup is useful if you:

- do ongoing research on a topic
- want answers to accumulate instead of vanish in chat
- prefer plain markdown over closed SaaS note systems
- want an LLM to maintain structure, summaries, and cross-links for you

## Repo Status

The scaffold is complete, but the knowledge base is still early-stage.

To make it valuable, you need to:

- add real sources
- run ingest cycles
- save reports
- keep refining the wiki through use

## License / Reuse

You can use this repo structure as a template for your own second-brain vault. If you adapt it for a different topic, update `Memory.md`, the seed pages, and `AGENTS.md` to match your domain.
