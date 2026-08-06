# Water-Alarm-PCB-
Water Alarm PCB designed in KiCad and built/tested. 
An autonomous liquid detection circuit that sounds an alarm upon water contact. Designed using KiCad 9.0.1



## 3D CAD Render

![3D PCB Render](PATH_TO_YOUR_IMAGE.png)

---

## Technical Overview 

The circuit works as an automatic switch that activates upon contact. 

2. A pull-down resistor connects the MOSFET gate to ground when there is no water. This drains away random electrical noise so the alarm doesn't go off by accident. 
3. When the water bridges the gap, positive voltage reaches the gate of the N-channel MOSFET, turning it on and making it act just like a closed switch.
4. Once the MOSFET turns on, it allows power to flow through the buzzer to ground, completing the circuit and making the alarm sound.
---

## Key Specifications

* **Input Voltage:** [e.g., 9V DC]
* **Switching Element:** N-Channel MOSFET
* **Alert Output:** Piezoelectric Buzzer
* **EDA Tool:** KiCad 9.0.1
* **Manufacturing Deliverables:** Gerber X2, NC Drill, Bill of Materials (BOM)

---

## Hardware Design Files

* `/CAD` - Raw KiCad schematic (`.kicad_sch`) and board layout (`.kicad_pcb`) files.
* `/OUTPUTS` - Production-ready Gerber files, drill files, and BOM CSV.
* `/DOCS` - Exported PDF schematic and 3D STEP models.

---

## Physical Verification & Testing

*(Update this section once physical components arrive)*

![Assembled PCB](PATH_TO_YOUR_PHOTO.png)

* **Assembly:** Hand-soldered board using lead-free solder.
* **Testing Procedure:** Verified nominal voltage across supply rails, tested gate thresho
