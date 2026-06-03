# Crude Oil Preheat Train Digital Twin System

## scada_dashboard.md — SCADA Dashboard Design

---

## 1. Purpose of This Interface

This document defines the design of the SCADA-style dashboard used to visualize and interact with the crude oil preheat train digital twin system.

The interface serves as the operational “control room view” of the heat exchanger network, translating engineering computations into visual, interpretable insights.

---

## 2. Design Philosophy

The dashboard is designed based on industrial SCADA principles:

* Real-time system visibility (simulated or live data)
* Clear visualization of process flow
* Emphasis on key performance indicators (KPIs)
* Early detection of abnormal system behavior
* Engineering-focused interpretability over aesthetic complexity

The goal is to replicate the decision-making environment of a process engineer.

---

## 3. Dashboard Layout Overview

The interface is structured into four main sections:

### 3.1 Process Flow Visualization Panel

### 3.2 Key Performance Indicators (KPIs)

### 3.3 Heat Exchanger Performance Panel

### 3.4 Trend & Diagnostic Analysis Panel

Each section serves a specific role in system interpretation.

---

## 4. Process Flow Visualization Panel

This section displays the heat exchanger network as a process flow diagram (PFD).

### Features:

* Representation of heat exchangers as connected nodes
* Flow direction of crude and utility streams
* Visual mapping of energy transfer pathways
* Highlighting of underperforming units

### Function:

This panel provides a system-level spatial understanding of how thermal energy moves through the network.

---

## 5. Key Performance Indicators (KPIs)

This section summarizes system-wide performance metrics.

### Core KPIs include:

* Total heat recovered in system
* Overall thermal efficiency
* Total energy loss
* Fuel savings potential
* Average exchanger efficiency

### Function:

These indicators provide a high-level overview of system health and performance.

---

## 6. Heat Exchanger Performance Panel

This section focuses on individual equipment performance.

### Features:

* Heat exchanger ID selection
* Real-time or simulated heat duty values
* Inlet and outlet temperature display
* Efficiency indicator per unit
* Fouling impact visualization

### Function:

This allows detailed inspection of each heat exchanger within the network.

---

## 7. Trend and Diagnostic Analysis Panel

This section displays time-based and comparative performance data.

### Features:

* Efficiency degradation trends (fouling behavior)
* Heat recovery variation over time
* Comparison between ideal and actual performance
* Detection of performance drift

### Function:

This panel supports diagnostic reasoning and maintenance decision-making.

---

## 8. Alert and Status Indicators

The system includes visual indicators for abnormal conditions:

* Reduced heat transfer efficiency
* Excessive fouling levels
* Deviation from expected thermal performance
* Underperforming heat exchanger units

These indicators support early detection of system inefficiencies.

---

## 9. User Interaction Model

The dashboard is designed for interaction through:

* Heat exchanger selection
* Time range filtering (future extension)
* Scenario comparison (clean vs fouled state)
* System-level vs unit-level switching

This allows flexible exploration of system behavior.

---

## 10. Data Integration Layer

The dashboard receives processed outputs from the simulation system:

* heat exchanger performance data
* network-level efficiency metrics
* fouling-adjusted results
* system aggregation outputs

It does not perform calculations; it only visualizes processed engineering data.

---

## 11. Design Constraints

The interface follows these constraints:

* No direct physics calculations in UI layer
* All data originates from backend simulation engine
* Visualization must remain interpretable for engineers
* System must remain modular for future expansion

---

## 12. Future Enhancements

Future versions may include:

* real-time sensor integration (IoT-based inputs)
* interactive process simulation controls
* predictive maintenance alerts
* AI-driven recommendation overlays
* 3D process visualization of heat exchanger networks

---

## 13. Role in Digital Twin System

This dashboard acts as the **operator interface layer** of the digital twin system.

It translates complex thermodynamic and simulation results into actionable engineering insights.

It bridges the gap between computational results and operational decision-making.

---

## 14. Summary

The SCADA dashboard provides a structured, industrial-style visualization system for the heat exchanger digital twin.

It enables engineers to monitor system performance, identify inefficiencies, and interpret simulation results in a clear and actionable format.
