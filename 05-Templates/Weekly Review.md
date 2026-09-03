---
type: weekly
week: <% tp.date.now("gggg-[W]ww") %>
---
# Week <% tp.date.now("gggg-[W]ww") %>

> 30–45 minutes, Friday afternoon, calendar-blocked and defended. This is the only ritual here that genuinely cannot be skipped — the daily notes decay into noise without it.

## 1. Production verification pass

Ask Claude Code: *"List all Jira issues across my projects that moved to Done between [last Friday] and today, grouped by project, with assignee and resolution date."*

For each one, confirm it's actually deployed and update the client's Delivery Log. Anything Done-but-not-deployed goes in the client's Unverified table.

- [ ] Delivery Logs updated for every client
- [ ] Unverified queue reviewed — anything older than 2 weeks escalated

## 2. Client sweep

One pass per client hub note. Re-rank priorities if the client said anything that changes them. Set health honestly.

| Client | Health | Changed this week | Needs from me next week |
|---|---|---|---|
|  |  |  |  |

## 3. Commitments audit

Open [[Commitments]].

- [ ] Nothing overdue without an explicit new date
- [ ] "No due date" section emptied
- [ ] "Waiting on" list — nudge anything stale
- [ ] Boss list reviewed line by line

## 4. Team

Anyone I haven't spoken to properly this week?

```dataview
TABLE role, file.mtime AS "Last updated"
FROM "03-People"
WHERE type = "person"
SORT file.mtime ASC
```

Notes to self from this week's dailies worth raising in a 1-1:
- 

## 5. Me

**What I did that only I could do:**  
**What I did that someone else should have done:** (next week's delegation candidate)  
**Where I was the bottleneck:**  
**Practice from [[Role & Growth]] — did it happen?**  

## 6. Next week

Three outcomes, not tasks:

1. 
2. 
3. 

- [ ] Weekly update sent to my boss
