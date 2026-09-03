---
type: client
slug: banorte
health: green
am: 
review_cadence: weekly
---
# Banorte

## Who they are

**What they buy from us:**  
**Why they care:** (the business outcome behind the tickets)  
**How we get paid / measured:**  

## Contacts

| Name | Role | Channel | Notes |
|---|---|---|---|
|  |  |  |  |

## Their priorities — ranked, right now

Ranked, not listed. If everything is P1, you have no priorities and neither do they. Update this after every steering call and date the change.

| # | Priority | Why it matters to them | Our status | Epic |
|---|---|---|---|---|
| 1 |  |  |  |  |
| 2 |  |  |  |  |
| 3 |  |  |  |  |

_Last re-ranked: _

## Standing constraints

Compliance scope, environments, release windows, freeze periods, integration partners — the things that make an "easy" ticket not easy for this specific client.

- 

## Open commitments to this client

```dataview
TASK
FROM !"05-Templates"
WHERE !completed AND client = this.slug
SORT due ASC
```

## Risks and escalations

| Date | Risk | Impact | Owner | Status |
|---|---|---|---|---|
|  |  |  |  |  |

## Recent meetings

```dataview
TABLE kind AS "Type", date AS "Date"
FROM "02-Clients"
WHERE type = "meeting" AND client = this.slug
SORT date DESC
LIMIT 10
```

## Links

- Delivery Log: [[Delivery Log]]
- Jira board: 
- Repos: 
- Runbook: 
