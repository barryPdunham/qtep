# QTEP Changelog

This file documents changes to the canonical Quantum Tool Evaluation Protocol (QTEP).

Evaluations should identify the QTEP version under which they were performed.

Protocol versions are not applied retroactively to evaluations completed under earlier versions.

## [0.2] — on 2026-09-28

### Status

Experimental protocol refinement informed by initial calibration and practical tool evaluations.

QTEP v0.1 remains unchanged as the specification used for initial calibration.

### Added

* **Comparison boundary (Stage 1):** Explicitly identify the inputs, outputs, representations, and workflow stages included in an evaluation. Distinguish shared functionality from capabilities outside the comparison.
* **Equivalence method (Stage 4):** Identify an appropriate method for establishing equivalence and document its limitations. Where practical, use independent reference implementations, mathematical invariants, or established verification techniques.

### Clarified

* **Practical value (Stage 5):** Consider whether demonstrated benefits justify relevant adoption, integration, and maintenance costs relative to the baseline.
* Successful execution does not, by itself, establish equivalent functionality or material improvement over a reasonable baseline.
* Equivalence conclusions apply only to the semantics and conditions actually tested.

### Unchanged

* The three primary evaluation questions: Does it work? Does it help? For whom?
* The standard nine-stage evaluation sequence.
* The five verdict categories.
* Independence, reproducibility, and sustainability principles.
* The minimum sufficient experiment and stop rule.

### Calibration

Initial evaluations highlighted the importance of distinguishing successful tool execution from semantic equivalence and demonstrated practical value.

These findings informed the v0.2 clarifications without retroactively changing the criteria applied under v0.1.

## [0.1] on 2026-08-27

### Status

Initial experimental release.

QTEP v0.1 is frozen for initial calibration testing.

### Added

* Defined the purpose and scope of QTEP.
* Limited the public QTEP review program to publicly available quantum software distributed under an identifiable open-source license.
* Established the three primary evaluation questions:

  * Does it work?
  * Does it help?
  * For whom?
* Established the standard nine-stage evaluation sequence:

  1. Define the claim.
  2. Establish the baseline.
  3. Run the happy-path test.
  4. Apply the equivalence gate.
  5. Measure value added.
  6. Run a path-of-pain test.
  7. Assess developer experience.
  8. Characterize limitations.
  9. Reach a verdict.
* Defined five QTEP verdicts:

  * PASS
  * CONDITIONAL PASS
  * NO MATERIAL ADVANTAGE
  * FAIL
  * INCONCLUSIVE
* Established minimum evidence and reproducibility requirements.
* Defined independence and conflict-of-interest principles.
* Explicitly excluded security auditing, vulnerability assessment, certification, and assurance of production readiness from QTEP scope.
* Established a sustainability and stop rule separating evaluation from unpaid software maintenance or development.
* Established lightweight governance for canonical QTEP releases and community contributions.

### Calibration

QTEP v0.1 will undergo initial private calibration before the methodology is used for public independent tool reviews.

Findings from calibration may inform a future protocol version. QTEP v0.1 itself will remain unchanged so that the calibration is performed against a stable specification.
