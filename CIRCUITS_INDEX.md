# Arduino Circuits Index

Complete catalog of all circuits in this repository with descriptions, difficulty levels, and links to documentation.

## Category 1: Basic LED & Button Circuits

### 1.1 LED Blinking
**Difficulty**: Beginner  
**Time to Complete**: 15 minutes  
**Components**: Arduino Uno, LED, 220Ω Resistor, Breadboard, Jumper wires

**Description**: The fundamental Arduino circuit that teaches GPIO output. The built-in LED blinks at regular intervals using digitalWrite() and delay() functions.

**Key Concepts**:
- digitalWrite() for digital output
- delay() for timing
- pinMode() for pin configuration
- LED polarity (anode/cathode)

**Tinkercad Link**: Available in Tinkercad dashboard

---

### 1.2 LED Control using Push Button
**Difficulty**: Beginner  
**Time to Complete**: 20 minutes  
**Components**: Arduino Uno, LED, Push Button, Resistors (220Ω, 10kΩ), Breadboard, Jumper wires

**Description**: Interactive circuit where pressing a button toggles an LED on/off. Demonstrates digital input reading with pull-up resistors.

**Key Concepts**:
- digitalRead() for input
- Debouncing techniques
- Pull-up resistor circuits
- Conditional logic (if/else)

---

### 1.3 Multiple LEDs (Red & Green)
**Difficulty**: Beginner  
**Time to Complete**: 20 minutes  
**Components**: Arduino Uno, Red LED, Green LED, Resistors (220Ω), Breadboard, Jumper wires

**Description**: Control multiple LEDs independently using different pins. Creates visual patterns and demonstrates parallel GPIO control.

**Key Concepts**:
- Multiple output pins
- Sequential control
- Pattern generation
- Pin state management

---

## Category 2: Sensor Circuits

### 2.1 PIR Motion Sensor
**Difficulty**: Intermediate  
**Time to Complete**: 30 minutes  
**Components**: Arduino Uno, PIR Sensor Module, LED, Buzzer, Resistors, Breadboard, Jumper wires

**Description**: Detects motion in a room using Passive Infrared sensor. When motion is detected, activates LED and/or buzzer alarm.

**Key Concepts**:
- PIR sensor interfacing
- Sensor calibration and warmup time
- Event detection
- Output triggering

**Applications**:
- Security systems
- Automatic lighting
- Motion-triggered alarms

---

### 2.2 Ultrasonic Distance Sensor with Buzzer
**Difficulty**: Intermediate  
**Time to Complete**: 45 minutes  
**Components**: Arduino Uno, HC-SR04 Ultrasonic Sensor, Buzzer, Resistors, Breadboard, Jumper wires

**Description**: Measures distance using ultrasonic waves. Frequency of buzzer changes based on distance (closer = faster beeps).

**Key Concepts**:
- Ultrasonic pulse timing
- Distance calculation from time-of-flight
- PWM for tone generation
- Sensor pulse reading
- Speed of sound calculations

**Applications**:
- Proximity detection
- Obstacle avoidance
- Distance measurement tools
- Parking assist systems

---

### 2.3 Digital Thermometer using Arduino
**Difficulty**: Intermediate  
**Time to Complete**: 40 minutes  
**Components**: Arduino Uno, TMP36 Temperature Sensor, LCD Display (16x2), Breadboard, Jumper wires

**Description**: Reads temperature from analog sensor and displays on LCD. Demonstrates analog-to-digital conversion and data display.

**Key Concepts**:
- Analog input reading (analogRead)
- Voltage to temperature conversion
- LCD interfacing
- Data formatting for display
- Calibration techniques

**Applications**:
- Temperature monitoring
- Environmental sensors
- Data logging systems
- Alarm systems for overheating

---

## Category 3: Display Circuits

### 3.1 LCD Display with Arduino
**Difficulty**: Intermediate  
**Time to Complete**: 30 minutes  
**Components**: Arduino Uno, 16x2 LCD Display, 10kΩ Potentiometer, Resistors, Breadboard, Jumper wires

**Description**: Interfaces parallel LCD display to show custom text and data. Foundation for data display projects.

**Key Concepts**:
- LCD pin configuration
- Parallel communication
- LiquidCrystal library usage
- Display initialization
- Cursor positioning

**Applications**:
- Data display for sensors
- Menu systems
- Information boards
- System status displays

---

### 3.2 7-Segment Display Counter (000-999)
**Difficulty**: Intermediate  
**Time to Complete**: 50 minutes  
**Components**: Arduino Uno, 7-Segment Displays (3x), Driver ICs, Resistors, Breadboard, Jumper wires

**Description**: Displays 3-digit numbers using individual 7-segment displays. Demonstrates multiplexing and display encoding.

**Key Concepts**:
- 7-segment pinout
- Common anode/cathode configurations
- Segment encoding (a-g pins)
- Display multiplexing
- Timing and refresh rates

**Applications**:
- Counters and timers
- Frequency displays
- Score boards
- Numerical readouts

---

### 3.3 LCD with Relay Control
**Difficulty**: Advanced  
**Time to Complete**: 60 minutes  
**Components**: Arduino Uno, 16x2 LCD, Relay Module, Components (LED/Motor), Breadboard, Jumper wires

**Description**: Combines LCD display with relay control. Shows current state on display while controlling high-power devices.

**Key Concepts**:
- Relay switching
- HIGH power vs LOW power circuits
- Display state updates
- Relay protection (flyback diodes)
- Power isolation

**Applications**:
- Home automation
- Industrial control panels
- Equipment management systems
- Remote device control

---

## Category 4: Motor Control Circuits

### 4.1 Servo Motor Control
**Difficulty**: Intermediate  
**Time to Complete**: 25 minutes  
**Components**: Arduino Uno, Servo Motor, Potentiometer, Resistors, Breadboard, Jumper wires

**Description**: Controls servo position using PWM signal. Demonstrates precision control of mechanical movement.

**Key Concepts**:
- PWM signal generation
- Servo library usage
- Angle control (0-180°)
- Signal timing requirements
- Potentiometer-based control

**Applications**:
- Robotic arms
- Camera positioning
- Door locks
- Machine automation

---

## Category 5: Advanced Integration Projects

### 5.1 LCD with Arduino and Servo
**Difficulty**: Advanced  
**Time to Complete**: 75 minutes  
**Components**: Arduino Uno, 16x2 LCD, Servo Motor, Buttons, Resistors, Breadboard, Jumper wires

**Description**: Integrates multiple components. LCD shows servo angle, buttons control position, real-time updates.

**Key Concepts**:
- Multi-component integration
- State management
- User interface design
- Data synchronization
- Complex timing

**Applications**:
- Robotic control systems
- Automation platforms
- Interactive demonstrations
- Industrial controllers

---

### 5.2 Serial LCD Display
**Difficulty**: Advanced  
**Time to Complete**: 45 minutes  
**Components**: Arduino Uno, LCD Display, Serial Communication Module, Breadboard, Jumper wires

**Description**: Controls LCD via serial communication instead of parallel pins. Saves GPIO pins and simplifies wiring.

**Key Concepts**:
- Serial communication (UART)
- I2C protocol basics
- Serial library usage
- Data packet formatting
- Baud rate configuration

---

## Difficulty Summary

| Difficulty | Count | Best For |
|-----------|-------|----------|
| Beginner | 3 | Learning fundamentals |
| Intermediate | 7 | Practical projects |
| Advanced | 2 | Integration & real-world apps |

## Total Circuits: 12+

## Getting Started Path

**Recommended learning order:**
1. Start with LED Blinking
2. Try LED with Push Button
3. Explore PIR or Ultrasonic sensors
4. Graduate to LCD displays
5. Attempt servo control
6. Combine projects

## Skills Developed

✓ Digital I/O (input/output)  
✓ Analog input reading  
✓ PWM signal generation  
✓ Sensor interfacing  
✓ Display integration  
✓ Motor control  
✓ Serial communication  
✓ Problem solving  
✓ Electronics fundamentals  
✓ Microcontroller programming  

---

**More detailed documentation available in individual circuit folders.**
