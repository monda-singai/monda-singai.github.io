---
title: "Pinched Flow Fractionation (PFF) Microfluidic Device"
excerpt: "Pinched flow fractionation (PFF) is a microfluidic technique used to separate particles based on size using laminar flow and channel geometry. In this method, a particle-containing stream is compressed against a channel wall by a buffer stream in a narrow pinch region. As the flow enters a wider channel, streamlines expand, and particles separate based on their size-dependent positions relative to the wall."
header:
  image: assets/img/PFF Mold CAD Layout Singai.jpg
  teaser: /assets/img/PFF Device Assembled Singai.jpg
gallery:
  - [Watch Device Test](https://youtu.be/w1lRtcusky)
---

---

## Design

Unlike filtration, PFF enables continuous separation without clogging and does not rely on physical barriers.

### Geometry and Approach

The device consists of:
- Two inlet channels (particle stream + buffer stream)
- A pinch region
- A broadening region (~15 mm)
- Three outlet channels

A symmetric inlet design was used, where both streams meet at the pinch region. The intention was to compress the particle stream against one wall before entering the expansion region.

---

## Experimental Setup

Trial A|Trial B|Trial C
--|--|--
<img src="[Watch Device Test](https://youtu.be/yrD9zQNNkFU)" width="400" />|<img src="[Watch Device Test](https://youtu.be/MLZGYL1cggM)" width="400" />|<img src="[Watch Device Test](https://youtu.be/9X9Z9WsOq_w)" width="400" />

The device was connected to tubing and tested using a syringe-driven flow system. During setup:
- Air bubbles were present in the tubing and device  
- Tubing lengths and orientations varied  
- Flow rates were manually controlled  

The device did not achieve successful separation due to several design limitations:

- The pinch width was too large relative to particle size, preventing proper alignment against the wall  
- The inlet configuration did not strongly force particles to one side  
- Outlet channels had similar dimensions, resulting in equal resistance  
- No mechanism was included to control flow distribution across outlets  

Because of this, particles were not focused into a narrow streamline and instead remained distributed across the channel.

---

For PFF devices, outlet flow must match the distribution of streamlines exiting the broadening region. In this design, all outlets had similar geometry, so flow followed the path of least resistance rather than separating based on particle position.

To fix this:
- Particle outlets should be longer and narrower (higher resistance)  
- Buffer outlet should be shorter and wider (lower resistance)  

This ensures that flow distribution aligns with streamline behavior and prevents collapse into a single outlet.

---

## Fabrication Process

### Workflow

1. Designed mold in Fusion 360  
2. Exported and printed mold using SLA resin printing  
3. Washed and post-cured printed mold  
4. Coated mold with parylene  
5. Mixed PDMS (10:1), degassed, and poured into mold  
6. Cured PDMS and removed from mold  
7. Punched inlet and outlet holes  
8. Plasma treated PDMS and glass slide  
9. Bonded PDMS to glass  

---

Parylene coating is applied to resin-printed molds because SLA resins can inhibit PDMS curing. Residual chemicals from the printing process interfere with the crosslinking of PDMS, preventing proper solidification.

Parylene acts as a barrier layer that:
- Prevents chemical interaction between resin and PDMS  
- Improves mold release  
- Produces smoother channel surfaces  

---

## Results

### Observations

- Particles were not fully pinched to one wall  
- Flow was unstable and frequently disrupted  
- Significant bubble formation occurred  
- Particles mixed instead of separating  
- Most flow exited through a single outlet  

---

A working PFF device demonstrates:
- Strong particle alignment in the pinch region  
- Smooth, laminar flow  
- Clear separation into distinct streams  
- Balanced flow across multiple outlets  

In contrast, this device showed:
- Weak or nonexistent pinching  
- Bubble-dominated flow  
- No clear separation  
- Flow dominance through one outlet  

---

## Failure Analysis

### 1. Bubble Formation (Primary Failure)

Air bubbles were present throughout the device and tubing. These bubbles:
- Disrupted laminar flow  
- Blocked channels  
- Created fluctuating resistance  
- Caused unpredictable flow behavior  

---

### 2. Insufficient Pinching

Particles were not compressed against the channel wall. This prevented formation of distinct streamlines, which is required for size-based separation.

Likely causes:
- Pinch width too large  
- Insufficient buffer flow relative to particle stream  

---

### 3. Outlet Flow Imbalance

Most fluid exited through one outlet, indicating:
- Unequal or poorly designed hydraulic resistance  
- No control over flow distribution  

This caused all particles to follow the same path regardless of size.

---

### 4. Geometry-Induced Issues

Channel features and transitions likely:
- Trapped bubbles  
- Created dead zones  
- Disrupted smooth flow expansion  

---

## Improvements

### Geometry
- Reduce pinch width to ~1.2–1.5× largest particle size  
- Smooth channel transitions  
- Remove internal features that trap air  

---

### Flow Control
- Increase buffer-to-sample flow ratio  
- Ensure stable flow before introducing particles  

---

### Outlet Design
- Add long, narrow (or serpentine) particle outlets  
- Keep buffer outlet short and wide  
- Design for controlled resistance differences  

---

### Bubble Mitigation
- Degas PDMS before curing  
- Prime tubing before connection  
- Pre-fill device slowly to avoid trapped air  
- Use consistent tubing lengths  

---

## Conclusion

The device did not achieve successful particle separation due to bubble formation, insufficient pinching, and lack of outlet flow control. While the overall structure followed PFF principles, key functional requirements were not met.

Future improvements will focus on stronger pinching, controlled outlet resistance, and eliminating bubbles. With these changes, the device is expected to achieve effective size-based separation.
