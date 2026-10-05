# ESPHome MultiSensor – Decora

A compact **ESPHome multi-sensor designed to fit into a standard Decora-style wall plate**.

This project is based on my original ESPHome MultiSensor, redesigned to create a cleaner, wall-mounted installation. It combines **human presence detection, ambient light, temperature, and humidity sensing** into one device that integrates directly with ESPHome and Home Assistant.

<p align="center">
  <img width="350" alt="Decora Multi-Sensor Assembly" src="https://github.com/user-attachments/assets/1c8466a2-de4e-4e23-90db-ebf8baf1f53b" />
  <img width="350" alt="Decora Wall Plate Front" src="https://github.com/user-attachments/assets/203d0dd1-3c14-47d9-b6b2-7f3a692d36b6" />
  <img width="350" alt="Decora Wall Plate Back" src="https://github.com/user-attachments/assets/7e219685-9b3e-45d3-bb33-f54c38a45d30" />
</p>

## What It Does

The goal of this project is to give Home Assistant a better idea of what is **actually happening in a room**.

With presence and environmental data available in Home Assistant, you can create automations such as:

- Turn lights off when a room is no longer occupied
- Turn lights on based on both presence and ambient light
- Adjust HVAC based on room occupancy and temperature
- Track temperature and humidity throughout the house
- Build room-level dashboards and occupancy indicators
- Use presence information as part of more advanced automations

Whether you're interested in home automation, energy savings, environmental monitoring, or just collecting some cool data, this little sensor can do quite a bit.

## Features

- Human presence detection
- Ambient light sensing
- Temperature monitoring
- Humidity monitoring
- ESP32-C3 based
- ESPHome firmware
- Native Home Assistant integration
- Designed for a Decora-style wall plate
- Optional custom PCB
- 3D-printable enclosure components

## Hardware

### Main Components

- **ESP32-C3 Super Mini** → [Amazon](https://amzn.to/46SiDOh)  
  Larger pack → [Amazon](https://amzn.to/4jtJqYC)

- **HLK-LD2410C mmWave Presence Sensor** → [Amazon](https://amzn.to/4z05qyP)

- **BH1750 Ambient Light Sensor** → [Amazon](https://amzn.to/4e47EFg)

- **DHT22 Temperature & Humidity Sensor** → [Amazon](https://amzn.to/4ys3nUs)

- **Breadboards** → [Amazon](https://amzn.to/3TvAQ0U)

### A Note About Ceiling Fans

Some mmWave presence sensors can detect the movement of a ceiling fan and report the room as occupied.

I've used the **LD2410C** in rooms with ceiling fans and have generally had good results, although you may need to adjust the sensor configuration or account for the fan in your automations.

Other versions of the LD2410, such as models that support configurable detection or exclusion zones, may provide additional options depending on your installation.

## Optional Supplies

Depending on how you build the project, you may also want:

- [Breadboard](https://amzn.to/3TvAQ0U)
- [Wire](https://amzn.to/4AUwiCm)
- [Jumper Wire Kit](https://amzn.to/4ypj52L)
- [Connectors](https://amzn.to/4rFU4hc)
- [USB-C Cables](https://amzn.to/3VaIoXF)
- [USB Power Adapters](https://amzn.to/4hkBdoj)

## Tools

A few basic electronics tools will make the build much easier:

- [Soldering Station](https://amzn.to/4jf3w9d)
- [Solder Flux](https://amzn.to/3VYDqgL)
- [Wire Strippers](https://amzn.to/4jf3zBV)

> **Affiliate Disclosure:** Some of the Amazon links above are affiliate links. I may receive a small commission if you purchase through them at no additional cost to you. These are components and tools that I personally purchased or used for this project.

## ESPHome Firmware

The ESPHome configuration for this project is located in the **Firmware** folder.

Have a look through the configuration before using it. Depending on your hardware and Home Assistant setup, you may need to copy or modify portions of the configuration for your own ESPHome device.

### Programming the ESP32-C3 Super Mini

Some new ESP32-C3 Super Mini boards may repeatedly enter a sleep/reset cycle and can be difficult to flash initially.

If the board will not enter programming mode:

1. Press and hold the **BOOT** button.
2. While continuing to hold BOOT, press and release **RESET**.
3. Release the **BOOT** button.
4. Try flashing the ESP32-C3 again over USB.

Once programmed, ESPHome should be able to manage subsequent firmware updates normally.

## Automation Examples

Check out the **Automation Examples** included with the project for ideas on how the sensor data can be used inside Home Assistant.

Presence, light level, temperature, and humidity become much more useful when they're combined into room-level automations.

## Home Assistant Dashboard

Here's an example of some simple room-status badges using the sensor data:

<p align="center">
  <img width="500" alt="Home Assistant room sensor badges" src="https://github.com/user-attachments/assets/5e5d9b20-d28b-472b-a55c-b2dee6bfa59b" />
</p>

## Custom PCB

I designed a custom PCB for the Decora MultiSensor to make the project cleaner and easier to reproduce.

Instead of assembling everything on a breadboard or using a large amount of point-to-point wiring, the PCB provides a dedicated platform for the ESP32-C3 and sensor components.

<p align="center">
  <img width="350" alt="Decora Multi-Sensor PCB" src="https://github.com/user-attachments/assets/46c16b05-94ea-4fc2-b687-688e333620cf" />
  <img width="350" alt="Assembled Decora Multi-Sensor PCB" src="https://github.com/user-attachments/assets/1c8466a2-de4e-4e23-90db-ebf8baf1f53b" />
</p>

The PCB design files are available in the **PCB** folder of this repository.

Gerber files are also included if you'd like to have the board manufactured yourself.

The design is also available on [OSHWHub / OSHWLab](https://oshwlab.com/rockdown/project_jdyzuzoz).

You can still build the sensor without the custom PCB. The PCB is simply intended to make the finished project cleaner, more compact, and easier to assemble.

---

## 3D Printed Enclosure

A custom 3D-printable enclosure and Decora-style faceplate were designed specifically for this project.

The enclosure holds the sensor hardware behind the wall plate while providing the necessary openings for the presence, light, temperature, and humidity sensors.

### Printed Parts

The 3D-printable files can be found in the **3D Print** folder of this repository.

**Front**

<img width="350" alt="Decora 3d Print Front" src="https://github.com/user-attachments/assets/5aa9dc7d-66fc-4684-86fa-1d7737969b84" />

**Back**

<img width="350" alt="Decora 3d Print Back" src="https://github.com/user-attachments/assets/021b8a54-d299-475c-9904-b61ca8b34ae0" />

### Print Settings

Recommended starting settings:

- **Material:** PLA or PETG
- **Layer Height:** 0.20 mm
- **Supports:** TBD
- **Infill:** TBD
- **Wall Loops:** TBD

I'll update these settings as the enclosure design is finalized and tested.

The enclosure is still being refined, so check the repository for the latest version before printing.


---

## Project Status

This project is actively being developed and improved. PCB revisions, enclosure updates, firmware changes, and additional automation examples may be added as I continue testing the design.

If you build one, modify the design, or come up with a useful automation for it, feel free to share your version.

## Purchase Options

If you'd rather skip some of the fabrication and assembly, I have several options available for the **ESPHome MultiSensor Decora**.

You can still build everything yourself using the PCB, 3D print, and project files included in this repository.

### 3D Printed Decora Enclosure

For anyone who wants the custom printed Decora enclosure without printing it themselves:

[Purchase 3D Printed Enclosure](https://py.pl/9J00K)

### Decora MultiSensor PCB

For anyone who wants the custom PCB and plans to supply and assemble their own components:

[Purchase MultiSensor Decora PCB](https://py.pl/2Ezptq)

### Fully Built MultiSensor Decora

Want to skip the soldering and assembly? This option includes the PCB with all of the MultiSensor components installed.

[Purchase Fully Built MultiSensor Decora](https://py.pl/29uClh)

> **Note:** The project remains open for DIY builds. PCB design files, firmware, 3D-printable files, and project documentation are available in this repository if you'd rather build your own.

**Learn it. Build it. Put it into practice.**## Purchase Options

If you'd rather skip some of the fabrication and assembly, I have several options available for the **ESPHome MultiSensor Decora**.

You can still build everything yourself using the PCB, 3D print, and project files included in this repository.

### 3D Printed Decora Enclosure

For anyone who wants the custom printed Decora enclosure without printing it themselves:

[Purchase 3D Printed Enclosure](https://py.pl/9J00K)

### Decora MultiSensor PCB

For anyone who wants the custom PCB and plans to supply and assemble their own components:

[Purchase MultiSensor Decora PCB](https://py.pl/2Ezptq)

### Fully Built MultiSensor Decora

Want to skip the soldering and assembly? This option includes the PCB with all of the MultiSensor components installed.

[Purchase Fully Built MultiSensor Decora](https://py.pl/29uClh)

> **Note:** The project remains open for DIY builds. PCB design files, firmware, 3D-printable files, and project documentation are available in this repository if you'd rather build your own.

## 📜 License

This project is open source, with licensing based on the type of material:

- **Software, ESPHome configurations, Home Assistant automations and code:** MIT License
- **PCB designs, mechanical designs and functional 3D-printable parts:** CERN-OHL-W-2.0
- **Documentation, photos and Purpose in Practice branding:** Copyright © 2026 Lee Perkins unless otherwise noted

See [LICENSE.md](LICENSE.md) for complete licensing information.

You're welcome to learn from it, build it, modify it, and improve it.

**Learn it. Build it. Put it into practice.**
