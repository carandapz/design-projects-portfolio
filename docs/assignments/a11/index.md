# A11 – Motor Selection

## Objective


#Motor Selection Design 

For this assignment, we are continuing with the work from last week which included the designing of a leadscrew tensile tester. This week we are in charge of selecting and adding the motor to the tester, designing a frame, and designing a floating bearing. In this assignment we also utilize FEA analysis to ensure our frame holds up. Towards the end we have provided a full bill of materials, labor cost and our entire process for the assignment. 

Our team is composed of Carlos Aranda Perez, Jason Swanchara, and Gavin Winningham. 

### Motor selection and Attachments - Carlos Aranda Perez

For this part of the assignment, I was tasked with selecting an appropriate motor using the torque and speed requirement from the last assignment which for us was the following values: Max Torque at 1.72 N*m= 15.2233 in*lb = 243.57 in*oz_f; and our range for our RPM’s were the following: 0.4711-25.7 rotations per minute.  Looking through the motor selection, I was able to use the NEMA 23 stepper motor ([found here](https://www.mcmaster.com/6627T631/ )) that closely resembled our values. The max holding torque in this motor is 262 in*oz_f which is more than enough for our measly 244 in*oz_f. The rest of the specs for this motor includes a max RPM of 3000 which again, is so much greater than our calculated values. The voltage for the motor was given at 24 V, and current at 7 amps. This holds for when you go with the parallel wiring of the motor, it is also worth noting that we get a better torque speed curve with the parallel wiring, allowing us to stay in a continuous operating zone.

![givenmotor.png](givensmotor.png)


![drawinganddimensionsofmotor.png](drawinganddimensionsofmotor.png)


![speedtorqueplotmotor.png](speedtorqueplotmotor.png)


Now with the motor picked out, I had to design a bracket in which the motor could securely attach to the tensile tester. Starting off with the knowns and unknowns, then creating an FBD of the bracket. For the material we have been using 1018 carbon steel, using the following values MOE = 205 GPa= 29700 ksi, which were found [here](https://www.azom.com/article.aspx?ArticleID=6115 ). Taking the dimensions of the motor I decided it was best to give it some room to be able position it properly, opting for a 4 by 4 bracket. 

![mmbasegivens.png](mmbasegivens.png)

Using an equation for deflection provided by The Machinery’s Handbook, I was able to calculate the minimum thickness for the motor bracket. The minimum thickness came out to be 0.0415 in, which in my opinion was extremely small, so when my teammate modeled it in SolidWorks he changed it to be .3 inches as this worked better for the use in the frame.

Afterwards I began the design process for the coupler. Doing the same old same old process of listing the knowns and unknowns, drawing the FBD’s. We were tasked with finding the outer diameter and thickness of the coupler, to find them we had to use shear stress torsion analysis to find the inner and outer diameter of the coupler. 

Using the following equations, I solved for it algebraically then plugged and chugged. Doing so allowed me to find a thickness of 0.788.With that being said, I found that the outer diameter was 1.0795 inches, so I ended up choosing the Servomotor Precision Flexible Shaft Coupling. This coupler has ⅜” by ½” shaft diameter and an outer diameter of 1-1/16”. I chose this one because the outer diameter was extremely close to our calculated outer diameter and the inner diameter of ⅜” would nicely house our lead screws. The coupler used can be found [here](https://www.mcmaster.com/6854N105/) 

![couplergivenandsolved.png](couplergivenandsolved.png)

## Analyze and Design a Frame - Jason Swanchara

![A11_part4](A11_part4.png)

To find suitable connectors, I used 1018 steel again to keep consistency.  Using the Sy, T, the distance between the center of the center of the beam and bolts, and factor of safety, I found the minimum thickness required of the connectors to be very small.  This likely meant that the thickness would be governed by other factors.  I ended up choosing the 40-4481 5-hole L plate to connect the beam to the two columns.





## Floating Bearing Mount - Jason Swanchara

The floating bearing mount is vital to centering the leadscrew while still enabling slight vertical motion when necessary.  Only the top is fixed and carries the load, 1 KN per screw.  The assignment requires an RC3 fit, which allows for free spinning of the screws and very little wobbling.  Assuming a quarter inch bolt, using Table 8a in the Machinery’s Handbook, clearance would be between 0.5 - 1.5 thousandths of an inch.


## Bill of Materials - Jason Swanchara

| Item Number | Quantity | Name | Cost per Item | Cost | Purchase Link |
|---|---:|---|---:|---:|---|
| 47065T102 | 4 | T-Slotted Frame | $18.76 | $75.04 | [Purchase Here](https://www.mcmaster.com/47065T102/) |
| 95120A592 | 2 | Flange Nut | $111.78 | $223.56 | [Purchase Here](https://www.mcmaster.com/95120A592/) |
| 99030A992 | 2 | Lead Screw | $17.04 | $34.08 | [Purchase Here](https://www.mcmaster.com/99030A992/) |
| 6627T631 | 2 | Motor | $100.92 | $201.84 | [Purchase Here](https://www.mcmaster.com/6627T631/) |
| 6854N105 | 2 | Coupler | $191.33 | $382.66 | [Purchase Here](https://www.mcmaster.com/6854N105/) |
| 40-4481 | 4 | T-Slot Connector | $15.89 | $63.56 | [Purchase Here](https://www.grainger.com/product/80-20-T-Slot-Framing-System-Connecto-906TA2?searchQuery=40-4481&searchBar=true&tier=Tier+6&s_e=false&s_c=solr9) |
| **Total** | **16** | | | **$980.74** | |

| Person | Hours Worked | Cost/Hour | Cost |
|---|---:|---:|---:|
| [Carlos Arando-Perez] | [12] | $35.00 | $[420] |
| [Jason Swanchara] | [12] | $35.00 | $[420] |
| [Gavin Winningham] | [14] | $35.00 | $[490] |
| | | **Total Cost** | **$[1,330]** |

**Total Cost of Project:** = $980.74 + 1,330=**2,310.74**



## Lessons Learned 

This assignment really pushed the team’s limits. We learned how to apply the lessons taught in last week’s lecture in real life. We also learned that time management is critical to completing these assignments on time. We learned how to apply bearing stress to the bracket that supports the motor, it took hours to get right. We also learned how to optimize an assembly in solidworks, and how to troubleshoot issues on the fly. One of our laptops wasn't happy with the assembly being created. Finally, the last thing we learned was to make sure to double check dimensions before adding materials to the list, because it just wastes time having to look back through the database for the correct size for the assembly.




