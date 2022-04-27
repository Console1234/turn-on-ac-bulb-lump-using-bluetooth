# ABSTRACT

There are use of wireless technology such as Bluetooth, in this project  Bluetooth wireless technology and a smart phone application are used to turn on a bulb . relay is used to connectinput/ output ports of the board.The use of wireless Bluetooth connection in control board enables a simplified way to system installation. In briefly the use of Bluetooth and Arduino is presented. Android technique in smart phone is also presented. These components are the main parts of the proposed mini project. This project is a low cost and using a new technology and devices for this application.











# PRPBLEM STATEMENT
Here this project has the target establish a wireless protocol for switching a bulb ON and OFF using an app on a smart phone.  Using a wireless become a solution in home application and industries  Increases mobility eliminates expensive and maintenance-heavy transmission media such as flexible cables,   Overcoming large and problematic zones has to achieve fast and efficient installation and commissioning.  Ensure personnel safety in hazardous areas.  [2]




















# Block diagram



	 	 	 		 	


# Description
In this project, consist of four main components such as: Android smartphone Bluetooth application, Bluetooth transceiver, Arduino device, and  Relay module.

Here the Android app sends the Serial data to the connected Bluetooth Module HC-05 by clicking ON button. The Bluetooth devices receive the data from the app and send it through TX pin of Bluetooth module to RX pin of Arduino. The Arduino device read the input data and process it according to program uploaded inside it and generate the output to 1 Chanel Relay Module.
When the Bluetooth application’s button turns ON, It sets the bulb ON, and when the Bluetooth application’s button turns OFF, it sets the bulb OFF.
[1]






# Circuit diagram drawn in fritzing

 







# Arduino IDE Developed Source Codes


char Incoming_value = 0;
void setup() {
Serial.begin(9600);
pinMode(13,OUTPUT);
}
void loop() {
if (Serial.available() > 0)
{
Incoming_value = Serial.read();
Serial.print(Incoming_value);
if (Incoming_value == '1')
digitalWrite(13,HIGH);
else if(Incoming_value == '0')
digitalWrite(13,LOW);
}
}






# SIMURATION IN PROTEUS

 








# References


