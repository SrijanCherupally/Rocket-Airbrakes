# Project Journal


I am participating in a rocket competition. I need to build a rocket that goes to a specific altitude. However, due to wind, air pressure, humidity, and multiple other factors, it is virtually impossible to reach that altitude consistently. To solve this problem I am developing an active altitude control module that uses Active Control Airbrakes that adjust the drag of the rocket to get to the altitude very consistently.

To solve this problem, I will need to do the following things in order: 
- Use CAD programs to design an Airbrake Mechanism
- Use Fusion 360 and Autodesk CFD to assess whether or not the mechanism can survive Mach 0.35 (Redesign if necessary)
- Use KiCad or EasyEda PRO to design a PCB to control the angle of the Airbrakes
- Use ArduinoIDE to code the PCB how to control the angle of the Airbrakes

# Day 1 - 6/5/2025

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

# Day 2 - 6/8/2025

Today, I decided to work on CADding the Slider Mechanism. 
To do this, I decided on using Onshape, and later shift it to Fusion to run some CFD Tests. 
I wanted my Airbrakes to fit in a BT 80 tube, so I cadded a 65 mm diameter circle first, and then added my airbrakes

![image](https://github.com/user-attachments/assets/79fefaa9-bf95-46bb-ba74-cae272058e6e)

To make sure the Airbrakes could slide, I added these rail guides to allow the Airbrakes to fit in, and slide smoothly

![image](https://github.com/user-attachments/assets/bbca8fa9-8217-4e21-8325-acb3a9810a4c)

This was the full Airbrake Base, with rail guides for 3 Airbrakes Fins

![image](https://github.com/user-attachments/assets/42ef57d8-2f3c-41c8-baf7-cfa88366afa3)

Work done today - Cadded Slider Mech Airbrake Base

Time Spent: 4 hours
Date: 5/21/2025

# Day 3 - 6/9/2025

Today I was wondering about calculating the force exerted on the Airbrakes. To do this, I simulated the airbrakes I designed earlier, by exporting it and importing it into Onshape. From here, I was able to find out that a total of around 6 newtons would be exerted on the Airbrakes. If these Slider Airbrakes werent CNC'd they wouldnt be strong enough to withstand the force, and break. 

I went to JLC PCB and tried to quote the airbrakes I designed. Even without the motor mechanisms and mounts, the cost was 80 dollars + tax + shipping, which is going to be around 110 dollars, way above my budget. 

So I decided that I had to design the Airbrakes using the Umbrella Method, that would be much stronger, and could be made from my 3d printer

Time Spent: 2 hours

# Day 4 - 6/11/2025

Today, I hopped on Onshape and started designing the Umbrella Airbrake. To start, I first designed the transition bay, in which the Airbrakes would be mounted to. This transition bay would be held inside the rocket, and would hose the airbrakes, and the electronics. 

This is the Transition/Coupler I designed: 

![image](https://github.com/user-attachments/assets/68b9ec6f-3e6d-4782-9e6c-3a4d2c1192e2)

The mounts popping out of the Transition bay, are there to mount the Airbrakes which the Airbrakes can actuate freely.

Next, I designed the Airbrake Fins, which were designed to have as much surface area as possible to maximize control authority.

This is the Airbrake I designed: ![image](https://github.com/user-attachments/assets/be1b9bbc-7bda-4d58-af71-237abf3ad8da)

The top mount popping out of the Airbrake, are supposed to screw onto the mounts on the Transition bay to actuate the Airbrake. 
The mount on the bottom is there so I can connect a hinge to it, so I can actuate it. I will explain the mechanism in a bit.

This is the Airbrake Fins attached to the Transition Bay. 

https://github.com/user-attachments/assets/e155a5e2-65f9-4150-ba08-11984518a05b

Time Spent: 7 hours

# Day 5 - 6/13/2025

Today, I focused on designing the other mechanisms to help the Airbrakes Actuate. I made these links here:
![image](https://github.com/user-attachments/assets/eec14abd-7f1d-4682-8fb6-a28223cbc820)
And this is the link holder I designed: ![image](https://github.com/user-attachments/assets/bee97b8c-5376-462f-aff7-c6a59f2cade1)

This is how the system works. When the bottom link holder moves up and down, the link also moves, which then rotates the airbrakes. This provides a very strong actuating mechanism, that can withstand a lot of G's

Here is a video showing how the Airbrakes Actuate: 


https://github.com/user-attachments/assets/33ceb665-7843-46b2-b39d-c41374ad93c8

Time Spent: 7 hours

# Day 6 - 6/17/2025

Today I worked on figuring out a motor to use. I also wanted this to be actuated with a Lead Screw. 
After some reasearch I decided on this motor: 
![image](https://github.com/user-attachments/assets/399e683b-cef4-4ecd-bb38-2c01605c6e67)

The reason I chose this motor, was because it had a high rpm, 10k rpm, twice as much torque as I needed, as calculated, and had an encoder, which would be helpful for the PID Control

In order to actuate the Airbrakes, I chose a T4 Lead Screw. The reason for this was because it could withstand high loads, had a 1 mm pitch, for fast actuation, and lots of torque to work with. This meant it would be perfectly compatible with the motor. 

However, the motor has an output shaft of a gear, and I had no way to connect that to the leadscrew, without some cad work.
I hopped onto Onshape, and quickly designed this ![image](https://github.com/user-attachments/assets/9a257c3d-5ca5-44b2-910d-36e7574811a5)

With this, I could clamp a threaded T4 Leadscrew, and clamp the motor gear to coupler. This way I could easily transfer the motion of the shafts. 

This is the fully assembled Motor Leadscrew Configureation:   ![image](https://github.com/user-attachments/assets/dd486b7a-cdd2-488e-b5ed-2ae1fbf87201)

Adding this motor, also meant I had to CAD a motor mount in the transition bay of the electronics to get the motor screwed and fixed on, to move the airbrakes. 
To do this, I added this circular mount here, intended to hold the motor in place, and 2 screw holes to screw into the motor and fasten it. The other mount, forward of the Motor mount, is the battery mount, to power the PCB and the Motor.

Here is the full assembly - ![image](https://github.com/user-attachments/assets/f1127872-4086-4637-914f-75140e01e7a4)

Time Spent: 6 hours

# Day 7 - 6/18/2025

Today I worked on the PCB of the Rocket. For this PCB, I had some requirements and criteria. First off, this PCB will be a flight computer, so that it will change the angle of the airbrakes throughout the launch, so that we will get a good altitude. 
In order to change the angle of the airbrakes, there needs to be an altitude sensor, and an accelerometer. Using an altitude sensor and an accelerometer, we can measure the height of the rocket, and the acceleration of the rocket at any given time. Using this data, we can derive the velocity of the rocket, by taking the derivative of the height of the rocket, and integrating the acceleration of the rocket. We can then use a complementery filter to combine the results of the altitude sensor and accelerometer, giving us a very smooth graph of velocity of the rocket at a given time. 
With this velocity graph, we can do a couple things. We can check whether or not the rocket's velocity is lower than, or higher than, the expected velocity, at the given time, to get to the expected altitude. If the rocket's velocity is lower than the optimal velocity, we lower the angloe of the airbrakes, to gain airspeed. If the rocket's velocity is higher than optimal velocity, we increase the angle of the airbrakes to lower airspeed. If we run this loop for the entire time of the flight, we can get very close optimal altitudes. 

Requirements for PCB: 
1) Barometeric sensor (altitude sensor) - resolution of under 1 ft and fast update to mcu
2) IMU (accelerometer) - fast update to mcu
3) MCU - chip that computes all the simulations and figures out whether to increase or decrease angle of airbrakes
4) Motor Driver - in order to actuate the airbrakes, we are using a motor, so we need a motor driver to control how fast the motor spins (when the motor spins, the airbrakes will open or close, depending on the direction the motor is spinning)
5) LED Lights - For testing purposes, and making sure the PCB functions properly
6) USB Micro/C port - For sending code

Parts I selected for PCB: 
1) Barometer - MS5607, 30 mhz refresh rate, 20cm accuracy
2) IMU - ICM42688, 25 mhz refresh rate, very precise
3) MCU - ESP32-Wroom-32e, 240mhz calculation speed, 2 xtensa cores, 2 spi ports, motor pwm support
4) Motor Driver - DRV8874, 6A Output Current (Max current of motor I am using), up to 12V (im using 7.4), uses EN/PH
5) Common LED Lights and USB Micro for easy connection

Time Spent: 4 hours

# Day 8 - 6/19/2025

Today I worked on the Schematic of the PCB
![image](https://github.com/user-attachments/assets/da8864f0-77fa-4878-893c-aaf2d1935334)
I designed this PCB in Easy EDA PRO. 
In order to get the voltage of the battery, 7.4V, down to 3.3V, I also had to use an LDO, which I didnt anticipate before. I also included some Boot and Reset Switches. 

Time Spent: 10 hours

# Day 9 - 6/21/2025

Today I worked on routing the PCB

I had some requirements: 
1) The USB had to be sticking out of the pcb
2) The 6 pin encoder header had to be on the top of the board
3) The 8 pin power header had to be on the bottom of the board
4) The LED's had to be in visual locations
5) 4 m3 screw holes
6) Optimally 2 layer pcb, but 4 layer is fine

This was the finished product: I used a 4 layer pcb because it was easier to route that way. I made the top and bottom layers signal layers, and the inner 2 layers, as 3.3v plane and GND plane, respectively, making it easier to route. 
![image](https://github.com/user-attachments/assets/5289a35a-6036-4012-ad1d-965ca61e29c4)
PCB 3d Model:
![image](https://github.com/user-attachments/assets/0263ebae-c166-4616-82e7-670d280157e9)

Time spent: 12 hours





