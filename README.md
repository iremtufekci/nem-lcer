# nem-lcer
int sensorPin=9;
int buzzer=8;
int veri;
int analogPin = A0;
int analogdeger;
void setup() {
  pinMode(sensorPin,INPUT);
  pinMode(buzzer,OUTPUT);
  Serial.begin(9600);

}
void loop() {
 analogdeger = analogRead(analogPin);  // Sensörden analog veri okunuyor
  Serial.println(analogdeger);  // Okunan veri seri port üzerinden yazdırılıyor
  delay(500);
 
 
  veri=digitalRead(sensorPin);


  if(veri==true){
    digitalWrite(buzzer,HIGH);
    delay(100);
    digitalWrite(buzzer,LOW);
  }
  else{
    digitalWrite(buzzer,LOW);
  }
}
