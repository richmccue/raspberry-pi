---
layout: default
title: 2 - Kiosk Computer
nav_order: 4
parent: Workshop Activities
---
<img src="images/RasPi_kiosk.PNG" style="float:right;width:180px;" alt="image description">

# Raspberry Pi: Kiosk Computer
If you have any questions or get stuck as you work through this in-class exercise, please ask the instructor for assistance. Enjoy!

## Installing Necessary Software
1. In order to set up the Raspberry Pi as a Kiosk Computer, you will need to significantly alter the Pi’s software.
  - The [previous step](https://richmccue.github.io/raspberry-pi/set-up-RasPi.html){:target="_blank"} has instructions on how to do so: 
2. Firstly, prepare the pi by entering these commands:
  - **sudo apt-get clean**
  - **sudo apt-get autoremove -y**
3. Now the latest versions must be installed, to do so, enter these commands:
  - **sudo apt-get update**
4. This may take a while, so as it is updating, let’s set up the slides we will display.
  - You can display any website you like, or you can use a google slideshow.
  - You can either create one now or use this one [here](http://bit.ly/dsc-signage2){:target="_blank"}.
5. Once the Pi is done updating, install xdotool and sed using this command:
  - **Sudo apt-get install xdotool unclutter sed**
  - **Sudo apt-get install x11-xserver-utils**
6. Navigate to the autostart directory, to do this, enter the command:
  - **cd /etc/xdg/lxsession/LXDE-pi/**
7. Now enter the command:
  - **sudo nano autostart**
8. In this nano editor, copy in these lines:
  - **@chromium-browser --kiosk --incognito [your url]**
  - **@xset s noblank**
  - **@xset s off**
  - **@xset -dpms**
  - **@unclutter -idle 0.1 -root**
9. Now, save and exit from nano.
  - In nano, do this keystroke: **ctl o** then **enter**, then **ctrl x**
10. Enter in this command to the command line:
  - **Sudo nano /etc/lightdm/lightdm.conf**
11. Now in this new nano window, find and uncomment (delete the # symbol) and edit this line:
  - **Xserver-command = X -s 0 -dpms**
12. Reboot the Pi:
  - **Sudo reboot**
13. To exit kiosk mode, do keystroke: **ctrl w**.




**UPDATE**
[NEXT STEP: Retro Pi](https://richmccue.github.io/raspberry-pi/retro_pi.html){: .btn .btn-blue }
