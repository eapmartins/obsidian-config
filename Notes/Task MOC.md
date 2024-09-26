---
created-date: 2024-09-26 09:41
tags: "type/MOC"
summary: All tasks!
---

### Open

```dataview
TASK WHERE icontains(text, "#task")
AND !completed
GROUP BY file.name as filename
SORT filename DESC
```

### Closed

```dataview
TASK WHERE icontains(text, "#task")
AND completed
GROUP BY file.name as filename
SORT filename DESC
```