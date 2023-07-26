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
	- Thickness of blade, lift, and drag induced noise
- Narrow-Band Noise
	- Periodic motion of propeller blades in unsteady flow conditions
	- Propeller axis is misaligned with flow
- Broadband Noise
	- Interaction with turbulence
	- Found at all frequencies

- Current ways to reduce are to find individual noise source and reducing their impact
	- tonal - thinner blade sections, tip speed, changing blade number, blade length, etc
	- broadband - controlling turbulent vortices
	- Create significant design changes, losses in efficency and outweight the benefits in noise reduction