# Grover's Algorithm: SAT Puzzle Solver (Track F2)

## 📌 Project Overview
This repository contains a quantum computing solution to a Boolean Satisfiability (SAT) constraint problem using **Grover's Algorithm**, built with IBM's Qiskit. 

## 🚀 How to Run (Reproducibility)
Anyone can rerun this notebook locally or in a cloud environment (like qBraid).
1. Clone this repository.
2. Install the requirements: `pip install -r requirements.txt`
3. Open `grovers_puzzle_solver.ipynb` in Jupyter Notebook or qBraid Lab.
4. Run all cells to see the quantum circuit and amplitude amplification graph.

## ⚖️ Classical Baseline & Fair Comparison
To prove a **Quantum Advantage**, we must compare Grover's algorithm against a classical baseline.
* **The Problem Space:** A 3-variable SAT puzzle has $2^3 = 8$ possible combinations.
* **Classical Baseline:** A classical computer evaluating states randomly has a **12.5%** ($1/8$) chance of finding the correct target on its first evaluation. In the worst-case scenario, it must check $O(N)$ times.
* **Quantum Approach:** Grover's Algorithm searches unstructured databases in $O(\sqrt{N})$ time. 
* **Fair Comparison Result:** Our Qiskit simulation demonstrates that after just **2 quantum iterations** (evaluations of the Oracle), the probability of finding the target state jumps from the 12.5% classical baseline to **94.5%**. This visually and mathematically proves the quadratic quantum speedup.
