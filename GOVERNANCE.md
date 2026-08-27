# QTEP Governance

The Quantum Tool Evaluation Protocol (QTEP) is an openly licensed methodology maintained as a canonical specification through this repository.

This governance model is intentionally lightweight. QTEP is an experimental methodology, and governance should evolve only when practical experience demonstrates a need for additional structure.

## 1. Stewardship

Quantum Harmonic Systems, LLC (QHS) serves as the initial steward of the canonical QTEP specification.

The QTEP maintainers are responsible for:

* maintaining the canonical specification;
* reviewing proposed changes;
* assigning official QTEP version numbers;
* publishing canonical releases;
* maintaining supporting documentation and templates;
* preserving the independence and methodological integrity of the protocol.

Stewardship of the canonical specification does not restrict the rights granted under the QTEP license.

## 2. Open Participation

Community participation is encouraged.

Anyone may:

* use QTEP subject to its license;
* raise issues or methodological concerns;
* suggest improvements;
* propose new tool categories or category-specific criteria;
* submit pull requests;
* reproduce or critique published evaluations;
* adapt or fork QTEP subject to its license.

A contribution does not automatically become part of the canonical QTEP specification.

Acceptance of changes into the canonical specification remains at the discretion of the QTEP maintainers.

## 3. Canonical QTEP

The version of QTEP maintained and released through this repository is the canonical QTEP specification.

Only maintainers of the canonical repository may:

* assign official QTEP version numbers;
* designate a specification as an official QTEP release;
* represent a modified protocol as the canonical QTEP specification.

The ability to use, adapt, or redistribute QTEP does not confer authority to represent a derivative methodology as an official QTEP release.

## 4. Derivative Versions

QTEP is designed to be reusable and adaptable under its applicable license.

Derivative versions should:

* provide appropriate attribution;
* identify material modifications;
* comply with applicable ShareAlike requirements;
* avoid representing themselves as canonical QTEP releases unless their changes have been accepted into the canonical project.

Forks and adaptations are welcome. Clear identification of modifications helps users distinguish between the canonical methodology and derivative approaches.

## 5. Protocol Changes

Changes to the canonical protocol should be driven by evidence, practical experience, or a clearly identified methodological need.

Potential sources of change include:

* lessons from completed evaluations;
* reproducibility problems;
* ambiguity discovered during application of the protocol;
* new classes of quantum development tools;
* community feedback;
* evidence that an existing criterion produces misleading or unfair conclusions.

Changes should not be made merely to alter the outcome of a particular evaluation.

## 6. Versioning

QTEP uses explicit protocol version numbers so that evaluations can identify the methodology under which they were performed.

The initial experimental release is:

**QTEP v0.1**

During the experimental phase, subsequent versions may introduce meaningful methodological changes as practical experience accumulates.

Changes to the canonical protocol should be documented in `CHANGELOG.md`.

Published evaluations should identify the QTEP version used.

An evaluation completed under an earlier protocol version should not be silently recharacterized as having been conducted under a later version.

## 7. Independence and Conflicts

Governance decisions should preserve QTEP's purpose as an independent evaluation methodology.

Software developed by QHS may be evaluated internally using QTEP, but QHS-developed software should not be represented as having received an independent QTEP review from QHS or its maintainers.

If QHS or an evaluator has a material interest in software that competes with an evaluated project, that relationship should be disclosed prominently.

QTEP methodology should not be modified for the purpose of favoring QHS software, disadvantaging competing software, or predetermining an evaluation outcome.

## 8. Maintainer Judgment

No evaluation methodology can anticipate every quantum software tool, technical claim, or edge case.

Maintainers may exercise judgment when interpreting QTEP, provided that:

* the interpretation is consistent with the protocol's core principles;
* material deviations or assumptions are documented;
* equivalent cases are treated consistently;
* interpretations are not selected merely to produce a preferred verdict.

Repeated ambiguities should be considered candidates for clarification in a future QTEP version.

## 9. Future Governance

This governance model reflects QTEP's current experimental stage.

If QTEP develops a substantial external contributor or user community, future governance models may include additional maintainers, formal review processes, technical working groups, or other community structures.

Such mechanisms should be introduced only when they solve an observed governance problem.

---

**Governance principle:**

> Keep the methodology open, keep the canonical specification identifiable, welcome evidence and criticism, and add governance only when experience demonstrates that it is needed.
