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
- [ ] 28x MX, Alps, or Kailh Choc style switches of your choice
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

Remove the 3M adhesive strip on the back of your LED strip and place it on the bottom of the PCB. Cut 3 wires of similar length, preferably of different colors. Connect VCC, GND, and Data pins on the strip to their respective pins on the PCB.

v1.1 and onwards has pins labeled and in the same order as they come on the strip!

[**If you are using a v1.0 PCB (one that does not have RGB pins or version number labeled) see here for wiring guide**](photos/instructions/rgb.jpg)

## Step 5: Case and firmware

Assemble the case: for each hole, pass a screw through the top plate, screw in a standoff to finger tightness, then screw in through the bottom plate. Once all screws and standoffs are installed, use a screwdriver to tighten as needed (but not too tight, as acrylic can be brittle!). Flash using QMK (use my firmware, or kbfirmware.com), and enjoy!

Flash steps:

- Download [QMK Toolbox](https://github.com/qmk/qmk_toolbox)
- Ensure that you have an appropriate firmware file.
  - For Vial, you can download one off of [keyboard.gay](https://keyboard.gay)
- Open QMK Toolbox. Plug your PCB in, and press the SKQG reset button (or short the appropriate headers). You should see the device connect for ~10 seconds, then disconnect.
- Within QMK Toolbox, choose your appropriate firmware file, then check the "Auto-Flash" button.
- Reset your board again. The firmware should be automatically flashed onto the board.

Don't forget to send me a pic of your build at @PyroL#7672 on Discord or /u/pyrocrastinator! I'd love to see what you guys do with these! 

# Changelog
* v1.1 3/2/19

Added SKQG reset button pads (no need to manually short reset!) and fixed RGB pin order to match common SK6812/WS2812 pinout, and added silkscreen labels to RGB pins.

* v1.2 4/27/19

Diodes now are combo through-hole and SMD compatible! Breakout pins for artisan column ("tmo28") added on both sides. Routing cleaned up etc. 

* v2.0 7/21/19

Choc footprints added! Also support for first version of "TMO28", an artisan column that's still being worked on. 

* v2.1 9/1/19

Fixed disconnected D4, see [here](https://www.instagram.com/p/B15MHgMnYID/?igshid=1266ym89zlw4w) or contact me for fix if you are affected. Only affects v2.0.

* v2.2 7/24/20

Removed TMO28 breakout pins for cleaner look. Version with breakouts still available in `breakoutholes` branch. 
