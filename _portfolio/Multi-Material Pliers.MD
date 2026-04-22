---
title: "Multi-Link Needle-Nose Pliers with Dual-Material FDM Fabrication"
excerpt: "A multi-part, clearance-fit plier mechanism using rigid-body linkages and dual-material printing (PLA + PETG) to enable smooth rotational motion and precision gripping."
header:
  image: /assets/img/pliers real.jpg
  teaser: /assets/img/pliers singai.png
gallery:
  image: /assets/img/concept sketch.jpg

---

# Features

* **Rigid-Body Linkage Mechanism for Controlled Motion**  
  The pliers operate through a multi-link kinematic system, where rotational motion is achieved via clearance-based circular joints. This approach allows smooth actuation without requiring pins or fasteners.

* **Dual-Material Construction (PLA + PETG)**  
  PLA is used for primary structural elements due to its stiffness and dimensional accuracy, while PETG is strategically incorporated in joint regions to improve durability, reduce brittleness, and better withstand repeated motion cycles.

* **Clearance-Based Rotational Joints (Print-in-Place / Press-Fit Compatible)**  
  Circular interfaces are designed with intentional tolerances to enable motion directly off the print bed or after light manual separation. 

* **Precision Needle-Nose Geometry for Electronics Handling**  
  The jaw profile is optimized for gripping small components such as through-hole resistors.

* **Multi-Link Force Transmission for Mechanical Advantage**  
  The linkage system distributes input force across multiple pivot points, improving control and enabling consistent jaw closure with minimal user effort.

* **Parametric CAD Design in Fusion 360**  
  The model is fully constrained and parameterized, allowing rapid iteration of joint diameters, clearances, jaw length, and handle geometry to refine motion and manufacturability.

---

## Specs

| Printer Type | Bambu Lab P1S |
| Layer Height | 0.2 mm |
| Nozzle Diameter | 0.4 mm |
| Infill | 20% PETG / 15% PLA |
| Wall Count | 2 (legs) / 5 (pivot + cap) |
| Print Speed |90 mm/s |
|----------|------|------|
| Overall Length | ~120–150 mm | Compact handheld size |
| Jaw Length | ~25–40 mm | Optimized for precision work |
| Jaw Capacity | ~10–20 mm | Dependent on linkage geometry |
| Assembly | No tools required | Print-in-place / press-fit |

--- 

| Component | Material | Function |
|----------|----------|----------|
| Handles (x2) | PLA | Structural rigidity and grip |
| Jaw Sections | PLA | Precision gripping interface |
| Linkage Arms | PLA | Force transmission |
| Joint Interfaces | PETG | Rotational motion + wear resistance |

---

## Design & Iteration Process

The design process focused on achieving reliable motion through **geometric precision rather than compliant materials**:

* Early concepts explored single-body print-in-place mechanisms but were limited by friction and inconsistent movement due to layer adhesion and surface irregularities inherent to FDM printing.
* A key design constraint was maintaining an overall footprint approximately within the dimensions of a standard business card (80 mm × 50 mm).
* The design evolved into a multi-link rigid-body system, improving motion control and distributing forces across multiple rotational joints.
* A dual-material strategy (PLA + PETG) was introduced, where PLA provides structural rigidity in the handles and linkages, while PETG is used in select regions to improve durability and introduce localized compliance at contact interfaces.

---

## Context

Print-in-place mechanisms allow multiple moving components to be fabricated in a single build without assembly. These systems rely on:

* Carefully designed clearances between moving parts  
* Print orientation to prevent fusion at interfaces  
* Material selection to balance strength and wear resistance  

Applications include hinges, articulated tools, and mechanical linkages. Unlike compliant mechanisms, which rely on elastic deformation, this design uses **rigid-body motion through discrete joints**.

Reference: https://all3dp.com/3d-printed-flexible-pliers/

---

## Performance Evaluation & Design Limitations

| Performance | Design Limitations |
|------------|-------------------|
| Smooth rotational motion after initial separation of clearance-fit joints | No integrated spring return—pliers must be manually reopened |
| Capable of gripping and manipulating through-hole resistors with adequate precision | Motion quality is sensitive to printer calibration and tolerance accuracy |
| PETG integration improves joint durability and reduces brittleness | PETG does not provide true elastic behavior for passive actuation |
| No fasteners, adhesives, or tools required (assembly-free / press-fit) | Performance dependent on precise clearance design (~0.2–0.4 mm) |

---

## Gallery

| First Print | Second Print |
|------------|-------------|
| ![First Print](/assets/pliers first cap.jpeg) | ![Second Print](/assets/pliers second cap.jpeg) |
| ![First Print](/assets/pliers first cap 2.jpeg) | ![Second Print](/assets/img/pliers second cap 2.jpeg) |
| [![First Print](https://img.youtube.com/vi/689a25_TDfA/0.jpg)](https://youtu.be/689a25_TDfA) | [![Second Print](https://img.youtube.com/vi/B4Junn79zOE/0.jpg)](https://youtube.com/shorts/B4Junn79zOE?feature=share) |
---

# CAD Model

<iframe src="https://a360.co/4tTH9rC" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>
