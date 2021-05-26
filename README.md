# Trabajo-sensores
#include<DHT.h>//LIBRERIA DHT11
DHT dht(8,DHT11);


void setup() {

dht.begin();
  Serial.begin(9600);
  

}

void loop() {
  
   Serial.println(lecturaPorcentaje);
  
  float TemC = dht.readTemperature();
  Serial.println (TemC);

  delay(9600);
