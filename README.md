//# Vibration-Sensor
//This is the code ofow to use a vibration sensor with an ESP32

const int VibrationSensor = 14;
const int Led = 13;

void setup() {
  // put your setup code here, to run once:
 pinMode(VibrationSensor, INPUT);
 pinMode(Led, OUTPUT);
 Serial.begin(9600);

}

void loop() {
  // put your main code here, to run repeatedly:
  int VibrationState = digitalRead(VibrationSensor);

  if(VibrationState == HIGH){
    digitalWrite(Led, HIGH);
    Serial.println("Vibration detected");
    delay(1000);
  }
  else{
    digitalWrite(Led, LOW);
    Serial.println("Vibration not detected"); 
   // delay(1000);
  }
}
