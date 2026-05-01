---
title: "Generative Design Skateboard Truck Hanger with Integrated Motor Mount"
excerpt: "A generatively designed skateboard hanger integrating a motor mount, optimized for multi-load structural performance and validated through physical prototyping and motion testing."
header:
  image: assets/img/back-assembly.jpeg
  teaser: assets/img/front-part.jpeg

---

<table>
  <tr>
    <td align="center">
      <iframe src="https://a360.co/4t4dV8V" width="320" height="240" frameborder="0" allowfullscreen></iframe>
    </td>
    <td align="center">
      <iframe src="https://a360.co/4w4x2lS" width="320" height="240" frameborder="0" allowfullscreen></iframe>
    </td>
    <td align="center">
      <iframe src="https://a360.co/4didzql" width="320" height="240" frameborder="0" allowfullscreen></iframe>
    </td>
  </tr>
  <tr>
    <td align="center"><b>AlSi10Mg</b></td>
    <td align="center"><b>17-4 PH</b></td>
    <td align="center"><b>Nylon 12 (Prototype)</b></td>
  </tr>
  <tr>
    <td align="center">
      Lightweight, organic geometry optimized for mass reduction.  
      Lower density results in thinner members and more aggressive material removal.
    </td>
    <td align="center">
      Thicker, more robust geometry due to higher strength and stiffness.  
      Increased density results in more conservative load paths.
    </td>
    <td align="center">
      Used for fit and assembly validation only.  
      Confirms clearances, accessibility, and motion requirements.
    </td>
  </tr>
</table>

---

| Load | Magnitude | Location | Direction | Rationale |
|---|---|---|---|---|
| Rider + board | 800 N | Axle ends | Downward | Represents rider weight through wheels |
| Turning | 200 N | Axle ends | opposite and parallel in the vertical direction | Simulates carving forces |
| Braking | 250 N | Axle ends | Longitudinal | Represents deceleration |
| Belt Force | 250 N | Motor mount | Along belt path | Simulates belt tension |
| Torque (moment) | 5 N·m | Motor interface | About shaft axis | Represents motor output |

## Constraints
* Fixed: pivot interface + kingpin/bushing region  
* Free: axle, motor mount, wheels  

---

| [![Turning Clearance](https://img.youtube.com/vi/wKyO-cM58ZA/0.jpg)](https://youtube.com/shorts/wKyO-cM58ZA?si=Mojr8-GFGCTmXXn6) | [![Motor Belt Rotation](https://img.youtube.com/vi/fBsBa_YhUW4/0.jpg)](https://youtube.com/shorts/fBsBa_YhUW4?si=F9TkQBfTNW-uFVhH) |
| Does not demonstrate rotational clearance about the pivot/kingpin interface since hanger-truck geometry was preserved for this generative study. The generated body presented as an obstacle when trying to insert into the designated pivot. | Validates continuous rotation of the belt-driven system. Confirms proper clearance between hanger geometry and drivetrain components under motion. |
---

# Discussion

Generative design is most effective when paired with powder bed fusion because both enable complex geometries that cannot be manufactured using traditional methods. General Motors’ generatively designed a seat bracket, reducing an 8-part assembly into a single component while achieving a 40% weight reduction and increased stiffness https://www.autodesk.com/customer-stories/general-motors-generative-design

---

Generative design results are entirely dependent on applied loads. If loads are unrealistic or incomplete, the resulting geometry will not reflect real-world performance.

Loads in this study were determined by analyzing force flow in the system:
* Rider loads enter through the axle  
* Motor forces enter through the motor mount  
* Loads transfer to the deck through the pivot and kingpin  

Improving this process could include:
* Experimental measurement of belt tension  
* Dynamic loading conditions (impacts, vibration)  

---

The 17-4 PH outcome prioritized weight reduction, producing thinner, more organic structures due to its lower density. In contrast, the AlSi10Mg solution resulted in thicker, more conservative geometries. I filament printed the aluminum model (after editing analogous features off), though I like the steel model much more.
* Aluminum → efficiency-driven design  
* Steel → strength-driven design  

---

Generative design is highly effective for identifying efficient load paths and reducing unnecessary material, but its usefulness depends heavily on input quality.

## Strengths:
* Produces lightweight, optimized structures  
* Enables integration of multiple components  
* Explores a large design space quickly  

## Limitations:
* Highly sensitive to load and constraint assumptions  
* Results may be difficult to manufacture or validate  
* Requires post-processing to remove impractical features  

## Most useful applications:
* Weight-critical components which do not need to be mass-produced   
* Complex structural brackets / mounts  
* Robotics and electromechanical systems  
