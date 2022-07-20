#define PWM_A 3
#define PWM_B 6
#define PWM_C 5
#define WC   2
#define WA   4
#define WB   7
int STANDARD_SPEED = 100;
float VA,VB,VC ;
float TO_RADIAN = 3.14159/180 ; 
void setup()
{ 
  Serial.begin(9600);
 IO();
}
void loop()
{
   OMMI(100,270,0);
}
void IO()
{
  pinMode(PWM_A,OUTPUT);
  pinMode(PWM_B,OUTPUT);
  pinMode(PWM_C,OUTPUT);
  pinMode(WA,OUTPUT);
  pinMode(WB,OUTPUT);
  pinMode(WC,OUTPUT);
}

void OMMI(float V,float THETA ,float w )
{ IO();
  float Vx = Vcos(THETATO_RADIAN);
  float Vy = Vsin(THETATO_RADIAN);

  VC = -(Vx + w) ;
  VB = Vxcos(60TO_RADIAN) - Vysin(60TO_RADIAN) + w ;
  VA = Vxcos(60TO_RADIAN) + Vysin(60TO_RADIAN) + w ;

  MOTOR_A(VA);
  MOTOR_B(VB);
  MOTOR_C(VC);

}
void  MOTOR_A(float x)
{
  IO();
  if  (0< x  )
  {
   digitalWrite(WA,LOW);
   analogWrite(PWM_A,x255/100);
  }
  else if  ( x < 0)
  {

   digitalWrite(WA,HIGH);
   analogWrite(PWM_A,abs(x)255/100);

  }
  else if  (x == 0 )
 {
  digitalWrite(WA,LOW);
  analogWrite(PWM_A,0);
  }
}




void  MOTOR_B(float x)
{
  IO();
  if  (0< x  )
  {
   digitalWrite(WB,LOW);
   analogWrite(PWM_B,x255/100);
  }
  else if  ( x < 0)
  {

   digitalWrite(WB,HIGH);
   analogWrite(PWM_B,abs(x)255/100);

  }
  else if  (x == 0 )
 {
  digitalWrite(WB,LOW);
  analogWrite(PWM_B,0);
  }
}


void  MOTOR_C(float x)
{
  IO();
  if  (0< x  )
  {
   digitalWrite(WC,LOW);
   analogWrite(PWM_C,x255/100);
  }
  else if  ( x < 0)
  {

   digitalWrite(WC,HIGH);
   analogWrite(PWM_C,abs(x)255/100);

  }
  else if  (x == 0 )
 {
  digitalWrite(WC,LOW);
  analogWrite(PWM_C,0);
  }
}
  //Serial.print(VA);Serial.print("");Serial.print(VB);Serial.print("");Serial.println(VC);
