# Temperature and Humidity Sensor

Both the DHT11 and DHT22 are sensors that measure ambient temperature (°C / °F) and relative humidity (%RH).

|DHT11         | range          |
|:--------     |:--------       |
| Temperature: | 0 to 50 °C     | 
| Humidity:    | 20% to 80% RH  | 


| DHT22            | range          |
|:--------         |:--------       |
| Temperature:     | –40 to +80 °C  | 
| Humidity:        | 0% to 100% RH  | 

More info : [here](https://learn.adafruit.com/dht)

----
### WHEN TO USE IT

Ideal for sensing ambient conditions.

----
### DHT vs OTHER SENSORS

The [TEMP102](https://github.com/kingston-hackSpace/TEMP102) is a temperature-only sensor that provides fast and precise readings. If you require high-precision and a wider temperature range, then the TEMP102 is a more suitable choice.

The [Si7021](https://github.com/kingston-hackSpace/Si7021) is a temperature-and-humidity sensor very similar to the DTH11 and DHT22, however more precise and (generally) more expensive. 

----
### DHT11 or DHT22?

Detailed comparison : [here](https://www.estartrade-ic.com/dht22-vs-dht11-which-one-to-choose/)

DHT11 vs DHT22 chart : [here](https://github.com/kingston-hackSpace/DHT/blob/main/20240905173850055.png)

----
# TUTORIAL : SENSING AMBIENT TEMPERATURE AND HUMIDITY

In this tutorial, we will cover the DHT11 only.

----
### HARDWARE
- ARDUINO UNO
- DHT11
- Resistor 10k ohms (x1)

----
### WIRING

Depending on the sensor model you have, different wiring order will apply. However, the follow the same logic as follows:

DHT11 DATA pin -------- Arduino Pin 2

DHT11 VCC+ pin -------- Arduino 5V

DHT11 GND- pin -------- Arduino GND

Please identify your sensor and wire it accordingly. Reference image [here](https://github.com/kingston-hackSpace/DHT)

----
### CODE AND INSTRUCTIONS

- First, install the corresponding libraries ("Adafruit_Sensor" and "DHT-sensor-library"). Download [here](https://github.com/kingston-hackSpace/DHT/tree/main/Libraries)
  
- Once donwloaded, follow the installation instructions. In this case, we install via [Importing a .zip Library](https://docs.arduino.cc/software/ide-v1/tutorials/installing-libraries/)

- Upload [this code](https://github.com/kingston-hackSpace/DHT/blob/main/DHT11.ino) to your Arduino board.

- Open Arduino's Serial Monitor to see the incoming data

----
### UNDERSTANDING THE CODE

Based on our DHT11 library, we use specific functions to read temperature and humidity:

**Read Ambient Temperature in °C (Celsius)** --> dht.readTemperature()

**Read Ambient Temperature in °F (Fahrenheit)** --> dht.readTemperature(true)

**Read Relative Humidity(RH) in %** --> dht.readHumidity()

**Read Heat Index  (“Feels Like” Temp °C/°F)** --> dht.computeHeatIndex(t, h, false/true);



 

