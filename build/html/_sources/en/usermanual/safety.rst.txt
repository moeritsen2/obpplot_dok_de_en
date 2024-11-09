Safety instructions
===================

General information
-------------------

The information published on this website is the result of a hobby project. The open source project is to be understood as a feasibility study intended to show the limited possibilities with which private projects can be realised. The quality in terms of functionality, security and documentation is not comparable with commercial products. The use of open source software and hardware is at the user's own risk, excluding any liability claims.

... danger::
Anyone interested should be aware that the use of the project presented here is at their own risk and that errors and malfunctions are to be expected, which can have serious consequences. Before using the OBP-Plotter V4, carry out a risk analysis and take suitable measures to avoid damage and danger to other persons.

. note::
**NMEA2000** (TM), **NMEA0183** (TM), **SeaTalk** (TM), **SeaSmart** (TM) are registered trademarks of their respective owners. The names are used on this page as synonyms for these protocol types. Where reference is made to them in the descriptions, this refers to open source implementations that do not meet the quality requirements and specifications of the respective brand owners in all respects. The software and hardware are intended to be experimental for the purpose of gaining knowledge and should not be connected and operated with safety-critical systems such as an autopilot. No guarantee can be given for the correct implementation of the protocols and their functional safety.

... danger::
The integration of open source implementations in certified bus systems can lead to errors, malfunctions and total failures.

If problems or defects occur, please send us information via the `contact form`_. This will enable us to respond to quality and safety problems and take remedial action.

.. _Contact form: https://open-boat-projects.org/de/kontakt/

Security in WiFi networks
---------------------------	

You should only connect the OBP plotter V4 to trustworthy WiFi networks. The device only offers very limited protection against network sniffing or denial of service attacks. As long as you use the OBP-Plotter V4‘s own self-sufficient WiFi network, unauthorised persons cannot easily access the OPB60’s WiFi network. In this way, data transmission is protected in your own WiFi network. Never connect the device directly to the Internet without a firewall and avoid direct connections to open harbour WLANs. This will also allow unauthorised persons to access your devices on the network.

... note::
You can increase security by using a separate WiFi or LTE router in your boat. The routers can be set up so that you can set up your own WiFi network to which all devices on board are connected. Common mobile routers usually have a firewall already switched on, which you can use to connect your own WiFi network to the internet. The firewall prevents unauthorised external access to your devices. This means that all devices in your network have shared Internet access and are sufficiently protected at the same time.

. image:: ../pics/WiFi_Channels.png
scale: 35%

The connection quality of WiFi networks depends largely on the utilisation of the radio channels currently in use in your area, as your device shares the same radio channels with other participants in other WiFi networks. The OBP plotter V4 uses the radio channels of the 2.4 GHz frequency band.

... warning::
At high utilisation levels, e.g. in harbours, the connection quality of your own WiFi network may be impaired. You must then expect delays in data transmission, especially if you are using TCP data connections to or from the OBP plotter V4. In any case, make sure that the boat guidance is not impaired in such situations.

. hint::
If the channel utilisation is high, use channels with low utilisation. Channels 1, 13 and 14 have only one neighbouring channel and are much more robust against high utilisation than the other channels. Channel 13 is best suited as it is used less frequently. In the USA, channel 14 can also be used. Modern mobile routers often offer an automatic function in their configuration that helps to optimise channel selection.

When changing the configuration of the OPB60, you will always be asked for the admin password. The password is always transmitted in encrypted form. However, if you change the password for the WLAN access point or the WiFi client password, it will be sent in plain text. If you activate ``Remember me`` for the admin password, it is sent in plain text.