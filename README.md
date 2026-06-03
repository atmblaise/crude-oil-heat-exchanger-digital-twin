# Crude Oil Preheat Train Digital Twin System

## Overview

This project is a physics-based digital twin system for modeling and analyzing heat exchanger networks in crude oil preheat trains.

It simulates thermal energy transfer, evaluates system efficiency, and models performance degradation due to fouling. The system is designed as a modular engineering software platform combining thermodynamic modeling, system simulation, and industrial-style visualization.

---

## Problem Statement

Heat exchanger networks in industrial crude oil systems degrade over time due to fouling and operational inefficiencies. This leads to:

- Reduced heat recovery efficiency  
- Increased fuel consumption in furnaces  
- Poor visibility of system-wide performance  
- Delayed detection of equipment degradation  

Existing tools are often either too simplified or too complex for practical system-level analysis.

This project addresses the gap by providing a structured, modular digital twin for heat exchanger networks.

---

## System Objectives

- Model heat exchanger networks as interconnected thermal systems  
- Simulate steady-state heat transfer behavior  
- Represent performance degradation using fouling models  
- Compute system-level energy recovery and efficiency  
- Provide SCADA-style visualization concepts for industrial interpretation  

---

## System Architecture

The system is designed in layered form:

- **Data Layer** → Process streams and operating conditions  
- **Physics Layer** → Heat exchanger + fouling models  
- **Simulation Layer** → System execution flow  
- **Analysis Layer** → Performance evaluation and insights  
- **Interface Layer** → SCADA-style visualization (design stage)

---

## Key Features

- Heat exchanger energy balance modeling  
- LMTD-based thermal analysis (conceptual design stage)  
- Fouling-based performance degradation simulation  
- Heat exchanger network simulation framework  
- System-level energy efficiency evaluation  
- Modular architecture for future industrial expansion  

---


## Project Structure

```
crude-oil-preheat-train-digital-twin/
│
├── README.md
├── LICENSE
├── requirements.txt
├── .gitignore
│
├── docs/
│   └── design-notebook/
│       ├── 00_overview.md
│       ├── 01_problem_definition.md
│       ├── 02_system_architecture.md
│       ├── physics_models/
│       ├── system_design/
│       ├── ui_design/
│       ├── experiments/
│       └── future_work.md
│
├── src/
│   ├── physics/
│   ├── simulation/
│   ├── analysis/
│   └── utils/
│
├── data/
│   ├── raw/
│   ├── processed/
│   └── examples/
│
├── app/
│   ├── api/
│   └── frontend/
│
├── notebooks/
│   └── validation/
│
└── tests/
```

---


## Current Status

This project is currently in the **design and architecture phase**.

Completed:
- System design documentation  
- Physics modeling framework definition  
- Simulation workflow design  
- SCADA-style interface specification  
- Test case definition  

Next Phase:
- Python-based simulation engine implementation  
- Jupyter-based model validation  
- FastAPI backend development  
- SCADA dashboard implementation  

---

## Technology Direction

Planned stack:

- Python (core simulation engine)  
- NumPy / SciPy (numerical computation)  
- FastAPI (backend services)  
- JavaScript / HTML (SCADA dashboard UI)  
- Jupyter Notebook (model validation and testing)  

---

## Long-Term Vision

This system is designed as the foundation of a scalable industrial digital twin platform capable of expanding into:

- HVAC system optimization  
- Cement plant waste heat recovery systems  
- Industrial boiler and furnace optimization  
- Multi-plant energy efficiency platforms  

---

## License

This project is licensed under the MIT License.

---

## Author Intent

This project is developed as an engineering software portfolio demonstrating:

- Industrial process modeling  
- Digital twin architecture design  
- Thermal system simulation  
- Engineering software development practices  
