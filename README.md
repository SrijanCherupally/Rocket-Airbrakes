# Rocket-Airbrakes

I am participating in a rocket competition. I need to build a rocket that goes to a specific altitude. However, due to wind, air pressure, humidity, and multiple other factors, it is virtually impossible to reach that altitude consistently. To solve this problem I am developing an active altitude control module that uses Active Control Airbrakes that adjust the drag of the rocket to get to the altitude very consistently.


There are 3 parts to this project. 1) Designing the mechanism of the Airbrakes to actuate, 2) Designing the PCB to control the Airbrakes, 3) Building the Airbrakes, 4) Coding and optimizing the Airbrakes.

I have documented my journey towards step 2, and will continue documenting as I will build the Airbrakes and Code them in the future. 


Airbrake Image: ![image](https://github.com/user-attachments/assets/e4fb83cd-f052-4559-a8c0-0434a8f0971d)

PCB 3d Image: ![image](https://github.com/user-attachments/assets/672eac3e-356c-41ce-8417-036675c4c187)

PCB Image: ![image](https://github.com/user-attachments/assets/22efb334-d5de-45bb-a409-8770c8de8b84)

## Bill of Materials

| **Item Name**            | **Purpose**                                                   | **Link**                                                                                                                                                    | **Cost (USD)** | **Note**                                                                                     | **Quantity** |
|--------------------------|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------|----------------------------------------------------------------------------------------------|--------------|
| Flight Computer PCB      | To control the motor, and get to right altitude               | Online Quotation *(Can't share)*                                                                                                                            | 160.66          | 2 qty's inside the order because minimum order                                               | 1            |
| Polulu DC Motor          | To actuate the Airbrakes using lead screw                     | [Pololu DC Motor](https://www.pololu.com/product/4800)                                                                                                      | 60.00          |                                                                                              | 1            |
| JLC CNC Shaft Adapter    | Shaft adapter between Motor Shaft and Lead Screw              | Online Quotation *(Can't share)*                                                                                                                            | 100             |                                                                                              | 1            |
| T4 Lead Screw            | To convert motor rotation to linear movement                  | [AliExpress - T4 Lead Screw](https://www.aliexpress.us/item/3256804956186452.html)                                                                         | 15             |                                                                                              | 1            |
| 6, 3, 2, 8 pin Headers   | To solder onto the PCB for less money charged                 | Online Quotation *(Can't share)*                                                                                                                            | 10             | This actually saves money compared to having JLC wave solder it for me                      | 1            |

**Total Cost:** **$345.66**
