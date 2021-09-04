Filament sensor before and after extruder for Dragon Mini AB. Not tested in Dragonfly but it _should_ work.

# BOM
  
- [2x digital hall sensor](http://aliexpress.com/item/32312432947.html), doesn't matter if it's [latching or not latching](https://maker.pro/arduino/tutorial/how-to-use-a-hall-effect-sensor-with-arduino). I'm using U18
- [7x 4mm ball bearings](http://www.aliexpress.com/item/1005002383413769.html)
- [4x Disc magnets, diameter 5mm width 3mm](https://www.aliexpress.com/item/1005002226737225.html)
- 2x 10k ohm resistor

BOM If you only want a sensor before the extruder:
- 1x hall sensor
- 1x 4mm ball bearings
- 2x Disc magnets
- 10k ohm resistor

## Tools needed
- Multimeter

# Printed parts
- _Mid_Body.stl_ - Needed
- Recommended to print 2 copies of every hall sensor holder
- _Cowling_Dragon.stl_ - Not needed, print only if you don't have something to file

# Instructions
![Cut2](https://user-images.githubusercontent.com/67475249/132077526-349f1146-a096-41ef-b85d-1fae97070d25.png)
1. Insert 6 balls in **1**
2. Insert magnet in **1**
3. Make sure that magnet is around 2mm inside the tunnel, if not, then push it using filament or something similar
4. Load and unload filament checking that the magnet is moving around 2mm every time, it should reach the end of the tunnel. If the magnet is stuck, repeat step 3
5. Insert magnet in **3**, it has to repel magnet in **1**. If they atract, insert a 1.5 or 2mm drill bit in the hole in **3** to remove the magnet and insert again
6. Prepare hall sensor

 ![u18](https://user-images.githubusercontent.com/67475249/132078144-125efee8-cbf2-4fad-b4a4-a07cc85edf7b.PNG)
 
7. Test your circuit, move the hall sensor towards both magnets and check with a multimeter. Close to one it should read 5v and 0v in the other
8. Insert hall sensor in _HallSensorHolder145-145.stl_, and then in hole **2**, small face of sensor pointing towards **3**. **DON'T** use force yet
9. Load and unload filament and check with a multimeter, if voltage doesn't change, rotate hall sensor and check again
   * If it works, use force to push _HallSensorHolder145-145.stl_
   * If it doesn't work, remove _HallSensorHolder145-145.stl_ and use another one, the last 2 numbers in the filename are the wall width for each side. Repeat this step until it works
10. Repeat steps 1-9 for second sensor, but insert only 1 ball in **4**
11. Bend pins in both hall sensors, nothing can be taller than the highlighted part in the picture. Hot glue could be needed

![Capture](https://user-images.githubusercontent.com/67475249/132079892-3765e3a6-2719-4336-a23c-b147f8357271.PNG)

13. Route the cables. In the black circle in the second picture can be seen what needs to be filed. If you dont want to file, print _Cowling_Dragon.stl_


![Cable path](https://user-images.githubusercontent.com/67475249/132078872-913ee597-7d4d-4c8c-8d2f-637c7ced4135.jpeg)
![file](https://user-images.githubusercontent.com/67475249/132079048-aeaa3e7a-c9e1-4481-bddb-add37ee8c292.PNG)

 12. Choose any pin available in your board and connect the wires. RX2 and TX2 are recommended because they are next to each other and GND +5V. See _TestCode.txt_
 
 ![skr e3 2 0](https://user-images.githubusercontent.com/67475249/132079748-d0abf244-5354-479a-8e0c-bf18af6764ff.png)

# Photos
![Mid Body](https://user-images.githubusercontent.com/67475249/131930646-4e525b9a-e959-4d66-a8ba-3105bf5979fa.png)
![Final](https://user-images.githubusercontent.com/67475249/131932295-15f4ab81-08fd-4978-9525-03dfe47383a3.jpeg)
![Final 2](https://user-images.githubusercontent.com/67475249/131932313-80a32543-3dc1-4280-85ae-4797c5f7eb73.jpeg)
![Cut](https://user-images.githubusercontent.com/67475249/131930642-4eed7b00-6c50-4ca0-8c28-58445fdcd040.png)
