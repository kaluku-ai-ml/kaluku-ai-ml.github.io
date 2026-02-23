---
title: "VoltVision AI: Automated Utility Integrity"
excerpt: "Edge-AI for high-precision power line and vegetation encroachment detection."
header:
  teaser: /assets/images/voltvision-teaser.jpg # Placeholder for an image later
sidebar:
  - title: "Vertical"
    text: "Energy & Utilities / Telecom"
  - title: "Tech Stack"
    text: "PyTorch, DeepLabV3+, TensorRT, OpenCV"
---

### The Challenge: High-Entropy Asset Monitoring
Utility providers face a multi-billion dollar challenge in vegetation management. The core technical hurdle is the **segmentation of low-contrast, thin-feature objects** (power lines) against high-entropy, chaotic backgrounds (dense foliage, urban structures). 

Traditional inspection is manual, subjective, and lacks the scalability required for modern grid reliability.

### The Kaluku Solution: VoltVision AI
VoltVision AI is a specialized Computer Vision framework designed for the automated detection of utility infrastructure and environmental encroachment. 

#### **Technical Architecture**
* **Semantic Segmentation:** Utilizes a modified DeepLabV3+ architecture with a specialized loss function to prioritize linear feature preservation, preventing the "vanishing wire" effect.
* **Edge-Optimized Inference:** Quantized for deployment on low-power edge modules (NVIDIA Jetson/OAK-D), enabling real-time processing on inspection drones.
* **Probabilistic Risk Scoring:** Beyond simple detection, the system calculates an "Encroachment Index" based on the spatial proximity of vegetation to energized conductors.

#### **Performance Metrics**
The model achieves a **Mean Intersection over Union (mIoU) of 0.89** in varied lighting conditions, significantly outperforming standard off-the-shelf segmentation models for thin-feature detection.

$$J(A, B) = \frac{|A \cap B|}{|A \cup B|}$$
*Optimizing for Intersection over Union (IoU) to ensure pixel-perfect wire segmentation.*

---

### Interactive Demonstration
We have developed a live inference application to demonstrate the model's capability in real-world scenarios. 

<div style="max-width: 800px; margin: 0 auto;">
  <video width="100%" style="max-height: 70vh; outline: none;" controls>
    <source src="{{ '/assets/videos/voltvision-demo.mp4' | relative_url }}" type="video/mp4">
    Your browser does not support the video tag.
  </video>
</div>

---

### Implementation & ROI
* **40% Reduction** in manual inspection man-hours.
* **Proactive Outage Mitigation:** Identifying high-risk encroachment zones before they lead to grid failure.
* **Scalable Data Pipelines:** Integrated with GIS for automated corridor mapping.
