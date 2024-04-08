# OnceUponAnArduino
Cardboard Co Final Project 

#include <Servo.h>
const int switchPin = 8;
Servo myservo;

void setup() {
// put set up here
  pinMode(switchPin, INPUT);
  myservo.attach(10);
  myservo.write(0);

  }

  void loop() {
    //runs repeatedly
    if (digitalRead(switchPin) == HIGH) {
      mysrvo.write(180):
    } else {
      myservo.write(0);
    }

  }
