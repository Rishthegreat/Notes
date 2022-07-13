**Session 1**

- $\alpha \ket{0} +  \beta \ket1$ Super position
	- a and b are complex numbers

- Electron spin as an example of a quibit
	- You can just change the spin to change the quibit value

- Electron in spin up direction in z  - $|0>$, spin down in z is $|1>$
- $1/sqrt(2) (|0> + |1>)$ - spin up in x
- $1/sqrt(2) (|0> - |1>)$ - spin down in x
- Spin up in z and spin down in z are orthogonal

- Quantum Mechanics needs imaginary numbers
- $e^(i*\phi) = cos\phi + isin\phi$ 

![[Graph with equation]]
- There are other ways of making a quibit
	- Superconducting current loops
		- Google's quantum computer is made from this technology
	- Atomic ions
	- Cold atoms
	- Photon polarization
	- Electron spin
	- Nuclear spin

- Operations on a quibit
	- An operation on an electron spin quibit corresponds to a rotation of the spin. A rotation is implemented by applying gates to the quibit
	- The X gate corresponds to a rotation about the x axis by 180 deg
	- The Hadamard, or H gate corresponds to a rotation about the 45 deg line between the x and z axis by 180 deg
		- The hadamard gate puts a quibit into superposition


**Session 2**

- If you apply the X gate to the $\ket{0} - \ket{1}$, it becomes $\ket{1} - \ket{0}$

**Measuring Quibits**

- A charged particle moving in a circle produced a magnetic field
- Because an electron is electrically charged and has spin, it has a magnetic moment $\mu$, and it acts like a tiny magnet
	- Its energy is a magnetic field is $E = -\mu \cdot B$
	- The energy is lowest when the the spin is in the opposite direction of the magnetic field
	- Since the electron in negatively charged, the magnetic moment is in the opposite direction of the spin
- Stern Gerlach Device
	- There is a magnetic field and when an electron goes through the device, the electron goes up if it is spin up or goes down if it is in spin down
	- Classically, there would be a distribution based on the component vector of the spin in the Z direction, but in quantum, it is either up or down
	- If an electron is in spin up with 100% probability, the device will result in the electron being spin up
	- Make an electron in spin up - 
		- Put the electron through the machine and see if it comes out as spin up. Discard the spin down electron and repeat
	- If you measure an electron that is spin-up in the x direction, there is a 50% chance of it being spin up in Z or spin down in Z
	- If an electron is in $\alpha \ket{\uparrow} +  \beta \ket{\downarrow}$, the probability of it coming in spin up in Z would be $\alpha ^2$ and the probability of it being in spin down in Z would be $\beta ^2$
	- Applying the H gate and then the Z gate and then the H gate makes a X
	- A -X gate is a X gate and adds a negative which goes away because $\alpha$ and $\beta$ are squared in the probabilities
- 2 quibits
	- A state of a 2 quibit system is a superposition of the 4 states of $\alpha _{00}\ket{00}, \alpha _{01}\ket{01}, \alpha _{10}\ket{10}, \alpha _{11}\ket{11}$
	- CNOT gate (Controlled NOT gate)
	- ![[CNOT]]
	- The Control quibit passes through unchanged
	- If the control is $\ket{0}$, the target is unchanged and if the control is $\ket{1}$, the X gate is acted on the target
- Oracles
	- Every algorithm is based on the algorithm
	- ![[Drawing 2022-07-08 11.04.08.excalidraw]]
	- By asking questions and getting answers, we want to find out what f(x) is
	- Single bit to single bit only has 4 possibilities, 0 to 1 or 0 and 1 to 1 or 0
	- The oracle is not reversable
		- Some functions are not one to one
		- To make the oracle quantum, it has to be reversable
		- ![[Drawing 2022-07-08 11.10.29.excalidraw]]
		- This is a quantum oracle


**Session 3**

- ![[Quantum Computing 2022-07-11 10.03.07.excalidraw]]
	- If output is initialized to 
- ![[Quantum Computing 2022-07-11 10.04.33.excalidraw]]
	- When we measure the input as 0, then the output would be f(0) and when we measure the input as 1, then the output would be f(1)
	- The quantum computer has done two things at once, it has evaluated f(0) and f(1) at the same time
	- The problem is that even though both are calculated in the ouput, we can only measure one of the outputs
		- We do not have access to all the information
- The Deutsch algorithm
	- The first quantum algorithm
	- Showed that although you cannot get more information out of a quantum computation that out of a classical computation, that information can be different from that for a classical computation
	- He developed an algorithm that would determine in just one query whether a 1 bit to 1 bit function is a constant function [f(0) and f(1) are the same] or balanced [f(0) and f(1) are different values]
	- A classical computer would take 2 queries
	- ![[Quantum Computing 2022-07-11 10.30.18.excalidraw]]
		- If f(x) is 0, then we get $\ket{x}(\ket{0}-\ket{1})$
		- If f(x) is 1, we get $-\ket{x}(\ket{0}-\ket{1})$


**Session 4**

- Superconducting Quantum Circuits
	- Making Quibits
		- Need a 2 level system to make a quibits; one level for each of the $\ket{0}$ and $\ket{1}$ states
		- Nature's atoms provie a good 2 level approximation but are hard to control because of their small size
		- But we can create artificial atoms
		- Quantum Harmonic Oscillator
			- Only certain, equally spaced energy levels are allowed
			- Can transition between levels by inserting packets of energy
			- Capacitors store energy in electric field
				- $E_C = \frac{Q^2}{2C} = 0.5C\phi$
			- Inductor stores energy in the magnetic field
				- $E_L = \frac{1}{2L}\phi^2$
			- The energy of their combination is simply 
				- $0.5C\phi+\frac{1}{2L}\phi^2$
			- ![[Quantum Computing 2022-07-12 10.13.25.excalidraw]]
			- When cooled to low temperatures, LC circuits behave as quantum harmonic oscillators
			- LC circuits as harmonic oscillators [Momentum <-> Charge, Position <-> Flux]
			- Problem: Computational Basis states(0 and 1) not isolated
		- Josephson Effects
			- Below a critical temperature, electrons attract rather than repelling each other. Hence they pair up
			- These Cooper pairs are not scattered by the ionic lattice (suffer no resistance)
			- Cooper pairs tenneling across the junction without any applied voltage
			- ![[Quantum Computing 2022-07-12 10.17.58.excalidraw]]
		- QHO to Quibit
			- Replace Inductor (linear) with Josephson Junction (non-linear)
			- New Potential Energy - 
				- $E_J$  $\alpha$  $cos(\phi)$
		- Superconducting helps reduce resistance and friction
		- Electrons rae more likely to be excited in hotter temperatues
			- Superconducting helps us avoid this
			- In order to achieve temperatures to avoid excitation, we need the temperatures to be at 30 miliKelvin
		- Dilution Refrigerator
	- Controlling Quibits
		- If we want to make a quibit from 0 state to 1
			- We give it $\pi$ pulses of energy
				- However, quibits are always rotating around the z axis
				- So, we sort of spiral it down
		- Quibit Measurements
			- Artificial atom inside a box <-> Quibit coupled to cavityu
			- Cavity is harmonic oscillator and transmon is an anharmonic oscillator
			- If both have similar energy spacings, then they can swap excitations (photons)
			- 
	- Protecting Quibits
		- You and the environment are both controlling the quibit
		- If you make the quibit easily controllable, then the environment can control is as well
			- Superconducting Quibits are easy to manipulate but have short lifetimes ($100\mu s$)
		- Noise
			- Energy relaxation ($T_1$): Quibit relaxes from excited to ground state
				- We want this number to be larger so that the quibit becomes a 0 much slower
				- In order to run a different circuit, we wait till the quibit cools to 0 and then we run the experiment again
			- Dephasing ($T_\phi$): Fluctuatinos in quibit's energy mess up its precession frequency
		- Error Correction Problem - 
			- If there is a quibit in superposition, you cannot measure it during a circuit in between and if there is an error, you cannot solve the error
				- If you could measure, you would lose information
			- So, we use helper quibits in order to detect errors
				- ![[Quantum Computing 2022-07-12 11.00.11.excalidraw]]
				- We can use the 3rd quibit with the CNOT gates on the top 2 gates to detect whether an error has occured without measuring the top quibits, so the superposition is not destroyed

- Multiple Quibits
	- A system of n quibits has $2^n$ basis states
	- The number of basis states grows exponentially with the number of quibits
	- For 300 quibits, that is $2^{300}$ which is more than the number of protons in the visible universe


**Session 5**

- Entanglement
	- State of quibit 1 - $\ket{\psi_1} = a_0\ket{0} + a_1\ket{1}$
	- State of quibit 2 - $\ket{\psi_2} = b_0\ket{0} + b_1\ket{1}$
	- State of 2 independent quibits - 
		- $\ket{\psi} = a_0b_0\ket{00} + a_0b_1\ket{01} + a_1b_0\ket{10} + a_1b_1\ket{11}$
	- It is easy to entangle two electron spins
	- Just bring them close together and wait a while
	- Since the lowest energy state is hwen the 2 electrons are spinning in the opposide direction, they will be in the entangled state
	- Their spins are maximally correlated
	- $\ket{\uparrow\downarrow} - \ket{\downarrow\uparrow} = \ket{01} - \ket{10}$
	- What ever direction the spin of one elctron is measured to be, the spin of the other electron will be opposite
- Alice and Bob
	- Bring 2 electrons close together, and they will become
		- $\ket{\uparrow\downarrow} - \ket{\downarrow\uparrow} = \ket{01} - \ket{10}$
			- Lower energy so this state is easier to make, other states are possible, but harder because it requires more energy
	- Bob takes his electron to one side of the galaxy and Alice takes it to the other
		- Cannot measure on the way because it would break the entanglement
	- If Alice measures her electron to be spin up, then instantaneously, the other electron would be spin down
		- Alice can measure her electron in any direction and it will be either spin up or spin down in that direction
		- Bob's will be the opposite spin in the same direction
	- Alice could send information to Bob faster than the speed of light, but this would violate special relativity, which is one of the pillars in physics
		- If Alice measures spin in Z, and Bob measures in X, both will result in a 50 - 50.
		- Therefore no information has travelled faster than the speed of light
		- The no-clone theorem
			- It is not possible to clone an arbitrary quantum system
			- In order to clone the electron, we need to measure (Destroy) the state of the electron
- Polarization States
	- Another example of a quibit is photon polarization
	- ![[Quantum Computing 2022-07-13 10.44.21.excalidraw]]
	- If 2 polarizers make an angle $\theta$ with respect to each other
		- Probability to get through ->  $cos^2\theta$
		- Probability to not get through -> $sin^2\theta$
		- ![[Quantum Computing 2022-07-13 10.53.44.excalidraw]]
			- Each individual line is a polarizer in the direction of the red arrows
- C