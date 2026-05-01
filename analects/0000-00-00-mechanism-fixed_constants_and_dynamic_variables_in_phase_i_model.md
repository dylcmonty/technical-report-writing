---
title: Fixed Constants and Dynamic Variables in Phase I Model
date: '0000-00-00'
slug_convention: mechanism
name: fixed_constants_and_dynamic_variables_in_phase_i_model
classification: mechanism
status: draft
kind: ''
source_path: analects/raw/mechanism--fixed-constants-and-dynamic-variables-in-phase-i-model.md
audience:
- general
tags:
- methodology
- simulation
- phase-i
source_type: conversation
source_ref: new-snips/gemeni_articulation_of_agronomic_cycle.txt
related:
- 0000-00-00-constraint-two_sided_feasibility_window
summary: ''
---

# Fixed Constants and Dynamic Variables in Phase I Model

Question: How should the feasibility model distinguish constants from variables?

Answer:
The model should treat known structural conditions as constants and test outcomes by varying only coordination-relevant parameters. Constants include baseline demand framing, existing centralized overhead assumptions, and bounded geographic context. Dynamic variables include farm acreage utilization, crop mix timing, adjacency, hub purchasing patterns, and coordination intensity. This separation makes results interpretable and prevents the analysis from confusing background conditions with intervention effects.

Boundaries:
- This does not claim the model is a full agronomic optimizer.
- This does not remove uncertainty; it isolates uncertainty into explicit scenario variables.
