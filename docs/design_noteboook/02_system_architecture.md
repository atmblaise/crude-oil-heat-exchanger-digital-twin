# Crude Oil Preheat Train Digital Twin System

## 02_system_architecture.md — System Architecture Design

---

## 1. Architectural Overview

The system is designed as a modular industrial digital twin platform for analyzing heat exchanger networks in crude oil preheat trains.

It follows a layered architecture that separates:

* data ingestion
* physics-based computation
* system-level analysis
* user interface visualization

This separation ensures modularity, scalability, and long-term extensibility into other industrial thermal systems.

---

## 2. High-Level Architecture

The system is structured into four main layers:

### 2.1 Data Layer

Responsible for capturing and organizing process data.

Includes:

* inlet and outlet temperatures
* mass flow rates
* heat capacities
* operating conditions
* time-series performance data (future extension)

This layer defines the input state of the physical system.

---

### 2.2 Engineering Model Layer (Core Physics Engine)

This is the core computational layer of the system.

It implements thermodynamic and heat transfer principles including:

* energy balance across heat exchangers
* heat duty calculations
* LMTD or NTU-based analysis methods
* fouling resistance modeling
* efficiency and performance degradation estimation

This layer represents the **physical truth model** of the system.

---

### 2.3 System Analysis Layer

This layer transforms raw physics outputs into engineering insights.

It performs:

* heat exchanger performance evaluation
* system-wide energy recovery analysis
* identification of bottlenecks in heat exchanger networks
* estimation of energy losses and fuel penalties
* comparative performance analysis over time

This layer bridges physics computation and operational decision-making.

---

### 2.4 Interface Layer (SCADA Dashboard)

This layer provides visualization and interaction for users.

It includes:

* process flow diagram (PFD) visualization of heat exchanger networks
* key performance indicators (KPIs)
* trend analysis charts
* equipment-level performance indicators
* alert and anomaly indicators

This layer represents the **operator view of the system**.

---

## 3. Data Flow Architecture

The system follows a unidirectional data flow:

1. User inputs or simulated data are provided
2. Data is processed by the engineering model layer
3. Results are passed to system analysis layer
4. Insights are generated
5. Interface layer visualizes results

This ensures traceability and prevents circular logic.

---

## 4. System Components Breakdown

### 4.1 Heat Exchanger Module

Responsible for:

* individual exchanger performance calculation
* heat duty estimation
* outlet temperature prediction

---

### 4.2 Network Module

Responsible for:

* connecting multiple heat exchangers
* simulating preheat train behavior
* calculating cumulative heat recovery

---

### 4.3 Fouling Module

Responsible for:

* modeling performance degradation over time
* adjusting heat transfer efficiency
* simulating realistic industrial conditions

---

### 4.4 Analysis Module

Responsible for:

* identifying performance deviations
* calculating energy losses
* generating engineering insights

---

## 5. Design Principles

The system is built based on the following principles:

### 5.1 Modularity

Each component operates independently and can be extended or replaced without affecting the entire system.

---

### 5.2 Physics-First Design

All computations are based on fundamental heat transfer and thermodynamic principles rather than empirical-only models.

---

### 5.3 System-Level Thinking

The system focuses on the behavior of the entire heat exchanger network rather than isolated units.

---

### 5.4 Extensibility

The architecture is designed to allow future expansion into:

* HVAC systems
* cement plant waste heat systems
* industrial boiler systems
* multi-industry digital twin platforms

---

## 6. Technology Mapping (Conceptual)

At this stage, the architecture maps to:

* Frontend Layer → SCADA-style dashboard (web UI)
* Backend Layer → FastAPI service
* Engineering Layer → Python physics engine
* Data Layer → structured datasets (CSV/SQL in MVP stage)

---

## 7. System Boundaries

### Included:

* steady-state thermal analysis
* heat exchanger network simulation
* simplified fouling behavior modeling
* performance analytics and visualization

### Excluded (initial version):

* real-time sensor integration
* CFD-based simulations
* automatic control systems
* advanced machine learning prediction models

---

## 8. Future Architectural Extensions

The system is designed to evolve into:

* real-time digital twin systems with live plant data
* predictive maintenance systems using AI models
* multi-plant industrial optimization platforms
* cloud-based industrial analytics services

---

## 9. Summary

This architecture defines a modular digital twin system for crude oil preheat train heat exchanger networks.

It establishes a clear separation between physics modeling, system analysis, and user interaction layers, enabling scalable development into a full industrial engineering software platform.
