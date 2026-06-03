# Crude Oil Preheat Train Digital Twin System

## fouling_model.md — Fouling Physics Model

---

## 1. Purpose of This Model

This model defines the behavior of heat exchanger performance degradation due to fouling in crude oil preheat train systems.

It introduces time-dependent thermal resistance effects that reduce heat transfer efficiency and system performance.

This model is used to simulate realistic industrial operating conditions where heat exchanger performance deteriorates over time.

---

## 2. Engineering Concept of Fouling

Fouling refers to the accumulation of unwanted material on heat transfer surfaces, which creates additional thermal resistance.

This results in:

* reduced heat transfer efficiency
* increased outlet temperature deviation
* reduced energy recovery
* increased fuel consumption in downstream heating systems

---

## 3. Fouling Representation in the System

In this system, fouling is modeled as an **additional thermal resistance layer** that increases over time.

This resistance reduces the overall heat transfer coefficient of the heat exchanger.

The effective heat transfer capability decreases as fouling increases.

---

## 4. Fouling Growth Behavior

Fouling is treated as a time-dependent process.

The system assumes that fouling increases gradually with operating time under normal conditions.

The growth rate depends on:

* fluid properties
* operating temperature
* flow conditions
* contamination level in the crude stream

---

## 5. Impact on Heat Exchanger Performance

As fouling increases:

* overall heat transfer coefficient decreases
* heat duty decreases
* temperature approach between hot and cold streams increases
* system efficiency declines

This directly affects the output of the heat exchanger model.

---

## 6. Integration with Heat Exchanger Model

The fouling model modifies the effective thermal resistance used in the heat exchanger calculations.

It acts as an adjustment layer on top of the base heat exchanger physics model.

This ensures that:

* clean condition performance represents ideal operation
* fouled condition represents real industrial degradation

---

## 7. Performance Degradation Representation

System performance degradation is represented through:

* reduction in heat transfer efficiency over time
* deviation from expected outlet temperatures
* reduction in heat recovery effectiveness

This allows comparison between ideal and actual system behavior.

---

## 8. Operational Interpretation

From an engineering perspective, fouling indicates:

* reduced equipment efficiency
* increased energy demand in furnaces or boilers
* need for maintenance or cleaning cycles
* declining system-level energy recovery performance

This model enables early detection of such conditions.

---

## 9. Model Assumptions

The following assumptions are used in this simplified fouling model:

* Fouling increases gradually over time (no sudden jumps)
* Fouling is uniformly distributed across heat transfer surfaces
* No chemical reaction effects are explicitly modeled
* Fouling is reversible only through maintenance (cleaning events not modeled in detail in this version)

---

## 10. Role in Digital Twin System

This model enables the system to simulate real-world degradation behavior and provides:

* time-based performance tracking
* predictive degradation trends (conceptual stage)
* system efficiency loss estimation
* maintenance insight generation

---

## 11. Summary

The fouling model introduces time-dependent performance degradation into the heat exchanger system.

It is a critical component that transforms the system from a static thermal calculator into a dynamic industrial digital twin capable of simulating real operating conditions.
