# Civil & Tunnelling Engineering — Meta-Discourse Reference

Meta-discourse is used here to control interpretation, define technical boundaries and connect multiple layers of engineering evidence. Use it when necessary; do not add caveats mechanically.

---

## 1. Clarifying What a Quantity Represents

Useful moves:

- define whether a quantity is measured, prescribed, derived or simulated;
- distinguish instantaneous, averaged and cumulative quantities;
- state the aggregation window;
- specify coordinate/sign convention when ambiguity is possible.

Pattern:

`Here, [quantity] denotes [precise definition] and is calculated from [inputs] over [window].`

---

## 2. Preventing Quantity Conflation

Use when similar engineering variables coexist.

Pattern:

`[Quantity A] and [Quantity B] are treated separately because [definition difference].`

Examples of distinctions to preserve:

- total thrust vs main thrust vs auxiliary thrust;
- control input vs measured machine response;
- raw sensor channel vs derived indicator;
- nominal vs effective stress;
- displacement vs convergence;
- advance rate vs penetration per revolution.

---

## 3. Observation vs Interpretation

Pattern:

`The measurements show [observation]. This pattern is consistent with [interpretation], although the available data do not independently identify [unresolved mechanism].`

This move is useful when the physical explanation is plausible but not directly measured.

---

## 4. Correlation vs Causality

When a study is observational:

`The association between [A] and [B] should be interpreted as a statistical/operational relationship rather than a causal effect.`

Use only when readers could otherwise overinterpret the result.

---

## 5. Verification vs Validation

### Verification boundary

`This comparison verifies [implementation/numerical property]; it does not by itself establish physical validity for [engineering setting].`

### Validation boundary

`The comparison with [independent experiment/field data] supports the model for [specific response and range].`

These distinctions are particularly important in numerical mechanics.

---

## 6. Calibration vs Independent Validation

If the same dataset influences parameters:

`Because [dataset] was used for parameter calibration, agreement with these data should be interpreted as calibration performance rather than independent validation.`

If a separate dataset is available, identify it explicitly.

---

## 7. Scale Boundary

Patterns:

- `The specimen-scale response may not transfer directly to tunnel scale because [documented scale-dependent factor].`
- `The model resolves [scale/process] but does not explicitly represent [larger/smaller-scale process].`

Do not add generic scale-effect caveats when irrelevant.

---

## 8. Geological Applicability Boundary

Pattern:

`The conclusions are supported for [geology/stress/groundwater range] represented in the investigated section.`

Use when the manuscript might otherwise read as universal.

---

## 9. Operational Applicability Boundary

For TBM/shield studies:

`The observed relationship reflects the investigated machine configuration and operating range; transfer to substantially different machines or control strategies requires separate evaluation.`

---

## 10. Data-Quality Intervention

Pattern:

`Records affected by [known condition] were [excluded/flagged/treated] according to [documented rule]. The remaining uncertainty primarily concerns [issue].`

Do not invent missing-data procedures.

---

## 11. Human-Entered or Derived Labels

Pattern:

`[Rock class/warning level/strength category] is an interpreted/derived label rather than a directly measured channel.`

This distinction matters in data-driven studies and when discussing label leakage.

---

## 12. Model Assumption Boundary

Pattern:

`The model assumes [assumption]. This assumption is appropriate for [demonstrated condition] but may affect [specific response] when [condition].`

Prefer stating the affected inference over generic “future work.”

---

## 13. Missing Physics Boundary

Pattern:

`[Process] is not represented explicitly; therefore, the analysis focuses on [what the model can support].`

Examples may include groundwater coupling, thermal effects, fragmentation, cutter wear, anisotropy or rate dependence — only when relevant to the actual model.

---

## 14. Analytical-to-Numerical Pivot

Use when closed-form analysis becomes intractable.

Structure:

[what can be derived analytically] → [where analytical treatment becomes impractical] → [why numerical analysis is introduced] → [what it resolves]

Do not present the numerical model as a substitute for missing physical evidence.

---

## 15. Layered Evidence Scaffolding

Useful sequence:

1. establish gross response;
2. isolate controlling variable;
3. examine spatial/temporal mechanism;
4. compare with independent evidence;
5. discuss scope.

This is often appropriate for combined field + numerical papers.

---

## 16. Explaining a Discrepancy

Pattern:

`The model captures [feature A] but under/overpredicts [feature B]. The discrepancy may be related to [documented difference in boundary condition, material representation, scale or measurement].`

Do not use discrepancy explanations that were never investigated as established facts.

---

## 17. Ambiguous Mechanisms

Pattern:

`Both [mechanism A] and [mechanism B] are consistent with the observed trend. The present measurements do not distinguish their relative contributions.`

This is preferable to selecting a mechanism merely for narrative completeness.

---

## 18. Scope of Engineering Recommendation

Pattern:

`For [specific condition], the results support [specific design/monitoring/operational implication].`

Avoid universal imperatives such as `should always` unless a standard or broad evidence base supports them.

---

## 19. Terminology Boundary

When terminology varies across literature:

`In this study, [term] refers specifically to [definition].`

Once defined, keep the term consistent throughout the manuscript.

---

## 20. Uncertainty Without Defensive Writing

State only uncertainty that changes interpretation.

Prefer:

`The available monitoring period does not resolve the long-term response.`

rather than:

`There are several limitations that should be noted and future studies are needed.`

Specific technical boundaries are more useful than generic limitation language.

---

## 21. Discussion Layering

A useful discussion progression is:

[result] → [mechanism] → [comparison with independent or prior evidence] → [reason for agreement/disagreement] → [applicability]

Not every paper needs a separate Discussion section; follow the manuscript and target-journal structure.

---

## 22. Conclusion Boundary

The conclusion should not introduce:

- new citations;
- new numerical results;
- new mechanisms;
- new model assumptions;
- new engineering recommendations unsupported by Results/Discussion.

If a conclusion sentence cannot be traced to the body, revise or remove it.
