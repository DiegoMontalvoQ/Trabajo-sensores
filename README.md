# Trabajo-sensores
#include<DHT.h>//LIBRERIA DHT11
DHT dht(8,DHT11);
int valorSensor = 0;


void setup() {

dht.begin();
  Serial.begin(9600);
  

}

void loop() {
  
   int lectura = analogRead(A0);
 int lecturaPorcentaje = map(lectura, 1023, 0, 0, 100);
   
  
  
  float TemC = dht.readTemperature();
  Serial.println (TemC);

  delay(2000);
