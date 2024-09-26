---
created-date: <% tp.date.now("YYYY-MM-DD HH:mm") %>
up:
	- "[[Project MOC]]"
related:
alias:
tags:
	- "#type/sub-project"
	- "#type/active"
summary:
---

## Meetings

```dataview
TABLE WITHOUT ID
	file.link as session,
	created-date,
	participants,
	summary,
	tags
FROM !"Templates"
WHERE icontains(up, this.file.link)
AND icontains(tags, "type/meeting")
SORT filename DESC
```

## Tasks and Questions

### Open

```dataview
TASK
WHERE icontains(up, this.file.name)
AND (icontains(text, "#task") OR icontains(text, "#question"))
AND !completed
GROUP BY file.name as filename
SORT filename DESC
```

### Closed

```dataview
TASK
WHERE icontains(up, this.file.name)
AND (icontains(text, "#task") OR icontains(text, "#question"))
AND completed
GROUP BY file.name as filename
SORT filename DESC
```