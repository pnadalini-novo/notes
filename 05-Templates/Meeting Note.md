---
type: meeting
client: 
date: <% tp.date.now("YYYY-MM-DD") %>
kind: standup
granola: 
attendees: []
---
# <% tp.date.now("YYYY-MM-DD") %> — <% tp.file.title %>

> **Granola already has the transcript. Do not paste it here.** Link it above and extract only the four things below. If a meeting produces none of them, delete the note — it was a status broadcast, and Jira already covers that.

## Decisions

Things that are now settled and would cost real money to revisit. Include *why*, because in three months the why is the only part you'll need.

- #decision 

## Commitments made

Anything anyone owes anyone as a result of this meeting. Yours get `[src:: ]`; other people's get `[who:: ]` so they show up in your "waiting on" list.

- [ ]  📅  [src:: client] [client:: ]
- [ ]  [who:: ]

## Risks surfaced

- #risk 

## Things that need to become tickets

Not tickets yet. Raw asks that came up verbally. Convert them in Jira today or drop them deliberately — never leave them here to rot.

- 

---

**Transcript:** [Granola](<% tp.frontmatter.granola %>)
