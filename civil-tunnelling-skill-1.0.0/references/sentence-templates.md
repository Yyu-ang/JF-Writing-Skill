# Civil & Tunnelling Engineering — Sentence Pattern Reference

This file replaces the finance/JF sentence-template corpus in the upstream architecture with discipline-oriented writing patterns for civil, geotechnical and tunnelling engineering.

These are **functional patterns**, not sentences to copy mechanically. Replace bracketed elements with content that already exists in the manuscript.

---

## 1. Opening an Introduction

### 1.1 Specific engineering problem

Use when the paper begins from a concrete construction, stability or performance issue.

Pattern:

`[Engineering phenomenon/problem] remains a critical issue in [specific tunnel/ground/construction context] because [direct physical or operational consequence].`

Prefer a specific problem such as face instability, excessive settlement, cutter wear, squeezing ground or lining response over broad claims about infrastructure development.

### 1.2 Mechanism-first opening

`The response of [system] is governed primarily by the interaction between [factor A] and [factor B], particularly under [condition].`

Useful for mechanics, constitutive and numerical papers.

### 1.3 Observation-first opening

`Field observations from [type of project/condition] show that [specific phenomenon], yet the controlling mechanism remains incompletely understood.`

Use only when such observations are actually documented.

### 1.4 Methodological challenge opening

`Accurate prediction of [quantity/response] is difficult because [specific modelling/measurement challenge].`

Suitable for papers where the contribution is mainly methodological.

### 1.5 Geological-condition opening

`Tunnelling through [faulted/squeezing/soft-hard interbedded/water-bearing/etc.] ground can produce [specific response], with consequences for [stability/support/TBM performance].`

Avoid generic adjectives unless the geology is documented.

---

## 2. Stating the Research Question

Useful patterns:

- `This study investigates how [factor] affects [response] under [condition].`
- `The central question is whether [mechanism/hypothesis] can explain [observed behavior].`
- `We examine the relationship between [measured quantity] and [engineering response] across [cases/conditions].`
- `The analysis focuses on the extent to which [method/model] reproduces [benchmark/field/experimental behavior].`
- `For TBM operation, the study asks how [geological/control variable] is reflected in [machine response/performance indicator].`

Do not replace a descriptive study with a causal question unless the design supports causality.

---

## 3. Framing a Knowledge Gap

Prefer a technically precise gap.

Patterns:

- `Existing studies have established [known result], but the influence of [specific mechanism/condition] remains insufficiently resolved.`
- `Current models reproduce [behavior A], whereas their ability to capture [behavior B] under [condition] has received less attention.`
- `Previous field studies document [phenomenon], but direct comparison with [independent measurement/model/condition] is limited.`
- `Most available analyses assume [assumption]; this becomes restrictive when [specific engineering condition].`
- `The main unresolved issue is therefore [specific problem], rather than the general occurrence of [broad topic].`

Avoid `few studies have...` as the only evidence for a gap.

---

## 4. Positioning Contributions

Contribution claims should correspond to actual work.

Patterns:

- `The main contribution is a [method/data/model/analysis] that [specific capability].`
- `Compared with existing approaches, the present formulation explicitly accounts for [technical distinction].`
- `The study combines [data/source A] with [method/source B] to evaluate [specific question].`
- `A second contribution is the validation of [model/method] against [independent benchmark/experiment/field observation].`
- `For engineering application, the analysis identifies [bounded implication] under [tested conditions].`

Avoid `for the first time` unless supported by a genuine literature search.

---

## 5. Literature Positioning

Patterns:

- `[Author/year] examined [problem] using [method], showing [relevant finding].`
- `These studies demonstrate [shared conclusion], but differ in their treatment of [mechanism/assumption].`
- `The literature can be grouped into [mechanism/method] approaches.`
- `Experimental studies emphasize [aspect], whereas numerical studies have primarily addressed [aspect].`
- `The present study differs in [specific technical dimension].`

Prefer comparison and synthesis over one-paper-per-sentence catalogues.

---

## 6. Describing Site and Geological Conditions

Useful patterns:

- `The tunnel passes through [geological unit] between [chainage/depth range], where [relevant condition].`
- `The overburden varies from [value] to [value], and the groundwater level is [description].`
- `The rock mass is characterized by [classification/properties], with [faults/joints/weak layers] concentrated in [location].`
- `Only the geological features relevant to [analysis] are summarized here.`
- `The investigated section was selected because [documented engineering reason].`

Keep project history separate from technical interpretation.

---

## 7. Describing Laboratory or Model Tests

Patterns:

- `Specimens were prepared from [material/source] with dimensions of [value].`
- `The loading path consisted of [sequence].`
- `[Quantity] was measured using [instrument/sensor] at [sampling rate/location], where available.`
- `Each condition was repeated [n] times.`
- `The reported value represents [mean/median/peak/etc.] over [window/replicates].`
- `Prior to analysis, [preprocessing] was applied to [signal/data].`
- `No instrument specification should be added if it is absent from the source manuscript.`

---

## 8. Describing Field Monitoring

Patterns:

- `Monitoring points were installed at [locations] to record [quantities].`
- `Measurements were referenced to [baseline/time/chainage].`
- `The monitoring interval was [value], covering [construction stages].`
- `To align the monitoring data with excavation progress, records were aggregated by [ring/chainage/time/depth window].`
- `Missing or invalid records were handled by [documented rule].`

If preprocessing is unknown, do not invent it.

---

## 9. Describing Numerical Models

### 9.1 Governing equations

- `The model solves [governing equations] subject to [key assumptions].`
- `The solid response is represented by [constitutive law], with parameters listed in [table/source].`

### 9.2 Geometry and discretization

- `The computational domain extends [dimensions], with [mesh/grid/particle] resolution of [value].`
- `Boundary conditions were applied as [description].`
- `The initial stress state was established using [documented procedure].`

### 9.3 Time integration and solver

- `A time step of [value] was used, satisfying [criterion if documented].`
- `Convergence was defined by [actual residual/tolerance].`

### 9.4 Contact/interface

- `Interaction between [components] was represented using [contact/interface formulation].`

Do not introduce numerical details that are not in the manuscript.

---

## 10. Verification and Validation

Keep these concepts distinct.

### Verification

- `The implementation was verified against [analytical/canonical benchmark].`
- `Mesh/particle/time-step refinement was used to assess numerical convergence.`
- `The residual decreased to [value], indicating [specific numerical property].`
- `Mass/momentum/energy conservation was evaluated using [metric].`

### Validation

- `Model predictions were compared with independent [laboratory/field] measurements.`
- `Agreement was evaluated using [metric/curve/quantity].`
- `The model reproduces [specific behavior] within [documented error/bound].`

Do not call a self-comparison or internal convergence test physical validation.

---

## 11. Reporting Results

### 11.1 Direct observation

- `[Quantity] increased from [A] to [B] as [condition] changed from [C] to [D].`
- `The maximum [response] occurred at [location/time/condition].`
- `A monotonic/non-monotonic trend was observed over [range].`

### 11.2 Scenario comparison

- `Compared with Case A, Case B produced [difference] in [quantity].`
- `The difference was most pronounced under [condition].`

### 11.3 Spatial/temporal evolution

- `The response developed first near [location] and subsequently propagated toward [location].`
- `After [stage], [quantity] approached a stable value.`

Prefer exact values to vague adjectives when numbers are available.

---

## 12. Integrating Figures and Tables

Patterns:

- `Figure X shows the evolution of [quantity] with [variable].`
- `As shown in Figure X, [specific trend]; the key feature is [interpretation].`
- `Table X compares [cases/parameters] using [metric].`
- `The contour in Figure X indicates [physical observation], particularly near [location].`

Avoid `Figure X clearly shows...` when the claim can be stated directly.

---

## 13. Explaining Mechanisms

Calibrate strength.

### Suggestive

- `This pattern is consistent with [mechanism].`
- `A plausible explanation is that [mechanism].`
- `The result suggests that [factor] contributes to [response].`

### Better supported

- `The combined [field/experimental/numerical] evidence indicates that [mechanism].`
- `This interpretation is supported by [independent evidence].`

Avoid causal language when only correlation is shown.

---

## 14. Sensitivity and Parametric Analysis

Patterns:

- `Increasing [parameter] from [A] to [B] resulted in [response].`
- `The response is more sensitive to [parameter A] than to [parameter B] over the tested range.`
- `Within the investigated range, [quantity] remained relatively insensitive to [parameter].`
- `The sensitivity analysis identifies [parameter] as influential under [conditions].`

Do not generalize beyond the sampled parameter range.

---

## 15. Robustness and Alternative Explanations

Patterns:

- `To examine whether the result depends on [assumption], the analysis was repeated using [alternative].`
- `The main trend remained unchanged after [documented modification].`
- `One alternative explanation is [mechanism]; however, [evidence] does not support this interpretation.`
- `The available data do not distinguish between [A] and [B].`

The last pattern is often stronger scientifically than forcing a single mechanism.

---

## 16. TBM / Shield / EPB Results

Patterns:

- `As the ground condition changed from [A] to [B], [machine response] changed by [amount].`
- `[Control/input variable] and [measured response] should be discussed separately.`
- `The derived indicator [name] was calculated from [documented inputs].`
- `The relationship between [geological variable] and [performance metric] was evaluated over [ring/chainage/time] windows.`
- `The observed increase in thrust coincided with [condition]; this association alone does not establish causality.`

Keep main thrust, total thrust and auxiliary thrust distinct when the data define them separately.

---

## 17. Data-Driven / Machine-Learning Results

Patterns:

- `The model was trained on [source/unit] and evaluated on [independent split].`
- `Data were split by [tunnel/ring/time/project/etc.] to reduce leakage between training and test sets.`
- `Performance was evaluated using [metrics].`
- `The improvement over [baseline] was [amount].`
- `Feature importance indicates an association between [feature] and [prediction], not necessarily a physical causal mechanism.`
- `Generalization has been demonstrated only for [tested domain].`

---

## 18. Discussion and Engineering Implications

Patterns:

- `The results indicate that [mechanistic finding] under [conditions].`
- `For tunnel design/construction, this implies that [bounded implication].`
- `The implication is most relevant to [geological/operational range].`
- `The discrepancy with [previous result] may arise from differences in [scale/stress path/geology/boundary conditions].`
- `The present evidence supports [specific interpretation], while [broader claim] remains outside the scope of the study.`

Avoid generic claims that the method “provides important guidance” without stating guidance for what and under which conditions.

---

## 19. Limitations and Applicability Boundaries

Use when technically relevant, not mechanically.

Patterns:

- `The conclusions apply to [tested conditions/range].`
- `The present model does not include [factor], which may become important under [condition].`
- `Because the field data are drawn from [scope], transfer to [different setting] requires further verification.`
- `The available measurements do not resolve [specific mechanism].`
- `This limitation affects [specific inference], but not [supported result], if justified.`

---

## 20. Conclusions

Patterns:

- `The main findings are as follows.` only when a list is actually useful.
- `Under [condition], [principal quantitative finding].`
- `[Mechanism] explains [specific behavior] as supported by [evidence].`
- `The proposed method reproduced [benchmark/field response] with [metric].`
- `For [engineering context], the results suggest [bounded implication].`

Do not introduce new mechanisms or literature in the conclusion.

---

## 21. Chinese-to-English Functional Replacements

Do not translate these mechanically.

| Chinese expression | Better decision |
|---|---|
| 可以看出 | state the actual observation directly |
| 值得注意的是 | state why the feature matters, or delete the filler |
| 具有重要意义 | specify the engineering/scientific implication |
| 由图可知 | identify the exact trend shown by the figure |
| 随着…增加而增加 | use `increased with`, `increased as`, or quantify the relation |
| 说明了 | choose `indicates`, `suggests`, `demonstrates`, or `is consistent with` according to evidence |
| 验证了 | distinguish `verified` from `validated` |
| 证明了 | use strong `demonstrates` only when the evidence truly warrants it |
| 影响规律 | translate the specific relationship, not `influence law` |
| 变化规律 | use `evolution`, `trend`, `variation`, or the explicit response pattern |

---

## 22. Final Sentence-Level Checks

Before finalizing:

- Is every technical noun unambiguous?
- Are units attached to quantities where required?
- Has any causal verb become stronger than in the source?
- Are `significant`, `robust`, `validated` and `accurate` supported by defined evidence?
- Are pronouns such as `it`, `this` and `they` clear in dense technical passages?
- Are the same variables named consistently across Abstract, Methods, Results and Discussion?
