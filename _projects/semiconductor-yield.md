---
title: "Sub-pixel Defect Detection"
excerpt: "Using Attention-gated U-Nets for SEM imagery."
header:
  overlay_image: /assets/images/semiconductor-yield-teaser.jpg
  overlay_filter: 0.5 # Dim the image to make text pop
  teaser: /assets/images/kaluku-logo.jpg
---
### The Problem
Reducing False Alarm Rates ($P_{FA}$) in 14nm fabrication.

### Our Architecture
We implemented a custom encoder-decoder model with spatial attention to isolate low-contrast defects.

$$Loss = \alpha \cdot CrossEntropy + \beta \cdot Dice$$
