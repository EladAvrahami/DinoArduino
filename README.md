# DinoArduino
google t-rex no internet game with servo motor and light sensors

<span>
  
//https://trex-runner.com/
#include <Servo.h> 
#define threshold  400   //sensor sensitivity
//servo motor range in press
#define unpress_angle  80
#define press_angle  100


Servo myservo;  // create servo object to control the motor
bool trig=true;

void setup() {          
  myservo.attach(9);  // attaches the servo on pin 9 to the servo object
myservo.write(unpress_angle);   
}

void loop() {

 myservo.write(unpress_angle);              // unpress the button
 delay(1);
 if(analogRead(A0)< threshold)
 {
    myservo.write(press_angle);          // press the button
    delay(100 );                       // waits 100ms for the servo to reach the position
                      
 }                     
}

</span>
