---
title: "Digital Twin: High-Fidelity Energy Simulation"
layout: single
mathjax: true 
excerpt: "A Python-based simulation engine for modeling the interaction between PV generation, battery storage, and stochastic residential loads."
header:
  teaser: /assets/images/home-energy-simulator-teaser.jpg
---

### The Challenge: Predicting the Unpredictable
Residential energy flows are highly stochastic. To accurately size a battery or predict a home's self-sufficiency, you need more than just "averages"—you need a high-resolution simulation that models the interplay of physics and human behavior.

### The Kaluku Solution
The **Home Energy Simulator** is a discrete-time simulation engine that models a household's energy balance at 1-minute intervals. It acts as a digital twin for testing control algorithms before hardware deployment.

* **Stochastic Load Profiling:** Generates realistic usage patterns for non-controllable loads (lighting, electronics).
* **Battery Dynamics:** Models State of Charge ($$SoC$$) with non-linear efficiency and depth-of-discharge constraints.

$$SoC_{t+1} = SoC_t + (\eta_{ch} \cdot P_{ch} - \frac{P_{dis}}{\eta_{dis}}) \cdot \Delta t$$

### Technical Highlights
- **Modular Architecture:** Easily swap models for heat pumps, EVs, or specific inverter topologies.
- **Scenario Testing:** Run Monte Carlo simulations to determine the ROI of storage under varying utility tariffs.
