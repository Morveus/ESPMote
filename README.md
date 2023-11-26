
# Telemancer Remote Controller

Prototype / Work in Progress

![image](https://github.com/Morveus/Telemancer/assets/2972468/2c8ca5fb-0bcc-4e78-be88-ea0fa42ffef1)

I've been looking for a good-looking, functional remote that can interact with my home automation setup. I've never been able to find something that works for me:

* That is simple,
* Open Source,
* Can interact with HTTP ; I don't care about infrared or RF, because my HomeAssistant instance can act as a bridge,
* Isn't tied to a hub: the calls would originate directly from the device,
* Isn't Not cloud-based,
* Isn't subscription-based,
* Can work with Kodi,
* Isn't a smartphone : can be used in the dark, with buttons you can feel with your fingers and know which one does which without looking,
* Uses a rechargeable battery, ideally a standard one like the 18650 or maybe a bit smaller

The idea is to build a WiFi remote that will send HTTP/HTTPS API calls to any endpoint (to me, it will be HomeAssistant, Yamaha MusicCast, Kodi, Philips Hue...). I also very much like the nVidia Shield remote's form factor, so that's the idea I've asked a CAD designer to work on.

Here's a TODO of the project and my current advancement:

 - 🟢 ESP32 running MicroPython
 - 🔴 Catching exceptions
 - 🟢 Rudimentary Web WiFi Setup
 - 🟢 Rudimentary Web Server
 - 🟢 Multiple Profiles (for instance 1 = Kodi, 2 = Trinnov, 3 = HomeAssistant, 4 = Yamaha)
 - 🟢 Up, Down, Left, Right, OK buttons
 - 🟢 Power and Reset Buttons
 - 🟢 Back and Home buttons
 - 🟢 Customizable behaviors: 
	 - 🟢 "Press Once": holding a button will only trigger the call once
	 - 🟢 "Press and repeat until released": such button would repeat the same command (navigation, volume...)
	 - 🟢 Repeat rate can be set (in ms) for each button
	 - 🟢 Buttons can have a secondary mode (longpress)
 - 🟠 WiFi connectivity
 - 🔴 4 diodes that tell you which profile is currently set
 - 🔴 (Maybe) backlit buttons
 - 🟠 Web Interface
 	- 🟢 Profile Names Management
  	- 🟢 Adding and Deleting API tokens
   	- 🟠 Managing buttons settings
   	- 🔴 Prettier UI/UX (ultimately limited, but not an excuse for an ugly UI)
 - 🔴 PCB design (made by a friend)
 - 🟠 Prototype mechanical design (awaiting quotations $$$)
	 - 🔴 First, 3D printable
	 - 🔴 Then, prototyped with silicon mold injection
 - 🔴 Beeper, to allow you to find the remote when lost between the seats by sending an HTTP call to its internal webserver
 - 🔴 Accelerometer allowing the backlight and profile LEDs to turn on when the remote is picked up (like on the nVidia Shield remote), before turning off after a specified, customizable amount of time
 - 🔴 Battery (18650) and charger
 - 🔴 USB-C connector

Maybe later, depending on how successful this project is:
 - 🔴 Infrared
 - 🔴 Bluetooth
 - 🔴 Charging base/dock

![image](https://github.com/Morveus/Telemancer/assets/2972468/af39033d-38a7-4694-a77c-d320b26f7710)

(please don't mind the PCB sketch which is totally random, I don't know anything about PCB design)
