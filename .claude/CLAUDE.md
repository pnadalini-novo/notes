# cifra - EM vault context

Obsidian vault for Pietro's engineering-manager work, built 2026-09-02 from an executable spec (`README-CONVENTIONS.md` at vault root has the full operating manual - read that first for folder/metadata conventions).

## Architecture decision (2026-09-03)

**Claude Code populates, Dataview displays.** Dataview is the only load-bearing plugin - it renders live, auto-refreshing queries with zero invocation. Templater, Tasks, Periodic Notes, Calendar are convenience/UI sugar, not capability - Pietro is trying them as installed per the spec and will remove any that aren't earning their keep. Don't assume the full plugin set is permanent; check `.obsidian/community-plugins.json` for what's actually still enabled before relying on Templater syntax (`<% tp.* %>`) still being live.

Claude Code's actual leverage here is reaching into systems no Obsidian plugin touches: Jira (via Atlassian MCP), Granola (meeting transcripts), Swarmia (engineer progress). When asked to update this vault, prefer writing directly into the correct file/frontmatter/inline-field format (`[src:: ]`, `[client:: ]`, `[jira:: ]`, `[who:: ]`, `📅 due date`) rather than improvising new structures.

## Clients

Only **BNP** (Banco Nacional de Panamá) is seeded (`02-Clients/BNP/`), deliberately - the spec's two-week rule says run the capture habit on one client before rolling out to the rest. Remaining clients, not yet created: Banorte, Coopcentral, BP (Banco Pichincha).

## Obsidian plugin config

Community plugins installed: Dataview, Templater, Tasks, Periodic Notes, Calendar (core vault function) plus Omnisearch and Paste Image Rename, copied byte-for-byte from `../novopayment/.obsidian` on 2026-09-03 so search and image-paste behavior matches Pietro's other vault. `app.json` sets `alwaysUpdateLinks: true` for the same reason (renamed pasted images shouldn't break links). If Pietro asks for another plugin/setting to match `novopayment`, that vault's `.obsidian/` is the reference copy - diff against it rather than guessing.
