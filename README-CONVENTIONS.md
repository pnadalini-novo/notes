# EM Vault — Operating Manual

## The one rule that keeps this alive

**Obsidian does not duplicate Jira or Granola.**

- **Jira** = source of truth for *work items and their status*.
- **Granola** = source of truth for *what was said in a meeting*.
- **Obsidian** = source of truth for *what you owe, what you decided, and what you'd otherwise forget*.

If you find yourself copying ticket titles into Obsidian, stop. Link the ticket key instead. The moment your notes try to mirror Jira, they go stale and you abandon the vault.

---

## Folder structure

```
00-Inbox/                  Quick capture. Empties daily.
01-Daily/                  One note per working day. YYYY-MM-DD.md
02-Clients/
   Acme/
      Acme.md              Client overview (the hub note)
      Delivery Log.md      What actually reached production, dated
      Meetings/            Stand-ups, syncs, escalations
   Globex/
      ...
03-People/
   Ana Perez.md            Running 1-1 log, one file per report
04-Me/
   Commitments.md          Dashboard: everything you owe, from anywhere
   Role & Growth.md        Expectations of you + what you're improving
   Notas y Observaciones.md   Running log of process/org observations, not tied to one person or client
   <Manager Name>.md       Your own upward 1-1 log - same "new entries at top" convention as reports
   Weekly Reviews/
05-Templates/
06-Reference/              ADRs, standards, runbooks, links out (Apps Team & Pods, Feedback Framework, etc.)
```

Clients get folders because they accumulate meetings. People get single files because a 1-1 is a *continuous conversation*, not a series of events — you want to scroll one person's history in one place. New log entries go at the **top** of the file, so the current state is always the first thing you see; scroll down for their whole arc, which is what makes promotion cases and hard conversations writable.

---

## Plugins

| Plugin | Why |
|---|---|
| **Dataview** | Every dashboard in these templates. Non-negotiable. |
| **Templater** | `<% %>` syntax, auto-filenames, folder-triggered templates. |
| **Tasks** | Due dates, recurring tasks, snoozing. Optional but recommended. |
| **Periodic Notes** | One hotkey to today's daily note. |
| **Calendar** | Visual jump between daily notes. |

Dataview reads the Tasks plugin's emoji dates (`📅 2026-09-03`) directly into its `due` field, so the two systems share one syntax. Turn on **Dataview → Settings → Enable inline field highlighting**.

If you're on a recent Obsidian version you also have **Bases** (core database views). Bases is better for browsing files-as-rows; Dataview is better for pulling *tasks* out of many files, which is most of what's below. Start with Dataview.

---

## Metadata conventions

Every actionable line is a checkbox with inline fields:

```md
- [ ] Draft the BIN validation memo 📅 2026-09-03 [src:: boss] [client:: acme] [jira:: PAY-1421]
```

| Field | Values | Meaning |
|---|---|---|
| `[src:: ]` | `boss`, `client`, `team`, `self` | Who this obligation came from |
| `[client:: ]` | lowercase client slug | Which client it serves, if any |
| `[jira:: ]` | issue key | Link to the real work item |
| `[who:: ]` | person name | Delegated — you're waiting on them |
| `📅 ` | YYYY-MM-DD | Due date |

Only `src` is mandatory. Everything else is optional and the dashboards degrade gracefully without it.

**Tags** stay minimal — a taxonomy you don't maintain is worse than none:
`#decision` `#risk` `#feedback` `#prod` `#blocked`

---

## Frontmatter

Client hub notes:
```yaml
---
type: client
slug: acme
health: green      # green | yellow | red
am: "Name of account contact"
---
```

People notes:
```yaml
---
type: person
role: Senior Backend
started: 2024-03-01
---
```

Meeting notes:
```yaml
---
type: meeting
client: acme
date: 2026-08-31
kind: standup      # standup | sync | escalation | planning
granola: "https://..."
---
```

---

## Naming

- Daily: `2026-08-31.md`
- Meetings: `2026-08-31 Acme Standup.md`
- Weekly reviews: `2026-W35.md`

Date-first names sort chronologically for free and never collide.
