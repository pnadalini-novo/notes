---
type: daily
date: <% tp.date.now("YYYY-MM-DD") %>
---
# <% tp.date.now("dddd, DD MMMM YYYY") %>

## Open loops (auto)

Everything you owe, anywhere in the vault, that isn't done:

```dataview
TASK
FROM !"05-Templates"
WHERE !completed AND src
SORT due ASC
GROUP BY src
```

## Waiting on others

```dataview
TASK
FROM !"05-Templates"
WHERE !completed AND who
SORT due ASC
GROUP BY who
```

---

## Today — max 3

Not a to-do list. The three things that, if done, make today a win.

1. 
2. 
3. 

---

## Captured

Raw dump for anything that shows up mid-day. Triage at end of day: every line either becomes a task with `[src:: ]`, moves into a client or person note, or gets deleted.

- 

---

## Meetings today

```dataview
LIST kind
FROM "02-Clients"
WHERE type = "meeting" AND date = date("<% tp.date.now("YYYY-MM-DD") %>")
```

---

## Production check

Items Jira says are Done — did they actually ship?

| Jira | Client | Jira status | In prod? | Verified |
|---|---|---|---|---|
|  |  |  |  |  |

---

## Notes to self

Observations about the team, a person, a process, yourself. One line each. These are the raw material for 1-1s and for your own growth log, and they're worthless a week later if you don't write them the day they happen.

- 

---

## End of day

- [ ] `00-Inbox/` empty
- [ ] Captured section triaged
- [ ] Meeting commitments extracted from Granola
- [ ] Unfinished tasks rescheduled, not silently abandoned
