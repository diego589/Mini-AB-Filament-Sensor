# UNDER CONSTRUCTION - NOT RECOMMENDED TO PRINT YET
Working on bowden fitting

# Filament sensor for Dragon Mini AB
I wanted to create an invisible filament sensor inside the toolhead to check if the filament runs out or if there is a clog in the extruder gears. Tested on Dragon normal flow, not tested on Dragonfly, but it should work.

![f1](/Images/Comparison.jpeg)

# BOM
## For both (before and after the extruder's gears)
- [2x digital hall sensor](http://aliexpress.com/item/32312432947.html), it doesn't matter if it's [latching or not](https://maker.pro/arduino/tutorial/how-to-use-a-hall-effect-sensor-with-arduino). I'm using U18
- [7x 4mm ball bearings](http://www.aliexpress.com/item/1005002383413769.html)
- [4x 5mm x 3mm Round Neodymium Magnets](https://www.aliexpress.com/item/1005002226737225.html)
- 2x 10k ohm resistor
- [Thin wires, 32 AWG recommended](https://www.aliexpress.com/item/32882386535.html)

## BOM If you only want a sensor before the gears:
- 1x Digital hall sensor
- 1x ball bearing
- 2x Magnets
- 1x resistor
- Thin wires

## BOM If you only want a sensor after the gears:
- 1x Digital hall sensor
- 6x ball bearings
- 2x Magnets
- 1x resistor
- Thin wires

## Tools
- Multimeter

# Printed parts
- _[a]FS_Mid_Body.stl_ - Needed
- Recommended to print 2 copies of every hall sensor holder
- _[a]FS_Cowling_Dragon.stl_ - Not needed at all, but print it if you don't want to sand it down (step 13)

# Assembly
![f2](/Images/Numbers.png)
1. Insert 6 balls in **1**
2. Insert magnet in **1**
3. Make sure that magnet is around 2mm down the tunnel, if not, then push it using filament or something similar
4. Test your clearances by inserting filament, when there is no filament the magnet should be 2mm down the tunnel and when the filament is loaded, the magnet should raise up about 2mm

https://user-images.githubusercontent.com/67475249/134376186-ed08a0d5-9afd-461a-8bc8-b10c32558bfe.mp4

6. Insert a magnet in **3**, it should repel the magnet in **1**. If you inserted it in the wrong orientation use an 1.5 or 2mm drill bit to remove it out of the hole
7. Prepare hall sensor, solder resistor at no less than 10 cm from the sensor

![f5](/Images/u18.PNG)
 
8. Test your circuit, move the hall sensor towards each magnets and check with a multimeter between GND and OUT, it should read 5v next to one and 0v next to the other
9. Insert the hall sensor in _[a]HallSensorHolder145-145.stl_, then insert the holder with the sensor in **2** (small face of sensor pointing towards **3**). **DO NOT** force it yet
11. Load and unload filament and check with a multimeter if there is any variation, if the voltage doesn't change, rotate hall sensor and repeat
   * If everything is working, push the hallsensor holder in place
   * If it's not working, remove it and try with a different sensor holder, then repeat
12. For the sensor that goes before the gears follow the same instructions but use just 1 ball bearing instead
13. Bend the sensor pins until they are below the highlighted part (image below)

![f6](/Images/Limit.PNG)

13. Route your cable following the path as shown in the image below. If you didn't print _[a]FS_Cowling_Dragon.stl_ you have to sand a path down yourself (black circle in image below)

<img src = "/Images/Path.jpeg" height = 300> <img src = "/Images/Path2.PNG" height = 300>

14. Choose any available pin on your board. In this case I am using RX2 and TX2 because they are right next to GND and +5v. See _TestCode.txt_
 
![f9](/Images/skre3-2.0.png)

# Photos
<img src = "/Images/Cut.png" height = 400> <img src = "/Images/Final.jpeg" height = 400>
<img src = "/Images/MidBody.png" height = 400> <img src = "/Images/Sensors.jpeg" height = 400>
