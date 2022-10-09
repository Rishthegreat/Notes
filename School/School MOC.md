# School MOC

## Classes

```dataview
table block
from #course and !"Templates"
sort block
```

## Assignments
```dataview
task
from #assignments 
```
```dataview
table length(filter(file.tasks, (t) =>)) AS "Uncompleted"
from #assignments

```

## Notes

