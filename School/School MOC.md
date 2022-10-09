# School MOC

## Classes

```dataview
table block
from #course and !"Templates"
sort block
```
Today is `$= `
## Assignments
```dataview
task
from #assignments 
sort due
```
```dataview
table length(filter(file.tasks, (t) => !t.completed)) AS "Uncompleted"
from #assignments

```

## Notes

