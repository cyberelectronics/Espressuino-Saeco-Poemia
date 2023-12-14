# Espressuino-Saeco-Poemia
**Espressuino – DIY PID Espresso Controller on Poemia**

[**>>> Here is the new Gaggia Classic version <<<**](https://github.com/cyberelectronics/Espressuino-Gaggia-Classic)

This is a homemade PID controller, based on Arduino (connected to my Saeco Poemia.
Added LCD support and some modifications to the software of [BBCC (BareBones Coffee Controller) project by Tim Hirzel](http://playground.arduino.cc/Main/BarebonesPIDForEspresso) (Thank you!).

[In this video](https://youtu.be/DuDwQY8FdDg) I used a simple NTC 10K thermistor for temperature measurement, a pressure sensor (200psi) from ebay, 2pcs of SSR for controlling the heater and the pump. For power supply I used a small cell phone charger (output between 7 – 12Vdc, 400mA or more).

The thermistor was calibrated using a multimeter with thermocouple and Capgo thermistor calculator software (for 60C – 95C – 120C).

It is possible to use a high precision thermistor (1% or 0.1%) without calibration, just using the table with resistance values from the datasheet and Capgo software. You can use the  published source code without any modifications, using this thermistor (for v1.4 or higher; better resolution): EPCOS – B57560G104F – THERMISTOR 100K 1%  ( and EPCOS – B57551G1103F005 – 10K 1% for v1.3 or lower).
For PID tuning the controller must be connected to a PC (USB), using BBCC Plotter for [Processing](http://processing.org/).

- Finished mini Espressuino board (with miniUSB and bootloader for Arduino): https://youtu.be/72RFxjzXu7s
- Automatic Software Pressure Control (v1.5): https://youtu.be/ySqIIzoYjFY
- Grinder Timer Function  (v1.6): https://youtu.be/_HfGKKBOd9I
- Delay for Preheat Group head (v1.2): https://youtu.be/DrznD0hoHtQ
- AutoFill -up boiler while steaming (v1.5): https://youtu.be/-6zXfB7G6B4
- Shot videos:
   - https://youtu.be/ZaCQd3ru9e0?list=UUsI-1bf-SNGxmkffuQS3RtA
   - https://youtu.be/P4WNeG77YKs?list=UUsI-1bf-SNGxmkffuQS3RtA
 
**Functions:**

- [Manual or Automatic mode](http://youtu.be/DuDwQY8FdDg)
  - **Manual:**  Start (Stop) the pump manually for max. 99 seconds or Volume in ml (+ Preinfusion)
  - **Automatic:** The pump will start automatically when the temperature reach the set value (Duration in Seconds or (Volume) = Preinfusion + (Shot value) )
- [Time or Volumetric Mode](http://youtu.be/Kw45bSvZ_xM) (TIM / VOL, v3.0)
- Espresso and Steam temperature settings
     - Espresso temperature:  min. 60°C  –  max. 110°C
     - Steam temperature:      min. 100°C  –  max. 155°C
- [Grinder Timer function](http://youtu.be/_HfGKKBOd9I) (1 > 40 seconds, using SSR,  v1.6)
- [AutoFlush function](http://youtu.be/HFyjEgGiXRI) (v1.8)
- [Power Save Mode](http://youtu.be/HFyjEgGiXRI) (default 30 minutes, v1.8)
- [Automatic Descale Function](http://youtu.be/AEIfKNq4NL8) (default 1 cycle with 15 minutes delay, v1.9)
- [Set 2 different User preferences](http://youtu.be/gyKxrWVTUnU)
- [Set 2 different Grinder Timer parameters](http://youtu.be/gyKxrWVTUnU) (0.1 sec interval, v2.0, Grinder T2 available only when AutoFlush is deactivated, same button used)
- [Automatic Software Pressure Control:](http://youtu.be/ySqIIzoYjFY)    min. 8.0bar – max. 15bar (v1.5)
- [AutoFill -up function](http://youtu.be/-6zXfB7G6B4) for the boiler, while steaming (for longer steam possibility – v1.5)
- 3 Way Electrovalve control (v1.7)
- PID controll for heater (real time P – I – D tuning, using BBCC Plotter)
- Pump controll
- Improved Pressure measurement ( 0 > 15bar, using pressure transducer 0.5V > 4.5V, v1.8 )
- [Improved Preinfusion function](http://youtu.be/HFyjEgGiXRI) (duration settings  0 > 20 cycle, delay must be included)
- 2 buttons (shared) for different Shot duration settings ( Time Mode, 1 > 60 seconds, v3.0 )
- 2 buttons (shared) for different Volume settings ( in Volumetric Mode, 5 > 250ml, v3.0)
- [Learn Mode (Volume) for 2 (shared) different buttons](http://youtu.be/x6J6yWfXBuo) (v3.0)
- [AutoBackflush Mode](http://youtu.be/8K8InC9s4Uk) (for cleaning GroupHead and 3 way valve, v3.0)
- display different Volume Units (number of pulses from volumetric sensor or ml, v3.0)
- display Shot duration in Volumetric Mode (seconds, v3.0)
- Espresso counter (any extraction longer than 15 seconds, will increment this counter v3.0)
- [Delay for Preheat Group Head](http://www.youtube.com/watch?v=DrznD0hoHtQ) ( 0 > 99 minutes – v1.2 )
- Buzzer (Sound ON / OFF from menu – v1.1 to v1.4)
- Backlight Control (not implemented in software, removed from v3.0 due to HW changes)

**Protections:** 
- short or unconnected thermistor pins ( “Terr” message on the display, push buttons and SSRs  are blocked until problem solved and system restarted).
- in Manual and Volumetric Mode, after 99 seconds the pump will turn Off automatically.
- Power Save Mode, will Turn Off the Heater after a preset period (default 30 minutes)

**Documentation for connecting to Gaggia Classic :**
For SW v3.0 and HW v1.2 (or above):
- [Controller PID Espressuino Doc_v1.6 ( Romanian )]()
- [Controller PID Espressuino Doc_v1.6 ( Hungarian )]()

**For older SW and HW:**

- [Controller PID Espressuino Doc_v1.5 ( Romanian )]()
- [Controller PID Espressuino Doc_v1.5 ( Hungarian )]() 

**Circuit Diagram :**
- [Espressuino v1.2]()
- [Espressuino v1.0]()
