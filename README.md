# Arduino Smart Gate System

This project is an automatic gate system controlled by an ultrasonic sensor. When an object is detected within 15 cm, a servo motor opens the gate, a buzzer sounds in a pattern, and an LED indicator changes to show the gate status. After 5 seconds, the gate closes automatically.

## Components

- Ultrasonic sensor (HC-SR04)
- Servo motor
- Red and blue LEDs
- Piezo buzzer
- Arduino board
- Jumper wires

## Pin Configuration

| Component         | Arduino Pin |
|------------------|-------------|
| Ultrasonic Trigger | D2        |
| Ultrasonic Echo    | D3        |
| Red LED            | D4        |
| Blue LED           | D5        |
| Servo              | D6        |
| Ground Pin 1       | D7        |
| Ground Pin 2       | D8        |
| Buzzer             | D12       |

## Behavior

- Starts with the gate closed (red LED on).
- Opens the gate (80°) when something is detected closer than 15 cm.
- While open, the blue LED is on and the buzzer beeps.
- After 5 seconds, the gate closes, buzzer stops, and red LED turns back on.

## Notes

- D7 and D8 are used as software-controlled ground pins.
- Distance readings are shown in the Serial Monitor.
