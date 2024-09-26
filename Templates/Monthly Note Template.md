```dataview
TABLE WITHOUT ID
file.link as Date,
summary
FROM "Journal/01 Daily/<% moment(tp.file.title, 'YYYY-MM-DD').format("YYYY") %>/<% moment(tp.file.title, 'YYYY-MM-DD').format("MM")%>"
SORT date ASC
```