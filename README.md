# ESPHome-MultiSensor-Decora
This is a clone of my multisensor but designed to fit in a Decora plate package. It reliably detects human presence while tracking real-time changes in light, temperature, and humidity—all in one compact device.

You can automate environments based on what's actually happening in a room. Turn off lights when nobody’s around, adjust climate control to match the current occupancy, or simply collect detailed environmental data for your next project. Whether you’re into home automation, energy savings, or just cool data, this has got you covered.

Features:
* Human presence detection for responsive automation
* Ambient light sensingTemperature monitoring
* Humidity tracking
* Simple integration the popular platforms ESPHome and Home Assistant

Supplies:
  * esp32-c3 supermini → [Amazon](https://amzn.to/46SiDOh) bigger pack [Amazon](https://amzn.to/4jtJqYC)
  * breadboards → [Amazon](https://amzn.to/3TvAQ0U)
  * HLK-LD2410C Presence Sensors → [Amazon](https://amzn.to/4z05qyP)  FYI some precense sensors do not like ceiling fans. I have these in rooms with ceiling fans and they think that the room is occupied when the fan runs. I just take steps to avoid that. The b model can supposidly create an ignore zone but I do not have much issue with ceiling fans and this c model.
  * BH1750 Light Sensors → [Amazon](https://amzn.to/4e47EFg)
  * DHT22 Temperature and Humidity Sensors → [Amazon](https://amzn.to/4ys3nUs)

I do get a small commision for these links but I personaly did purchase these for this project.

OPTIONALS:

Any wiring accessories you may want like a [breadboard](https://amzn.to/3TvAQ0U), [wire](https://amzn.to/4AUwiCm), [jumper wire kit](https://amzn.to/4ypj52L) , [connectors](https://amzn.to/4rFU4hc), [usb-c cords](https://amzn.to/3VaIoXF) and [powerbricks](https://amzn.to/4hkBdoj).

Tools:

[Soldering station](https://amzn.to/4jf3w9d), [solder flux](https://amzn.to/3VYDqgL), [wire strippers](https://amzn.to/4jf3zBV)

Programing:

The esphome builder code is in the firmware folder. Please have a look and read. You must copy the components of the code you want into your own esphome builder device.

If you have a new C3 supermini it probably defaults to sleep and awake, over and over. You need to press and hold boot, then press reset and release, then release boot buttons. This method will allow the C3 supermini to program via usb.

Check out the Automation Examples.

Dashboard:

Example of fun badges for a room <img width="413" height="57" alt="Screenshot 2025-12-27 at 10 17 55 AM" src="https://github.com/user-attachments/assets/5e5d9b20-d28b-472b-a55c-b2dee6bfa59b" />

PCB: This is a PCB for this sensor. If you do not feel like building this on breadboard, purchase the PCB or have it made with the files.



Or the Gerber files are attached so you can have the PCB built yourself. Design also available at [oshwlab]()
