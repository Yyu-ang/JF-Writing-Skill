# Civil & Tunnelling Engineering — Phrase Bank

A lookup reference for polishing and Chinese-to-English translation. These are discipline-appropriate collocations and evidence-calibrated expressions, not a target-journal frequency list.

---

## 1. Observation and Measurement

Useful verb + noun combinations:

- measure displacement / stress / strain / pore pressure / thrust / torque
- monitor deformation / settlement / convergence / vibration
- record machine response / operational parameters / excavation progress
- quantify deformation / error / sensitivity / variability
- characterize rock mass / soil behavior / joint network / ground conditions
- identify a trend / transition / failure mode / critical zone
- capture temporal evolution / spatial variation / localized deformation
- resolve a response / gradient / interface effect
- derive an indicator / index / normalized quantity
- estimate a parameter / uncertainty / error bound

Prefer `measure` for direct measurement and `estimate` for inferred quantities.

---

## 2. Numerical and Computational Mechanics

Useful collocations:

- solve the governing equations
- discretize the computational domain
- impose boundary conditions
- initialize the stress state
- calibrate constitutive parameters
- implement a contact algorithm
- refine the mesh / grid / particle resolution
- reduce the time step
- satisfy a convergence criterion
- evaluate conservation error
- reproduce a benchmark response
- compare numerical predictions with measurements
- resolve localization / contact / large deformation
- track energy evolution / momentum balance
- assess mesh dependence / time-step sensitivity

Avoid importing software-engineering phrases such as `API boundary`, `microbenchmark` or asymptotic complexity unless the paper is genuinely about software performance.

---

## 3. Geotechnical and Rock-Mechanics Language

Common technical combinations:

- stress redistribution
- plastic zone development
- shear localization
- strain softening
- post-peak response
- confining pressure
- loading path
- unloading response
- dilation / contractancy
- joint opening / slip
- anisotropic behavior
- rock-mass degradation
- face stability
- ground loss
- excavation-induced deformation
- support pressure
- lining response
- soil-structure interaction
- rock-support interaction
- groundwater inflow
- fault / weak-zone crossing
- squeezing behavior
- brittle / ductile failure

Use the manuscript's exact terminology when a term has a specific constitutive or classification meaning.

---

## 4. TBM / Shield / EPB Language

Keep categories distinct.

### Machine/control variables

- cutterhead rotational speed
- penetration per revolution
- advance rate
- total thrust
- main thrust
- auxiliary thrust
- cutterhead torque
- chamber pressure
- screw-conveyor speed
- grouting pressure
- articulation / steering parameters

### Performance and response

- penetration response
- specific energy
- field penetration index / FPI-type indicator
- cutter consumption / wear
- torque fluctuation
- thrust demand
- excavation efficiency
- machine utilization
- stoppage / downtime

### Writing combinations

- correlate machine response with ground conditions
- align operational data with chainage / ring number
- aggregate records over a depth / time / ring window
- distinguish control settings from measured response
- derive performance indicators from raw channels
- identify anomalous operating states
- compare geological zones

Do not combine similarly named thrust quantities unless their definitions are identical.

---

## 5. Experimental and Field Studies

Useful phrases:

- prepare specimens from
- subject specimens to
- apply confining pressure / axial load
- conduct repeated tests
- install monitoring points
- calibrate sensors
- establish a baseline
- sample at a frequency of
- synchronize data streams
- remove invalid records
- aggregate measurements over
- report mean / median / peak response
- quantify repeatability / dispersion
- compare independent measurements

Only mention calibration, accuracy, resolution or repeat count when documented.

---

## 6. Reporting Trends and Comparisons

### Increase/decrease

- increased from A to B
- decreased by X%
- increased with increasing X
- declined as X increased
- remained approximately constant
- approached a plateau
- exhibited a non-monotonic response
- reached a maximum/minimum at

### Comparison

- was higher/lower than
- exceeded that of
- differed by
- showed a similar trend to
- remained within
- was most pronounced under
- produced a smaller/larger response

Prefer explicit magnitudes when available.

---

## 7. Mechanism and Interpretation Verbs

Choose by evidence strength.

### Low-to-moderate commitment

- may reflect
- may arise from
- is consistent with
- suggests
- is associated with
- can be attributed to, only when justified
- provides a plausible explanation for

### Stronger, evidence-supported

- indicates
- demonstrates, when directly supported
- confirms, only against a pre-specified test/benchmark
- is governed by, when mechanism is established
- results from, when causality is supported

Avoid using `proves` for ordinary engineering evidence.

---

## 8. Verification, Validation and Credibility

### Verification language

- verify the implementation against
- recover the analytical solution
- demonstrate convergence with refinement
- satisfy the numerical tolerance
- reduce the residual
- conserve mass / momentum / energy within
- reproduce the canonical benchmark

### Validation language

- validate against independent field measurements
- compare with laboratory observations
- reproduce the measured response
- achieve agreement within
- capture the observed trend

### Caution

- `verified` ≠ `validated`
- agreement with another numerical model is usually a benchmark comparison, not independent physical validation
- a visually similar curve is not automatically `excellent agreement`

---

## 9. Sensitivity, Robustness and Uncertainty

Useful phrases:

- sensitive to changes in
- relatively insensitive to
- remains stable over the tested range
- preserves the main trend
- depends strongly on
- varies within
- exhibits limited variation
- uncertainty is dominated by
- the result is conditional on
- the conclusion applies within
- the available data do not resolve

Use `robust` only when the manuscript actually tests relevant alternatives.

---

## 10. Evidence-Calibrated Hedging

### Speculative

- may be associated with
- could arise from
- one possible explanation is
- the available evidence does not distinguish between

### Suggestive

- suggests that
- is consistent with
- supports the interpretation that
- indicates a possible role of

### Strong

- demonstrates that
- confirms that
- establishes that

The last group should be reserved for clearly supported claims.

---

## 11. Literature Comparison

Useful expressions:

- consistent with previous observations of
- differs from earlier results under
- extends prior work by considering
- complements experimental evidence on
- provides field evidence for
- reproduces the benchmark reported by
- differs primarily in the treatment of
- adopts a different constitutive assumption from
- addresses a condition not considered in

Avoid generic `fills the research gap` when the specific difference can be named.

---

## 12. Engineering Implications

Prefer bounded formulations:

- has implications for the design of
- informs the selection of
- may assist interpretation of
- provides a basis for evaluating
- is relevant to tunnels constructed in
- suggests that additional attention is required when
- indicates a need to distinguish between

Avoid `provides important guidance for engineering practice` unless the guidance itself is stated.

---

## 13. Logical Transitions

Use only when logic is not already obvious.

### Contrast

- however
- in contrast
- by comparison
- whereas
- despite this

### Cause/reason

- because
- owing to
- as a result of
- this behavior can be explained by

### Consequence

- therefore
- consequently
- as a result
- which leads to

### Continuation

Often no explicit connector is needed. Repeating `Moreover`, `Furthermore` and `Additionally` at paragraph starts makes technical writing mechanical.

---

## 14. Words That Need Evidence

Before using these, check what supports them:

- significant — statistical or practically important?
- accurate — compared with what metric/reference?
- robust — tested against which alternatives?
- validated — against independent physical evidence?
- reliable — evaluated how?
- effective — effective for which objective?
- superior — compared with which baseline?
- substantial — quantify if possible
- negligible — define relative scale
- critical — critical according to what criterion?

---

## 15. Chinese-to-English Collocation Guide

| Chinese idea | Preferred English choices |
|---|---|
| 变形特征 | deformation characteristics / deformation response |
| 演化规律 | evolution / temporal development / response trend |
| 分布规律 | distribution / spatial pattern |
| 影响因素 | influencing factors / factors associated with / controlling factors, depending on evidence |
| 影响机制 | mechanism / controlling mechanism, only when supported |
| 力学响应 | mechanical response |
| 围岩稳定性 | surrounding-rock stability / stability of the surrounding ground, depending on terminology |
| 地层损失 | ground loss |
| 掌子面稳定 | face stability |
| 隧道收敛 | tunnel convergence |
| 地表沉降 | surface settlement |
| 掘进参数 | tunnelling / excavation / operational parameters |
| 掘进性能 | tunnelling performance / machine performance |
| 施工过程 | construction / excavation sequence |
| 数值模型 | numerical model |
| 本构模型 | constitutive model |
| 边界条件 | boundary conditions |
| 初始应力 | initial stress state / in-situ stress state |
| 参数敏感性 | parameter sensitivity |
| 模型验证 | verification or validation — decide which is actually meant |

---

## 16. Phrases to Replace with Specific Content

These are not banned; they are warnings that specificity is usually better.

- `It is worth noting that...`
- `It can be clearly seen that...`
- `The results are very good.`
- `The method has high accuracy.`
- `This has important engineering significance.`
- `The model is reasonable.`
- `The results verify the correctness of the model.`
- `There is a certain relationship between...`

Replace them with the actual observation, metric, benchmark, condition or implication.
