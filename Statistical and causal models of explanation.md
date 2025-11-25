> Explore, compare and evaluate statistical vs causal models of explanation

**Argument**
Classical theories of scientific explanation: Deductive-Nomological (DN), Statistical Relevance (SR), and Causal Mechanical (CM) have challenges when translating into the needs and capabilities of automated decision-making systems
- Each model reflects a different level of explanation
- Key tension - modern systems operate statistically, but human ethical demands require causal, human-like reasoning.
- The gap between the CM ideal and the SR practice is a core ethical problem. Human accountability requires explanations that are grounded, justified, and warranted NOT complex statistical models
### Models of Explanation

**Deductive-Nomological (DN) Model**
* Explained phenomena (explanandum) is deduced from general laws and initial conditions
	* Newton's laws and initial conditions -> explain the planet's orbit
* This conceptually lines up with **white box** system or interpretable model (Slides, Week 4) eg. decision tree or linear regression
* Limitation: With AI, models use probabilistic weights and billions of parameters NOT universal laws

**Statistical Relevance (SR) Model**
* Explains via correlation or probability. (statistical relevance or conditional dependence)
* Statistically relevant factors contribute to explanation
* **De facto mode of explanation** achieved by most practical XAI methods
	* Post-hoc explanation techniques like **LIME** (Local Interpretable Model-agnostic Explanations) and **SHAP** (SHapley Additive exPlanations) function by identifying which input features contributed most significantly to a prediction (Slides, Week 4) -> these identify statistical association NOT deep casual mechanisms
* Limitation: High correlation DOES NOT imply causation
	* Critical contexts like medical diagnosis, loan approval or criminal justice (COMPAS) SR explanations are fragile, correlations may not be actual reasons accepted by humans
	* System remains opaque and non-linear, explanation may only confirm what human already believed (cognitive bias)
* **The Unsatisfiable Triad:** SR reinforces the unsatisfiability of fairness, accountability and transparency (Reading 2, Week 4)
	1. **Accuracy vs. Transparency:** Accuracy from large set of weighted parameters -> inhibits transparency (black box)
	2. **Fairness vs. Accountability:** Fairness is often contingent on **accuracy**. However, the high complexity prevents a casual explanation (CM) model -> the decision lacks accountability for all its outputs so fairness costs accountability

**Causal Mechanical (CM) Model**
* Explanation from **physical causal processes and interactions**
* Explanatory depth ethical AI ideally requires but not delivered by current systems - high interpretability since reasoning chain is comprehensible and deterministic
* Understand *why* something happened by identifying causal processes (Reading 2, Week 4)
* Limitation: Deep neural networks (DNNs) are "black boxes" - we can inspect weights but not understand meaning (semantically opaque)
* Desired for high-stakes automated decision making, such as recidivism prediction (COMPAS) (Reading 2, Week 4)