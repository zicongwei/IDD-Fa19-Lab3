# Data Logger (and using cool sensors!)

*A lab report by Irene Wei. Student.*

## Part A.  Writing to the Serial Monitor
 
**a. Based on the readings from the serial monitor, what is the range of the analog values being read?**  
0~1023
 
**b. How many bits of resolution does the analog to digital converter (ADC) on the Arduino have?**  
10 bits

## Part B. RGB LED

**How might you use this with only the parts in your kit? Show us your solution.** . 
Use the RGB with different resistors can light up different colors. 

## Part C. Voltage Varying Sensors 
 
### 1. FSR, Flex Sensor, Photo cell, Softpot

**a. What voltage values do you see from your force sensor?**  
0~1023, which means 0~5v

**b. What kind of relationship does the voltage have as a function of the force applied? (e.g., linear?)**  
It is logrithmatic relationship between the force and the voltage.

**c. Can you change the LED fading code values so that you get the full range of output voltages from the LED when using your FSR?**  
Yes. Map the values that FST read to the LED.
`outputLED = map(inputFSR, 0, 1023, 0, 255);`

**d. What resistance do you need to have in series to get a reasonable range of voltages from each sensor?**  
10k Ohm.

**e. What kind of relationship does the resistance have as a function of stimulus? (e.g., linear?)**  
soft pot and flex sensor - linear
photocell and force sensor - logrithmatic

### 2. Accelerometer
 
**a. Include your accelerometer read-out code in your write-up.**
[https://github.com/zicongwei/IDD-Fa19-Lab3/blob/master/lab3_partD.ino]

## Optional. Graphic Display

**Take a picture of your screen working insert it here!**

## Part D. Logging values to the EEPROM and reading them back
 
### 1. Reading and writing values to the Arduino EEPROM

**a. Does it matter what actions are assigned to which state? Why?**  
Yes, because we cant do 'read' after 'clear, for the actions of read, clear, and write.  

**b. Why is the code here all in the setup() functions and not in the loop() functions?**  
because we only want to do the action once, instead of constantly reading, wriitng, and clearing etc. 

**c. How many byte-sized data samples can you store on the Atmega328?**  
1024 bytes

**d. How would you get analog data from the Arduino analog pins to be byte-sized? How about analog data from the I2C devices?**  
We can map the 10 bits to 8 bits by using linear equations. For I2C devices, we can also use the same byte-sized mapping.

**e. Alternately, how would we store the data if it were bigger than a byte? (hint: take a look at the [EEPROMPut](https://www.arduino.cc/en/Reference/EEPROMPut) example)**  
If it is bigger than a byte, the extra parts will be written to the following addresses. 

**Upload your modified code that takes in analog values from your sensors and prints them back out to the Arduino Serial Monitor.**  
[code](https://github.com/zicongwei/IDD-Fa19-Lab3/blob/master/state2.ino.ino)

### 2. Design your logger
 
**a. Insert here a copy of your final state diagram.**
![Diagram](https://github.com/zicongwei/IDD-Fa19-Lab3/blob/master/Screen%20Shot%202019-09-27%20at%2011.38.59%20PM.png)

### 3. Create your data logger!
 
**a. Record and upload a short demo video of your logger in action.**  
[video](https://youtu.be/s0KFSCcnupw)
