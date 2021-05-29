// https://www.tinkercad.com/things/6H61FA0Chk5  
long seg1 = 0;
long seg2 = 0;
void setup()
{
  Serial.begin(9600);
}

void loop()
{
  seg1=millis();
  if((seg1-seg2)>2000){
 seg2=seg1;
  Serial.println("Timer Activo");
  }
}
