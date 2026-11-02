#  Battery Level Indicator

A simple electronic **Battery Level Indicator** designed to monitor the approximate voltage level of a battery using multiple LED indicators.

The prototype was developed on a breadboard using discrete electronic components and LED indicators.

---

## 📌 Project Overview

The purpose of this project is to provide a simple visual indication of battery voltage.

As the battery voltage changes, different LEDs indicate the approximate battery level.

### Basic concept

```text
          Battery
        +         -
        │         │
        ▼         ▼
   Voltage Sensing
        │
        ▼
   Comparator /
   Transistor Stages
        │
        ├──────► 🔴 Low
        ├──────► 🟠 Medium-Low
        ├──────► 🟡 Medium
        ├──────► 🔵 High
        └──────► 🟢 Full
```

---

# 🎯 Project Objectives

- Monitor battery voltage
- Display battery level visually
- Use multiple LEDs for different voltage ranges
- Create a low-cost electronic circuit
- Understand voltage comparison
- Learn transistor/comparator-based indication
- Develop practical electronics troubleshooting skills

---

# 💡 Working Principle

The battery voltage is sampled by a voltage-sensing network.

The sensed voltage is compared with predefined threshold levels.

When the battery voltage crosses a particular threshold, the corresponding LED turns ON.

Conceptually:

```text
Battery Voltage
      │
      ▼
Voltage Divider
      │
      ▼
Threshold Detection
      │
      ├── Level 1 → LED 1
      ├── Level 2 → LED 2
      ├── Level 3 → LED 3
      ├── Level 4 → LED 4
      └── Level 5 → LED 5
```

---

# 🔋 Battery Level Indication

A typical 5-level indication can be represented as:

| Level | Approx. Condition | Indicator |
|---|---|---|
| Level 1 | Very Low | 🔴 Red |
| Level 2 | Low | 🟠 Orange |
| Level 3 | Medium | 🟡 Yellow |
| Level 4 | High | 🔵 Blue |
| Level 5 | Full/High | 🟢 Green |

> ⚠️ The exact voltage thresholds depend on the battery chemistry, nominal voltage, circuit design, and component values used in the prototype.

---

# 🧰 Components

The prototype may contain components such as:

- LEDs
- Resistors
- Transistors and/or comparator ICs
- Voltage-divider resistors
- Breadboard
- Jumper wires
- Battery connector
- Battery
- Power switch
- Current-limiting resistors

> The exact component values should be documented after verifying the physical circuit.

---

# 🔌 Block Diagram

```text
             ┌──────────────────┐
             │     BATTERY      │
             └────────┬─────────┘
                      │
                      ▼
             ┌──────────────────┐
             │ Voltage Divider  │
             └────────┬─────────┘
                      │
                      ▼
             ┌──────────────────┐
             │ Threshold /      │
             │ Comparison Stage │
             └────────┬─────────┘
                      │
          ┌───────────┼───────────┐
          │           │           │
          ▼           ▼           ▼
       Level 1      Level 2     Level 3
          │           │           │
          ▼           ▼           ▼
        🔴 LED      🟠 LED       🟡 LED

             ┌──────────────────┐
             │ Higher Levels    │
             └────────┬─────────┘
                      │
                  ┌───┴───┐
                  ▼       ▼
                🔵 LED  🟢 LED
```

---

# 🧪 Testing Procedure

## Step 1 — Visual Inspection

Check:

- LED polarity
- Transistor orientation
- IC orientation
- Resistor connections
- Battery polarity
- Breadboard connections

---

## Step 2 — Power Test

Connect the battery carefully.

Check that:

- No component becomes excessively hot
- There is no short circuit
- LEDs operate as expected

---

## Step 3 — Voltage Measurement

Use a multimeter to measure the battery voltage.

Record:

```text
Battery Voltage:
________ V
```

Then observe which LED is active.

---

## Step 4 — Level Testing

Record the measured threshold of every LED.

| LED | Measured Voltage |
|---|---:|
| LED 1 | ____ V |
| LED 2 | ____ V |
| LED 3 | ____ V |
| LED 4 | ____ V |
| LED 5 | ____ V |

This table should be updated after final calibration.

---

# 📊 Calibration

For accurate battery indication, each threshold should be measured using a multimeter.

Example:

```text
Battery Voltage ↑

LOW
│
├── LED 1
│
├── LED 2
│
├── LED 3
│
├── LED 4
│
└── LED 5
      HIGH
```

The threshold values should be selected according to the actual battery type.

---

# 🧠 Electronics Concepts Demonstrated

This project demonstrates:

- Voltage measurement
- Voltage divider
- Threshold detection
- Comparator operation
- Transistor switching
- LED indication
- Current limiting
- Battery monitoring
- Breadboard prototyping
- Electronic troubleshooting

---

# 📸 Prototype

The project was initially developed and tested on a breadboard.

The prototype contains multiple LED indicators connected to a battery-level sensing circuit.

The LED indicators provide a visual representation of the battery condition.

---

# 🚀 Future Improvements

- [ ] PCB design
- [ ] Accurate voltage calibration
- [ ] Low-battery warning buzzer
- [ ] Over-voltage protection
- [ ] Reverse-polarity protection
- [ ] Battery percentage display
- [ ] 7-segment display
- [ ] OLED display
- [ ] Microcontroller-based monitoring
- [ ] ESP32 version
- [ ] Mobile monitoring
- [ ] Battery voltage logging

---

# 🔬 Possible Microcontroller Version

A future version can use an ESP32 or Arduino.

```text
Battery
   │
   ▼
Voltage Divider
   │
   ▼
ADC Input
   │
   ▼
ESP32 / Arduino
   │
   ├── LED 1
   ├── LED 2
   ├── LED 3
   ├── LED 4
   └── LED 5
```

This version could calculate the battery percentage and display the voltage digitally.

---

# ⚠️ Safety

Do not connect an unknown battery directly to sensitive electronic components.

Always verify:

- Battery voltage
- Battery polarity
- Maximum component voltage
- Resistor values
- LED current
- Comparator/transistor ratings

For rechargeable lithium batteries, use an appropriate protection/BMS system and charger.

---

# 👨‍💻 Developer

**Md Taslim Islam Oyon**

Electronics Engineer | PLC Programmer | Industrial Automation Enthusiast

### Interests

`Electronics` • `Embedded Systems` • `PLC` • `Industrial Automation` • `Arduino` • `ESP32`

---

## ⭐ Project Status

**Prototype / Experimental**

The circuit is currently a breadboard prototype and can be further improved through calibration, PCB design, and enclosure development.
