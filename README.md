# OnceUponAnArduino
Cardboard Co Final Project 
#include <Servo.h> 
const int switchPin = 8; 

int switchVal = 0
int prevSwitchVal = 0; 

Servo myservo; 

void setup() {
  // put your setup code here, to run once:
  pinMode(switchPin, OUTPUT);
  myservo.attach(10); 
  myservo.write(0); //startingAngle 


}

void loop() {
  // put your main code here, to run repeatedly:
  switchVal = digitalRead(switchPin); 

  if (switchVal != prevSwitchVal) {
    //previously low and has become high
    if(switchVal = HIGH) {
      //include code you want when the switch is flipped 
      myservo.write(180); 
    } else {
      servoAngle = 0
    }
    myservo.write(servoAngle);

  }

  prevSwitchVal = switchVal

}
