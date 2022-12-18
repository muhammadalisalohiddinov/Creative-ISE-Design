# Creative-ISE-Design-Source-Code


#include <Servo.h>
Servo servo;
int const trigPin = 6;
int const echoPin = 5;
void setup()
{
  pinMode(trigPin, OUTPUT); 
  pinMode(echoPin, INPUT); 
  servo.attach(3);
}
void loop()
{      
  long duration;
  int distance;
  digitalWrite(trigPin, HIGH);
  delayMicroseconds(10);
  digitalWrite(trigPin, LOW);
  duration = pulseIn(echoPin, HIGH);
  distance = duration * 0.034 / 2;
    servo.write(0);
    }
  delay(60);
}
