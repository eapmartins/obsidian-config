---
created-date: 2024-09-26 09:54
tags: "type/MOC"
summary: All notes that is not MOC's, people or projects.
---

```dataview
TABLE WITHOUT ID
	file.link as "Name",
	summary,
	tags
FROM "Notes"
WHERE !icontains(tags, "type/person")
AND !icontains(tags, "type/meeting")
AND !icontains(tags, "type/project")
AND !icontains(tags, "type/sub-project")
AND !icontains(tags, "type/MOC")
```