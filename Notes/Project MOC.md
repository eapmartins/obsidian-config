---
created-date: 2024-09-26 09:41
tags: "type/MOC"
summary: All projects!
---

### Open

```dataview
TABLE WITHOUT ID
	file.link as "project",
	up,
	created-date,
	summary,
	tags
FROM !"Templates"
WHERE icontains(tags, "type/project")
AND !icontains(tags, "status/complete")
SORT filename DESC
```

### Closed

```dataview
TABLE WITHOUT ID
	file.link as "project",
	up,
	created-date,
	summary,
	tags
FROM !"Templates"
WHERE icontains(tags, "type/project")
AND icontains(tags, "status/complete")
SORT filename DESC
```