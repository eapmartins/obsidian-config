---
created-date: 2024-09-26 09:57
tags: "type/MOC"
summary: All People!
---

```dataview
TABLE WITHOUT ID
	file.link as "name",
	summary,
	tags
FROM !"Templates"
WHERE icontains(tags, "type/person")
```