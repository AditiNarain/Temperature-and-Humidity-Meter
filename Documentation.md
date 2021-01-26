#Humidity and Temperature Meter
  ## Abstract: Humidity and Temperature Meter is a device which will determine the the temperature and humidity of a room or container.It will keep you updated with realtime temperature and humidity of room. Wherever you want to check these two factor. Can also be used in agriculture to know the temperature and humidity for man-made cultivation environment.
It can be used as monitoring device which works as a thermometer for measuring temperature and humidity inside a building; it is capable of measuring humidity and temperature outdoors. It can be used as weather monitoring system

### Components:
1.	DHT11
2.	Arduino UNO

### About Component:
   • For measuring temp it have : NTC TEMPERATURE SENSOR THERMISTER
    THERMISTER: It is a type of resistor whose resistance is depended on 
    the temperature. Two types: PTC, NTC
                    Thermistor=thermal +resistor
    NTC: Negative Temp. Coefficient, when temperature increases
    resistance  decreases.    
For measuring humidity it have : Two electrode plates separated by 
    moisture holding substrate which hold water vapor. As humidity 
    changes conductivity of substrate changes hence resistance changes.   

 Arduino UNO:Input Voltage Range  5-12v, Operating Voltage5v  40mA current at Input Output pins (A0 to A5)  It can be used as analog 
input pins but not as analog output
because it  don't have DAC
(Digital to Analog Converter).
(D0 to D13)  It can be used as digital
 input and digital output pin.    

                          
		 
### Circuit Diagram:


 for DHT11, 
      VCC     -  5V or 3V
      GND    -  GND
      DATA -   7

### Working: 
	In this project we have done interfacing of DHT i.e. temperature and humidity sensor and Arduino UNO. DHT sensor will measure real time humidity and temperature which is read by arduino uno.
                    Rest all the measuring parameters are done using programming. by downloading the dht library in arduino uno.The program will automaticall give command to read the data. 

### Program Logic:


#include "DHT.h"
#define DHTPIN 7     // Digital pin connected to the DHT sensor
#define DHTTYPE DHT11   // DHT 11

DHT dht(DHTPIN, DHTTYPE);

  // Reading temperature or humidity takes about 250 milliseconds!
  // Sensor readings may also be up to 2 seconds 'old' (its a very slow sensor)
  float h = dht.readHumidity();
  // Read temperature as Celsius (the default)
  float t = dht.readTemperature();

