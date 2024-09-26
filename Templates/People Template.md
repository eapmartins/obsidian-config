---
created-date: <% tp.date.now("YYYY-MM-DD HH:mm") %>
related:
alias:
tags: "#type/person"
---

>**summary**::

```dataview
TABLE WITHOUT ID
file.link AS "Contact note",
file.day + ": **" + T + " days**" AS "Last contact"
FROM [[]]
FLATTEN (date(today) - file.day).days AS T
SORT file.day DESC
LIMIT 1
```

## Log

>```dataview
>TASK
>WHERE icontains(text, this.file.name)
>AND !icontains(text, "#task")
>AND !icontains(text, "#question")
>GROUP BY file.name as filename
>SORT rows.file.ctime DESC
>```

## Tasks and Questions

>```dataview
>TASK
>WHERE icontains(text, this.file.name)
>AND (icontains(text, "#task")
>OR icontains(text, "#question"))
>GROUP BY file.name as filename
>SORT rows.file.ctime DESC
>```