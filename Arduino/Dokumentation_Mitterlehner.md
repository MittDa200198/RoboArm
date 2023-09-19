# Dokumentation Mitterlehner

### 19.09.2023

Der Motor hat sich mit hilfe des standartscripts der Arduino IDE in betrieb nehmen lassen.

```c
 Created 11 Mar. 2007
 Modified 30 Nov. 2009
 by Tom Igoe

 */

#include <Stepper.h>

const int stepsPerRevolution = 200;  // change this to fit the number of steps per revolution
// for your motor

// initialize the stepper library on pins 8 through 11:
Stepper myStepper(stepsPerRevolution, 8, 9, 10, 11);

void setup() {
  // set the speed at 60 rpm:
  myStepper.setSpeed(60);
  // initialize the serial port:
  Serial.begin(9600);
}

void loop() {
  // step one revolution  in one direction:
  Serial.println("clockwise");
  myStepper.step(stepsPerRevolution);
  delay(500);

  // step one revolution in the other direction:
  Serial.println("counterclockwise");
  myStepper.step(-stepsPerRevolution);
  delay(500);
}
```

Das Oziloskop war eingestellt auf: 12V mit max. 3A

**Verkabelung:**

![](C:\Users\Whoadie\OneDrive%20-%20Linzer%20Technikum\Schule\4te%20Klasse\Repos\RoboArm\Arduino\images\Verkabelung_Smaler_Picture.jpg)
