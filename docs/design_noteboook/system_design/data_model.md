# Crude Oil Preheat Train Digital Twin System

## data_model.md — System Data Model Design

---

## 1. Purpose of This Model

This document defines how data is structured, represented, and managed within the crude oil preheat train digital twin system.

It ensures that all engineering calculations, simulations, and analyses are based on consistent and traceable data definitions.

The data model acts as the interface between real-world process conditions and the digital twin simulation engine.

---

## 2. Data Model Overview

The system is built around three primary data categories:

* Process Stream Data
* Heat Exchanger Unit Data
* System Performance Data

Each category represents a different level of abstraction in the digital twin system.

---

## 3. Process Stream Data

Process streams represent fluid movement through the heat exchanger network.

### 3.1 Input Variables

Each stream includes:

* Stream identifier
* Inlet temperature
* Outlet temperature
* Mass flow rate
* Specific heat capacity
* Fluid type (crude oil, utility fluid, etc.)

---

### 3.2 Role in System

Stream data defines the thermal boundary conditions for heat transfer calculations.

It is used directly in:

* heat exchanger energy balance calculations
* system-wide heat integration analysis

---

## 4. Heat Exchanger Unit Data

Each heat exchanger is treated as a discrete computational unit in the system.

### 4.1 Structural Variables

Each unit contains:

* Heat exchanger ID
* Associated hot stream ID
* Associated cold stream ID
* Heat transfer area
* Overall heat transfer coefficient (clean condition)
* Fouling resistance factor
* Operational status

---

### 4.2 Functional Variables

Derived or computed values include:

* Heat duty (Q)
* Outlet temperatures (hot and cold streams)
* Effectiveness
* Performance efficiency index
* Degradation factor (from fouling model)

---

## 5. System Performance Data

This category represents aggregated system-level behavior.

### 5.1 Key Metrics

* Total heat recovered in network
* Total energy loss
* Overall thermal efficiency
* Fuel saving potential
* Deviation from ideal performance

---

### 5.2 Time-Based Data (Future Extension)

The system is designed to support time-series tracking of:

* efficiency degradation trends
* fouling progression
* performance drift over operational time

---

## 6. Data Flow Structure

The data flow follows a structured transformation pipeline:

1. Raw process data (streams and conditions)
2. Heat exchanger unit calculations
3. Network-level aggregation
4. System performance evaluation
5. Visualization output layer

This ensures traceability from input data to final engineering insight.

---

## 7. Data Relationships

The system is built on the following relationships:

* Multiple streams interact through heat exchangers
* Each heat exchanger connects exactly two streams
* Heat exchanger outputs feed into downstream stream conditions
* System performance is derived from all unit-level results

This creates a connected network model rather than isolated components.

---

## 8. Data Consistency Rules

To maintain system integrity:

* All stream data must be uniquely identifiable
* Heat exchanger units must reference valid stream IDs
* No orphaned streams or disconnected units are allowed
* All derived values must be traceable to input data

---

## 9. Data Storage (Conceptual Layer)

In the initial system version, data may be stored using:

* structured JSON objects
* CSV-based datasets
* in-memory Python data structures

Future versions may migrate to:

* SQL-based systems
* time-series databases for performance tracking

---

## 10. Role in Digital Twin System

This data model acts as the foundation for:

* physics model execution
* simulation consistency
* system-level analysis
* visualization and SCADA dashboard rendering

Without this layer, the system cannot maintain structured simulation logic.

---

## 11. Summary

The data model defines how industrial process information is structured and processed within the digital twin system.

It connects raw process conditions to engineering calculations and ensures system-wide consistency across simulations and analyses.
