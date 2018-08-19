# Alpha
A 28-key semi-ortholinear mechanical keyboard designed by PyroL


# Build instructions
Orient the PCB correctly before you start the build: the blockers on the side closer to you, and the Pro Micro holes on the left. You should be able to read the "Too. Many. Keys." slogan on the side facing up.

![orientation](./instruction_photos/orientation.jpg) 

Step 0 (OPTIONAL): Install the stabilizer.

Step 1: Install and solder the diodes on the bottom of the PCB, with the black line facing the square pad. Cut the excess leads. 

Step 2: Mount the switches in the plate, and solder them all in.

Step 3 (OPTIONAL): place your LED strip on the bottom of the PCB, and cut three wires. The LEDs connect to the three-pin header next to the Pro Micro holes. Connect GND to the hole with a square pad, power to the middle hole, and Data In to the last hole.

Step 4a: Insert the short side of the Pro Micro standoffs into the bottom of the PCB, and solder them in. 

Step 4b: Mount the Pro Micro on the bottom of the PCB, smooth side facing you. Solder.

Final step: Assemble the case, flash (use my firmware or kbfirmware.com), and enjoy!

# To add:

- Plate design in both .svg and .ai (for lasercutting)

- PCB gerbers

- screenshots of default keymaps
