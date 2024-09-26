---
created-date: <% tp.file.title %>
summary:
---

>Prev: [[<% moment(tp.file.title, 'YYYY-MM-DD').add(-1, 'days').format("YYYY-MM-DD") %>]]
>Next: [[<% moment(tp.file.title, 'YYYY-MM-DD').add(1, 'days').format("YYYY-MM-DD") %>]]
>Week: [[<% moment(tp.file.title, 'YYYY-MM-DD').format("YYYY-[W]ww") %>]]

## Tasks
```dataview
TASK
WHERE !completed
AND icontains(text, "[[<% moment(tp.file.title, 'YYYY-MM-DD').format("YYYY-MM") %>")
AND icontains(text, "#task")
GROUP BY file.name as filename
SORT rows.file.ctime DESC
```

## Log