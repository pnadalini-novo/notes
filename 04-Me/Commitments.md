# Commitments

> You never add tasks *to* this file. It's pure Dataview — every checkbox you've written anywhere in the vault surfaces here, sliced by who it came from. Capture happens where the context is (the meeting note, the 1-1, the daily); review happens here.

## From my boss

The list that decides whether you keep your job. Check it every single day.

```dataview
TASK
FROM !"05-Templates"
WHERE !completed AND src = "boss"
SORT due ASC
```

## From clients

```dataview
TASK
FROM !"05-Templates"
WHERE !completed AND src = "client"
SORT due ASC
GROUP BY client
```

## From my team

Promises you made in 1-1s. These are the quietest to break and the most expensive.

```dataview
TASK
FROM !"05-Templates"
WHERE !completed AND src = "team"
SORT due ASC
```

## Self-directed

The things nobody is chasing you for. First to slip, and usually the ones that actually move you forward.

```dataview
TASK
FROM !"05-Templates"
WHERE !completed AND src = "self"
SORT due ASC
```

---

## Overdue

```dataview
TASK
FROM !"05-Templates"
WHERE !completed AND due AND due < date(today)
SORT due ASC
```

## No due date

A commitment without a date is a wish. Empty this list weekly by adding a date or deleting the line.

```dataview
TASK
FROM !"05-Templates"
WHERE !completed AND src AND !due
```

## Waiting on someone else

```dataview
TASK
FROM !"05-Templates"
WHERE !completed AND who
SORT due ASC
GROUP BY who
```

## Closed in the last 7 days

Evidence for your weekly update, and a decent antidote to the feeling that you did nothing all week.

```dataview
TASK
FROM !"05-Templates"
WHERE completed AND completion AND completion >= date(today) - dur(7 days)
SORT completion DESC
```
