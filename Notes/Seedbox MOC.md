---
created-date: 2024-09-26 09:59
tags: "type/MOC"
summary: All notes that need processing!
---

## Seed Logs

```dataview
TASK
WHERE icontains(text, "log/seedbox")
```

## Seed Notes

```dataview
TABLE
dateformat(file.mtime, "yyyy-MM-dd") AS "Last modified"
FROM "Seedbox"
SORT file.ctime ASC
```