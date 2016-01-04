# Connairpi

## About
Lets the Raspberry Pi pretend to be a ConnAir remote control

Receive commands from the PowerSwitch Android App
http://power-switch.eu/download/


## Credits
* sui li for creating RCSwitch for the arduino
* r10r for porting RCSwitch to the raspberry

## Required Hardware
* Raspberry Pi
* 434 Mhz transmitter
* Some radio controlled power sockets

## Setup
* Install wiringPi. See https://projects.drogon.net/raspberry-pi/wiringpi/
* Checkout this project
* Compile it
* Connect pin11 of the raspberry to the transmitter
* Edit the location of the daemon in the init script (raspberry-remote-powerswitch)
* Copy it to /etc/init.d: sudo cp raspberry-remote-powerswitch /etc/init.d
* Make it start on boot: sudo update-rc.d raspberry-remote-powerswitch defaults

## Usage
Configure PowerSwitch with the IP of the Raspberry and the outlets you want to control
