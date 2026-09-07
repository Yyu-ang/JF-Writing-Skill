# Method Supplement: Numerical Simulation and Computational Mechanics

Version: 1.0

Use this supplement for FEM, FDM, DEM, MPM, meshfree methods, analytical-
numerical methods, coupled multiphysics, constitutive modelling and related
computational mechanics studies.

## Numerical method presentation

Where relevant, make the following traceable:

1. physical problem and idealization;
2. governing equations;
3. constitutive law / failure criterion;
4. geometry and dimensionality;
5. material parameters and their sources;
6. initial and boundary conditions;
7. contact/interface formulation;
8. mesh/grid/particle/discretization;
9. time integration and time step;
10. solver/convergence criteria;
11. loading/excavation/construction sequence;
12. output quantities and post-processing.

## Verification and validation

Keep these concepts distinct:

- verification: whether the equations/algorithm are solved as intended;
- validation: whether the model reproduces physical/experimental/field
  behaviour adequately for the intended use.

Useful checks, when relevant and already supported by the work:

- analytical benchmark;
- canonical benchmark;
- mesh/grid/particle refinement;
- time-step sensitivity;
- parameter sensitivity;
- conservation checks;
- energy balance;
- momentum balance;
- contact-penetration or constraint residual;
- convergence history;
- comparison with laboratory or field data;
- comparison with published benchmark curves or dimensionless quantities.

Do not fabricate a verification/validation exercise that was not performed.

## Constitutive-model papers

State:
- physical meaning of the model;
- parameter definitions and units;
- calibration source;
- loading paths represented;
- implementation assumptions;
- scope of demonstrated behaviour.

Do not describe numerical agreement as physical validation unless independent
physical evidence is present.

## MPM / particle / meshfree studies

When relevant, preserve and report:
- particles per cell / material points;
- grid resolution;
- transfer/interpolation scheme;
- contact algorithm;
- boundary treatment;
- CFL/time-step logic;
- stabilization/filtering;
- conservation or drift diagnostics;
- benchmark setup.

For collapse/runout problems, use dimensionless or literature-standard
quantities when they already exist in the manuscript, and distinguish numerical
artifact from physical behaviour.

## Results writing

A strong numerical-results paragraph usually follows:

observable numerical result
→ quantitative metric
→ physical/mechanical explanation
→ benchmark/experiment comparison when available
→ implication for the studied problem

Avoid reporting contour plots without extracting the mechanical meaning.

## Computational cost

Report computational cost only when it matters to the contribution or method
comparison. Do not import CS-style API, software-architecture or asymptotic-
complexity conventions unless the actual paper is about those topics.
