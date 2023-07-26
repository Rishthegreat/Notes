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
objective of the study is to understand and reduce the perceived noise from general avaiation propellers with uneven blade spacing.
- SHow than you can use rapid prototyping to test propellers
- The noise can be predicted with simplified theoretical models
- 

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
	- Blade sweep is done and it improved aerodynamic efficiency and noise reduction

- Uneven blade spacing distributes the tonal noise over a larger number of tones spread across a broader range of frequencies, making the percieved noise lesser (more like white noise)
- equation says that noise due to drag is considered negligible because it is small compared to lift (has correlation between experiment and theory)
	- the equations predict noise of 