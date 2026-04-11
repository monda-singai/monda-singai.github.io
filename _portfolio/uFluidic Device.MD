---
title: "Pinched Flow Fractionation (PFF) Microfluidic Device"
excerpt: "Unlike filtration, PFF enables continuous separation without clogging and does not rely on physical barriers."
header:
  image: /assets/img/PFF Device Assembled Singai.jpg
  teaser: /assets/img/PFF Mold CAD Layout Singai.jpg
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

![Plasma Treating Process](assets/img/Plasma-Treating-Image.jpg)

Parylene acts as a barrier layer that:
- Prevents chemical interaction between resin and PDMS  
- Improves mold release  
- Produces smoother channel surfaces  

Parylene coating is applied to resin-printed molds because SLA resins can inhibit PDMS curing. Residual chemicals from the printing process interfere with the crosslinking of PDMS, preventing proper solidification.

---

## Experimental Setup

| Trial A | Trial B | Trial C |
|--------|--------|--------|
| [![Trial A](https://img.youtube.com/vi/yrD9zQNNkFU/0.jpg)](https://youtu.be/yrD9zQNNkFU) | [![Trial B](https://img.youtube.com/vi/MLZGYL1cggM/0.jpg)](https://youtu.be/MLZGYL1cggM) | [![Trial C](https://img.youtube.com/vi/9X9Z9WsOq_w/0.jpg)](https://youtu.be/9X9Z9WsOq_w) |

The device was connected to tubing and tested using a syringe-driven flow system. [Watch Reference Device](https://youtu.be/w1lRtcusky)

| Phase           | Observation                                      | Impact on Performance                          |
|-----------------|--------------------------------------------------|-----------------------------------------------|
| Setup           | Air bubbles present in tubing and device         | Disrupted laminar flow; introduced resistance |
|                 | Tubing lengths and orientations varied           | Created uneven backpressure and flow imbalance|
|                 | Flow rates manually controlled                   | Reduced consistency and repeatability         |
| Testing         | Particles not fully pinched to one wall          | Prevented proper streamline alignment         |
|                 | Flow unstable and frequently disrupted           | Compromised separation reliability            |
|                 | Significant bubble formation                     | Blocked channels and altered flow paths       |
|                 | Particles mixed instead of separating            | No size-based differentiation achieved        |
|                 | Most flow exited through a single outlet         | Indicates poor hydraulic resistance design    |

The device did not achieve successful separation due to several design limitations:

- The pinch width was too large relative to particle size, preventing proper alignment against the wall  
- The inlet configuration did not strongly force particles to one side  
- Outlet channels had similar dimensions, resulting in equal resistance  
- No mechanism was included to control flow distribution across outlets  

Because of this, particles were not focused into a narrow streamline and instead remained distributed across the channel.

---

| Performance Aspect       | Working PFF Device (Ideal)                  | This Device (Observed)                    | Outcome                                   |
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

## Failure Analysis

|               | Description                                                                 | Root Cause(s)                                      | Impact on Performance                          |
|---------------------------|-----------------------------------------------------------------------------|----------------------------------------------------|-----------------------------------------------|
| Bubble Formation (Primary)| Air bubbles present throughout device and tubing                           | Entrapped air during setup; inadequate priming     | Disrupted laminar flow; blocked channels; unpredictable flow behavior |
| Insufficient Pinching     | Particles not compressed against channel wall                              | Pinch width too large; insufficient buffer flow    | No streamline alignment; prevents size-based separation |
| Outlet Flow Imbalance     | Majority of flow exited through a single outlet                            | Unequal hydraulic resistance; lack of flow control | Streamline collapse; all particles follow same path |
| Geometry-Induced Issues   | Channel features disrupted smooth flow                                     | Sharp transitions; internal features; dead zones   | Bubble trapping; stagnant regions; poor flow expansion |

---

## Barrier Redesign - Flow Resistance Control

|                    | Key Points                                                                 | Engineering Insight                                  | Impact on Device Performance                      |
|---------------------------|--------------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------|
| Problem Observed          | Flow exited primarily through a single outlet; no separation achieved    | Hydraulic resistance not balanced                    | Streamlines collapsed into lowest-resistance path |
| Role of Barriers in PFF   | Separation depends on preserving streamlines through outlet region       | Outlet design actively controls flow distribution    | Prevents merging of particle trajectories         |
| Increased Resistance      | Particle outlets made longer and/or narrower                             | Raises hydraulic resistance in particle paths        | Prevents flow dominance in a single outlet        |
| Low-Resistance Buffer     | Buffer outlet kept short and wide                                        | Provides stable, dominant flow path                  | Stabilizes upstream pinching conditions           |
| Indirect Flow Paths       | Avoid straight outlet channels; use extended/constrained paths           | Introduces passive flow barriers                     | Redistributes flow more evenly                    |
| Engineering Rationale     | Flow ∝ 1 / resistance                                                    | Small variations otherwise dominate flow behavior    | Enables controlled streamline preservation        |
| Without Redesign          | Streamlines collapse; particles follow identical paths                   | No resistance differentiation                        | Separation fails                                  |
| With Redesign             | Flow distributed across outlets; streamlines maintained                  | Controlled hydraulic resistance                      | Enables size-based particle separation            |
| Connection to Results     | Observed single-outlet flow confirms imbalance                           | Matches theoretical failure mode                     | Justifies redesign approach                       |

---

## Improvements

|             | Design Change                                      | Engineering Rationale                              | Expected Impact                                  |
|---------------------|----------------------------------------------------|----------------------------------------------------|--------------------------------------------------|
| Geometry            | Reduce pinch width to ~1.2–1.5× largest particle   | Ensures proper particle alignment at pinch         | Enables initial condition required for separation|
|                     | Smooth channel transitions                         | Reduces flow disturbances and stagnation zones     | Improves laminar flow stability                  |
|                     | Remove internal features that trap air             | Eliminates bubble nucleation points                | Reduces flow disruption and blockage             |
| Flow Control        | Increase buffer-to-sample flow ratio               | Strengthens pinching force against channel wall    | Improves particle focusing                       |
|                     | Ensure stable flow before introducing particles    | Prevents transient flow disturbances               | Improves repeatability and consistency           |
| Outlet Design       | Add long, narrow (or serpentine) particle outlets  | Increases hydraulic resistance in particle paths   | Prevents flow dominance through one outlet       |
|                     | Keep buffer outlet short and wide                  | Maintains low resistance path for bulk flow        | Stabilizes overall flow distribution             |
|                     | Design for controlled resistance differences       | Aligns outlet flow with streamline distribution    | Preserves separation across outlets              |
| Bubble Mitigation   | Degas PDMS before curing                           | Removes dissolved gases from material              | Reduces bubble formation during operation        |
|                     | Prime tubing before connection                     | Eliminates trapped air in system                   | Prevents initial flow disruption                 |
|                     | Pre-fill device slowly                             | Avoids air entrapment in channels                  | Maintains continuous laminar flow                |
|                     | Use consistent tubing lengths                      | Minimizes pressure and resistance differences      | Improves flow balance across outlets             |
