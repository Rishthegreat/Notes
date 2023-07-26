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

Laser Settings
Old Laser
- 1/8 Wood
	- Old - 25/100/700 cut
- 1/8 Acrylic
	- 15/100/Chart cut
	- default settings on laser




### Reduction of Tonal Propeller Noise by Means of Uneven Blade Spacing
- Harmonic/Tonal Noise
	- Created just by spinning
	- As Blade Passage Frequency increases, tonal noise increases
- Narrow-Band Noise
	- 
- Broadband Noise
	- Interaction with turbulence
	- Found at all frequencies