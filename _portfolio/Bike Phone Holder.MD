---
title: "Rotating Bicycle Phone Holder & Top-Down CAD & FDM Prototyping"
excerpt: "A top-down modeled, parametric phone holder featuring a detent-based rotational mechanism and clearance-tuned joints, designed for FDM fabrication to enable secure mounting and controlled orientation adjustment."
header:
  image: assets/img/phone-holder-final.jpeg
  teaser: assets/img/phone-holder-teaser.png
gallery:
  - image_path: assets/img/initial-sketch.jpg
  - image_path: assets/img/inspiration-1.jpg
  - image_path: assets/img/inspiration-2.jpg

---

{% include gallery caption="Initial sketch and design considerations as well as inspirations used to guide the phone holder form, mounting strategy, and rotating interface." %}

---

### Top-Down Modeling Approach

In this method, the design process begins with a master layout that defines the overall system geometry, key dimensions, and functional relationships between components. Rather than modeling parts independently, a central skeleton sketch was created to establish critical parameters such as handlebar diameter, phone dimensions, and the rotational axis of the holder.

All components were derived from this master geometry and constrained accordingly. This ensured that any dimensional changes propagated consistently across the entire assembly. This approach was particularly effective for this assignment because the device’s performance depends on precise alignment between multiple interacting parts, especially within the rotational mechanism.

### Detent Mechanism Implementation

A detent mechanism was incorporated into the rotational interface to provide discrete positional locking at key orientations (portrait and landscape). This was implemented using raised protrusions on one component and corresponding recesses on the mating surface.

As the holder rotates, these features engage and disengage, producing a tactile “click” that helps maintain orientation. The detent mechanism works effectively in the final design, providing sufficient resistance to prevent unintended rotation while still allowing manual adjustment. However, its performance is influenced by print resolution and material behavior, requiring iterative refinement of feature size and spacing.

---

### CAD Model Comparison

<table>
  <tr>
    <td align="center">
      <iframe src="https://a360.co/4mRaLUq" width="320" height="240" frameborder="0" allowfullscreen></iframe>
    </td>
    <td align="center">
      <iframe src="https://a360.co/41S8kHG" width="320" height="240" frameborder="0" allowfullscreen></iframe>
    </td>
  </tr>
  <tr>
    <td align="center">
      Early top-down CAD model showing the initial layout and component relationships.
    </td>
    <td align="center">
      Refined CAD model with updated geometry and print-aware dimensions.
    </td>
  </tr>
</table>

### Design Rationale

The primary objective of the design was to develop a **stable, rotatable mounting system** that allows a phone to switch between portrait and landscape orientations while remaining secure during use. The design prioritizes:

- **Mechanical stability** 
- **Ease of use**
- **Manufacturability** 
- **Minimal assembly**

To achieve this, a multi-component system was developed consisting of a clamp interface, a rotating joint, and a phone support structure, all dimensioned and constrained through the top-down model.

### Material Selection

The device was fabricated using a Bambu Lab P1S printer. This method was selected due to its accessibility, speed, and suitability for producing functional prototypes with moderate mechanical requirements.

- **PLA** was used for the primary structural components due to its stiffness and dimensional accuracy
- In high-wear or motion-critical regions, **PETG** was considered or used to improve durability and reduce brittleness

|----------|------------------|----------|
| Clamp | PLA | Requires rigidity and dimensional accuracy for secure mounting |
| Phone Support | PLA | Provides stable platform for device |
| Rotational Interface | PLA | Requires controlled clearance and durability under repeated motion |
| Spring x2 | PETG | Enables discrete positioning without additional hardware |


Several dimensional modifications were required to account for the constraints of the printing process:

- Clearance gaps (~0.2 mm) were made for press-fit regions to ensure proper assembly without excessive force
- Tolerance adjustments were introduced at rotational interfaces to prevent fusion between moving part 
- Minor offsets were applied to compensate for material expansion and layer-based inaccuracies

### Iteration Timeline

|----------|-------|---------------|--------|
| Initial Concept | ![Initial Sketch](/assets/img/initial-print.jpg) | Established overall holder form, handlebar mount, and rotating phone interface. Defined the baseline design direction. |
| Second Concept | ![Second Print](/assets/img/second-print.jpg) | Adjusted dimensions for smoother rotation and better handlebar fit. Improved printability, usability, and mechanism reliability. |

---

### Assembly & Instructions

The phone holder is designed for minimal assembly, relying primarily on print-in-place features and press-fit connections.

To assemble this device:
1. **Prepare Printed Components**
   - Remove all printed parts from the build plate and clear any support material.
   - Lightly clean mating surfaces to ensure proper fit and smooth rotation.

2. **Assemble Rotational Interface**
   - Align the rotating phone holder component with the base mount along the central axis.
   - Insert the springs

3. **Attach Phone Holder to Base**
   - Secure the phone holder structure to the rotating interface. Ensure all connections are fully seated and aligned.

4. **Install Handlebar Clamp**
   - Position the clamp around the bicycle handlebars.
   - Insert and tighten the fastener until the mount is firmly secured.
   - Confirm that the mount does not rotate or slip under moderate force.

To use the device:
1. Attach the mount securely to the bicycle handlebars.
2. Insert the phone into the holder.
3. Rotate the holder between portrait and landscape orientations as needed. The detent mechanism will engage to hold the selected position during use.

---


