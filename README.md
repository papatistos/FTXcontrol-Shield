# FTXcontrol-Shield
An Arduino shield for controlling the FläktWoods RDKR ventilation unit

In this project, I'm monitoring and controlling the ventilation of my house. My ventilation unit is a **FläktWoods RDKR** (which as a rotating heat exchanger, hence FTX) but it should be possible to use at least parts of this project with other systems.

## Features
* Monitor and log temperature and humidity of 
  * outside air (_uteluft_)
  * incoming air (_tilluft_)
  * inside air (_frånluft_)
  * outgoing air (_avluft_)
* Monitor the efficiency of the heat (and humidity) exchanger.
* Automatically change ventilation state (low, middle, high) based on temperature and/or humidity values. For example: 
  * Set ventilation to low when outside temperature is higher than inside temperature (Don't have the ventilation heat up the house on hot summer days.)
  * Set venilation to high when oustide temperature is lower than inside temperature and insider temperature is over 25°C. (Cool down the house during the night.)

## Hardware used
* Arduino Uno
* 3-4 [Sonoff Si7021](https://www.itead.cc/wiki/Sonoff_Sensor_Si7021) temperature and humidity sensors
* Various electronic components to build the shield (see schematic). Most importantly:
  * A photoresistor for reading the current ventilation state via the LED on the ventilation unit's control board
  * An optocoupler to switch the ventilation state on the control board


  
