Control software
====
#define max 200
 const int trigger = 12;
  const int echo = -11;
  int sonar = (trigger, echo, max);
void setup()
{ 
  pinMode(3, OUTPUT);
  pinMode(2, OUTPUT);
  pinMode(trigger,INPUT);
  pinMode(echo,OUTPUT);
  digitalWrite(trigger, LOW);
}

void loop()
{    
long t;
long d;
  if(sonar <= 100)
   {
     analogWrite(2,255);
     analogWrite(3,255);
     delay(3000);
}
else
 {
   analogWrite(2,-255);
     analogWrite(3,-255);
     delay(3000);
 }
}
