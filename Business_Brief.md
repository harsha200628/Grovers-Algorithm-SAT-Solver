# One-Page Business Brief: Quantum Optimization

### 👤 The Customer
**Supply Chain & Logistics Companies** (e.g., FedEx, Amazon, Airlines). These companies constantly solve complex Constraint Satisfaction Problems (CSPs), such as determining the optimal routing for thousands of delivery trucks while adhering to strict constraints like fuel limits, traffic, and delivery windows.

### 💸 The Cost of the Problem
In logistics, routing problems scale exponentially ($O(2^n)$). Adding just a few more constraints or delivery stops doubles the amount of computing power required to find the perfect route. Because classical computers cannot handle this exponential wall, companies are forced to use "good enough" approximation algorithms. This failure to find the *absolute optimal* route leaves billions of dollars wasted in excess fuel, vehicle maintenance, and delayed delivery times every year globally.

### 📈 The Result (Quantum Solution)
**Grover's Algorithm** provides a quadratic speedup ($O(\sqrt{N})$) over classical brute-force search. 
In our prototype, we modeled a basic constraint problem using a Quantum Phase Oracle. 
* **Classical approach** yielded a 12.5% baseline success rate per evaluation.
* **Our Quantum approach** achieved a **94.5% success probability in just 2 hardware iterations**. 
Applied at scale, this means future quantum computers could search massive logistics databases quadratically faster, finding the *true* optimal route instead of an approximation.

### ⚠️ Limits of the Result
While mathematically superior, deploying this today has physical limits due to the current **NISQ (Noisy Intermediate-Scale Quantum)** era:
1. **Decoherence & Hardware Noise:** Our algorithm mathematically hits 100% accuracy at 6 iterations. However, on physical quantum hardware, running deeper circuits introduces decoherence errors. The practical limit today forces us to stop at 2 iterations (94.5%) to avoid noise corruption.
2. **Scaling Limitations:** Mapping millions of real-world logistics variables requires thousands of stable logical qubits. Until Quantum Error Correction (QEC) matures over the next decade, we are restricted to solving small-scale optimization proofs-of-concept rather than enterprise-scale routing.
