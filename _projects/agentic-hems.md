---
title: "Agentic HEMS: LLM-Driven Grid Flexibility"
math: true
mathjax: true 
excerpt: "A multi-agent framework using LLMs to autonomously coordinate residential load scheduling and price-responsive demand."
header:
  teaser: /assets/images/agentic-hems-teaser.jpg
---

### The Challenge: Interaction Complexity
Most Home Energy Management Systems (HEMS) require users to input technical parameters for optimization. This high barrier to entry prevents widespread adoption of demand response. Users don't want to program their dishwasher; they want it to "run when it's cheapest."

### The Kaluku Solution
We built an **Agentic AI Framework** using the **ReAct (Reasoning + Acting)** pattern. A central Orchestrator Agent communicates with specialized agents for Weather, Pricing, and Appliance Control to autonomously shift loads.

* **Autonomous Orchestration:** Decomposes natural language requests (e.g., "Charge my EV by 7 AM using solar") into executable schedules.
* **Price Optimization:** Fetches real-time Day-Ahead Market (DAM) prices to minimize the cost function ($$J$$).

$$J = \min \sum_{t=1}^{24} (P_{load, t} - P_{pv, t}) \cdot C_{grid, t}$$

### Technical Highlights
- **Reasoning Chains:** Transparent logs showing the "why" behind every scheduling decision.
- **Zero-Shot Reliability:** Operates across diverse appliance types without custom hardcoding.
