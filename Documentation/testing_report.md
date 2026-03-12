# Objective of Testing

The objective of testing was to verify that the circuit correctly detects when the input voltage crosses the preset threshold value and provides proper visual indication using LEDs.

# Testing Setup

The following equipment and components were used during testing:
Power supply (adjustable DC supply or battery)
Multimeter for measuring voltage
Voltage Threshold Indicator PCB
Potentiometer for adjusting reference voltage
Red and Green LEDs for indication
The circuit was powered and the reference voltage was adjusted using the potentiometer. The input voltage was gradually varied to observe the output response.

# Testing Procedure

The circuit was connected to the DC power supply.
The potentiometer was adjusted to set the desired reference (threshold) voltage.
The input voltage was slowly increased from a lower value.
The LED indicators were observed to determine the switching point.
Voltage values were measured using a multimeter to confirm the threshold level.

# Test Cases and Observations
Test Case	Input Voltage Condition	Expected Result	Observed Result	Status
Test 1	Input voltage < Threshold	Green LED ON	Green LED ON	Pass
Test 2	Input voltage = Threshold	Switching point	LED changes state	Pass
Test 3	Input voltage > Threshold	Red LED ON	Red LED ON	Pass
Test 4	Adjust threshold using potentiometer	Switching point changes	Threshold changes correctly	Pass

# Results

The testing confirmed that the LM393 comparator successfully compares the input voltage with the reference voltage and switches the output accordingly.
When the input voltage was below the threshold, the green LED indicated normal condition.
When the input voltage exceeded the threshold, the red LED indicated warning condition.
Adjusting the potentiometer changed the threshold level as expected.

# Conclusion of Testing

The testing process verified that the Voltage Threshold Indicator circuit functions correctly and reliably. The system responds quickly to voltage changes and accurately indicates when the voltage crosses the preset threshold. This confirms that the circuit is suitable for voltage monitoring applications such as battery monitoring and power supply protection systems.
