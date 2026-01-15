---
title: "Modular Syringe Pump for Low-Flow, High-Precision Applications"
excerpt: "A fully 3D-printed, Arduino-controlled syringe pump delivering precise, programmable fluid flow with real-time safety feedback."
header:
  image: /assets/img/Syringe Pump Real Singai.png
  teaser: /assets/img/Syring Pump Rendering Singai.jpg
gallery:
  - image_path: assets/img/Syringe Pump Wiring Diagram Singai.jpg
     
---

# Features

* **Precision-Controlled Fluid Delivery** The syringe pump delivers accurate, continuous flow across a wide operating range using a stepper motor–driven lead screw and microstepping control. Flow rate is calculated in software based on syringe diameter, lead screw pitch, and motor resolution to ensure consistent volumetric output.
* **Multi-Syringe Compatibility** The mechanical syringe holder and software configuration support both 10 mL and 20 mL syringes. Syringe diameter is parameterized in the Arduino code, allowing flow calculations to automatically adjust without redesigning hardware.
* **Lead Screw Linear Actuation for High Resolution Dispensing** Rotational motion from a NEMA-17 stepper motor is converted into smooth linear displacement via an 8 mm pitch lead screw. With 8× microstepping (1600 steps/rev), the system achieves sub-microliter minimum dispense volumes per step.
* **Arduino-Based Control with AccelStepper Library** The pump is controlled by an Arduino using the AccelStepper library to provide stable, constant-speed motor motion. This enables smooth plunger travel, reduced vibration, and improved low-flow accuracy.
* **Integrated User Interface with Safety Feedback** A latching start/pause button, jog controls, potentiometer-based flow adjustment, and RGB LED indicators provide intuitive operation. LED status clearly communicates system state: running (green), paused (yellow), or syringe empty (red).
* **Automatic Empty Detection via Limit Switch** A limit switch detects when the syringe plunger reaches the end of travel, automatically stopping the motor to prevent dry operation and signaling the condition to the user.
* **3D-Printed Modular Enclosure** All mechanical and electronic components are housed in a custom 3D-printed enclosure designed to minimize fluid exposure, protect users from moving parts, and maintain clean cable management.
* **Fully Parametric CAD Design in Fusion 360** All custom parts were modeled with fully constrained, parametric sketches to support rapid iteration, tolerance adjustment, and future design scaling.

## Off-the-Shelf Components

| Component | Specification | Quantity | Notes |
|----------|---------------|----------|-------|
| Stepper Motor | NEMA 17, 200 steps/rev | 1 | Drives lead screw |
| Stepper Driver | A4988 compatible | 1 | Microstepping set to 8 |
| Arduino Board | Arduino Uno | 1 | Main controller |
| Power Supply | 120 V AC to DC (bench-style) | 1 | Supplies motor + logic power |
| Lead Screw | 8 mm pitch | 1 | Converts rotation to linear motion |
| Linear Rods | 8 mm diameter steel | 2 | Guide carriage motion |
| Linear Bearings | LM8UU | 2 | Press-fit into carriage |
| Limit Switch | Normally open | 1 | Detects empty syringe |
| Latching Button | Panel-mounted | 1 | Start / pause control |
| Jog Buttons | Momentary push buttons | 2 | Manual forward / reverse |
| Potentiometer | 10 kΩ | 1 | Flow rate adjustment |
| RGB LED | Common cathode | 1 | Status indication |
| Breadboard | Standard | 1 | Prototyping electronics |
| Wiring | Jumper wires + soldered leads | Assorted | Heat-shrink used |
| Fasteners | M3 / M4 screws and nuts | Assorted | Mechanical assembly |

## 3D Printed Components

| Part Name | Material | Quantity | Function |
|----------|----------|----------|----------|
| Enclosure | PLA | 1 | Houses electronics |
| Enclosure Lid | PLA | 1 | Covers enclosure, mounts UI |
| Shelf Insert | PLA | 1 | Supports electronics internally |
| Motor Mount Plate | ABS | 1 | Mounts stepper motor (heat resistant) |
| Carriage | PLA | 1 | Transfers motion to syringe plunger |
| Syringe Holder | PLA | 1 | Secures syringe (10 mL / 20 mL) |
| End Support (Motor Side) | PLA | 1 | Supports lead screw and rods |
| End Support (Free Side) | PLA | 1 | Stabilizes linear rods |

{% include gallery caption="Electrical wiring diagram of the syringe pump system, illustrating the Arduino-based control architecture, stepper motor driver connections, limit switch, user input buttons, LED status indicators, and regulated power supply integration." %}

# CAD Model
<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH90d2dQT28d5b602811b83ca271a5617c0c?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

