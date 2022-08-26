---
layout: default
title: 1 - Setting up a Raspberry Pi
nav_order: 3
parent: Workshop Activities
---
<img src="images/Pi-logo.jpeg" style="float:right;width:180px;" alt="image description">

# Raspberry Pi: Getting Setup...
If you have any questions or get stuck as you work through this in-class exercise, please ask the instructor for assistance. Enjoy!

## Formatting the SD card and Installing Raspberry Pi OS

3. Download a copy of Raspberry Pi Imager from the [Raspberry Pi website](https://www.raspberrypi.org/downloads/raspbian/){:target="_blank"}. Instructions on how to set up your SD card with Raspberry Pi OS can be found [here](https://projects.raspberrypi.org/en/projects/raspberry-pi-setting-up/2){:target="_blank"}. 
4. Raspberry Pi OS is now installed onto the SD card! 
   - If you are on windows, eject the drive before removing the SD card.
   - If you are on a mac the drive will be ejected for you. Go ahead and remove the SD card.
   - Insert the card into the SD port of the Raspberry Pi, connect the peripherals, and power it up.

## Initial Setup of Raspberry Pi OS
5. With all peripherals installed, allow the Raspberry Pi to boot into the desktop.
   - The first thing you’ll be prompted to do will be to set up a new password, for the purposes of this lab set the password to be raspberry, or skip this step. 
   - When prompted, reboot your raspberry pi. 
   - Set the date and time on your raspberry pi:
      - Open the terminal by clicking on the icon on the top bar (see icon on right).
 <img src="images/setting_up_RasPi_image1.PNG" style="float:right;width:80px;height:100px;" alt="terminal."> 
      - In the terminal enter this command & press enter: **sudo date -s “mm/dd/yyyy hh:mm”**.
      - Once this is done, enter this command & press enter: **sudo apt-get update**. (Outside of workshop, you would want to upgrade as well, but that would take a long time so we will not!)
   - Navigate around, you’ll see a taskbar at the top of the desktop with the Chromium web browser icon (see right). Try launching it!
<img src="images/setting_up_RasPi_image2.PNG" style="float:right;width:80px;height:100px;" alt="taskbar."> 
      - After launching the web browser, see if you can connect to **google.ca**.
      - If you can, then your network settings are set up.

## Installing new Software on Raspberry Pi OS
6. In a new terminal shell, we will install Python.
7. Enter the command **sudo apt-get install gimp**.

## Basic Python Programming, Hello World and Nano
8. With Python installed, open the terminal and enter: **python3** l. A new prompt should show up “>>>”. This is the Python shell.
9. Here simple Python commands can be executed. Try entering **x = 5**, then **y = 8**. These variables, x and y, are now set as the values 5 and 8. 
   - Type in **x+y** and press enter. 
   - Try some other basic arithmetic commands with these variables!
   - When you’re done type: **exit()** and press enter.
10. In case we want to save a program, we need to be able to create new files. To do so, we will use nano.
   - Enter this command, **sudo nano hello_world.py**.
   - In the nano window, type in **message = ‘Hello, world!’** then on a new line **print(message)**.
   - Now, to save the file, enter the keystroke **ctrl+x**, then press **Y**, then **Enter**. You should now be back in the terminal.
   - From here, type in **python3 hello_world.py**.

## Extended Configuration
11. In the case that you need to, or want to, edit any of the core settings of the Raspberry Pi, open a terminal and execute this command: **sudo raspi-config**.
12. There are multiple configuration options here, to learn more checkout [this website](https://elinux.org/RPi_raspi-config){:target="_blank"}.
13. For an example of a useful feature, we will enable auto-login on the Raspberry Pi.
     - After executing **raspi-config** navigate to **Boot Options** and press **Enter**.
     - Navigate to **Desktop/CLI** then to **Desktop Autologin** and **Enter**.
     - You’ve now enabled autologin to the desktop.
    - Navigate to the main menu, and hit **Tab** then **Exit** and reboot the Pi. It should now autoboot.
    
## Important Things:
14. How to shutdown the Raspberry Pi
     - In the terminal, enter this command **sudo shutdown -h now**.
     - After installing large applications, update and upgrade your raspberry pi (ONLY UPGRADE WHEN YOU HAVE A LOT OF TIME).
















[NEXT STEP: Kiosk Computer](https://richmccue.github.io/raspberry-pi/kiosk-computer.html){: .btn .btn-blue }
