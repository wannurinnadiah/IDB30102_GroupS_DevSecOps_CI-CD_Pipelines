\# Expected Research Outcomes and Evaluation Metrics



Since this project is at the proposal stage, the following outlines the expected results and the specific evaluation metrics that will be used to measure the success of the Adaptive Security Gate prototype.



\## 1. Evaluation Metrics



The proposed context-aware security gate will be evaluated against a traditional, non-adaptive SAST/SCA gate. The comparison will be measured using three primary metrics:



\* \*\*False Positive Reduction:\*\* Measuring the decrease in non-exploitable or low-relevance alerts (e.g., vulnerabilities flagged in intentional benign test/mock directories).

\* \*\*Detection Accuracy:\*\* Ensuring that genuine, high-risk vulnerabilities in production paths are not missed or incorrectly suppressed.

\* \*\*Pipeline Execution Overhead:\*\* Measuring the total execution time to ensure the context extraction and scoring modules do not introduce severe runtime penalties (avoiding the 41.8% overhead seen in previous proxy architectures).



\## 2. Expected Outcomes



The expected outcomes are:



\* \*\*Working Prototype:\*\* A fully functional prototype of a context-aware security gate integrated with an open-source SAST/SCA tool (e.g., Semgrep/SonarQube) in a GitHub Actions environment.

\* \*\*Reduced Developer Friction:\*\* The adaptive gate is expected to significantly reduce false positives for test/mock-directory findings compared to baseline severity-only gates, mitigating alert fatigue.

\* \*\*Efficient Pipeline Execution:\*\* The overhead from the proposed 5-component architecture and two-stage thresholding logic is expected to stay within an acceptable margin, proving that contextual risk prioritization is a practical, lower-overhead alternative to traditional security gates.

