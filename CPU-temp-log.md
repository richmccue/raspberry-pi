---
layout: default
title: 4 - CPU Temperature Log
nav_order: 6
parent: Workshop Activities
---
<img src="images/CPU_temp_log_image1.PNG" style="float:right;width:180px;" alt="image description">

# Raspberry Pi: CPU Temperature Monitor 

## Installing Necessary Software
1. Open up a terminal shell, this can be done by clicking on this icon on the right: 
<img src="images/setting_up_RasPi_image1.PNG" style="float:right;width:80px;height:100px;" alt="terminal."> 
  - Alternatively, a new shell can be opened by pressing **crtl + alt + t**.   
2. Next, ensure that matplotlib is installed by entering the command **sudo apt-get install python3-matplotlib**. 
3. If it installs or confirms that matplotlib is installed, proceed to the next step. 

## Creating the Python Script
1. Open a new blank Python file by **Menu > Programming > Mu**. 
  - The menu is the RaspberryPi logo in the top left.  
2. After launching Mu, select **Python 3** and click **OK**.  
3. In Mu, under the first commend enter in these lines of code:
  - **from gpiozero import CPUTemperature**
  - **cpu = CPUTemperature()**
4. Save the program as **temp** then click **Run**.
  -  A run time menu will appear with a >>> as a prompt. 
  -  Type in **cpu.temperature** to this prompt to get a temperature readout of the CPU in Celcius. 
5. Now, let’s make the script more robust by having a log of the temperatures. To do this, copy in the following lines:


**from gpiozero import CPUTemperature**

**from time import sleep, strftime, time**

**from gpiozero import CPUTemperature**

**cpu = CPUTemperature()**

**with open(“cpu_temp.csv”, “a”) as log:**

**while True:**             
	
**temp = cpu.temperature**
		
**log.write(‘{0},{1}\n’.format(strftime(‘%Y-%m-%d %H:%M:%S’), str(temp)))**
		
6. Running this code will keep a log in the form of a CSV in the designated folder. This folder can be found in /home/pi and will be called cpu_temp.csv. 
7. Try running the code and finding the file.
8. Now that a log is kept, visualization in the form of a real time graph can be scripted.
9. Copy over the following code to the script, save and run.

**from gpiozero import CPUTemperature**

**from time import sleep, strftime, time**

**import matplotlib.pyplot as plt**

**cpu = CPUTemperature()**

**def write_temp(temp):**

**with open(‘cpu_temp.csv’, ‘a’) as log:**

**log.write(‘{0},{1}\n’.format(strftime(‘%Y-%m-%d %H:%M:%S’), str(temp)))**
		
**def graph(temp):**

**y.append(temp)**
**x.append(time())**
**plt.clf()**
**plt.scatter(x,y)**
**plt.plot(x,y)**
**plt.draw()**

**while True:**

**temp = cpu.temperature**
**write_temp(temp)**
**graph(temp)**
**plt.pause(1)**

10. Save and run this script to get a graph of the current cpu temperature.

## Automating the Script
1. This Python script can be made to run automatically on boot.
2. Open a new terminal and enter in **crontab -e** to open crontab. If prompted, choose nano from the options given. 
3. Scroll to the bottom of the opened file and enter in this line in a new line:
    **@reboot python3 /home/pi/temp.py**
4. Now, reboot the Raspberry Pi by entering the command **sudo reboot**.
5. Once the pi has reboot and run for a bit, enter the command **cat cpu_temp.csv**.
6. This will display a log of the recent CPU temperature.
