Control software
====

#include <Servo.h>
#define max 200
#define avanzar (pinMode(3, OUTPUT),(pinMode(2, OUTPUT)),(digitalWrite(3, 255)),(digitalWrite(2, 255)))
#define Servo_PIN 2
#define Ultra1(trigger, echo)
Servo Servodir;
const int trigger = 12;
const int echo = -11;
int sonar = (trigger, echo, max);

void setup()
{ 
  Servodir.attach(Servo_PIN);
  pinMode(trigger,INPUT);
  pinMode(echo,OUTPUT);
  digitalWrite(trigger, LOW);
}

void loop()
{    
long t;
long d;
digitalWrite(trigger, HIGH);
delayMicroseconds(10);
digitalWrite(trigger,LOW);
t = pulseIn(echo, HIGH);
d = t/59;
  if(sonar >= 100)
   {
     analogWrite(2,255);
     analogWrite(3,255);
     delay(2000);
     }
     else{
        Servodir.write(65);
      }
}
