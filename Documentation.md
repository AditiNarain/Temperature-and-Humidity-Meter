# Humidity and Temperature Meter
  ## Abstract: 
Humidity and Temperature Meter is a device which will determine the the temperature and humidity of a room or container.It will keep you updated with realtime temperature and humidity of room. Wherever you want to check these two factor. Can also be used in agriculture to know the temperature and humidity for man-made cultivation environment.
It can be used as monitoring device which works as a thermometer for measuring temperature and humidity inside a building; it is capable of measuring humidity and temperature outdoors. It can be used as weather monitoring system

## Components:
1.	DHT11
2.	Arduino UNO

## About Component:
### DHT11
   • For measuring temp it have : NTC TEMPERATURE SENSOR THERMISTER
    THERMISTER: It is a type of resistor whose resistance is depended on the temperature.
                It have two types: PTC, NTC
                Thermistor=thermal +resistor
    NTC: Negative Temp. Coefficient, when temperature increases, resistance  decreases.    
    
    
   • For measuring humidity it have : Two electrode plates separated by moisture holding substrate which hold water vapor. As humidity changes conductivity of substrate changes                    hence resistance changes.   
### Arduino UNO
   Input Voltage Range  5-12v, Operating Voltage 5v  40mA current at Input Output pins (A0 to A5). It can be used as digital
 input and digital output pin(D0 to D13)  .    

                         		 
### Circuit Diagram:
![Circuit](https://user-images.githubusercontent.com/73650233/105816651-927b5e80-5fda-11eb-942a-ff4e72926d53.png)

 #### for DHT11, 
      VCC     -  5V or 3V
      GND     -  GND
      DATA    -   7

### Working: 
In this project we have done interfacing of DHT i.e. temperature and humidity sensor and Arduino UNO. DHT sensor will measure real time humidity and temperature which is read by arduino uno.

Rest all the measuring parameters are done using programming by downloading the dht library in arduino uno.The program will automaticall give command to read the data. 

You can import library by importing it as given in image or by downloading the zip file given in the repository and select import zip file.


![Screenshot (621)](https://user-images.githubusercontent.com/73650233/105816900-e6864300-5fda-11eb-9dd0-34248c8524de.png)

![1](https://user-images.githubusercontent.com/73650233/105817015-12092d80-5fdb-11eb-8de5-d35a7a06fa1c.PNG)

#### Proteus working simulation:

![working](https://user-images.githubusercontent.com/73650233/105817574-ce62f380-5fdb-11eb-9a12-b47f9f824bb1.PNG)


### Program Logic:

initialise and headers :

    #include "DHT.h"
    #define DHTPIN 7     // Digital pin connected to the DHT sensor
    #define DHTTYPE DHT11   // it stated that we used DHT 11 sensor 
    DHT dht(DHTPIN, DHTTYPE);

Logic :

    float h = dht.readHumidity();//Read and calculate humidity
    // Read temperature as Celsius (the default)
    float t = dht.readTemperature();//Read and calculate temperature

