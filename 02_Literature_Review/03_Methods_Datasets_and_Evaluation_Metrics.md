# Summary of Methods, Datasets and Evaluation Metrics from Prior Studies

## Methods / Algorithms Identified from Previous Studies

| Study | Method / Algorithm |
|---|---|
| Cruz et al. (2023) | Multi-tool SAST/DAST/SCA comparative pipeline |
| Rida (2026) | Proxy CI/CD pipeline architecture with automated quality gate enforcement |
| Esposito (2024) | Comparative benchmarking of static application security testing (SAST) tools |
| De Vito et al. (2025) | SecLLM — LLM-based security smell detection for Infrastructure as Code (IaC) |
| Kandadi et al. (2026) | Hybrid Transformer–GNN ensemble for threat classification |
| Kalwani (2026) | Random Forest + RNN sequence analyser for predictive vulnerability detection |
| Nagvekar (2025) | Multi-agent LLM with reinforcement learning for autonomous pipeline remediation |
| Abdiukov (2024) | AI-based vulnerability discovery with automated compliance validation |
| Gangina (2024) | AI-enhanced compliance automation for cloud-native CI/CD pipelines |

## Relevant Datasets Identified

| Dataset / Data Source | Used In | Notes |
|---|---|---|
| CICIDS-2017 (synthetic network traffic) | AI/ML triage studies (e.g., Kandadi et al., 2026) | Flagged in the literature as a limitation — synthetic data does not reflect real CI/CD execution logs |
| Vulnerable benchmark applications (OWASP-style) | Proxy pipeline studies (Rida, 2026) | This research will use similarly structured open-source benchmark applications containing known vulnerabilities and intentionally benign configurations |
| Real-world CI/CD execution logs | Not widely available in reviewed literature | Identified gap — this research collects its own execution logs during baseline and adaptive-gate testing (see `05_Data_or_Sample_Input/`) |

## Evaluation Metrics Identified from Previous Research

| Metric | Reported in Literature | Application to This Research |
|---|---|---|
| False-positive rate | 10–15% (Rida, 2026, proxy pipeline) | Primary metric — False Positive Reduction (RO3) |
| Pipeline execution overhead | Up to 41.8% increase (Rida, 2026) | Primary metric — Pipeline Overhead (RO3) |
| Detection accuracy | 93.8%–99.98% across AI/ML studies (Kalwani, 2026; Kandadi et al., 2026) | Primary metric — Detection Accuracy (RO3), used as an upper-bound reference rather than a direct benchmark since this research uses rule-based scoring, not ML |
| Latency / scan response time | 680 ms (Kandadi et al., 2026); 83% latency reduction (Kalwani, 2026) | Secondary consideration under pipeline overhead |
| Deployment/build success rate | 80–95% first-attempt success (Nagvekar, 2025) | Not directly used — out of scope (this research targets alert prioritisation, not remediation) |

*This content is consistent with Chapter 2 (Section 2.2) of the Research Proposal and supports the Proposed Evaluation Plan in Chapter 3 (Section 3.9).*
