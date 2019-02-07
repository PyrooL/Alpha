# Alpha 

A 28-key semi-ortholinear mechanical keyboard designed by PyroL.

![example](https://i.imgur.com/LnNOKbX.jpg)

###### Photo by /u/Polyzhu.

## History

[First ever post](https://www.reddit.com/r/MechanicalKeyboards/comments/7nz4ge/ic_i_was_challenged_to_reduce_the_gherkin_and/?ref=share&ref_source=link)

[PCB protos arrive](https://www.reddit.com/r/MechanicalKeyboards/comments/887hxn/its_so_cute_c/?ref=share&ref_source=link)

[GB opens](https://www.reddit.com/r/MechanicalKeyboards/comments/8djw3d/gb_alpha_28key_keyboard/?ref=share&ref_source=link)

# Build instructions

## Parts

- [ ] 1x Alpha PCB
- [ ] 28x 1N4148 or equivalent diodes
- [ ] 1x Pro Micro (**NOTE:** USB-C ports are experiencing some clearance issues since it's taller than Micro-B)
- [ ] 1x Case or plate set
- [ ] 5x 10mm M3 standoffs
- [ ] 10x 5mm M3 screws
- [ ] 28x MX or Alps style switches of your choice
- [ ] 1x Micro USB cable

## Tools

- [ ] Soldering station
- [ ] Wire cutter
- [ ] Screwdriver

## Before you start

Orient the PCB correctly before you start the build: the blockers on the side closer to you, and the Pro Micro holes on the left. You should be able to read the "Too. Many. Keys." slogan on the side facing up.

![orientation](photos/instructions/orientation.jpg) 

(OPTIONAL): Install a 2u stabilizer.

## Step 1: Diodes

Install and solder the diodes on the bottom of the PCB, with the black line facing the square pad. Cut the excess leads. 

![diodes](photos/instructions/diodes.jpg)

## Step 2: Pro Micro
Insert the short side of the Pro Micro standoffs into the bottom of the PCB, and solder them in from the top.

![pmicro standoff bottom](photos/instructions/pmicro1.jpg)

![pmicro standoff soldered](photos/instructions/pmicro2.jpg)

Mount the two switches that will sit in between the Pro Micro standoffs in the plate and solder them into the PCB at that location. Clip the extruding switch pins after soldering to ensure the Pro Micro will sit flat. 

![pmicro switches](photos/instructions/pmicroswitches.jpg)

Mount the Pro Micro on the bottom of the PCB, smooth side facing you. Solder.

![pmicro](photos/instructions/pmicrosoldered.jpg)

[bakingpy has an awesome guide](https://imgur.com/a/M9r3EW9) for an even lower-profile Pro Micro mounting solution that works with Alpha!

**Very important:** after soldering, (regardless of if you mounted normally or bakingpy-style,) use a wire cutter to clip as much of the protruding standoff as possible. With 10mm standoffs this is a snug fit, and it is impossible with the standoffs at full length. Reflow your solder if it climbed up the wire.

## Step 3: Switches

Mount the switches in the plate, and solder them all in. Careful for bent pins!

![switches](photos/instructions/switches.jpg)

## Step 4 (OPTIONAL): LED strip

Remove the 3M adhesive strip on the back of your LED strip and place it on the bottom of the PCB. Cut 3 wires of similar length, preferably of different colors. The LEDs connect to the three-pin header next to the Pro Micro holes. Connect GND to the hole with a square pad, power to the middle hole, and Data In to the last hole.

If there ever is a rev 2, I will put the holes in the right order...

![arrgeebee](photos/instructions/rgb.jpg)

## Step 5: Case and firmware

Assemble the case: for each hole, pass a screw through the top plate, screw in a standoff to finger tightness, then screw in through the bottom plate. Once all screws and standoffs are installed, use a screwdriver to tighten as needed (but not too tight, as acrylic can be brittle!). Flash using QMK (use my firmware, or kbfirmware.com), and enjoy!

Don't forget to send me a pic of your build at @PyroL#7672 on Discord or /u/pyrocrastinator! I'd love to see what you guys do with these!
