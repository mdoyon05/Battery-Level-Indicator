# 🔌 Battery Level Indicator — Circuit Documentation

## 1. Circuit Architecture

The battery level indicator is based on voltage threshold detection.

```text
Battery
   │
   ▼
Voltage Divider
   │
   ▼
Threshold Detection
   │
   ├──── Level 1 ────► LED 1
   ├──── Level 2 ────► LED 2
   ├──── Level 3 ────► LED 3
   ├──── Level 4 ────► LED 4
   └──── Level 5 ────► LED 5
```

---

## 2. Voltage Divider

A voltage divider can be represented as:

```text
       R1
Vin ──/\/\/───┬──── Vout
              │
             R2
              │
             GND
```

The output voltage is:

```text
Vout = Vin × R2 / (R1 + R2)
```

The resistor values should be selected according to the maximum battery voltage and the input limits of the comparison circuit.

---

## 3. LED Driver

Each LED should have an appropriate current-limiting resistor.

```text
Supply
  │
  │
 Resistor
  │
  ▼
 LED
  │
  ▼
 GND
```

The resistor value depends on:

- Supply voltage
- LED forward voltage
- Desired LED current

---

## 4. Threshold Detection

The sensing voltage is compared with predefined reference levels.

Conceptually:

```text
Battery Voltage
       │
       ▼
Voltage Divider
       │
       ▼
 ┌───────────────┐
 │ Comparator /  │
 │ Switching     │
 │ Circuit       │
 └───────┬───────┘
         │
    ┌────┼────┬────┬────┐
    ▼    ▼    ▼    ▼    ▼
   LED1 LED2 LED3 LED4 LED5
```

---

## 5. Important Note

The exact component values and threshold voltages must be recorded from the physical prototype.

Do not assume values from this documentation without measuring the actual circuit.

---

## 6. Recommended Documentation

After finalizing the circuit, record:

```text
Battery Type:
Battery Nominal Voltage:
Maximum Voltage:
Minimum Voltage:

R1:
R2:

Comparator / Transistor:
Reference Voltage:

LED 1 Threshold:
LED 2 Threshold:
LED 3 Threshold:
LED 4 Threshold:
LED 5 Threshold:
```

---

## 7. PCB Version

The next version should replace the breadboard with a PCB.

Recommended PCB features:

- Battery input terminal
- Reverse-polarity protection
- Fuse/protection
- Clearly labeled LED indicators
- Test points
- Screw terminals
- Proper component spacing
- Mounting holes
- Battery voltage test point
