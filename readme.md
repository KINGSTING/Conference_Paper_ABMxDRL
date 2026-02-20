# Optimizing Household Waste Segregation Policy in the Municipality of Bacolod: An Agent-Based Modeling and Heuristic-Guided Deep Reinforcement Learning Approach

**Authors:** Hussam M. Bansao, Jemar John J. Lumingkit, and Dante D. Dinawanao, M.Sc.  
**Affiliation:** College of Computer Studies, MSU-Iligan Institute of Technology, Iligan City, Philippines  

---

## 📌 Overview
This repository contains the methodology, simulation models, and findings for our study on municipal solid waste management (SWM) policy optimization. The implementation of the Ecological Solid Waste Management Act (RA 9003) remains a critical challenge for Local Government Units (LGUs) in the Philippines. Compliance is often hindered by budget constraints, lack of behavioral data, and the complexity of enforcing segregation at the household level.

This project presents a novel computational framework that combines **Agent-Based Modeling (ABM)** with **Heuristic-Guided Deep Reinforcement Learning (HuDRL)** to simulate and discover the most cost-effective policy interventions for the Municipality of Bacolod, Lanao del Norte.

## 🧠 Methodology
Our virtual laboratory was developed using Python's MESA framework. The architecture models the decentralized governance of Bacolod as a Markov Decision Process (MDP) operating on quarterly time steps.

### 1. Agent-Based Model (ABM)
* **Household Agents:** Decision-making is grounded in the Theory of Planned Behavior (TPB). Agent behavior dynamically evolves in response to LGU interventions (fines, incentives, education) and is influenced by the compliance of neighboring households (Social Norms).
* **Barangay Agents:** Represent the seven local government units managing fiscal allocation and personnel deployment.
* **Enforcement Agents:** Conduct stochastic inspections to enforce the "No Segregation, No Collection" policy.

### 2. Heuristic-Guided Deep Reinforcement Learning (HuDRL)
To overcome the "Sparse Reward Problem" in high-dimensional municipal resource allocation, we implemented a custom Actor-Critic architecture utilizing Deep Proximal Policy Optimization (Deep PPO).
* **Reward Shaping:** Guides the agent away from sub-optimal, equitable fund distributions.
* **Targeted Amplification:** Multiplies intent signals to critically underperforming nodes to accelerate the discovery of optimal tipping points.

## 📊 Key Findings
Through 10,000 simulated periods, our experiments yielded the following insights:

* **Superior Compliance:** The HuDRL agent significantly outperformed traditional "Status Quo" manual policies and standard PPO agents, achieving a 92.8% terminal compliance rate (compared to 57.1% for the baseline).
* **Sequential Saturation Strategy:** The AI discovered that focusing 51%-69% of the municipal budget sequentially on single barangays builds resilient social norms much more effectively than diluting funds equally across all areas.
* **The Convenience Barrier:** A Sobol Global Sensitivity Analysis revealed that the physical "Cost of Effort" is the primary barrier to compliance, accounting for 83% of the variance in outcomes.
* **The Value-Action Gap:** Internal "Attitude" showed near-zero sensitivity, mathematically proving that educational campaigns have reached diminishing returns and must be paired with structural support to bridge the gap between intent and action.

## 📎 Repository Structure
*(Note: Structure this section based on your actual uploaded files)*

```text
├── data/                  # Calibration data, socio-demographic profiles, and LGU operational budgets
├── models/                # Python files for the MESA Agent-Based Model and Household logic
├── rl_agent/              # Deep PPO implementation and HuDRL custom reward shaping scripts
├── notebooks/             # Jupyter notebooks containing Sobol Sensitivity Analysis and data visualization
├── paper/                 # LaTeX source files, compiled PDF, and references (.bib)
└── README.md
```

## 🤝 Acknowledgments
The authors thank the Bacolod LGU and its component barangays for their support and data.

*Use of Generative AI:* The authors used Gemini 3.1 Pro for grammatical corrections and maintain full responsibility for the final manuscript.
