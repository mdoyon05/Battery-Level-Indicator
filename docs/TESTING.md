# 🧪 Battery Level Indicator — Testing

## Prototype Testing

The circuit should be tested progressively rather than connecting the maximum battery voltage immediately.

### Test 1 — Continuity

Check the circuit for:

- Short circuits
- Incorrect connections
- Reversed polarity
- Broken jumper wires

### Test 2 — Power

Connect the battery and measure:

```text
Input Voltage = ______ V
```

### Test 3 — LED Test

Verify each indicator:

| Indicator | Status |
|---|---|
| LED 1 | ☐ |
| LED 2 | ☐ |
| LED 3 | ☐ |
| LED 4 | ☐ |
| LED 5 | ☐ |

### Test 4 — Threshold Measurement

Use a multimeter to record the voltage at which each LED changes state.

| Level | Voltage |
|---|---:|
| Level 1 | ____ V |
| Level 2 | ____ V |
| Level 3 | ____ V |
| Level 4 | ____ V |
| Level 5 | ____ V |

### Test 5 — Battery Discharge Test

Monitor the indicator while the battery voltage decreases.

Record:

```text
Initial Voltage:
Final Voltage:

LED sequence:
________________________________
________________________________
```

### Test 6 — Final Verification

- [ ] Correct LED sequence
- [ ] No excessive current
- [ ] No component overheating
- [ ] Correct battery polarity
- [ ] Thresholds documented
- [ ] Circuit stable
- [ ] Prototype ready for PCB design

---

# ⚠️ Safety

Always use a multimeter during initial testing.

Do not intentionally short-circuit a battery.

For lithium batteries, use an appropriate BMS/protection system and charger.
