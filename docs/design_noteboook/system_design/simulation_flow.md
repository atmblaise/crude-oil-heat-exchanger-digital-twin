# Crude Oil Preheat Train Digital Twin System

## simulation_flow.md — Simulation Flow Design

---

## 1. Purpose of This Document

This document defines how the digital twin system executes a complete simulation of a crude oil preheat heat exchanger network.

It describes the step-by-step transformation of input process data into engineering outputs, performance metrics, and system-level insights.

The simulation flow ensures that all calculations follow a deterministic and traceable sequence.

---

## 2. Simulation Overview

The simulation represents a steady-state evaluation of a heat exchanger network under defined operating conditions.

It processes:

* process stream data
* heat exchanger configurations
* fouling conditions
* system constraints

to generate:

* thermal performance results
* energy recovery metrics
* efficiency indicators
* degradation insights

---

## 3. High-Level Simulation Pipeline

The simulation follows a structured sequence:

1. Input data initialization
2. Stream validation and preprocessing
3. Heat exchanger unit-level calculations
4. Network-level energy integration
5. Fouling effect application
6. System performance aggregation
7. Output generation and visualization

---

## 4. Step-by-Step Simulation Flow

---

### 4.1 Input Initialization

The simulation begins by loading all system inputs:

* process stream conditions
* heat exchanger parameters
* fouling state variables
* system configuration data

At this stage, the system defines the initial thermal state of the network.

---

### 4.2 Data Validation and Consistency Check

Before calculations begin, the system verifies:

* all stream identifiers are valid
* all heat exchangers are properly connected
* no missing input variables exist
* physical constraints are satisfied (e.g., temperature feasibility)

This ensures simulation stability.

---

### 4.3 Heat Exchanger Unit Simulation

Each heat exchanger is evaluated individually using the heat exchanger physics model.

For each unit:

* inlet stream conditions are retrieved
* heat transfer is calculated
* outlet temperatures are computed
* heat duty is determined

This step produces unit-level performance results.

---

### 4.4 Network Interaction Calculation

After individual units are solved, the system evaluates interactions between connected heat exchangers.

This includes:

* sequential heat recovery across the network
* updated stream conditions propagation
* cumulative thermal effects

This step ensures system-level consistency.

---

### 4.5 Fouling Effect Application

The fouling model is applied to adjust heat exchanger performance.

For each unit:

* thermal resistance is updated based on fouling level
* effective heat transfer coefficient is reduced
* performance degradation is reflected in recalculated outputs

This introduces realistic operational behavior.

---

### 4.6 System-Level Aggregation

The system aggregates all unit results into global performance metrics:

* total heat recovered
* total energy loss
* overall thermal efficiency
* deviation from ideal operation
* fuel saving potential

This transforms unit-level results into system-level insights.

---

### 4.7 Performance Analysis Layer

The system interprets aggregated results to identify:

* underperforming heat exchangers
* bottlenecks in heat recovery
* inefficiencies in network configuration
* impact of fouling on overall system performance

This layer converts numerical outputs into engineering insights.

---

### 4.8 Output Generation

Final simulation outputs include:

* heat exchanger performance report
* network efficiency summary
* energy balance results
* degradation indicators
* system optimization suggestions (future extension)

These outputs are used by the visualization layer.

---

### 4.9 Visualization Interface Trigger

The final step sends processed results to the SCADA-style interface layer.

This enables:

* process flow visualization
* KPI display
* trend analysis charts
* equipment-level performance monitoring

---

## 5. Data Flow Logic

The simulation follows a strict unidirectional flow:

Input Data → Unit Simulation → Network Propagation → Fouling Adjustment → Aggregation → Analysis → Output Visualization

This ensures:

* no circular dependencies
* traceable computation steps
* reproducible simulation results

---

## 6. Simulation Assumptions

The simulation operates under the following assumptions:

* steady-state conditions
* no transient thermal dynamics
* constant fluid properties (initial version)
* no phase change effects
* deterministic system behavior (no randomness)

---

## 7. Error Handling Concept (Future Design Consideration)

Future versions may include:

* detection of invalid stream configurations
* convergence checks for network stability
* anomaly detection in performance results

These are not implemented in the initial version but are considered in system scalability design.

---

## 8. Role in Digital Twin System

This simulation flow is the operational backbone of the digital twin.

It defines:

* how the system executes computations
* how data moves through the physics engine
* how results are structured and interpreted

Without this layer, the system would remain static and non-operational.

---

## 9. Summary

The simulation flow defines a structured, step-by-step execution process for modeling and analyzing heat exchanger networks.

It ensures that the digital twin system operates in a deterministic, modular, and physically consistent manner from input data to final engineering insights.
