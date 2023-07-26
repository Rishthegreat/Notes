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
	- the equations predict noise of evenly spaced blades, but for uneven, you add a phase shifts
	![[Pasted image 20230726191555.png]]

- Blade used → Beechcraft King Air 350 series aircraft (older model and modified for reinforcement) (factor of safety of 1.2 under certifugal loads at 50, 000 rpm)
	- ![[Pasted image 20230726191520.png]]

- 3 designs chosen to be manufactured using sterolithography (20 deg and 30 deg)
	- less than 20 would cause oo much interference and losses in efficiency
![[Pasted image 20230726191841.png]]

- Results
	- Uneven blade spacing typically reduced thrust
		- the 20 deg one experieneced 8.5% loss in thrust
			- Reason is interaction and the trailing blade getting caught in the downwash of the leading blade
				- Possible modification is to change angle of attack to account for this
	- uneven produce twice as many tones as regular
	- ![[Pasted image 20230726193205.png]]
	- ![[Pasted image 20230726193520.png]]
	- There is more broadband noise due to unknown effects due to close proximity of blades
		- One reason is that as the propellers get closer to the hub, they begin to merge
		- Another experiment was done with hobby grade propellers with axial separation and was proven that with the separation this increase was broadband noise was not present
	- What was found was that there was an increase in the total tonal intensity and that increase is mostly concentrated in the lower frequencies. The upper frequencies have been split off into more frequencies, reducing their individual impact. human ear is less sensitive to the lower frequencies and a wider range of frequencies is more like white noise and more pleasing than a concentrated range of frequencies.
	- Taking into account the human capability to hear certain frequencies and then weighting the recorded sound, the E20 and E30 showed 2 and 5 decibels reduction near the plane of the rotor. behind the propeller, is when uneven spacing had more sound