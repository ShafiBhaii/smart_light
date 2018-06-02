# smart_light
You can switch on/off or change the colour of the rgb lights using google assistant/IFTTT. This can be done from anywhere around the world using internet.
To make this you need a rgb wire strip, nodemcu, smartphone with IFTTT app, motor driver, 12V power supply or 220V to 12v converter, jumpers and breadboard.
I am using l293D motor driver for 2 motor output. This is because the led strip need 12V power supply but the nodemcu board can give out max 3.3. Instead of motor driver you can use any other device that does the same. Overall principle is the same.
The .ino file and config.h file should be placed in the same folder.
I am using a common cathode RGB wire strip, which means that the positive terminal is made common. The led strip has 4 outputs - Red, Green, Yellow, and +12V.
Pin connections (Wire strip to motor driver):
+12V and Red to M1, Green and Yellow to M2.
Pin connections (Motor driver to nodemcu):
IN1 to D3
IN2 TO D5
IN3 to D6
IN4 to D7
+5v terminal to 3.3v
Gnd to Gnd 
E1 to D2
E2 to D1
To power the motor driver connect its +12V and gnd terminal to external power source of 12v. I am using a 220V to 12V converter to power this up, you can also use a 12V battery.
Make an adafruit account and in the dashboard make a new project. Add a new feed of remote.
The username and key which you get in adafruit put it in config.h file.
Add your wifi name and password to the config.h file.
To the smartlight.ino file add your feed name.
Upload this code to the nodemcu board.
Wait for it to get connected to adafruit IO website. When it does it will show a message in your serial monitor. 
When you get this message, your project 70 percent done. 
Each button you click from 1-9 you get a different light as the output.
