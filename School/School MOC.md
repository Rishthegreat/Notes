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

- Good if used correctly
	- Inherently it is good, but the people that use it determine whether it is good or bad
	- Same thing with any thing (a chair)
		- It is useful but if I throw it at someone, then it is bad