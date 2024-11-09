Technische Daten
================

.. image:: ../pics/OBP_Logo.png
   :scale: 30%

Funktionen
----------

* 10-Zoll Touch-Display (tageslichttauglich)
* 3 Sensor-Tasten (u.a. geeignet für Android Buttons)
* Akustischer Signalgeber (Lautsprecher)
* NMEA2000 (vollduplex, isoliert)
* NMEA0183 (RX oder TX, konfigurierbar, isoliert)
* NMEA2000/NMEA0183 Gateway (bidirektional)
* I2C (isoliert)
* USB-C (OTG, Debug, NMEA0183)
* GPS-Empfäger (GPS, Glonas, Baidu, interne oder externe GPS-Antenne)
* WiFi 2.4GHz (HTTP, TCP, UDP)
* Bluetooth (aktuell ungenutzt)
* Low Power Modus


Aufbau
------


Spezifikation
-------------

+----------------------+-----------------------------+
| Versorgungsspannung  | 10...28 V                   |
+----------------------+-----------------------------+
| Stromverbrauch       | 0.5...3.5 W, typisch 1 W    |
+----------------------+-----------------------------+
| Prozessor            | ESP32-S3, Dual Core         |
+----------------------+-----------------------------+
| Clock Speed          | 80, 160, 240 MHz            |
+----------------------+-----------------------------+
| RAM                  | 512 kB                      |
+----------------------+-----------------------------+
| Flash                | 16 MB                       |
+----------------------+-----------------------------+
| PSRAM                | 8 MB                        |
+----------------------+-----------------------------+
| Displaygröße         | 400 x 300 pix, 120 dpi      |
+----------------------+-----------------------------+
| Refreshrate          | 1 Hz                        |
+----------------------+-----------------------------+
| Sensortasten         | kapazitiv                   |
+----------------------+-----------------------------+
| NMEA0183-Bus         | RS485, max. 115.2 kBd, 30 m |
+----------------------+-----------------------------+
| NMEA2000-Bus         | CAN, 250 kBit/s, 30 m       |
+----------------------+-----------------------------+
| I2C-Bus              | 5V, 100 kBit/s, 10 m        |
+----------------------+-----------------------------+
| 1Wire-Bus            | 3.3V, 10 m                  |
+----------------------+-----------------------------+
| 5V-Ausgang           | 200 mA, isoliert            |
+----------------------+-----------------------------+
| ESD-Schutz           | 8 kV                        |
+----------------------+-----------------------------+
| Schutzgrad           | IP68, frontseitig           |
+----------------------+-----------------------------+
| Abmessungen          | 110 x 115 x 30 mm           |
+----------------------+-----------------------------+
| Gewicht              | 280 g                       |
+----------------------+-----------------------------+

Anschlussbelegung
-----------------
   
Schaltplan
----------


Nutzbare I2C-Sensorik
---------------------

**Umgebungssensoren**
	* BMP085, BMP180, BMP280, BME280, SHT20, HTU21