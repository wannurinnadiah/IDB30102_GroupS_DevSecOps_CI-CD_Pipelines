# Runtime Decision Logic

This diagram shows the decision logic each finding follows at runtime. A code commit triggers the CI/CD pipeline, which runs the SAST/SCA tool and extracts security alerts. 

## Context-Aware Path Evaluation

The system checks whether the affected file path lies in a test or mock directory:
* **Test/Mock Paths:** Receive a lower risk weighting.
* **Production Paths:** Receive standard risk weighting.

This demonstrates how the Context Extraction Module's path data is applied directly before scoring, rather than just collected.

## Threshold Evaluation & Pipeline Actions

Both branches converge at a final risk score (0–100), which is evaluated against two sequential thresholds:

1. **Blocking Threshold (High Risk)**
   * **Score:** At or above the blocking threshold.
   * **Action:** Halts the pipeline and raises an urgent alert.

2. **Advisory Threshold (Medium Risk)**
   * **Score:** Below the blocking threshold, but at or above the advisory threshold.
   * **Action:** Passes the pipeline with warning logs.

3. **Suppressed Findings (Low Risk)**
   * **Score:** Below the advisory threshold.
   * **Action:** Suppressed as low relevance.

This two-stage design enables three distinct outcomes (**suppress**, **warn**, **block**) based on tuneable thresholds rather than fixed severity labels.
