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
{
 // local variable to hold the pushbutton states
  int buttonState;  
  //read the digital state of buttonPin with digitalRead() function and store the           //value in buttonState variable
  buttonState = digitalRead(buttonPin);
  //if the button is pressed increment counter and wait a tiny bit to give us some          //time to release the button
  if (buttonState == LOW) // light the LED
  {
    counter++;
    delay(150);
  }
  prevSwitchVal = switchVal

}
