.. _Plotter and network:

Plotter and network
=======================

WLAN
-------------------------



NMEA 2000
----------------

The `NMEA2000-Gateway`_ is an open source project by Andreas Wellenvogel. It is a software that can be used to perform bidirectional data conversions between NMEA2000 and NMEA0183. The software is designed in such a way that it can support different commercial hardware. For example, the NMEA2000 gateway runs on a range of `M5Stack`_ products such as the **M5Stack Atom**, but also on ESP32 developer boards such as the **ESP32 Node MCU**. ESP32 CPUs of various types are supported, such as the ESP32-Wroom and the ESP32-S3. The hardware control of the OBP60 is implemented via independent tasks and utilises the basic functionality of the NMEA2000 gateway.

.. NMEA2000 gateway: https://open-boat-projects.org/de/nmea2000-gateway-mit-m5stack-atom/

.. _M5Stack: https://shop.m5stack.com/collections/all-products/m5stack-atom

The entire data processing of all bus systems and conversions is part of the NMEA2000 gateway. In addition to NMEA2000 (**CAN**), other bus systems such as **I2C** are supported. The main task of the NMEA2000 gateway is to receive all incoming data from the bus systems and map it in a common data pool. This data can be viewed via the **Data** website.

* NMEA2000
* Wired NMEA2000 bus (half-duplex)
* Via WiFi via SeaSmart (full duplex)
* **I2C** (half-duplex)

The wired NMEA2000 bus is the current standard in boat networking. Various devices are connected to the bus system via a CAN-based NMEA2000 backbone. All bus participants can read and write data. Sensors are data suppliers that transmit their data to displays and plotters. The NMEA2000 backbone can also supply sensors with power. The supply voltage is fed in via a plotter or a supply cable.


Nothing needs to be specially configured for NMEA2000 operation. The default settings are set so that operation is possible without any problems. If required, the transmission of NMEA2000 telegrams can be disabled. Only NMEA2000 telegrams can then be received. 


NMEA0183 - USB
--------------

NMEA0183 telegrams can also be transmitted full-duplex via USB. This means that data can be sent and received simultaneously. The USB port for data transmission can be found on the back of the OBP60 below the **CN2** connector. It is designed as USB-C. The USB interface in the OBP60 is implemented as a serial RS232 device and supports transmission speeds of 1,200...460,800 Bd. The default setting for data transmission is set to 115,200 Bd and should be fast enough for most applications. The data is transmitted exclusively as NMEA0183 data via USB.

The following hardware could be used as possible endpoints:

* Raspberry Pi 3, 3B, 4B, 5
* Android car radio
* Laptop
* PC

The NMEA0183 data can be integrated into various software such as:

* AVnav
* OpenPlotter
* OpenCPN
* BBN
* SignalK
* qtVlm
* Navionics
* WinGPS
* NMEA Simulator






	
