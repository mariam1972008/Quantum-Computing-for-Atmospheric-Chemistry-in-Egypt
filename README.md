# Quantum-Computing-for-Atmospheric-Chemistry-in-Egypt
# Project Name: Quantum AI Hackathon Project

This project was submitted for the *Quantum AI Hackathon* by *team-2-atmospheric_chem*.

---

## Team Members

| Name             | Role in Project             |
|------------------|-----------------------------|
| Mariam Khaled    | Model Development           |
| EzzEldin Khaled  | Project Coordinator    |
| Nada Mohamed     | Data Preprocessing          |

---

## Project Overview

This project was developed to participate in the Quantum AI Hackathon. The project addresses the problem of air pollution in the Nile Delta, specifically the formation of sulfate aerosols.

The problem tackled is that the Nile Delta is characterized by very high humidity (exceeding 80%) year-round. This high humidity accelerates the formation of sulfate aerosols resulting from industrial emissions.

To address this challenge, Team 2-atmospheric_chem performed a quantum simulation of how humidity affects the chemical reaction chain that leads to the formation of these particles. 

By taking this approach, the team combined classical and quantum AI methodologies to tackle this important environmental challenge.


 
 
---

## Step-by-Step Explanation

### 1. Data Preprocessing
*Responsible Team Member: Nada Mohamed*  

---

### 2. Classical Model Development
*Responsible Team Member:* Mariam Khaled

The classical model optimizes the geometries of SO₃ + nH₂O → H₂SO₄ clusters (n = 1–3) and computes their reaction pathway energy surfaces using classical methods HF. It then predicts reaction rates at 60–100% relative humidity using models like TST.

---

### 3. Quantum Model Development
*Responsible Team Member: Mariam Khaled*

This project uses a hybrid quantum-classical model to simulate the reaction pathway for:

$$
SO_3 + nH_2O \rightarrow H_2SO_4 \quad (n = 1–3)
$$

#### 1. Purpose of the Quantum Model
- Compute reaction pathway energy surfaces (PES) using quantum methods.  
- Calculate ΔE (reaction energy differences) for each cluster size.  
- Map these quantum results to reaction rate predictions and aerosol nucleation probabilities.

#### 2. Quantum Methods
- *VQE (Variational Quantum Eigensolver)* was used to compute the ground state electronic energy of each molecular configuration.  
- *Qiskit Nature* was used to:  
  1. Generate the electronic structure problem from molecular coordinates.  
  2. Map fermionic Hamiltonians to qubit Hamiltonians (Jordan–Wigner mapping).  
  3. Optimize the variational circuit to get the lowest energy.  

Results are combined with classical molecular geometry optimization to construct the PES.

#### 3. Workflow
1. Generate molecular coordinates for SO₃ + nH₂O clusters (optimized classically).  
2. Compute ground-state energy of reactants and products with VQE.  
3. Calculate $ΔE = E_{products} – E_{reactants}$ for each step of the pathway.  
4. Feed ΔE into a classical kinetic model to estimate reaction probabilities.

---

### 4. Project Coordinator
*Responsible Team Member: EzzEldin Khaled*  

Contributions to the project's success were made through several key tasks, including:

Presentation Development: Responsibility for creating the project's presentation to effectively communicate the team's findings.

Workflow Coordination: Assistance in coordinating team efforts to ensure a smooth and efficient workflow.

Guidance and Feedback Implementation: Meticulous implementation of all instructions and feedback provided by supervisors.

Knowledge Development: Attendance at relevant lectures and workshops to stay updated on the latest information and recommendations, which helped keep the team informed.

These contributions were essential for achieving the project's goals.

---

## Requirements
Placeholder: List required software (e.g., Python, Jupyter, Qiskit, TensorFlow) and dependencies in requirements.txt. Include instructions for setting up the environment, including quantum libraries.

---

## How to Run the Project
Using Qiskit simulator and Hartee Fock solver for classical solution.  

---

## Results and Visualizations

### Quantum Results
<p align="center">
  <img src="./Quantum result.png" width="500"/>
</p>
<p align="center">
  <img src="./Quantum result 2.png" width="500"/>
</p>

### Classic Results
<p align="center">
  <img src="./Classic result.png" width="500"/>
</p>
<p align="center">
  <img src="./Classic result 2.png" width="500"/>
</p>


---

## Challenges and Solutions
The biggest challenge is quantum hardware limitations, we handled it by reduce the number of electrons and orditals in the simulator.

---

## Future Improvements
Use FCI solver instead of Hartree Fock solver because it is more accurate.
 
