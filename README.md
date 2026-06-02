# Crude Oil Preheat Heat Exchanger Digital Twin

## Overview

This project presents a **first-principles digital twin** of a refinery crude oil preheat shell-and-tube heat exchanger. The system combines **process simulation (DWSIM)** with a **Python-based dynamic modeling layer** to replicate real industrial behavior including fouling, sensor noise, and process disturbances.

The goal is to bridge the gap between **steady-state process simulation** and **real-time industrial operation**, aligning with modern **Industry 4.0 digitalization practices**.

---

## Industrial Context

In petroleum refineries, crude oil is preheated using heat recovered from hot process streams before entering the distillation unit. This reduces furnace fuel consumption and improves energy efficiency.

However, real systems suffer from:

* Heat exchanger fouling
* Sensor noise and drift
* Flow and temperature disturbances
* Performance degradation over time

This project models these effects to create a realistic operational digital twin.

---

## Objectives

* Develop a steady-state heat exchanger model using **DWSIM**
* Implement first-principles heat transfer equations
* Simulate fouling and degradation effects over time
* Introduce sensor noise and measurement uncertainty
* Build a Python-based dynamic digital twin
* Create performance monitoring and data logging system

---

## System Architecture

The system is composed of three layers:

### 1. Process Simulation Layer (DWSIM)

* Steady-state shell-and-tube heat exchanger
* Thermodynamic property modeling
* Energy balance validation

### 2. Digital Twin Layer (Python)

* Time-dependent simulation
* Fouling resistance evolution
* Sensor noise modeling
* Control logic simulation

### 3. Data & Visualization Layer

* SCADA-style monitoring (Streamlit planned)
* Performance tracking
* Historical data logging

---

## Key Engineering Models
This project is based on fundamental heat transfer and thermodynamic principles commonly used in refinery heat exchanger analysis.

### Energy Balance
The system assumes conservation of mass under steady-state conditions. The total mass entering the heat exchanger equals the total mass leaving it for both hot and cold streams. This ensures no accumulation or loss of material within the system.

---

### Heat Transfer Equation
The heat exchanger operates based on conservation of energy. The thermal energy lost by the hot stream is equal to the energy gained by the cold stream, assuming no heat losses to the environment. This relationship defines the overall heat duty of the system.

---

### Fouling Model
Over time, unwanted material deposits accumulate on the heat transfer surfaces. This fouling layer increases thermal resistance, reduces heat transfer efficiency, and gradually decreases the performance of the exchanger. The model captures this as a time-dependent degradation process.

---

### Sensor Model
In real industrial systems, measurements are never perfectly accurate. Temperature and flow readings are affected by noise, calibration errors, and signal disturbances. The model introduces controlled uncertainty to replicate real sensor behavior in plant conditions.

---

## Dynamic System Behavior

Unlike steady-state simulations, the digital twin introduces time dependence. System performance evolves over time due to fouling, disturbances, and control actions, allowing the model to reflect realistic refinery operating conditions.

---

## Tools & Technologies

* DWSIM (Process Simulation)
* Python (NumPy, Pandas, SciPy)
* LaTeX (Engineering report writing)
* Git & GitHub (Version control)
* Streamlit (planned SCADA-style dashboard)

---

## Project Structure

```
crude-oil-heat-exchanger-digital-twin/
│
├── paper/              # LaTeX engineering report
├── dwsim/             # Process simulation model
├── python/            # Digital twin engine
├── data/              # Simulation datasets
├── figures/           # Diagrams and plots
├── README.md
└── requirements.txt
```

---

## Expected Outcomes

* Realistic heat exchanger performance simulation
* Fouling impact visualization over time
* Sensor behavior under uncertainty
* Industrial-style performance monitoring system
* Foundation for predictive maintenance modeling

---

## Engineering Basis

This project is grounded in:

* First-law thermodynamics
* Heat transfer theory
* Shell-and-tube exchanger design principles
* Fouling resistance modeling
* Digital twin architecture principles (Industry 4.0)

---

## Future Work

* Integration with real-time SCADA data
* Machine learning-based fouling prediction
* Multi-exchanger heat integration network
* Deployment as web-based industrial dashboard

---

## Author

**Blaise Atambo**
Chemical and Process Engineering
Nairobi, Kenya

---

## Note

This repository is part of a broader portfolio of engineering digital twin systems focused on industrial simulation, process optimization, and energy systems modeling.
