---
title: "Pinched Flow Fractionation (PFF) Microfluidic Device"
excerpt: "Unlike filtration, PFF enables continuous separation without clogging and does not rely on physical barriers."
header:
  image: /assets/img/PFF Device Assembled Singai.jpg
  teaser: assets/img/PFF Mold CAD Layout Singai.jpg
gallery:
  video: [Watch Reference Device](https://youtu.be/w1lRtcusky)
---

---

## Design

Pinched flow fractionation (PFF) is a microfluidic technique used to separate particles based on size using laminar flow and channel geometry. In this method, a particle-containing stream is compressed against a channel wall by a buffer stream in a narrow pinch region. As the flow enters a wider channel, streamlines expand, and particles separate based on their size-dependent positions relative to the wall.

### Geometry and Approach

The device consists of:
- Two inlet channels (particle stream + buffer stream)
- A pinch region
- A broadening region (~15 mm)
- Three outlet channels

A symmetric inlet design was used, where both streams meet at the pinch region. The intention was to compress the particle stream against one wall before entering the expansion region.

---

## Experimental Setup

| Trial A | Trial B | Trial C |
|--------|--------|--------|
| [![Trial A](https://img.youtube.com/vi/yrD9zQNNkFU/0.jpg)](https://youtu.be/yrD9zQNNkFU) | [![Trial B](https://img.youtube.com/vi/MLZGYL1cggM/0.jpg)](https://youtu.be/MLZGYL1cggM) | [![Trial C](https://img.youtube.com/vi/9X9Z9WsOq_w/0.jpg)](https://youtu.be/9X9Z9WsOq_w) |

The device was connected to tubing and tested using a syringe-driven flow system.

| Phase           | Observation                                      | Impact on Performance                          |
|-----------------|--------------------------------------------------|-----------------------------------------------|
| Setup           | Air bubbles present in tubing and device         | Disrupted laminar flow; introduced resistance |
| Setup           | Tubing lengths and orientations varied           | Created uneven backpressure and flow imbalance|
| Setup           | Flow rates manually controlled                   | Reduced consistency and repeatability         |
| Testing         | Particles not fully pinched to one wall          | Prevented proper streamline alignment         |
| Testing         | Flow unstable and frequently disrupted           | Compromised separation reliability            |
| Testing         | Significant bubble formation                     | Blocked channels and altered flow paths       |
| Testing         | Particles mixed instead of separating            | No size-based differentiation achieved        |
| Testing         | Most flow exited through a single outlet         | Indicates poor hydraulic resistance design    |

The device did not achieve successful separation due to several design limitations:

- The pinch width was too large relative to particle size, preventing proper alignment against the wall  
- The inlet configuration did not strongly force particles to one side  
- Outlet channels had similar dimensions, resulting in equal resistance  
- No mechanism was included to control flow distribution across outlets  

Because of this, particles were not focused into a narrow streamline and instead remained distributed across the channel.

---

| Performance Aspect        | Working PFF Device                          | This Device (Observed)                     | Impact on Outcome                          |
|--------------------------|---------------------------------------------|-------------------------------------------|-------------------------------------------|
| Pinch Region Behavior    | Strong particle alignment to one wall       | Weak or nonexistent pinching              | No initial condition for separation        |
| Flow Regime              | Smooth, stable laminar flow                 | Bubble-dominated, unstable flow           | Disrupted streamlines and flow paths       |
| Streamline Separation    | Clear separation into distinct streams      | No clear separation (mixing observed)     | Particles not differentiated by size       |
| Outlet Flow Distribution | Balanced flow across multiple outlets       | Flow dominated through one outlet         | Collapse of streamlines into single path   |

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

Parylene acts as a barrier layer that:
- Prevents chemical interaction between resin and PDMS  
- Improves mold release  
- Produces smoother channel surfaces  

Parylene coating is applied to resin-printed molds because SLA resins can inhibit PDMS curing. Residual chemicals from the printing process interfere with the crosslinking of PDMS, preventing proper solidification.

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
