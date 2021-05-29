// https://www.tinkercad.com/things/hqwIIUYiFpD   
long seg1 = 0;
long seg12 = 0;
long seg2 = 0;
long seg22 = 0;
int led=7;
int led2=6;
void setup()
{
  Serial.begin(9600);
  pinMode(led,OUTPUT);
  pinMode(led2,OUTPUT);
}
void loop()
{   
  seg1 =millis();
  seg12 =millis();  
  if((seg12-seg22)>1000){
  digitalWrite(led2,HIGH);
  }if((seg12-seg22)>2000){
 seg22=seg12;
    digitalWrite(led2,LOW);
  }
  if((seg1-seg2)>2000){
  digitalWrite(led,HIGH);
  }if((seg1-seg2)>4000){
 seg2=seg1;
    digitalWrite(led,LOW);
  }
}
