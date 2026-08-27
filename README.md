# Quantum Tool Evaluation Protocol (QTEP)

**QTEP** is an open methodology for independently evaluating the practical functionality and utility of open-source quantum software development tools.

The protocol is designed around three questions:

1. **Does it work?**
   Does the tested functionality perform as represented for the evaluated use case?

2. **Does it help?**
   Does the tool materially improve the workflow relative to a reasonable baseline?

3. **For whom?**
   Under what users, workloads, assumptions, or constraints does that improvement matter?

QTEP evaluates specific claims and workflows rather than attempting to determine whether a software project is universally "good" or "bad."

## Status

**Current version:** QTEP v0.1
**Status:** Experimental

Version 0.1 is the initial frozen protocol and will be tested through calibration evaluations before later versions are proposed.

The canonical QTEP specification is maintained through this repository.

## Public Review Scope

Public reviews conducted as part of the QTEP review program are limited to **quantum software that is publicly available under an identifiable open-source license**.

QTEP may also be used by others to evaluate proprietary, internal, or otherwise non-public software, but such evaluations fall outside the scope of the public QTEP review program.

## What QTEP Evaluates

Depending on the type of tool, QTEP may evaluate areas such as:

* functional correctness;
* practical developer utility;
* workflow complexity;
* interoperability;
* compilation or circuit characteristics;
* performance where relevant;
* documentation and developer experience;
* limitations and difficult use cases;
* value relative to a reasonable baseline.

Different classes of tools should be evaluated according to criteria appropriate to their intended purpose.

A simulator, compiler, verification tool, library, and visualization utility should not be judged as though they are interchangeable tools.

## What QTEP Does Not Evaluate

QTEP is **not**:

* a security audit;
* a vulnerability assessment;
* a software certification;
* a legal or regulatory review;
* an assurance of production readiness.

Users and organizations remain responsible for evaluating software according to their own security, privacy, licensing, compliance, operational, and risk-management requirements.

QTEP evaluations also do not create an obligation to diagnose, repair, maintain, or contribute code to evaluated projects.

## Independence

QTEP is intended to support transparent, independent evaluation.

Public evaluations should disclose material relationships or conflicts of interest involving the evaluator and the evaluated project.

Software developed by an evaluator or the evaluator's organization may be tested internally using QTEP, but such testing should **not** be represented as an independent QTEP review.

## Methodology

The complete QTEP v0.1 methodology is documented in [`PROTOCOL.md`](PROTOCOL.md).

The protocol follows a general sequence:

**Define the claim → Establish a baseline → Test the happy path → Verify equivalence → Measure value → Test a credible difficult case → Assess developer experience → Characterize limitations → Reach a verdict**

QTEP emphasizes the **minimum sufficient experiment**: testing should continue only as far as necessary to reach a defensible conclusion about the defined claim.

## Verdicts

QTEP uses five primary verdicts:

* **PASS**
* **CONDITIONAL PASS**
* **NO MATERIAL ADVANTAGE**
* **FAIL**
* **INCONCLUSIVE**

A tool that functions correctly does not automatically provide meaningful value over an existing workflow. Conversely, discovering a limitation or defect does not necessarily mean that a tool lacks practical utility.

## Open Methodology

QTEP is intended to improve through practical use and community feedback.

Issues, critiques, suggested methodological improvements, and pull requests are welcome.

The canonical QTEP specification and official version numbers are maintained through this repository. Modified or derivative versions should clearly identify their changes and should not represent themselves as canonical QTEP releases unless accepted by the maintainers.

## License

The QTEP methodology and documentation are licensed under the **Creative Commons Attribution-ShareAlike 4.0 International License (CC BY-SA 4.0)**.

You are free to share and adapt QTEP, including for commercial purposes, subject to the attribution and ShareAlike requirements of the license.

See [`LICENSE`](LICENSE) for the applicable license terms.

## Repository Roadmap

QTEP v0.1 will initially contain:

* the protocol specification;
* governance and contribution guidance;
* evaluation-plan and evaluation-report templates;
* disclosure guidance;
* protocol version history.

Executable evaluation software and public tool-review results are intentionally outside the initial v0.1 repository scope.

---

**QTEP principle:**

> Give the tool a fair opportunity to prove its value, verify that the comparison is legitimate, challenge the strongest credible weakness, preserve the evidence, and stop when the question has been answered.
