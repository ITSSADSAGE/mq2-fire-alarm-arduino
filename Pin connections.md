# Pin Connections (MQ-2 Gas Sensor Fire Alarm)

Below are the pin connections used for this prototype.

---

## MQ-2 Sensor
- VCC → 5V (Arduino)
- GND → GND (Arduino)
- AO → A0 (Arduino)

---

## Green LED (Safe Indicator)
- Anode (+) → Digital Pin 2 (via 220Ω resistor)
- Cathode (–) → GND

---

## Red LED (Alarm Indicator)
- Anode (+) → Digital Pin 3 (via 220Ω resistor)
- Cathode (–) → GND

---

## Buzzer
- Positive (+) → Digital Pin 4
- Negative (–) → GND

---

## Notes
- Resistor values can vary depending on LED brightness and availability (typically 220Ω or 3kΩ).
- Sensor output may vary with temperature, ventilation, and smoke density.
- Circuit implemented on breadboard for prototyping.
- Can connect RED LED and Buzzer as common GND and + pin through Breadboard to reduce Noise 
