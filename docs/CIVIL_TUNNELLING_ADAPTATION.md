# Civil / Geotechnical / Tunnelling Adaptation

## Upstream design influence

The workflow is adapted from the dynamic corpus approach used by `WantongC/journal-adapt-writing-skill`:

1. classify corpus roles;
2. extract one Style Card per paper;
3. aggregate recurring corpus patterns;
4. generate a reviewable dynamic writing skill;
5. revise the manuscript section by section without rereading reference papers.

This adaptation changes the professional layer and extends the analysis schema for civil, geotechnical and tunnelling research.

## Why a dedicated civil/tunnelling layer is needed

Generic "engineering" writing rules often assume computer systems or software papers and emphasize API boundaries, pseudocode, asymptotic complexity, hardware benchmarks and microbenchmarks. Those are not universal conventions for tunnels, geotechnics, rock mechanics, engineering geology or computational mechanics.

Civil/tunnelling papers instead often require explicit handling of:

- geological and hydrogeological context;
- tunnel geometry, overburden and construction sequence;
- support / lining interaction;
- TBM, shield or EPB configuration and operational quantities;
- laboratory or field instrumentation;
- raw measurements, processing, aggregation and interpreted labels;
- constitutive laws and material parameters;
- boundary / initial conditions and discretization;
- verification, physical validation and benchmarks;
- uncertainty, sensitivity, convergence and stability;
- evidence-bounded engineering implications.

## Method taxonomy

The adapted skill recognizes one or more of:

- field monitoring / case history;
- laboratory / physical model test;
- site investigation / geological characterization;
- analytical / theoretical;
- numerical simulation / computational mechanics;
- constitutive modelling;
- TBM / shield / EPB operational-data analysis;
- data-driven / ML within civil engineering;
- review / synthesis;
- mixed methods.

## Rule priority

```text
P1  Technical truth and manuscript content
P2  Reviewed target-journal corpus patterns
P3  Topic/method-similar corpus and author/lab exemplars
P4  Civil/tunnelling and method-specific defaults
P5  Clarity cleanup
```

A generic style rule never overrides a stronger target-journal pattern or a technical fact.

## Phrase policy

There is no global blacklist for expressions such as "Moreover" or "It should be noted that." A phrase is revised only when it is empty, repetitive, inflated, or inconsistent with the reviewed corpus and local rhetorical function.

This prevents generic anti-AI heuristics from erasing genuine journal, author or laboratory style.

## Numerical mechanics policy

For FEM/FDM/DEM/MPM and related methods, the skill distinguishes:

- **verification**: whether the numerical formulation/implementation solves the intended equations correctly;
- **validation**: whether the model reproduces physical, experimental or field behaviour adequately for its intended use.

Where relevant and already present in the research, the style profile may capture how the corpus presents analytical benchmarks, canonical tests, grid/mesh/particle refinement, time-step sensitivity, energy/momentum checks, contact residuals, convergence histories and experiment/field comparisons.

## TBM / shield / EPB data policy

When operational data are used, keep separate:

1. geology / ground conditions;
2. machine configuration;
3. operator/control inputs;
4. measured operational responses;
5. derived performance indicators;
6. interpreted or human-entered labels.

This helps prevent ambiguous definitions and accidental leakage when data-driven methods are involved.

## Future extensions

Useful optional method supplements include:

- `tbm_performance_and_fpi.md`;
- `shield_epb_operations.md`;
- `rock_mechanics.md`;
- `engineering_geology.md`;
- `mpm_dem_fem_validation.md`;
- `civil_data_driven.md`.

These should remain optional supplements rather than mandatory rules for every tunnel paper.
