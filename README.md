# Water-Alarm-PCB-
A liquid detection circuit that sounds an alarm upon water contact. Designed using KiCad 9.0.1



## 3D CAD Renders

<img width="873" height="481" alt="WaterAlarm3DRenderTopView" src="https://github.com/user-attachments/assets/abb58260-7cea-4302-ab2f-d574049ecebf" />
<img width="672" height="480" alt="WaterAlarm3DRenderBottomView" src="https://github.com/user-attachments/assets/211cae9e-c71a-4879-9326-68d2f4cfc1ce" />

---
## Schematic Diagram

<img width="1290" height="640" alt="WaterAlarmSchematic" src="https://github.com/user-attachments/assets/cf549f5a-e61a-4798-947d-363e15635a82" />

---
## Technical Overview 

The circuit works as an automatic switch that activates upon contact. After a 9V battery is plugged in, current moves through the VCC highway to three places.

1. The first path leads to the LED D1 and a resistor R2. The current fights through the resistor, powers the LED and flows into ground. This stays on constantly regardless of the actual water alarm.
2. The 9V of pressure also travels through to the positive pin of the buzzer BZ1. However, to reach ground and actually complete the circuit, it must pass through the MOSFET transistor Q1. This leaves the current trapped at the buzzer.
3. This leads to the last path the 9V of pressure travels to, pin 1 of the sensor J2.

When water eventually hits the sensor, current is able to pass through the water, out of pin 2, and through a wire to the gate of transistor Q1. Upon hitting the gate, the transistor is turned on, and the trapped current at the buzzer can pass through the transistor and reach ground. This completes the circuit and allows the buzzer to sound. The resistor R1 and capacitor C1 are attached to the wire that leads to transistor Q1. They act as drainage for the leftover pressure at the gate after the water is wiped away, stopping the alarm from sounding. 


---

## Hardware Design Files

* `/CAD` -  KiCad schematic (`.kicad_sch`) and board layout (`.kicad_pcb`) files.
* `/OUTPUTS` - Gerber files and bill of materials. 

---

## Testing

*(WIP)*


