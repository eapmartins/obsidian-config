---
created-date: 2024-09-26 09:51
tags: "type/MOC"
summary: All meeetings!
---

```dataview
TABLE WITHOUT ID
	file.link as "Meeting",
	up,
	summary,
	tags
FROM !"Templates"
WHERE icontains(tags, "type/meeting")
```