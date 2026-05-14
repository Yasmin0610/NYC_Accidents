# NYC_Accidents
# NYC Traffic Collision Analysis : Decision Support Model (2020)
*Research Question:* How can we identify dangerous hours and locations to prioritize enforcement resource allocation in New York City?

> **Operational Approach:** This project focuses on decision support with limited enforcement resources.
> The goal is not prediction but **prioritization**: to help city leadership allocate patrol forces where they are needed most.
<img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/30201d75-e2a2-4c8a-b173-3edf8d6885d2" />

---

---
## Research Assumptions and Framework

### Explicit Assumptions
- Higher collision severity indicates higher enforcement priority.
- Increased enforcement coverage may improve monitoring of high-risk areas.
- Budget scenarios are hypothetical operational simulations - not binding financial plans.
- **Budgets are presented as recurring monthly amounts** (overtime + patrol shifts paid monthly).

### Key Performance Indicator (KPI)
The central metric throughout the analysis- ” **Weighted Risk Coverage** (WRC):

$$\text{WRC} \;=\; \sum_{i} r_i \cdot u_i$$

where $r_i$ is the risk score of cell $i$ (Borough X Hour) and $u_i$ is the number of enforcement units allocated to it.
A higher score means more enforcement is concentrated where harm is greatest.

**Secondary validation metric** - Severe collision detection rate (Step 9, Monte Carlo):
$p_i = 1 - e^{-\alpha u_i}$, the probability that a collision in cell $i$ is captured by a patrol.

---
