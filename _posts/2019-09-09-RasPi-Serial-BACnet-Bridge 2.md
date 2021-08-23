---
layout: post
title: "Using a RasPi to Convert Serial Input, to BACnet (UDP) output."
date: 2019-09-09
---

I plan to update this as I go. Parts are set to arrive today, and I'll be initializing a new repo here: Serial to BACnet bridge [Repo](https://github.com/samstevenm/serial_BACnet_bridge).


Lutron Vive is a Lighting control system similar to Caseta. It supports BACnet [0] commands. Most other commerical lighting control systems, including other Lutron system, support integration via RS232 [1]. 

A common request for Vive is "Crestron integration." Typically this is a Crestron touchscreen that sends RS232 commands to the Lutron system. 

Lutron has a published standard [2] for integration and people are familiar with it. Serial has been around for 50+ years. You can get a USB to Serial Adapter and some FTDI [3] drivers to connect to an "Integration Access Point" [4] and start sending commands as defined in the protocol [2].

A device could be built that can accept serial input, and send output something else, like BACnet. It could run on a Raspi Zero, and be a simple solution.

[0] BACnet is a communications protocol for Building Automation and Control networks that leverage the ASHRAE, ANSI, and ISO 16484-5 standard protocol. BACnet.org

[1] In telecommunications, RS-232, Recommended Standard 232 is a standard introduced in 1960 for serial communication transmission of data.

[2] The Lutron integration protocol will allow third-party equipment, such as touch-screens, universal remote controls, and software applications, to control and monitor devices in a Lutron lighting control system. http://www.lutron.com/TechnicalDocumentLibrary/040249.pdf

[3] https://www.ftdichip.com/FTDrivers.htm

[4] An example of an Integration Access Point is the QS Network Interface (QSE-CI-NWK-E). http://www.lutron.com/TechnicalDocumentLibrary/040249.pdf#page=3