# Quantum Tool Evaluation Protocol (QTEP)

**Version:** 0.1
**Status:** Experimental - Frozen for Initial Calibration
**Date:** August 27, 2026

## 1. Purpose

The Quantum Tool Evaluation Protocol (QTEP) is an open methodology for independently evaluating the practical functionality and utility of open-source quantum software development tools.

QTEP is designed to answer three questions:

1. **Does it work?**
   Does the tested functionality perform as represented for the evaluated use case?

2. **Does it help?**
   Does the tool materially improve the workflow relative to a reasonable baseline?

3. **For whom?**
   Under what users, workloads, assumptions, or constraints does that improvement matter?

QTEP evaluates specific claims and workflows rather than attempting to determine whether a software project is universally "good" or "bad."

---

## 2. Scope

Public evaluations conducted as part of the QTEP review program are limited to quantum software that is:

* publicly available;
* distributed under an identifiable open-source license; and
* sufficiently accessible to permit meaningful independent evaluation and reproduction.

QTEP may be applied by others to proprietary, internal, or otherwise non-public software, but such evaluations fall outside the scope of the public QTEP review program.

### 2.1 Tool Categories

QTEP may be applied to categories including:

* SDKs and programming frameworks;
* compilers and transpilers;
* simulators and emulators;
* circuit and algorithm libraries;
* testing and verification tools;
* quantum error-correction tooling;
* benchmarking and resource-estimation tools;
* visualization and developer utilities.

This taxonomy is intentionally provisional.

Category-specific criteria should be developed where appropriate. Tools designed for fundamentally different purposes should not be ranked against one another using inappropriate common metrics.

---

## 3. Core Principles

### 3.1 Evaluate the Claim, Not the Project

Each evaluation begins with a narrowly defined and reasonably falsifiable claim about the functionality or utility being tested.

Broad questions such as "Is this tool good?" should be replaced with questions such as:

> Does this tool materially improve a defined workflow for its intended user compared with a reasonable baseline?

### 3.2 Establish a Reasonable Baseline

The evaluator determines how a competent developer could accomplish substantially the same task without the evaluated tool or abstraction.

A new abstraction demonstrates practical value only to the extent that it improves something relative to an appropriate alternative.

### 3.3 Compare Equivalent Work

Before comparing performance, complexity, developer effort, circuit characteristics, or other outcomes, the evaluator must establish that the baseline and tool-assisted approaches solve substantially equivalent problems.

Comparative conclusions should not proceed through the equivalence gate when this condition cannot reasonably be established.

### 3.4 Steelman Before Stress-Testing

The tool should first receive a representative workload aligned with its stated purpose and favorable to demonstrating its intended value.

Only after establishing this happy-path behavior should the evaluator investigate a credible difficult case, edge condition, or strong objection.

The objective is to test the strongest reasonable interpretation of the tool's value proposition rather than construct a "gotcha" test.

### 3.5 Match Rigor to the Claim

The strength of the evidence should be proportional to the strength of the conclusion.

Qualitative claims may be supported by qualitative evidence.

Quantitative performance claims require measurements, controls, repetitions, workloads, and statistical treatment appropriate to the claim.

### 3.6 Preserve Reproducibility

An evaluation should record enough information for another competent developer to understand how the conclusion was reached and, where practical, reproduce the test.

### 3.7 Separate Functionality From Utility

Software may function correctly without providing material improvement over the baseline.

Conversely, a useful tool may contain limitations or defects without losing all practical value.

"Works correctly" and "provides a valuable abstraction" are separate questions.

### 3.8 Use the Minimum Sufficient Experiment

Testing should continue only as far as necessary to reach a defensible conclusion about the defined claim.

Additional experimentation should resolve a meaningful uncertainty rather than merely accumulate results.

---

## 4. Standard Evaluation Sequence

### Stage 1: Define the Claim

Before testing begins, document:

* intended user;
* problem being solved;
* functionality being tested;
* claimed or hypothesized benefit;
* expected workflow;
* relevant assumptions;
* explicit exclusions.

The evaluation should target a sufficiently narrow claim that available evidence could reasonably support or challenge it.

### Stage 2: Establish the Baseline

Construct the smallest credible alternative workflow that accomplishes substantially the same task without relying upon the abstraction being evaluated.

The baseline should represent a reasonable alternative available to the intended user rather than an artificially weak comparison.

### Stage 3: Happy-Path Test

Test a representative workload that gives the tool a fair opportunity to demonstrate its intended value.

The happy-path test should establish basic functionality before more difficult cases are introduced.

### Stage 4: Equivalence Gate

Determine whether the baseline and tool-assisted workflows remain sufficiently equivalent for the intended comparison.

Equivalence may involve, depending upon the tool:

* functional output;
* quantum state or unitary behavior;
* circuit semantics;
* optimization objective;
* noise assumptions;
* computational task;
* input and output constraints.

If equivalence cannot be established, comparative claims should stop or be explicitly qualified.

### Stage 5: Measure Value Added

Evaluate only dimensions relevant to the tool's intended purpose.

Potential dimensions include:

* code or boilerplate removed;
* conceptual complexity;
* workflow steps;
* integration effort;
* execution time;
* memory requirements;
* compilation quality;
* circuit depth or gate characteristics;
* debugging effort;
* interoperability;
* reproducibility.

The evaluation should distinguish measurable improvement from subjective convenience where possible.

### Stage 6: Path-of-Pain Test

Identify a difficult but credible workload, edge case, or strong objection capable of exposing an important limitation in the tool or abstraction.

Prefer the smallest experiment capable of resolving the uncertainty.

A path-of-pain test should be technically relevant to the intended use of the tool rather than deliberately pathological.

### Stage 7: Developer-Experience Assessment

Consider, where relevant:

* installation;
* documentation;
* API clarity;
* error messages;
* interoperability;
* dependency burden;
* reproducibility;
* apparent project maintenance.

Developer-experience observations should be distinguished from functional or performance findings.

### Stage 8: Characterize Limitations

Document relevant:

* failures;
* unsupported cases;
* assumptions;
* unexpected behavior;
* dependency costs;
* workflow tradeoffs;
* defects.

Discovery of a defect does not create an obligation to diagnose or repair it.

The evaluator's responsibility generally ends at:

> **Reproduce → Verify → Document → Report when appropriate → Stop**

Additional contribution to the evaluated project is a separate activity from the QTEP evaluation.

### Stage 9: Reach a Verdict

The evaluation concludes by answering:

**Does it work?**

**Does it help?**

**For whom?**

The verdict should apply to the defined claim and evaluated conditions rather than the software project as a whole.

---

## 5. Verdict Vocabulary

### PASS

Testing demonstrates that the tool materially improves its intended workflow under the evaluated conditions.

### CONDITIONAL PASS

Testing demonstrates meaningful value under identifiable circumstances, workloads, users, or constraints.

### NO MATERIAL ADVANTAGE

The evaluated functionality works, but testing does not demonstrate meaningful improvement over the reasonable baseline for the evaluated use case.

This verdict is not equivalent to failure.

### FAIL

The tested functionality does not adequately deliver the defined claim under the evaluated conditions.

A FAIL applies to the evaluated claim and should not automatically be generalized to the entire software project.

### INCONCLUSIVE

Available evidence is insufficient to support a defensible conclusion.

Inconclusive results should identify the unresolved uncertainty where practical.

---

## 6. Evidence Requirements

Each evaluation should identify, where applicable:

* project name;
* public source repository;
* software license;
* tested release, version, or commit;
* evaluation date;
* execution environment;
* relevant dependencies;
* test inputs;
* assumptions;
* baseline implementation;
* tool-assisted implementation;
* relevant outputs;
* measurements;
* known limitations of the evaluation.

Source code, notebooks, configuration files, and machine-readable results should be preserved and published for public evaluations when practical and legally permissible.

Evidence should support the stated conclusion without requiring unnecessary experimental complexity.

---

## 7. Independence and Conflicts of Interest

QTEP evaluations should disclose material relationships between the evaluator and the evaluated project.

An independent public evaluation should normally be:

* uncompensated;
* editorially independent;
* conducted without approval of the verdict by project maintainers;
* transparent regarding material relationships or conflicts of interest.

Maintainers may be contacted to resolve factual or technical questions. Technical fact-checking does not grant editorial control over the evaluation.

Software developed by the evaluator or the evaluator's organization should not be presented as independently evaluated under QTEP.

QTEP may nevertheless be used internally to evaluate and improve such software, provided those results are not misrepresented as independent reviews.

When an evaluated project materially competes with software or intellectual property in which the evaluator has an interest, that relationship should be prominently disclosed.

---

## 8. Security and Production-Use Limitation

QTEP evaluates software functionality and practical developer utility.

A QTEP evaluation is **not**:

* a security audit;
* a vulnerability assessment;
* software certification;
* a legal or regulatory review;
* assurance of production readiness.

Successful functional evaluation should not be interpreted as evidence that software is secure or appropriate for production deployment.

Users and organizations remain responsible for evaluating software according to their own:

* security;
* privacy;
* licensing;
* compliance;
* operational;
* production;
* risk-management requirements.

---

## 9. Maintainer Interaction

Evaluators should make reasonable efforts to distinguish genuine software limitations from evaluator misunderstanding.

Before publishing a consequential negative finding, appropriate steps may include:

* reviewing relevant documentation;
* checking known issues;
* reproducing the behavior;
* contacting maintainers for factual clarification when warranted.

Maintainers may identify factual errors, explain intended behavior, or provide additional evidence.

Maintainers do not approve the final verdict.

Corrections should be made transparently when new evidence demonstrates that a published factual conclusion was incorrect.

---

## 10. Sustainability and Stop Rule

QTEP is an evaluation methodology, not an obligation to provide unpaid software development or continuing technical support.

Evaluators are not expected to:

* diagnose defects beyond what the evaluation requires;
* develop patches;
* submit pull requests;
* maintain evaluated software;
* provide continuing technical support.

Testing should stop when sufficient evidence exists to answer the defined question or when further testing would exceed the reasonable scope of the evaluation without resolving a material uncertainty.

---

## 11. Protocol Evolution

QTEP itself should be treated as an experimental methodology.

Changes should be versioned and documented.

Published evaluations should identify the version of QTEP under which they were performed.

Evaluation criteria should not be retroactively changed merely to produce a preferred verdict.

Lessons from completed evaluations may inform subsequent protocol versions.

Canonical QTEP releases are maintained according to the project's governance process.

---

## QTEP v0.1 Principle

> **Give the tool a fair opportunity to prove its value, verify that the comparison is legitimate, challenge the strongest credible weakness, preserve the evidence, and stop when the question has been answered.**
