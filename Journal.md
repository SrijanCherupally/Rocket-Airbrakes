# Project Journal


I am participating in a rocket competition. I need to build a rocket that goes to a specific altitude. However, due to wind, air pressure, humidity, and multiple other factors, it is virtually impossible to reach that altitude consistently. To solve this problem I am developing an active altitude control module that uses Active Control Airbrakes that adjust the drag of the rocket to get to the altitude very consistently.

To solve this problem, I will need to do the following things in order: 
- Use CAD programs to design an Airbrake Mechanism
- Use Fusion 360 and Autodesk CFD to assess whether or not the mechanism can survive Mach 0.35 (Redesign if necessary)
- Use KiCad or EasyEda PRO to design a PCB to control the angle of the Airbrakes
- Use ArduinoIDE to code the PCB how to control the angle of the Airbrakes

# Day 1

I was researching on possible Airbrake Mechanisms. There are a couple mechanisms:
- Slider mechanism which uses rails to move the Brake inside and outside the rocket to go to specific altitude.
![image](https://github.com/user-attachments/assets/a76cddea-041d-41a5-b93a-1cac99336e28)
- Umbrella mechanism, which similar to its name, uses the mechanisms of the Umbrella to actuate and go to specific altitude.
  ![image](https://github.com/user-attachments/assets/4c020a4d-be4c-4549-be43-ae70a1a7aa50)


Pros and Cons of each design:

Slider Mech Pros: 

- Easy to design
- Easy to assemble
- Easy to actuate

Slider Mech Cons:

- CNCing parts is expensive (60-80 dollars + shipping)
- Surface Area of the actuation is only 3000 mm^2, which is really low surface area, so it cant bring Rocket to a stop quickly, meaning it will have worse performance
- The mechanism is also very weak, because at Mach 0.3, there will be a cantilever of 10 pounds of force, which is much more than the Airbrakes can handle

Umbrella Mech Pros:

- Lots of surface area - 21000 mm^2, a lot of surface area, enough to bring the Rocket to a halt extremely quickly - goood performance
- Strong mechanism, beccause linkages support it as it unfolds, meaning it can withstand the 10 pounds of force
- Cheap, it can be made using my 3d printer for essentially 50 cents versus 80 dollars

Umbrella Mech Cons: 

- Lots of parts to design
- Difficult to assemble
- Little bit more difficult to actuate (via leadscrew or linear actuator)

What I am deciding on for now:
I'll CAD out the slider mechanism since its easy to design, and see how much it costs, how much surface area it has, and how weak it is. If its too expensive, too expensive, or too small, Ill switch to Umbrella Design

Time Spent: 3 hours
Date: 5/20/2025

# Day 2

Today, I decided to work on CADding the Slider Mechanism. 
To do this, I decided on using Onshape, and later shift it to Fusion to run some CFD Tests. 
I wanted my Airbrakes to fit in a BT 80 tube, so I cadded a 65 mm diameter circle first, and then added my airbrakes

![image](https://github.com/user-attachments/assets/79fefaa9-bf95-46bb-ba74-cae272058e6e)

To make sure the Airbrakes could slide, I added these rail guides to allow the Airbrakes to fit in, and slide smoothly

![image](https://github.com/user-attachments/assets/bbca8fa9-8217-4e21-8325-acb3a9810a4c)

This was the full Airbrake Base, with rail guides for 3 Airbrakes Fins

![image](https://github.com/user-attachments/assets/42ef57d8-2f3c-41c8-baf7-cfa88366afa3)

Work done today - Cadded Slider Mech Airbrake Base

Time Spent: 3 hours
Date: 5/21/2025



