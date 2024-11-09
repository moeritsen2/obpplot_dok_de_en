.. _Der Plotter im Netzwerk:

Der Plotter im Netzwerk
=======================

WLAN
-------------------------



NMEA 2000
----------------

Das `NMEA2000-Gateway`_ ist ein Open Source Projekt von Andreas Wellenvogel. Es ist eine Software, mit der man bidirektionale Datenkonvertierungen zwischen NMEA2000 und NMEA0183 durchführen kann. Die Software ist so gestaltet, dass sie unterschiedliche kommerzielle Hardware unterstützen kann. So läuft das NMEA2000-Gateway z.B. auf einer Reihe von Produkten der Firma `M5Stack`_ wie dem **M5Stack Atom**, aber auch auf ESP32-Entwicklerboards wie dem **ESP32 Node MCU**. Es werden ESP32-CPUs in unterschiedlicher Ausprägung unterstützt wie der ESP32-Wroom und der ESP32-S3. Die Hardwareansteuerung des OBP60 ist über eigenständige Tasks implementiert und nutzt die Grundfunktionalität des NMEA2000-Gateways.

.. _NMEA2000-Gateway: https://open-boat-projects.org/de/nmea2000-gateway-mit-m5stack-atom/

.. _M5Stack: https://shop.m5stack.com/collections/all-products/m5stack-atom

Die gesamte Datenverarbeitung sämtlicher Bussysteme und Konvertierungen ist Bestandteil des NMEA2000-Gateways. Neben NMEA2000 (**CAN**) werden weitere Bussysteme wie **I2C** unterstützt. Die Hauptaufgabe des NMEA2000-Gateways besteht darin, alle ankommenden Daten der Busssysteme zu empfangen und in einem gemeinsamen Daten-Pool abzubilden. Diese Daten können über die Webseite **Data** eingesehen werden.
	
* NMEA2000
	* Kabelgebunden NMEA2000-Bus (halbduplex)
	* Über WiFi via SeaSmart (vollduplex)
* **I2C** (halbduplex)

Der kabelgebundene NMEA2000-Bus ist der aktuelle Standard in der Bootsvernetzung. Über ein NMEA2000-Backbone auf CAN-Basis werden verschiedene Geräte an das Bussystem angeschlossen. Alle Bus-Teilnehmer können Daten lesen und schreiben. Dabei sind Sensoren Datenlieferanten, die ihre Daten an Displays und Plotter übertragen. Das NMEA2000-Backbone kann Sensoren auch mit Strom versorgen. Die Einspeisung der Versorgunsgspannung erfolgt über einen Plotter oder über ein Einspeisekabel.


Für den Betrieb von NMEA2000 muss nichts speziell konfiguriert werden. Die Standardeinstellungen sind so gesetzt, dass ein Betrieb problemlos möglich ist. Bei Bedarf kann das Senden von NMEA2000-Telegrammen unterbunden werden. Dann ist nur ein Empfang von NMEA2000-Telegrammen möglich. 


NMEA0183 - USB
--------------

NMEA0183-Telegramme lassen sich auch über USB vollduplex übertragen. Das bedeutet, dass Daten gleichzeitig gesendet und empfangen werden können. Den USB-Port für die Datenübertragung findet man auf der Rückseite des OBP60 unterhalb des Steckverbinders **CN2**. Er ist als USB-C ausgeführt. Die USB-Schnittstelle im OBP60 ist als serielles RS232 Device implementiert und unterstützt die Übertragungsgeschwindigkeiten 1.200...460.800 Bd. Die Defaulteinstellung für die Datenübertragung ist auf 115.200 Bd eingestellt und sollte für die meisten Anwendungen ausreichend schnell sein. Die Daten werden ausschließlich als NMEA0183-Daten über USB übertragen.

Als mögliche Endpunkte könnte folgende Hardware verwendet werden:

* Raspberry Pi 3, 3B, 4B, 5
* Android Autoradio
* Laptop
* PC

Die NMEA0183-Daten lassen sich in unterschiedliche Software einbinden wie:

* AVnav
* OpenPlotter
* OpenCPN
* BBN
* SignalK
* qtVlm
* Navionics
* WinGPS
* NMEA Simulator


	
