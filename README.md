# Sp33der
3D printer design for ultra fast and structural rigit toolhead

This design was heavily inspired by Fhesse doing 1100mm/s with 50K acceleration. I started to think a lot on how to achieve the highest possible Speed and acceleration. To do this while still printing well we need to reduce ressonance. By that i mean reducing the resonance amplitude and raising the resonance frequency.

The resonance frequency wouldent matter if the amplitude was close to zero, but given we cant make magic that strategy is doomed to fail.

A high amplitude of the system indicates the system is not damped verry well. To increase dampening we could add mass to reinforce the structure that resonates to achieve more dampening.. The problem with this is that increased mass would reduce the resonance frequency and that is the opposite of what we are trying to do. And this is not that simple in a system like a 3d printer. Serveral things can resonate and reinforcing one part wont will only reducing its resonance.

![image](https://user-images.githubusercontent.com/7197181/142935915-307cee66-d599-4b3f-8b1a-fdea6d6f4fbd.png)

This is not as simple as i just explained because both the belts and the x gantry resonates. The goal is to design the system so that both the belt and the x beam resonates as little as possible. 
Lets assume i used a 4x4mm extrusion for my x beam. This extrusion is more likely to bend than a 20x20 extrusion. Its easy to assume that the 4x4 extrusion would resonate more than a couple of 12mm gates belts would.

Anyway - To raise frequency and lower the amplitude we could to serval things:
- reduce mass         + frequency - amplitude
- Shorter belts       + frequency - amplitude
- Bigger/more belts   + frequency - amplitude

Note to my self: energy = freq*mass

Bigger belts stretch less under the same load. The same goes for more belts carrying the same load. Lets get back to that in a second.

Fhesse desing:
What i found interesting in fhesses design was that it did 3 things differently
1. It had more mooving mass because it had two mooving gantry beams.
2. It had shorter belts, but it also had more belts for the same mass
3. It was a cartesian design without a motor on the mooving mass (Ender 5). 

Point nr. 3 is the majour design argument for the CoreXY design. You could move both X and Y axis without having a motor on the moving mass. But as we know the CoreXY belts are long. if we compare the following we get:

CoreXY lenght     = 2*XLength+2*yLength   
Bedslinger lenght = 2*x or Y  
Fhesses length    = 2*x or y  

But what talks in Fhesses favour is that the load for x and y is chared between two belts in parallel. This is the equivalent of a belt that is double as wide.



