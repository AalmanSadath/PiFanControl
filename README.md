# PiFanControl
Low profile control of 5V non-PWM fan for Raspberry Pi with NPN transistor

## Components Required :
1. 5V Fan
2. 100 Ohm Resistor
3. C1815* NPN** transistor
4. 3 Pin Female Headers(like [these](https://cdn.sparkfun.com//assets/parts/1/0/5/00115-02-L.jpg))
5. 2 Pin Male Headers(like [these](https://s5.electrodragon.com/wp-content/uploads/2012/04/Break-Away-Header-Male-2.54-mm-Around-1.jpg))

*Other ECB NPN transistors can also be used.

**NON ECB transistors can also be used but tracks of PCB will need to be changed

All soldering and components are on the same side of the tracks to ensure short circuits and obstructions is not caused by other GPIO Pins

### Note
Pins 2,4 and 6 will be used by the PCB and Pins 3-24 will be blocked by the PCB (Pin Numbers are based on [this](https://cdn.sparkfun.com/assets/learn_tutorials/1/5/9/5/GPIO.png) diagram. *NOT GPIO NUMBERS*)

## Script to control Fan

### Dependencies
The only dependency is gpiozero library which is installed by default on Raspbian OS. If you are using any other OS install it with pip using

Python3:

`sudo pip3 install gpiozero`

Python2:

`sudo pip install gpiozero`

### Run the script 
Run the script on startup using crontab

`@reboot /wherever_the_script_is_located/fancontrol.py`
