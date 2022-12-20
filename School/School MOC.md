# School MOC

## Today is `$= dv.span(moment().format("dddd, MMMM, D - MM/DD"))`

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
where !completed
sort due
```
---
```dataview
table length(filter(file.tasks, (t) => !t.completed)) AS "Uncompleted"
from #assignments

```

## Notes

[[Projects]]

Laser Settings
- 1/8 Wood
	- Old - 25/100/700 cut
- 1/8 Acrylic