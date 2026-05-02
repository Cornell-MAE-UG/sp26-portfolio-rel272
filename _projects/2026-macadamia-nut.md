---
layout: project
title: Macadamia Nut Cracker
description: A nut cracker designed in statics class
technologies: Notability
image: /assets/images/nut-cracker.png
---

Problem statement and objective: Calculate the the Dimensions of a simple lever Nut Cracker needed to produce a high enough mechanical advantage so that the force of human grip strength could crack a macadamia nut.

Constraints and Input Parameters: 

    Force needed to crack a macadamia nut: = 2180N 

        Found in the appendix section of this paper: Schrauf et 
        al. Do capuchin monkeys use weight to select hammer 
        tools, Anim Cogn 11, 413–422 (2008). https://doi.org/10.1007/s10071-007-0131-2

    Macadamia nut size = 20mm on the large side

    Average human grip strength (at age 80-90)= 55.3lbs for 
    men, 42.7 for women. I used 15kg (33lbs) as my grip 
    strength. This is 147N.
Approach: 

    Assumptions: I drew a sketch of the nut cracker, making the 
    "hole" for the nut 2cm (20mm) in radius, and making various
    other reasonable assumptions: 2.5cm from the center of the
    pin to the end of the hole that would contain the 
    Macadamia nut, and 2cm from the edge of the nutcracker to 
    the center of the nut (vertically). I took my human grip 
    strength as 147N, and my force needed to crack the nut as 
    2180 N.

    I then drew a free body diagram of one of the handles, in 
    order to figure out how to find various dimensions. I then 
    set up a moment balance about the pin at the front of the 
    nut cracker and got: M_a = d1(F_n) + d4(F_a), where d1 is 
    the distance between pin A and where the nut contacts the 
    crackers, d4 is the distance between the pin A and the 
    location of the applied force from the hand, F_a is the 
    applied force, and F_n is the force of the nut on the 
    cracker. 


    I took d1 to be 1.75 cm, calculated from my previous 
    assumsions of hole size and distance from hole to pin. I 
    took F_n to be 2180, from the paper attatched above, and I
    took F_a to be 147N, also listed in my assumsions above. 
    Plugging these values in and solving for d4, I got 
    d4 = 25.95cm. I then added a few centemeters onto this 
    length in order to account for extra length of handle 
    beyond where the hand lies on the handle, and got 28.95cm 
    for the length of the pin A to the end of the handle, which 
    I called d2. In summary, we have d1 = 1.75, d2 = 28.95, and 
    d3 = 25.95.


    To calculate the distance between the handles when the nut 
    is about to be cracked, I used similar triangles. I used 
    the line horizontally from pin A to where the nut touches 
    the cracker, and the line vertically from where the nut 
    touches the cracker to the outside of the nut cracker 
    handle to create a right triangle that would be similar to
    that formed by the line horizontally through the center of
    the nut cracker between the handles, and vertically down
    from one of the handles. I created a ratio of 1.75cm/2cm 
    = 28.95cm/x, and solved for x. This gave me 33.09 
    centemeters This is only half the width, so multiplying 
    by 2 gives approximately 66cm.


Diagram: 
<img width="970" height="717" alt="IMG_0284" src="https://github.com/user-attachments/assets/5d27c9a1-cfee-46b7-86dc-578fe2d3e86d" />

Usability: The nut cracker is around a foot long, and the space
between the handles is over two feet. Thus this design is not 
only unweildly, but also impossible to grip with one hand.

Due to the lack of usability, another iteration was designed. The handheld 
design was abandoned, and a linear actuator was decided upon. Handle lengths 
were made to be 15 cm, with a space of 24 cm between them at the end. The 
required force to break the macadamia nut from a distance of  of 11 cm 
(to allow for extra space at the end of the handles) was calculated to be 346.81N. 
The 1P65 mini was selected from the list, with a max reace of 10 inches (25cm) 
and a max force of 752 N.
New Design:
<img width="1557" height="1136" alt="image" src="https://github.com/user-attachments/assets/5e7ebf13-7d20-49f7-af83-360c057af70a" />


To assess the integrity of this design in respect to bending, we found the equations
for deflection by approximating one of the handles with a simplified free body 
diagram. The simplifications that were made were: assuming the handles to be completely
straight, and assuming the forces exerted by the nut and actuator were point loads. 
I also assumed that the nut would remain completely rigid until the moment of cracking. 


I came up with two equations, one describing the behavior of the handle before
encountering the nut, and one for after. 
Before Nut:
<img width="344" height="98" alt="image" src="https://github.com/user-attachments/assets/28b7a3c7-7767-449d-b87d-149e0326904c" />

After Nut:
<img width="1180" height="146" alt="image" src="https://github.com/user-attachments/assets/4cdaaab1-dc09-48b4-8703-a3a7dcacbe69" />


Through this I found the maximum deflection occurs at the very end of the 
handle (0.15m), due to it being a free end, unfixed by any pins or rollers, 
or other supports, and thus having the most room to bend. 
Max Deflection:
<img width="721" height="536" alt="image" src="https://github.com/user-attachments/assets/66ffa386-0aa6-43b2-9136-633af006c9a9" />

With the goal of bending of less than 2% of the length (0.003m), using cold rolled 
stainless steel (often used in kitchen appliances) I found that a 9.2x9.2mm 
square cross section would be the minimum for a square cross section. This was
found through plugging in known values into the maximum deflection equation for the handle
after the nut, setting the equation equal to 0.003, and solving for I, and then
plugging this value into the equation I = (1/12)s^4, and solving for s.

Moment of Inertia Calculations:
<img width="483" height="659" alt="image" src="https://github.com/user-attachments/assets/443ac880-b993-48b3-96de-745e34181b8f" />


Full Bending Work: [hw 12port.pdf](https://github.com/user-attachments/files/27297062/hw.12port.pdf)

