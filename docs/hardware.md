# RKHP-01 Hardware

## Purpose

This document defines the hardware architecture, requirements, and planned
components for RKHP-01, the first experimental robotics platform developed
under RKHP.

RKHP-01 is intended to provide a modular physical platform for exploring:

- Sensing
- Sensor fusion
- Environmental perception
- Anomaly detection
- Issue estimation
- Decision systems
- Safe physical action
- Verification
- Learning from telemetry

This document will evolve as experiments provide evidence for hardware
selection.

---

## Current Status

**Status:** Architecture / Planning

No final hardware configuration has been selected yet.

Hardware decisions will be driven by:

1. Experiment requirements
2. Sensor requirements
3. Compute requirements
4. Control requirements
5. Safety requirements
6. Power requirements
7. Availability
8. Cost
9. Maintainability
10. Expandability

---

## Design Philosophy

RKHP-01 should be:

- Modular
- Experiment-friendly
- Observable
- Maintainable
- Replaceable
- Expandable
- Safe
- Cost-conscious
- Suitable for repeated testing

Hardware should allow individual components to be replaced without requiring
a complete redesign of the platform.

---

## High-Level Hardware Architecture

```text
                    RKHP-01
                       │
        ┌──────────────┼──────────────┐
        │              │              │
     SENSORS         COMPUTE        POWER
        │              │              │
        │              │              │
   ┌────┼────┐         │         ┌────┴────┐
   │    │    │         │         │         │
  IMU  Temp  Vibration │      Battery   Protection
   │    │    │          │         │         │
   └────┼────┘          │         └─────────┘
        │               │
        └───────┬───────┘
                │
          Control Layer
                │
        ┌───────┴───────┐
        │               │
     Motors         Actuators
        │               │
        └───────┬───────┘
                │
          Physical Motion
