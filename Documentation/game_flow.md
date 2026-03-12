# Game Flow

## Overview

The **Voltage Threshold Indicator System** follows a simple operational flow where the circuit continuously monitors the input voltage and compares it with a preset reference voltage. Based on this comparison, the system indicates the voltage condition using LED indicators.

---

## System Flow Description

1. **Power Initialization**
   The circuit is powered using a DC supply connected to the input connector. Once power is applied, the LM393 comparator and all components become active.

2. **Reference Voltage Setup**
   A potentiometer is used to set the reference voltage (threshold level). This voltage determines the point at which the indicator will change state.

3. **Input Voltage Monitoring**
   The system continuously receives the input voltage that needs to be monitored. This voltage is fed into one of the comparator inputs.

4. **Voltage Comparison**
   The LM393 comparator compares the input voltage with the reference voltage:

   * If the input voltage is **greater than the reference voltage**, the comparator output switches state.
   * If the input voltage is **less than the reference voltage**, the output remains in the opposite state.

5. **Output Indication**
   Based on the comparator output:

   * **Red LED turns ON** when the voltage is below the threshold (normal condition).
   * **Green LED turns ON** when the voltage exceeds the threshold (warning condition).

6. **Continuous Operation**
   The system continuously monitors the voltage and updates the LED indication whenever the voltage crosses the threshold level.

---

## Flow Diagram

```text
Start
  │
  ▼
Power Supply ON
  │
  ▼
Set Reference Voltage (Potentiometer)
  │
  ▼
Read Input Voltage
  │
  ▼
Compare Vin with Vref
  │
  ├── Vin < Vref → Green LED ON
  │
  └── Vin > Vref → Red LED ON
  │
  ▼
Repeat Monitoring
```

---

## Summary

The system flow ensures continuous monitoring of voltage levels and provides immediate visual feedback using LEDs. This simple flow enables reliable voltage threshold detection for electronic monitoring applications.
