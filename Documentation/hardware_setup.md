# Hardware Setup

## Overview

The hardware setup for the **Voltage Threshold Indicator** is designed to monitor an input voltage and indicate whether the voltage is above or below a predefined threshold. The system is built using the **LM393 Comparator**, resistors, LEDs, a potentiometer, and a power supply. The circuit is implemented on a **printed circuit board (PCB)** designed using KiCad.

---

## Components Used

| Component                      | Description                                            |
| ------------------------------ | ------------------------------------------------------ |
| LM393 Comparator IC            | Used to compare input voltage with reference voltage   |
| Resistors (R1, R2, R3, R4, R5) | Used for voltage division and LED current limiting     |
| Potentiometer (RV1)            | Used to adjust the reference voltage (threshold level) |
| Red LED (D1)                   | Indicates voltage above threshold                      |
| Green LED (D2)                 | Indicates voltage below threshold                      |
| Connector (J1)                 | Used for power supply and input voltage connection     |
| PCB Board                      | Platform for mounting and connecting components        |

---

## Hardware Connections

### 1. Power Supply Connection

The circuit is powered using a DC voltage source connected through the **J1 connector**.

* **Pin 1:** Positive supply voltage (VCC)
* **Pin 2:** Ground (GND)

The LM393 operates with a wide supply voltage range, making it suitable for different DC input sources.

---

### 2. Comparator Connections

The **LM393 comparator** is the main component of the circuit.

| Pin   | Function                |
| ----- | ----------------------- |
| Pin 1 | Output                  |
| Pin 2 | Inverting Input (−)     |
| Pin 3 | Non-Inverting Input (+) |
| Pin 4 | Ground                  |
| Pin 8 | VCC (Power Supply)      |

The comparator compares the input voltage with the reference voltage and changes the output state accordingly.

---

### 3. Reference Voltage Setup

A **potentiometer (RV1)** is used to set the reference voltage.

* One terminal is connected to the supply voltage.
* One terminal is connected to ground.
* The middle terminal (wiper) provides the adjustable reference voltage to the comparator input.

This allows the threshold level to be easily adjusted.

---

### 4. Voltage Divider Network

Resistors **R1 and R2** form a voltage divider that helps stabilize and scale the voltage level applied to the comparator.

Functions:

* Generates stable voltage levels
* Helps create the reference comparison point

---

### 5. LED Indicator Connections

Two LEDs are used to indicate the voltage condition.

* **Green LED (D2)** → Indicates normal voltage level
* **Red LED (D1)** → Indicates voltage above threshold

Resistors **R4 and R5** are connected in series with the LEDs to limit the current and protect them.

---

## PCB Implementation

The circuit was designed and routed using **KiCad PCB design software**. The PCB layout includes:

* Proper placement of the LM393 IC
* Short and optimized copper tracks
* Ground plane for improved stability
* Clearly labeled components

After PCB fabrication, all components were soldered onto the board according to the design.

---

## Testing Setup

To test the circuit:

1. Connect a DC power supply to the **J1 connector**.
2. Adjust the **potentiometer (RV1)** to set the threshold voltage.
3. Apply different input voltage levels.
4. Observe the LED indicators to verify correct operation.

* **Green LED ON** → Voltage below threshold
* **Red LED ON** → Voltage above threshold

---

## Summary

The hardware setup successfully implements the voltage threshold indicator using simple electronic components. The system provides a reliable and adjustable method for monitoring voltage levels and indicating their status using LEDs.
