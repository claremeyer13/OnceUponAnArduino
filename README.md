#include <Servo.h>
Servo myServo9;
Servo myServo3;
Servo myServo10;
Servo myServo11;

#define servoPin9 9
#define pushButtonPin2 2

int buttonPushed = 0;

#define servoPin3 3
#define pushButtonPin4 4

int buttonPushed2 = 0;

#define servoPin10 10
#define pushButtonPin7 7

int buttonPushed3 = 0;

#define servoPin11 11
#define pushButtonPin12 12

int buttonPushed4 = 0;

void setup() {
  Serial.begin(9600);
  myServo9.attach(9);
  pinMode(pushButtonPin2, INPUT_PULLUP);

  myServo3.attach(3);
  pinMode(pushButtonPin4, INPUT_PULLUP);

  myServo10.attach(10);
  pinMode(pushButtonPin7, INPUT_PULLUP);

  myServo11.attach(11);
  pinMode(pushButtonPin12, INPUT_PULLUP);

  pinMode(LED_BUILTIN, OUTPUT);

  myServo11.write(0);

}



void loop() {

  // put your main code here, to run repeatedly:
  if (digitalRead(pushButtonPin2) == LOW) {
    buttonPushed = 1;
    digitalWrite(LED_BUILTIN, HIGH);   // turn the LED off by making the voltage LOW
    delay(1000);
  }
    if (buttonPushed) {
      myServo9.write(150);
      buttonPushed = 0;
   }

  if (digitalRead(pushButtonPin4) == LOW) {
    buttonPushed2 = 1;
  }

    if (buttonPushed2) {
      myServo3.write(180);
      buttonPushed2 = 0;
      digitalWrite(LED_BUILTIN, LOW);  // turn the LED on (HIGH is the voltage level)
      delay(1000); 
   }

  if (digitalRead(pushButtonPin7) == LOW) {
    buttonPushed3 = 1;
  }
    if (buttonPushed3) {
      myServo10.write(180);
      buttonPushed3 = 0;
      myServo11.write(180);
   }

  if (digitalRead(pushButtonPin12) == LOW) {
    buttonPushed4 = 1;
  }
    if (buttonPushed4) {
      myServo11.write(0);
      buttonPushed4 = 0;
   }

  delay(100);

}
