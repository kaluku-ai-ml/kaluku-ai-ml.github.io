---
title: "Sub-pixel Defect Detection"
math: true
mathjax: true 
excerpt: "Using Attention-gated U-Nets for SEM imagery."
header:
  teaser: /assets/images/semiconductor-yield-teaser.jpg
---
### The Problem
Reducing False Alarm Rates ($P_{FA}$) in 14nm fabrication.

### Our Architecture
We implemented a custom encoder-decoder model with spatial attention to isolate low-contrast defects.

$$Loss = \alpha \cdot CrossEntropy + \beta \cdot Dice$$
