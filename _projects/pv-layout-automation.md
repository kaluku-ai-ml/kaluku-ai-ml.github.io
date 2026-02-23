---
title: "PV-Layout: Geometric Yield Optimization"
math: true
excerpt: "Automated computational geometry for high-density solar array placement on complex industrial rooftops."
---

### The Challenge: The Geometry of Irradiance
Manual layout design for large-scale solar installations often fails to account for complex obstructions, leading to suboptimal string sizing and shading losses. For industrial rooftops, a 5% error in layout efficiency can result in hundreds of megawatt-hours of lost generation over the system's lifecycle.

### The Kaluku Solution
We developed a **vector-based layout engine** that automates the placement of PV modules while maximizing the ground coverage ratio ($$GCR$$). The system performs real-time shadow casting to ensure that inter-row spacing ($$d$$) is optimized for the local solar altitude angle ($$\alpha$$).

* **Obstacle-Aware Packing:** Uses AABB (Axis-Aligned Bounding Box) and polygon clipping to navigate roof vents, HVAC units, and parapets.
* **Shadow Modeling:** Calculates the minimum row pitch to avoid self-shading during the winter solstice.

$$d = w \cdot \frac{\cos(180 - \beta)}{\sin(\alpha)}$$

*Where $$w$$is the module width,$$\beta$$is the tilt angle, and$$\alpha$$ is the sun's elevation.*

### Technical Highlights
- **Performance:** Reduced design time from hours to seconds for 1MW+ sites.
- **Yield Accuracy:** Integrated with PVSYST-grade horizon shading analysis.
