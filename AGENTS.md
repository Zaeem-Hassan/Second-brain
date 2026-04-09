# AI Agents Research Vault

This vault is a research-focused second brain for AI agents. Codex is the maintainer of the wiki layer. Obsidian is the primary interface for browsing, linking, and graph exploration.

## Goals

- Turn raw sources into a persistent, interlinked markdown wiki.
- Preserve every meaningful answer as a file, not disposable chat.
- Keep the raw source layer immutable.
- Make the vault easy to navigate through `index.md`, backlinks, and map pages.

## Directory Contract

- `raw/`: Immutable source material. Web clips, PDFs, exported notes, and attachments. Never edit files in this folder unless the user explicitly asks.
- `wiki/concepts/`: Core technical ideas and abstractions.
- `wiki/entities/`: Companies, tools, researchers, frameworks, products, and protocols.
- `wiki/summaries/`: Source-by-source summaries derived from raw materials.
- `wiki/maps/`: High-level map pages that organize major subdomains.
- `reports/`: Saved answers, comparisons, research briefs, and synthesis artifacts.
- `assets/`: Local images and attachments that support notes in the vault.

## Operating Rules

1. Read `index.md` before broad wiki queries so discovery starts from the catalog.
2. Update `index.md` whenever a new wiki or report page is created.
3. Append a dated entry to `log.md` for every ingest, report, or lint pass.
4. Prefer editing existing pages over creating near-duplicates.
5. When a source changes the current synthesis, update all impacted pages instead of adding isolated notes.
6. Preserve uncertainty explicitly. If sources conflict, record the contradiction and cite both sides.
7. Do not silently delete user-authored content. If consolidation is needed, ask first.

## Page Format

Unless a page has a better domain-specific structure, use this layout:

```md
# Title

## Summary
2-5 sentences with the current synthesis.

## Key Points
- Concise bullets with the most important claims or mechanisms.

## Related
- [[Related Page]]

## Sources
- [[Source Summary]]

## Open Questions
- Unknowns, contradictions, or follow-up research directions.
```

## Workflows

### Ingest

When the user adds one or more files to `raw/`:

1. Read the new source.
2. Create or update a page in `wiki/summaries/`.
3. Update any affected pages in `wiki/concepts/`, `wiki/entities/`, or `wiki/maps/`.
4. Update `index.md` with new or materially changed pages.
5. Append an entry to `log.md` describing what was added or updated.
6. Report every touched file in the final response.

### Query

When the user asks a substantive research question:

1. Read `index.md`.
2. Read the relevant wiki pages and source summaries.
3. Write the answer to `reports/` as markdown.
4. Link the report from `index.md`.
5. Append an entry to `log.md`.

### Lint

When the user asks for a health check:

1. Scan `wiki/` for contradictions, orphan pages, weak cross-links, and stale claims.
2. Write findings to `reports/lint-report-YYYY-MM-DD.md`.
3. Do not make large structural changes unless the user asks for fixes after reviewing the report.

## Naming Conventions

- Use clear title-case filenames for long-lived pages, for example `Agent Memory.md`.
- Prefix time-stamped reports with the date when chronology matters, for example `2026-04-10 Memory Architectures Report.md`.
- Keep names stable. Rename only when the new title is materially better and update references accordingly.

## Initial Topic Scope

This vault currently focuses on `AI agents`, including:

- agent architectures
- memory systems
- planning and tool use
- orchestration frameworks
- evaluation and reliability
- MCP and tool interfaces
- economic and product implications of agents

## Preferred Behavior

- Be concrete and synthesis-oriented.
- Favor a small number of high-value pages over a large number of thin pages.
- Store durable knowledge in the wiki and one-off outputs in reports.
- Keep the wiki readable by a human first.
