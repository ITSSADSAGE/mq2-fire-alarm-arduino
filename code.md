# Code (Arduino C++)

The following code handles smoke/gas detection, threshold-based alarm logic, 
and serial monitoring for debugging and calibration.

```cpp
int m2 = A0;       // MQ2 sensor analog pin 
int greenLed = 2;  // Green LED pin
int redLed = 3;    // Red LED pin
int buzzer = 4;    // Buzzer pin

int threshold = 600;   // Adjust this value after calibration 

void setup() {
  pinMode(greenLed, OUTPUT);
  pinMode(redLed, OUTPUT);
  pinMode(buzzer, OUTPUT);
  Serial.begin(9600);
}

void loop() {
  int sensorValue = analogRead(m2);
  Serial.println(sensorValue);

  if (sensorValue > threshold) {
    // Smoke detected
    digitalWrite(redLed, HIGH);
    digitalWrite(buzzer, HIGH);
    digitalWrite(greenLed, LOW);
  } else {
    // Safe condition
    digitalWrite(greenLed, HIGH);
    digitalWrite(redLed, LOW);
    digitalWrite(buzzer, LOW);
  }

  delay(500);
}
