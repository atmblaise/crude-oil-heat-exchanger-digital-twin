# Crude Oil Preheat Train Digital Twin System

## test_cases.md — System Test Cases and Validation Scenarios

---

## 1. Purpose of This Document

This document defines structured test cases used to validate the correctness, stability, and engineering realism of the crude oil preheat train digital twin system.

The objective is to ensure that the physics models, simulation flow, and data structures behave consistently under different operating conditions.

---

## 2. Testing Philosophy

The system is validated based on:

* physical consistency (energy balance correctness)
* engineering realism (expected thermal behavior)
* system stability (no breakdown in calculations)
* sensitivity to fouling and operational changes

The goal is not software testing alone, but **engineering validation of simulation behavior**.

---

## 3. Test Case Categories

The system is tested under four main categories:

* Baseline (clean system operation)
* Load variation scenarios
* Fouling degradation scenarios
* System stress conditions

Each category evaluates different aspects of system behavior.

---

## 4. Test Case 1 — Baseline Operation (Clean Condition)

### Objective:

Validate system performance under ideal clean conditions.

### Input Conditions:

* All heat exchangers operating without fouling
* Standard inlet temperatures and flow rates
* Nominal heat transfer coefficients

### Expected Behavior:

* Maximum heat recovery efficiency
* Stable energy balance across all units
* No performance degradation indicators

### Validation Criteria:

* Energy balance conservation maintained
* Outlet temperatures within expected engineering range
* System efficiency near theoretical maximum for given conditions

---

## 5. Test Case 2 — Increased Thermal Load

### Objective:

Evaluate system response to increased flow or temperature variation.

### Input Conditions:

* Increased crude oil flow rate
* Higher inlet temperature variation
* Constant exchanger configuration

### Expected Behavior:

* Reduced individual exchanger effectiveness
* Redistribution of heat across network
* Increased energy demand in downstream heating system

### Validation Criteria:

* System remains stable under load change
* Energy balance still conserved
* Predictable drop in efficiency

---

## 6. Test Case 3 — Fouling Progression Scenario

### Objective:

Validate fouling model integration and performance degradation behavior.

### Input Conditions:

* Gradual increase in fouling resistance over time
* Constant operating conditions otherwise

### Expected Behavior:

* Progressive decline in heat transfer efficiency
* Increasing temperature approach between streams
* Reduced overall heat recovery

### Validation Criteria:

* Smooth degradation trend (no abrupt discontinuities)
* Logical correlation between fouling level and performance loss
* System-level efficiency decreases consistently over time

---

## 7. Test Case 4 — Severe Fouling Condition

### Objective:

Test system behavior under extreme degradation conditions.

### Input Conditions:

* High fouling resistance values
* Long operating time simulation
* Reduced heat transfer effectiveness

### Expected Behavior:

* Significant drop in heat exchanger performance
* High energy loss in system
* Clear identification of underperforming units

### Validation Criteria:

* System does not fail or produce unstable results
* Outputs remain physically meaningful
* Clear degradation indicators are triggered

---

## 8. Test Case 5 — Network Imbalance Scenario

### Objective:

Evaluate system response to mismatched heat exchanger network conditions.

### Input Conditions:

* Uneven heat exchanger performance distribution
* Partial inefficiency in selected units
* Mixed clean and fouled conditions

### Expected Behavior:

* Uneven heat recovery across network
* Identification of bottleneck units
* Redistribution of thermal load effects

### Validation Criteria:

* System correctly isolates underperforming exchangers
* Network-level energy balance remains valid
* Performance degradation is localized correctly

---

## 9. Test Case 6 — Sensitivity Analysis (Future Extension)

### Objective:

Assess how system outputs respond to small variations in input parameters.

### Input Conditions:

* Slight variations in:

  * inlet temperature
  * flow rate
  * fouling resistance

### Expected Behavior:

* Smooth and predictable output variation
* No unstable oscillations in results

### Validation Criteria:

* System shows physical sensitivity consistency
* No computational instability

---

## 10. Validation Principles

All test cases must satisfy:

* Conservation of energy principle
* Thermodynamic consistency
* Logical degradation behavior
* Stability under all simulated conditions

---

## 11. Role in System Development

These test cases are used to:

* validate physics model correctness
* verify simulation flow accuracy
* ensure data model consistency
* support future model improvements
* provide baseline comparison for system upgrades

---

## 12. Summary

The test suite defines structured engineering scenarios to validate the crude oil preheat train digital twin system under varying operational and degradation conditions.

It ensures that the system behaves consistently with real-world thermodynamic and process engineering principles.
