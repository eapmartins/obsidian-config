---
created-date: <% tp.date.now("YYYY-MM-DD HH:mm") %>
up:
- "[[Project MOC]]"
related: 
alias: 
tags:
- "#type/project"
- "#status/active"
---

> **summary**:

## Sub Projects

```dataview
TABLE WITHOUT ID
	file.link as "Sub Project",
	up,
	created-date,
	summary,
	tags
FROM !"Templates"
WHERE icontains(up, this.file.link)
AND icontains(tags, "type/sub-project")
SORT filename DESC
```

## Meetings

```dataview
TABLE WITHOUT ID
	file.link as session,
	up,
	created-date,
	participants,
	summary
FROM !"Templates"
WHERE icontains(up, this.file.link)
AND icontains(tags, "type/meeting")
SORT filename DESC
```

