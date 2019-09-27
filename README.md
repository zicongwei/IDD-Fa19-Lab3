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
It is linear relationship between the force and the voltage.

**c. Can you change the LED fading code values so that you get the full range of output voltages from the LED when using your FSR?**  
Yes. Map the values that FST read to the LED.
`outputLED = map(inputFSR, 0, 1023, 0, 255);`

**d. What resistance do you need to have in series to get a reasonable range of voltages from each sensor?**  
10k Ohm.

**e. What kind of relationship does the resistance have as a function of stimulus? (e.g., linear?)**  
When the stimulus increases, the resistance decreases linearly. 

### 2. Accelerometer
 
**a. Include your accelerometer read-out code in your write-up.**
[https://github.com/zicongwei/IDD-Fa19-Lab3/blob/master/lab3_partD.ino]

## Optional. Graphic Display

**Take a picture of your screen working insert it here!**

## Part D. Logging values to the EEPROM and reading them back
 
### 1. Reading and writing values to the Arduino EEPROM

**a. Does it matter what actions are assigned to which state? Why?**

**b. Why is the code here all in the setup() functions and not in the loop() functions?**

**c. How many byte-sized data samples can you store on the Atmega328?**

**d. How would you get analog data from the Arduino analog pins to be byte-sized? How about analog data from the I2C devices?**

**e. Alternately, how would we store the data if it were bigger than a byte? (hint: take a look at the [EEPROMPut](https://www.arduino.cc/en/Reference/EEPROMPut) example)**

**Upload your modified code that takes in analog values from your sensors and prints them back out to the Arduino Serial Monitor.**

### 2. Design your logger
 
**a. Insert here a copy of your final state diagram.**

### 3. Create your data logger!
 
**a. Record and upload a short demo video of your logger in action.**
