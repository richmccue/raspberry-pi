---
layout: default
title: 3 - Retro Pi
nav_order: 5
parent: Workshop Activities
---
# Raspberry Pi: Retro Gaming with RetroPi
If you have any questions or get stuck as you work through this in-class exercise, please ask the instructor for assistance. Enjoy!

## Installing Necessary Software
- Install a copy of RetroPi at [this site](https://retropie.org.uk/download/){:target="_blank"} for the appropriate hardware.
- After getting the image, run etcher and load the image onto the microSD card.
- This may take a while, so as it loads, go to [this site](https://www.downloadroms.io/){:target="_blank"}  to find some ROMs you’d like to play! 
- Once finished, insert the microSD into the RaspberryPi and turn it on.
- You will now configure the game controller, for this lab, we will use the keyboard.
- TO SKIP OTHER STEPS hold down any already bound key. Continue doing this for keys not listed.
- Ensure that the d-pad up, down, left, right keys are set (suggest WASD for these).
- Ensure that the A,B,X, and Y buttons are bound (numpad up, right, left, and down are recommended).
- The A button will be your primary selection method as opposed to a keyboard and mouse.
- Ensure start and select are bound (z and x recommended).
- At this point, you will skip a lot of buttons until the botbutton is reached at the bottom of the menu.
- Ensure that the HOTBUTTON is set (suggest ENTER).

## Downloading and Running New Game Software
- After downloading a couple of ROMs, we need to setup a USB stick to hold these ROMs.
- With a blank USB stick, format it to a FAT32 or NTFS format.
- Create a file in the USB stick, and name it retropie.
- Ensure that the Pi is turned off at this point before continuing.
- Plug the USB into the pi, and wait for the pi to stop blinking (about a minute).
- Let the Pi completely boot to the retropie main menu. 
- Reboot the Pi by hitting the F4 key and typing into the terminal sudo reboot.
- Then shutdown the pi and unplug the usb.
- Load the ROMs into the retropie/roms folder.
- Now you can plug it back in and play.

## Accessories
-  If you would like to do this at home, a USB game control will work well for most games.
-  A keyboard and mouse are good things to have installed at all times. If something goes wrong you can quit to a terminal menu with the ctrl+f1 key combo.


[NEXT STEP: Retro Pi](https://richmccue.github.io/raspberry-pi/retro_pi.html){: .btn .btn-blue }
