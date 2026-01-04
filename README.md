# Revisiting the EPR Paradox: A Qiskit Simulation of Bell’s Inequality

This repository contains a **Qiskit-based simulation of the EPR–Bohm experiment and the CHSH Bell test**, reproducing the quantum-mechanical violation of Bell’s inequality and demonstrating nonlocal correlations using entangled qubits.

The project was developed as part of the *Advanced Quantum Mechanics – I* course and serves as a computational verification of foundational quantum concepts using modern quantum computing frameworks. :contentReference[oaicite:0]{index=0}

---

## 📌 Overview

Quantum entanglement challenges classical notions of locality and realism. In 1935, Einstein, Podolsky, and Rosen (EPR) argued that quantum mechanics might be incomplete. John Bell later showed that **no local hidden-variable theory can reproduce all quantum predictions**, formalized through Bell inequalities.

This project:
- Constructs entangled Bell states using quantum circuits
- Simulates correlated spin measurements for spatially separated observers
- Computes expectation values for different detector settings
- Evaluates the **CHSH Bell parameter** to test the inequality

The simulation results **violate the classical bound** \( |S| \leq 2 \), confirming quantum nonlocality.

---

##  Workflow

1. **Demonstrates quantum entanglement**
   - Creates a Bell state using Hadamard and CNOT gates
   - Verifies correlated measurement outcomes via repeated circuit execution

2. **Simulates the Bell–CHSH experiment**
   - Implements Alice–Bob measurements with rotated bases
   - Uses angle configurations known to maximize Bell violation

3. **Computes statistical correlations**
   - Calculates expectation values  
     \[
     E(\theta_a, \theta_b) = \frac{N_{00}+N_{11}-N_{01}-N_{10}}{N_{00}+N_{11}+N_{01}+N_{10}}
     \]
   - Evaluates the CHSH parameter  
     \[
     S = |E(a,b) - E(a,b') + E(a',b) + E(a',b')|
     \]

---

##  Key Result

From the simulation (with \(10^4\) shots per setting):

- **CHSH parameter obtained:**  
  \[
  S = 2.3868
  \]

- **Classical bound:** \( |S| \leq 2 \)  
- **Quantum maximum:** \( 2\sqrt{2} \approx 2.828 \)

The result **clearly violates the classical limit**, in agreement with quantum mechanical predictions.

---

##Requirements

- Python ≥ 3.9  
- Qiskit  

Install dependencies using:
```bash
pip install qiskit
