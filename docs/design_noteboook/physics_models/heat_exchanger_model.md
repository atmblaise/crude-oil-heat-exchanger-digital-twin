# Crude Oil Preheat Train Digital Twin System

## heat_exchanger_model.md — Heat Exchanger Physics Model

---

## 1. Purpose of This Model

This model defines the fundamental thermodynamic and heat transfer principles used to simulate individual heat exchangers within the crude oil preheat train system.

It serves as the core computational unit for determining heat transfer performance, energy recovery, and outlet stream conditions.

---

## 2. System Representation

Each heat exchanger is represented as a steady-state thermal energy transfer unit between a hot stream and a cold stream.

The model assumes no phase change unless explicitly defined and operates under steady-state conditions for the initial system version.

---

## 3. Energy Balance Principle

The fundamental energy balance is defined as:

* Heat lost by hot stream = Heat gained by cold stream

This can be expressed conceptually as:

* Q_hot = Q_cold = Q

Where Q represents the rate of heat transfer within the exchanger.

---

## 4. Heat Transfer Calculation

Heat transfer is modeled using the relationship:

* Heat duty depends on mass flow rate, specific heat capacity, and temperature change of the fluid streams.

The system calculates heat duty based on inlet and outlet conditions of both hot and cold streams.

---

## 5. Log Mean Temperature Difference (LMTD) Method

The thermal driving force for heat transfer is represented using the temperature difference between hot and cold streams.

The system uses the Log Mean Temperature Difference (LMTD) approach to estimate effective heat transfer conditions across the exchanger.

This allows realistic modeling of temperature variation along the exchanger length.

---

## 6. Effectiveness Concept (Alternative Representation)

For system-level analysis, the heat exchanger performance can also be expressed using effectiveness:

* Effectiveness represents the ratio of actual heat transfer to maximum possible heat transfer.

This allows comparison of performance under varying operating conditions.

---

## 7. Fouling Influence (Interface to Fouling Model)

Heat exchanger performance decreases over time due to fouling effects.

Fouling introduces additional thermal resistance, which results in:

* reduced heat transfer efficiency
* lower overall heat duty
* increased outlet temperature deviation

This model interfaces with the fouling model to adjust effective performance over time.

---

## 8. Output Variables

Each heat exchanger model produces:

* Heat duty (Q)
* Outlet temperature of hot stream
* Outlet temperature of cold stream
* Thermal efficiency indicator
* Performance deviation index

---

## 9. Assumptions

The following assumptions apply to this model:

* Steady-state operation
* Negligible heat loss to surroundings (initial version)
* Constant specific heat capacity (simplified model)
* No phase change unless specified
* Uniform heat transfer coefficients (initial version)

---

## 10. Model Role in System

This model acts as the foundational physics engine for:

* individual heat exchanger performance evaluation
* network-level heat integration analysis
* energy recovery calculations
* system degradation tracking (via fouling integration)

---

## 11. Summary

The heat exchanger model provides a simplified but physically grounded representation of thermal energy transfer in crude oil preheat systems.

It forms the computational core of the digital twin system and enables system-level performance evaluation when combined with network and fouling models.
