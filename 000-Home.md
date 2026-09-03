# Home

Pin this. It's the only note you need bookmarked.

## Needs attention

```dataview
TASK
FROM !"05-Templates"
WHERE !completed AND due AND due <= date(today)
SORT due ASC
```

## Clients

```dataview
TABLE health AS "Health", am AS "Contact", file.mtime AS "Touched"
FROM "02-Clients"
WHERE type = "client"
SORT health ASC
```

## People

```dataview
TABLE role AS "Role", file.mtime AS "Last 1-1 note"
FROM "03-People"
WHERE type = "person"
SORT file.mtime ASC
```

## This week

- [[Commitments]]
- [[Role & Growth]]

## Recent decisions

```dataview
LIST
FROM #decision
SORT file.name DESC
LIMIT 15
```

## Open risks

```dataview
LIST
FROM #risk
SORT file.name DESC
LIMIT 15
```

## Stale notes

Client or person notes nobody has touched in three weeks. Usually means a relationship is drifting, not that the note is fine.

```dataview
TABLE file.mtime AS "Last touched"
FROM "02-Clients" OR "03-People"
WHERE (type = "client" OR type = "person") AND file.mtime < date(today) - dur(21 days)
SORT file.mtime ASC
```
