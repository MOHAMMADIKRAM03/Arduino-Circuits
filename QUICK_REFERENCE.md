# Arduino Quick Reference Guide

## Circuits at a Glance

### All Circuits (20+)

```
LED & BUTTON (Beginner)
├─ LED Blinking
├─ LED Control with Push Button
└─ Red & Green LEDs

SENSORS (Intermediate)
├─ PIR Motion Sensor
├─ Ultrasonic Distance Sensor with Buzzer
└─ Digital Thermometer

DISPLAYS (Intermediate-Advanced)
├─ LCD Display (16x2)
├─ 7-Segment Counter (000-999)
├─ LCD with Relay Control
├─ Serial LCD Display
└─ LCD with Arduino & Servo

ACTUATORS (Intermediate)
└─ Servo Motor Control

OTHERS (Beginner-Advanced)
├─ Hard Way (LED Blinking)
├─ 1 Button Circuit
├─ 15-07-2023 Series
├─ Incredible Krunk
├─ Bodacious Blad
└─ Serial LCD Display LED On
```

---

## Arduino Pinout (Arduino Uno)

### Digital Pins (0-13)
```
D0  - RX (Serial Input)
D1  - TX (Serial Output)
D2  - Interrupt 0
D3  - PWM (~), Interrupt 1
D4  - Digital I/O
D5  - PWM (~)
D6  - PWM (~)
D7  - Digital I/O
D8  - Digital I/O
D9  - PWM (~)
D10 - PWM (~), SPI CS
D11 - PWM (~), SPI MOSI
D12 - SPI MISO
D13 - SPI CLK, Built-in LED
```

### Analog Pins (A0-A5)
```
A0 - Analog 0
A1 - Analog 1
A2 - Analog 2
A3 - Analog 3
A4 - SDA (I2C)
A5 - SCL (I2C)
```

### Power Pins
```
5V  - +5 Volts
3V3 - +3.3 Volts
GND - Ground (0V)
Vin - External voltage input
```

---

## Common Arduino Functions

### Digital I/O
```cpp
pinMode(pin, MODE);              // Set pin as INPUT or OUTPUT
digitalWrite(pin, state);         // Set pin HIGH or LOW
int val = digitalRead(pin);       // Read pin state (HIGH/LOW)
```

### Analog I/O
```cpp
int val = analogRead(pin);        // Read analog value (0-1023)
analogWrite(pin, value);          // PWM output (0-255)
analogReference(type);            // Set reference voltage
```

### Time Functions
```cpp
delay(ms);                        // Delay in milliseconds
delayMicroseconds(us);            // Delay in microseconds
unsigned long millis();           // Milliseconds since startup
unsigned long micros();           // Microseconds since startup
```

### Serial Communication
```cpp
Serial.begin(9600);               // Initialize serial at 9600 baud
Serial.print("Text");             // Print without newline
Serial.println("Text");           // Print with newline
Serial.write(data);               // Send byte
int data = Serial.read();         // Read byte
```

### Math Functions
```cpp
int abs(int x);                   // Absolute value
int min(a, b);                    // Minimum
int max(a, b);                    // Maximum
long map(val, from1, to1, from2, to2);  // Map range
float pow(x, y);                  // Power
float sqrt(x);                    // Square root
```

### Bit Operations
```cpp
bitSet(x, n);                     // Set bit n
bitClear(x, n);                   // Clear bit n
bitWrite(x, n, b);                // Write bit n
int bitRead(x, n);                // Read bit n
```

---

## Common Circuit Connections

### LED with Resistor
```
Arduino D13 --[220Ω]--[LED]-- GND
                       (Cathode)
Anode connects to D13 via resistor
```

### Pushbutton with Pull-up Resistor
```
Arduino D2 --[Button]-- GND
Arduino D2 --[10kΩ]-- 5V
Connect pin D2 to both button and resistor
```

### LCD Display (16x2)
```
RS   -> D12
E    -> D11
D4   -> D5
D5   -> D4
D6   -> D3
D7   -> D2
VSS  -> GND
VDD  -> 5V
V0   -> 10kΩ Pot (wiper to this pin)
RW   -> GND (always write mode)
A    -> 5V (backlight anode)
K    -> GND (backlight cathode)
```

### Servo Motor
```
GND (Brown)    -> GND
5V (Red)       -> 5V
Signal (Yellow)-> D9 (PWM pin)
Code: Servo.attach(9); Servo.write(angle);
```

### HC-SR04 Ultrasonic Sensor
```
VCC  -> 5V
GND  -> GND
Trig -> D7
Echo -> D6
```

### PIR Sensor
```
VCC  -> 5V
GND  -> GND
Out  -> D8
```

---

## Quick Code Templates

### Basic Blink
```cpp
void setup() {
  pinMode(13, OUTPUT);
}

void loop() {
  digitalWrite(13, HIGH);
  delay(1000);
  digitalWrite(13, LOW);
  delay(1000);
}
```

### Button Control
```cpp
int buttonPin = 2;
int ledPin = 13;

void setup() {
  pinMode(buttonPin, INPUT);
  pinMode(ledPin, OUTPUT);
}

void loop() {
  if (digitalRead(buttonPin) == LOW) {
    digitalWrite(ledPin, HIGH);
  } else {
    digitalWrite(ledPin, LOW);
  }
}
```

### Serial Monitor Output
```cpp
void setup() {
  Serial.begin(9600);
}

void loop() {
  int value = analogRead(A0);
  Serial.print("Value: ");
  Serial.println(value);
  delay(500);
}
```

### PWM Control
```cpp
int pwmPin = 3;  // PWM capable pin

void setup() {
  pinMode(pwmPin, OUTPUT);
}

void loop() {
  // Fade from 0 to 255
  for (int i = 0; i <= 255; i++) {
    analogWrite(pwmPin, i);
    delay(10);
  }
  delay(500);
}
```

---

## Troubleshooting Checklist

- [ ] Is Arduino connected and powered?
- [ ] Is the correct board selected (Tools > Board)?
- [ ] Is the correct COM port selected (Tools > Port)?
- [ ] Does code compile without errors?
- [ ] Are all components connected properly?
- [ ] Are polarities correct (LEDs, sensors)?
- [ ] Is correct voltage supplied to each component?
- [ ] Are pin numbers correct in code?
- [ ] Is there a short circuit?
- [ ] Are jumper wires making good contact?
- [ ] Is Serial monitor at correct baud rate (9600)?
- [ ] Are pull-up/pull-down resistors needed?
- [ ] Is there enough current from Arduino pins (max 40mA per pin)?

---

## Common Arduino Libraries

### Built-in Libraries
```cpp
#include <Wire.h>           // I2C communication
#include <SPI.h>            // SPI communication
#include <Serial.h>         // Serial communication
#include <EEPROM.h>         // Internal EEPROM
#include <Servo.h>          // Servo control
#include <LiquidCrystal.h>  // LCD display
```

---

## Useful Resources

- [Arduino Official Reference](https://www.arduino.cc/reference/)
- [Arduino Getting Started](https://www.arduino.cc/en/Guide)
- [Tinkercad Circuits](https://www.tinkercad.com/circuits)
- [Arduino Project Hub](https://create.arduino.cc/projecthub)

---

## Repository Navigation

- **README.md** - Main overview and getting started
- **CIRCUITS_INDEX.md** - Detailed catalog of all circuits
- **CIRCUIT_TEMPLATE.md** - Template for documenting new circuits
- **QUICK_REFERENCE.md** - This file

---

**Last Updated**: December 2025  
**Quick Reference for Arduino Circuits Collection**
