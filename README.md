# CPE 1040 - Spring 2020

## Assignment 5: Transistors

Author: Ivo Georgiev, PhD  
Last updated: 2020-02-22  
Code: 98ffb5e9c5964e27028001933faec10caa0e4709  

---

_**NOTE:** This assignment [README](README.md) is _intentionally_ blank. It is part of the assignment to fill it. Refer to the [submission template](submission-template.md) for expectations and guidance. Read the [requirements](requirements.md) and [criteria](criteria.md) for the assignment proper._

i somehow lost all the measuurments i took from the first two sections when i did it.
redo of data collection
1. MY voltage is starting at 4.5 from the switch tried both of your solutions and thats the closest i could come to 5V

measurments with the switch off, NPN
1. accross the resistor is 5v
2. at the collector is 3.15v
3. at the base is 0
4. at the emitter is 0

measurments of currents with the switch off, NPN
1. across Ic current is 0
2. the current of emitter is 0
3. the current of the base is 0

measurments with the switch turned on,
1. the resitior voltage is 2.23v
2. the voltage across the collector is 54.9 mV
3. the voltage across the base is .71v
4. the voltage across the emitter is 2.8v
5. the current of the collector is 6.8 mA
6. the current of the emitter is 7.15 mA
7. the current of the base is is.375 mA

6. the three currents of the collector, base and emitter are similar and they help share the load of the current. 
7. the ratio in this case would be 6.8/,375 which is a ration of 18 to 1
8. My NPN circuit [picture](https://imgur.com/gallery/J8gaPvO)

PNP transistor
measurments of the voltage with the switch off, PNP
1. accross the resistor .332 v
2. at the collector is 2.74v
3. at the base is 4.4v
4. at the emmiter is 5.069v

the currents with the switch off, PNP
1. the collector is .986 mA
2. the emmiter current is 1.42mA
3. the base current is .439 mA

Measurments with the switch turned on, PNP
1. voltage of resistor 2.5 mV
1. the voltage of collector 2.09mV
3. the voltage of base is 4.548v
4. the voltage of emitter is 5v
5. the current of collector is 7.87uA
6. the emitter current is 11.5uA
7. the base current is 3.8uA

PNP circiut [picture](https://imgur.com/gallery/RgALv6K)

**3. soil sensor**
...3.1 From looking at the schematic it looks as if the soil sensor works by seding a signal across the soil and to the opposite prong and read the voltage transfered. 

...3.2 to me fully soaked means  completely covered in water to be specific. There is max connectitivy so to measure the resistance in fully soaked soil the conection would need to be positive fully dry soil is 6, somewhat wet soil 292, and fully soaked soil 789. the set up looks like [this](https://imgur.com/gallery/OztG61S)

...3.3  to measure the base voltage of the sensor transistor i had to make a conection from sig and gnd to the multi reader to take a voltage reading. [Here](https://imgur.com/gallery/9w0xKla) is my setup, the measuremts were all close to the same, fully dry soil is 6, somewhat wet soil 345, and fully soaked soil 765.

...3.4 Not sure how to upload the javascript file but here is my code
basic.forever(() => {
    let value = pins.analogReadPin(AnalogPin.P1)
    basic.showNumber(value)
    pins.digitalWritePin(DigitalPin.P8, 1);
    input.onButtonPressed(Button.A, function () {
        pins.analogWritePin(AnalogPin.P12, 1023)
    })


});
this was a very challeging part of the project that i could barley do because i didnnt realize the concetion to the software after some time I got it but im not sure if i  did it correct. [video](https://imgur.com/a/LSO2Suh)


...3.5











3. a. looking at the schematic of the soil sensor i can see that there are two resistors and one transistor the right side only having 1 resistor that is 100 and it also explains to only have the sensor on whe using it and other important user information.


```
  _           _       _   _       _       _                 _    
 | |         | |     | \ | |     | |     | |               | |   
 | |     __ _| |__   |  \| | ___ | |_ ___| |__   ___   ___ | | __
 | |    / _` | '_ \  | . ` |/ _ \| __/ _ \ '_ \ / _ \ / _ \| |/ /
 | |___| (_| | |_) | | |\  | (_) | ||  __/ |_) | (_) | (_) |   < 
 |______\__,_|_.__/  |_| \_|\___/ \__\___|_.__/ \___/ \___/|_|\_\
                                                                                                                      
```
Art acknowledgement: [taag](http://patorjk.com/software/taag/)
