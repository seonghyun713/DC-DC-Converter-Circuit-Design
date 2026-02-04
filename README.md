# High-Efficiency Automotive DC-DC Converter Design & Control
> **From Component Selection to Particle Swarm Optimization (PSO) Control**

### 1. Project Overview
This project involves the full-cycle design of a DC-DC converter for automotive applications. It covers analog circuit design achieving **97% efficiency** through rigorous component selection and worst-case analysis, followed by the implementation of feedback controllers using both **Type 3 Compensation** and **Particle Swarm Optimization (PSO)** for optimal gain tuning.

* **Course:** Power Electronics (2025-2)
* **Tools:** Cadence PSpice, Psim, Matlab/Simulink (for PSO algorithm)
* **Key Achievement:** Achieved **97% Efficiency** in simulation & Verified Robustness (Worst-Case Analysis).

---

### 📂 Presentation Slides
For detailed analysis, design equations, and full results, please refer to the project reports.

* **Midterm Project (Open-Loop Design):**
  [📄 **View Midterm Presentation (PDF)**](./1_DC_DC_Converter_Mid_Project/전력전자_번개팀_연구모듈1_발표자료.pdf)

* **Final Project (Closed-Loop Control):**
  [📄 **View Final Presentation (PDF)**](./2_DC_DC_Converter_Final_Project/전력전자_번개팀_연구모듈2_발표자료.pdf)


---

### 2. Midterm Project: Robust Circuit Design (Open-Loop)
The goal was to design a hardware-feasible converter circuit that satisfies strict automotive standards.

<img width="862" height="437" alt="PE_mid" src="https://github.com/user-attachments/assets/ebe5988d-d065-4fb7-b098-42964e48e788" />

> **Figure 1.** PSpice Circuit Schematic with Selected Components.

* **Topology:** DC-DC Converter (Buck/Boost etc.)
* **Component Selection:**
    * Manually selected optimal MOSFETs/Diodes considering $R_{ds(on)}$, $Q_g$, and thermal characteristics.
    * Designed Inductor ($L$) and Capacitor ($C$) values for targeted ripple specifications.
* **Performance Verification:**
    * **Efficiency:** Achieved **97%** efficiency under nominal load.
    * **Reliability:** Passed **Worst-Case Analysis (WCA)**, ensuring stability under extreme temperature and component tolerance variations.

---

### 3. Final Project: Feedback Control System
Implemented closed-loop control to regulate output voltage against input voltage variations and load transients. Two different tuning strategies were applied and compared.

<img width="848" height="445" alt="PE_final" src="https://github.com/user-attachments/assets/6e480489-3905-4ce5-a96b-7b959f79c4a9" />

> **Figure 2.** Psim Control Loop Design & Optimization Results.

#### 🅰️ Classical Control (Type 3 Compensator)
* Designed a **Type 3 Compensator** to boost phase margin and ensure stability.
* Analyzed Bode plots to optimize bandwidth and transient response.

#### 🅱️ Intelligent Optimization (Particle Swarm Optimization - PSO)
* Applied **Particle Swarm Optimization (PSO)** algorithm to automatically tune the PID controller gains ($K_p, K_i, K_d$).
* **Objective:** Minimized the Integral Time Absolute Error (ITAE) to achieve faster settling time and reduced overshoot compared to manual tuning.

---

### 📂 Repository Structure
* `Mid/`: PSpice schematic (`.DSN`) and simulation profiles for open-loop design.
* `Final/`: Control logic implementation files (Type 3 & PSO code).
* `0_Doc/`: Project Presentation PDF and Datasheets.
