# Tamaguino
This is a fork of the Tamagotchi clone for Arduino. More information on the original creater can be found at:
https://alojzjakob.github.io/Tamaguino/

![20230727_final2](https://github.com/JackEverson/Tamaguino/assets/111256162/e29aaff4-94b3-4f63-adff-7dc8aa3477a1)

I wanted to undertake this project for a number of reasons:
1. Exposure to using LiPo rechargable batteries. This was a great introduction to being able to start making my electronic projects more portable.
2. Exposure to using OLED display module (SSD1306). This is a great way to display real-time information from a microcontroller and being able to control this sort of hardware opens up a lot of future potental in projects I undertake.
3. Exposure to the Arduino pro mini and the use of an external UART (FTDI USB to TTL) to program the microcontroller. Using the pro mini will allow me to produce devices with a much smaller form factor in the future. 
4. My wife really wanted an Tamaguino pet!

# Building the project
## Prototyping
Initially, I tested the code and peripheral hardware out using an Arduino Uno to make sure everything was working as it should be. I did find that there were some not enough memory issues initially and discovered this was due to the modern versions of <Adafruit_GFX.h> and <Adafruit_SSD1306.h> libraries. Changing these to version 1.1.5 and 1.1.2 respectively allowed for flashing the full program onto the Uno and allowed it to run as intended.

![20230720_prototyping](https://github.com/JackEverson/Tamaguino/assets/111256162/44eaab1a-4e54-4f20-9e93-2c9141626534)

## LiPo battery
The LiPo battery was very easy to intergrate. Attaching the Makerverse USB-C LiPo battery charging circuit was a simple case of reading the documentation, connecting the correct wires to the correct sockets, and ensuring the circuit was set to its maximum 500mA setting (the LiPo battery was rated to recieve 1A of charging current (well technically 2A, but the wires it came with were only rated to 1A) which gave a bit of piece of mind that my first endeavour with LiPo batteries wouldn't end poorly. 

![20230720_batterytest](https://github.com/JackEverson/Tamaguino/assets/111256162/82cdd539-1fdc-40ed-9d49-50ecae7c41ef)

## 3D Printing case
I downloaded a pre-designed case for this project (https://www.thingiverse.com/thing:2120692). In hindsight I wish I had designed my own case from scratch as I had a number of issues with hardware fitting and the case itself did not print very nicely due to a lot of overhang areas (despite putting in supports). In future I would like to come back to this project and build my own 'Tamaguino' from scratch at which time I would also like to design a better case (likely something that looks like a Gameboy shape than a Tamagotchi/digimon shape).

![20230722_3dprinting](https://github.com/JackEverson/Tamaguino/assets/111256162/613eb3a6-65b7-48ed-a83a-91d2415c5593)

## Assembly
I chose to handwire and hot glue this project together as it was the simplest solution at the time. While all the components ended up fitting it was very tight. I was hoping that handwiring and using connector pins I would easily be able to either upgrade or salvage components later on when I chose to revisit this. However, as it can be seen in the pictures, the handwiring ended up becoming very chaotic and spaghetti like and is not necissarily that upgradeable or salvageable due to the hot glue. In the future I would like to try my hand at designing a PCB that could incorporate all the components. This would make things look much neater on the inside of the device and make the device less painfull to open and close.

![20230723_assembly1](https://github.com/JackEverson/Tamaguino/assets/111256162/529da4df-5131-416c-a767-cc474fa70c95)

![20230727_assembly2](https://github.com/JackEverson/Tamaguino/assets/111256162/3619c544-5e5b-4398-84a7-45bd04fc9f90)

# Final product
The final product came out quite well (despite the dodgy 3D print job) and has so far worked without fault. 

![20230727_final1](https://github.com/JackEverson/Tamaguino/assets/111256162/7cbcb15a-58bf-4149-b272-201b75f38cbb)
