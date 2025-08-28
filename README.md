# Windows Experimentation Work Sample: Multi-Variant A/B Test
**Author:** Crystal M. Ford  

---

## Overview
This project simulates a Windows-style **multi-arm A/B test** to evaluate different feature designs.  
The dataset is simulated, but the process mirrors how Microsoft teams approach experimentation:

- Define clear hypotheses  
- Randomize and test across multiple variants  
- Use rigorous statistics to separate signal from noise  
- Provide a clear ship/no-ship recommendation with guardrails  

The goal: show how I design, analyze, and explain experiments to drive **smarter product decisions**.

---

## Study Design
- **Experiment:** 4 groups — Control + 3 design variants  
- **Metric:** Conversion (binary outcome: did the user take the target action?)  
- **Hypothesis:** At least one design improves conversion vs. Control  
- **Randomization:** Equal allocation across arms  
- **Duration:** Simulated as a 14-day test  
- **Decision Rule:**  
  - Significant lift vs. Control (α = 0.05, Bonferroni-adjusted)  
  - No guardrail metric degradation (e.g., latency, crash rate — not simulated here)  

---

Results

Here’s the core result (conversion rates with 95% CIs):

Executive Summary

Winner: Design C

Conversion: 10.82% (Control: 7.86%)

Relative Lift: ~38%

Bonferroni-adjusted p-value: 2.2e-06

Recommendation: Ship Design C, monitor guardrails (latency, crash rate, uninstall rate), and run a post-rollout holdback to validate long-term impact.
