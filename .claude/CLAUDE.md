# cifra - EM vault context

Obsidian vault for Pietro's engineering-manager work, built 2026-09-02 from an executable spec (`README-CONVENTIONS.md` at vault root has the full operating manual - read that first for folder/metadata conventions).

## Architecture decision (2026-09-03)

**Claude Code populates, Dataview displays.** Dataview is the only load-bearing plugin - it renders live, auto-refreshing queries with zero invocation. Templater, Tasks, Periodic Notes, Calendar are convenience/UI sugar, not capability - Pietro is trying them as installed per the spec and will remove any that aren't earning their keep. Don't assume the full plugin set is permanent; check `.obsidian/community-plugins.json` for what's actually still enabled before relying on Templater syntax (`<% tp.* %>`) still being live.

Claude Code's actual leverage here is reaching into systems no Obsidian plugin touches: Jira (via Atlassian MCP), Granola (meeting transcripts), Swarmia (engineer progress). When asked to update this vault, prefer writing directly into the correct file/frontmatter/inline-field format (`[src:: ]`, `[client:: ]`, `[jira:: ]`, `[who:: ]`, `📅 due date`) rather than improvising new structures.

## Template frontmatter convention

`05-Templates/1-1.md` deliberately has `type:` left blank (not `type: person`) - Pietro cleared it because Dataview's `type = "person"` queries were incorrectly matching the template file itself. Don't "fix" this back. Every real instantiated person note still needs `type: person` set explicitly (see Hector Corredor.md added 2026-09-03) - only the template omits it. Check whether Client Overview.md / other templates need the same treatment before assuming they're fine.

## People notes

One file per person, forever - new log entries go at the top so current state is always first, full history readable by scrolling down. This convention lives here and in `README-CONVENTIONS.md`, not as a repeated blockquote in every person file (removed 2026-09-03, one wording moved to source of truth instead of duplicated 9 times).

## Clients

All four are seeded under `02-Clients/`: BNP (Banco Nacional de Panamá), Banorte, Coopcentral, BP (Banco Pichincha) - slugs `bnp`, `banorte`, `coopcentral`, `bp`. Pietro asked for all four on 2026-09-03, overriding the spec's two-week single-client rollout suggestion.

## Obsidian plugin config

Community plugins installed: Dataview, Templater, Tasks, Periodic Notes, Calendar (core vault function) plus Omnisearch and Paste Image Rename, copied byte-for-byte from `../novopayment/.obsidian` on 2026-09-03 so search and image-paste behavior matches Pietro's other vault. `app.json` sets `alwaysUpdateLinks: true` for the same reason (renamed pasted images shouldn't break links). If Pietro asks for another plugin/setting to match `novopayment`, that vault's `.obsidian/` is the reference copy - diff against it rather than guessing.
