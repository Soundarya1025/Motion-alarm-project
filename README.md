A typical PIR Sensor looks like the one shown in the image below. To connect with external devices, it has only three pins namely VCC, Digital OUT (Data) and GND.

Arduino PIR Sensor Tutorial PIR Sensor 2

On the top of sensor board, there is a special type of lens called Fresnal Lens that is covering up the actual Pyroelectric Sensor. The job of the Fresnal Lens is to focus all the infrared radiation onto the pyroelectric sensor.

Arduino PIR Sensor Tutorial PIR Sensor 1

If you look at the back of the PIR Sensor board, the whole circuitry is housed there. The brain of the PIR Sensor Module is the BISS0001 PIR Motion Detector IC. Near this IC, we have two potentiometers, one for adjusting the Sensitivity and the other is for adjusting the delay time.

Using Sensitivity Adjust, you can control the range of field of view and in our sensor, it is up to 7 meters. Using the Delay Time Adjust, you can control the duration for which the Digital Out will stay HIGH when a moving object is detected.   

How PIR Sensor works?
PIR Sensors are complicated than most other sensors. PIR Motion Sensor may seem simple when implemented as all you need to do is check for a HIGH signal on the Digital Out Pin of the Sensor whenever motion is detected.

But, internally, there is a lot going on and the input and output of the sensor are dependent on several variables.

The actual PIR Sensor i.e. the one which is covered with a lens, consists of two slots and both these slots are made up of IR Sensitive materials. Under normal condition where there is no movement in front of the sensor, both the slots in the Sensor detect same amount of infrared radiation.

When there is movement in front of the sensor, like a human or a cat, their radiation is interpreted by one of the slots first and the differential output between the two slots becomes positive.

As the person moves away, the second slot detects the radiation and the differential output will become negative. Based these output pulses, a motion is detected.


Testing the PIR Sensor
Since the Digital Out Pin of the PIR Sensor is either HIGH or LOW based on the movement detected, you can build a simple circuit to test the PIR Sensor.

The first circuit consists of a PIR Sensor and an LED. When the PIR Sensor detects motions, the LED turns ON. The duration for which the LED is ON can be adjusted with the help of Delay Adjust POT.

Arduino PIR Sensor Tutorial Test Circuit 1

A similar PIR Sensor testing circuit is shown below but it consists of a buzzer. In order to drive the buzzer, an NPN Transistor like BC547 or 2N2222 can be used. The buzzer will be activated when the sensor detects any movement.  

  Arduino PIR Sensor Tutorial Test Circuit 2

Arduino PIR Sensor: PIR Motion Sensor using Arduino
Let us make a small Motion Sensor or Motion Detector project using Arduino and PIR Sensor. In this project, the PIR Sensor detects any movement in front of it and signals Arduino. Whenever any movement is detected, Arduino will activate an alarm in the form of a Buzzer.

This circuit doesn’t implement a major design but gives an idea about how to interface a PIR Sensor to Arduino and how to can we Arduino to use the data from the PIR Sensor and drive other output devices or loads like relay, GSM Module, buzzer etc.   

Circuit Diagram
Arduino PIR Sensor Tutorial Circuit Diagram

Components Required
Arduino UNO [Buy Here]
PIR Sensor [Buy Here]
5V Buzzer [Buy Here]
Breadboard [Buy Here]
Connecting Wires [Buy Here]
Power Supply
Circuit Design
The design of the PIR Motion Sensor using Arduino is very simple. The PIR Sensor Module has three pins: VCC, Digital Out and GND. Connect VCC and GND to +5V and GND respectively. Then connect the Digital Out Pin of the PIR sensor to the digital I/O pin 8 of Arduino.

As we need to indicate the detection of motion by the sensor, connect a buzzer to Pin 11 of the Arduino.

NOTE: Buzzer is connected directly to Arduino. I suggest you to connect it through a transistor as shown in the test circuit. 

Code
