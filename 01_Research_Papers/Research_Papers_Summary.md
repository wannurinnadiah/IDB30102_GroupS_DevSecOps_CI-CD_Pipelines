# Research Papers Summary

This file lists the research papers used to support the Research Proposal, particularly Chapter 2 (Literature Review). These are the 11 papers cited directly in the proposal's narrative and 2 papers also support the ideas.

**Note on copyright:** Full-text PDFs of these papers are not uploaded to this public repository. Citations, DOIs, and official article links are provided instead, in line with the assignment brief's requirement not to redistribute copyrighted material.

---

### 1. Esposito, M. (2024)

| Field | Detail |
|---|---|
| **Paper Title** | An Extensive Comparison of Static Application Security Testing Tools |
| **Author(s)** | Esposito, M. |
| **Year** | 2024 |
| **Research Problem** | Individual SAST tools may vary significantly in detection coverage across different codebases |
| **Method / Technique** | Comparative benchmarking of multiple static application security testing (SAST) tools |
| **Dataset / Tools** | Multiple open-source and commercial SAST tools tested across benchmark codebases |
| **Main Findings** | SAST tools generate inconsistent vulnerability counts on the same codebase, indicating no single tool provides complete coverage |
| **Limitation** | Focuses on tool comparison only; does not address false-positive filtering or contextual prioritisation |
| **Relevance to Proposed Research** | Supports the motivation for combining scanner output with contextual risk scoring rather than relying on any single SAST tool's severity rating |
| **DOI / Link** | https://doi.org/10.1145/3661167.3661199 |

---

### 2. Cruz, D. B., Almeida, J. R., & Oliveira, J. L. (2023)

| Field | Detail |
|---|---|
| **Paper Title** | Open Source Solutions for Vulnerability Assessment: A Comparative Analysis |
| **Author(s)** | Cruz, D. B., Almeida, J. R., & Oliveira, J. L. |
| **Year** | 2023 |
| **Research Problem** | Determine whether combining multiple open-source security testing tools improves vulnerability coverage |
| **Method / Technique** | Multi-tool SAST/DAST/SCA comparative pipeline evaluation |
| **Dataset / Tools** | Open-source vulnerability assessment tools integrated into a test pipeline |
| **Main Findings** | Multi-tool pipelines broaden vulnerability coverage but introduce severe execution overhead |
| **Limitation** | Overhead cost of multi-tool scanning is not addressed with any mitigation strategy |
| **Relevance to Proposed Research** | Establishes the coverage-vs-overhead trade-off that the proposed adaptive gate aims to resolve through contextual filtering |
| **DOI / Link** | https://doi.org/10.1109/ACCESS.2023.3315595 |

---

### 3. Rida, A. (2026)

| Field | Detail |
|---|---|
| **Paper Title** | Empirical Evaluation of a DevSecOps Proxy Pipeline for Multi-Tier Web Applications |
| **Author(s)** | Rida, A. |
| **Year** | 2026 |
| **Research Problem** | Quantify the execution overhead introduced by automated security testing in CI/CD pipelines |
| **Method / Technique** | Proxy CI/CD pipeline architecture with automated quality gate enforcement |
| **Dataset / Tools** | Multi-tier web application benchmark deployed through a proxy CI/CD pipeline |
| **Main Findings** | Automated security testing accounted for up to 41.8% of total pipeline execution time despite achieving 10–15% false-positive rates |
| **Limitation** | No adaptive mechanism proposed to reduce this overhead based on commit risk |
| **Relevance to Proposed Research** | Provides the key overhead benchmark (41.8%) used as the comparison baseline for the proposed evaluation plan (Section 3.9) |
| **DOI / Link** | https://doi.org/10.3390/fi18070371 |

---

### 4. De Vito, G., Palomba, F., & Ferrucci, F. (2025)

| Field | Detail |
|---|---|
| **Paper Title** | SecLLM: Enhancing Security Smell Detection in IaC with Large Language Models |
| **Author(s)** | De Vito, G., Palomba, F., & Ferrucci, F. |
| **Year** | 2025 |
| **Research Problem** | Static linters flag intentional test/mock configurations in Infrastructure-as-Code (IaC) as false security alerts |
| **Method / Technique** | Static analysis using custom IaC linters combined with large language models (LLMs) |
| **Dataset / Tools** | 1,200+ Ansible playbooks and Terraform scripts from public GitHub repositories |
| **Main Findings** | Misconfigured permissions and untrusted imports are widespread; linter rules frequently flag intentional test configurations as false alerts |
| **Limitation** | LLM-based filtering adds computational cost and is not evaluated for CI/CD pipeline latency impact |
| **Relevance to Proposed Research** | Directly supports the proposed gate's test/mock-directory risk-weighting logic (Section 3.6), which addresses the same false-positive pattern |
| **DOI / Link** | https://doi.org/10.1109/ACCESS.2025.3637505 |

---

### 5. Ebert, C., & Hochstein, L. (2023)

| Field | Detail |
|---|---|
| **Paper Title** | DevOps in Practice |
| **Author(s)** | Ebert, C., & Hochstein, L. |
| **Year** | 2023 |
| **Research Problem** | Understand how developers respond to blocking security gates under delivery pressure |
| **Method / Technique** | Practitioner-based analysis of DevOps workflows |
| **Dataset / Tools** | Industry DevOps practice observations |
| **Main Findings** | Developers tend to disable or bypass security gates to meet sprint deadlines when gates are overly strict |
| **Limitation** | Lacks quantitative measurement of bypass frequency or downstream security risk |
| **Relevance to Proposed Research** | Supports Problem Statement 1 (alert fatigue leading to gate bypass), motivating the advisory-first, non-blocking approach for low/medium-risk findings |
| **DOI / Link** | https://doi.org/10.1109/MS.2022.3213285 |

---

### 6. Cheenepalli, J., Hastings, J. D., Ahmed, K. M., & Fenner, C. (2025)

| Field | Detail |
|---|---|
| **Paper Title** | Advancing DevSecOps in SMEs: Challenges and Best Practices for Secure CI/CD Pipelines |
| **Author(s)** | Cheenepalli, J., Hastings, J. D., Ahmed, K. M., & Fenner, C. |
| **Year** | 2025 |
| **Research Problem** | Assess DevSecOps adoption challenges and best practices among small and medium-sized enterprises (SMEs) |
| **Method / Technique** | Mixed-method survey based on Technology Acceptance Model (TAM) and Diffusion of Innovations (DOI) theory |
| **Dataset / Tools** | Survey of 405 SME professionals |
| **Main Findings** | 68% of organisations adopted DevSecOps, but only 12% performed security scanning on every commit; tooling complexity was the primary barrier |
| **Limitation** | Self-reported survey data limited to SME context; does not measure actual pipeline telemetry |
| **Relevance to Proposed Research** | Justifies the research's SME focus (Section 1.7) and supports Problem Statement 2 regarding resource-constrained teams needing lightweight solutions |
| **DOI / Link** | https://doi.org/10.1109/ISDFS65363.2025.11011960 |

---

### 7. Kandadi, A., Muntean, C. H., Gupta, S., & Bhaskaran, R. (2026)

| Field | Detail |
|---|---|
| **Paper Title** | Scalable Threat Assessment Machine Learning Framework for CI/CD DevSecOps Pipelines |
| **Author(s)** | Kandadi, A., Muntean, C. H., Gupta, S., & Bhaskaran, R. |
| **Year** | 2026 |
| **Research Problem** | Detect cloud-native CI/CD threats with sub-second latency |
| **Method / Technique** | Hybrid Transformer + Graph Neural Network (GNN) ensemble |
| **Dataset / Tools** | CICIDS-2017 dataset (2.8 million records); AWS Fargate; Random Forest; GNN |
| **Main Findings** | Achieved 99.98% detection accuracy, 680 ms mean time to detect, and 0.0005% false-positive rate |
| **Limitation** | Tested on synthetic network flow data rather than native CI/CD audit logs, limiting real-world applicability |
| **Relevance to Proposed Research** | Illustrates the synthetic-evaluation-bias gap (Research Gap 3) that the proposed rule-based, real-benchmark-tested approach aims to avoid |
| **DOI / Link** | https://doi.org/10.1109/FLICS70075.2026.11621927 |

---

### 8. Kalwani, T. (2026)

| Field | Detail |
|---|---|
| **Paper Title** | AI for DevSecOps Optimization: Investigating the Role of AI/ML in Predictive Vulnerability Detection During CI/CD Pipeline Stages |
| **Author(s)** | Kalwani, T. |
| **Year** | 2026 |
| **Research Problem** | Predict vulnerabilities during CI/CD pipeline stages before build execution |
| **Method / Technique** | Machine learning (Random Forest + RNN) |
| **Dataset / Tools** | 416 commits and vulnerability logs |
| **Main Findings** | 93.8% detection accuracy with an 83% reduction in scan latency |
| **Limitation** | Small dataset (416 commits) may limit model generalisability to larger, more diverse codebases |
| **Relevance to Proposed Research** | Provides an accuracy/latency benchmark referenced in the Proposed Evaluation Plan (Section 3.9) and Expected Outcome (Section 3.11) |
| **DOI / Link** | https://doi.org/10.1109/ISDFS69419.2026.11458957 |

---

### 9. Nagvekar, R. (2025)

| Field | Detail |
|---|---|
| **Paper Title** | Agentic AI-Driven CI/CD Pipelines for Autonomous Software Delivery |
| **Author(s)** | Nagvekar, R. |
| **Year** | 2025 |
| **Research Problem** | Prevent CI/CD pipeline crashes and reduce test failures through automated remediation |
| **Method / Technique** | Multi-agent large language model (LLM) framework |
| **Dataset / Tools** | Jenkins, GitHub Actions, ArgoCD, Kubernetes; telemetry logs across cloud services |
| **Main Findings** | Cut delivery cycle time by 35%, reduced pipeline errors by 40%, achieved 95% remediation success rate |
| **Limitation** | Scalability testing in large multi-tenant environments remains limited |
| **Relevance to Proposed Research** | Represents the heavyweight, remediation-focused alternative approach that this research's lightweight prioritisation-only scope is positioned against |
| **DOI / Link** | https://doi.org/10.1109/ICTBIG68706.2025.11323919 |

---

### 10. Abdiukov, T. (2024)

| Field | Detail |
|---|---|
| **Paper Title** | Automated Security Testing in DevSecOps Pipelines: Integrating AI-Based Vulnerability Discovery and Compliance Validation |
| **Author(s)** | Abdiukov, T. |
| **Year** | 2024 |
| **Research Problem** | Review the role of AI-based methods in security testing and compliance validation across DevSecOps |
| **Method / Technique** | Conceptual literature review of AI applications across CI/CD stages |
| **Dataset / Tools** | Literature and industry reports (no primary dataset) |
| **Main Findings** | AI-based triage reduces false alarms compared to static rule-based engines |
| **Limitation** | Narrative review with no original empirical trials; explainability of AI decisions remains unresolved |
| **Relevance to Proposed Research** | Supports Research Gap 3 (explainability deficit in AI-based triage), motivating the proposed rule-based, transparent scoring approach instead of a black-box model |
| **DOI / Link** | https://doi.org/10.30574/wjarr.2024.22.1.1083 |

---

### 11. Gangina, P. (2024)

| Field | Detail |
|---|---|
| **Paper Title** | AI-Enhanced DevSecOps: Automating Security Compliance in Cloud-Native Pipelines |
| **Author(s)** | Gangina, P. |
| **Year** | 2024 |
| **Research Problem** | Propose an AI/ML-driven architecture for compliance, testing, and threat detection in cloud-native DevSecOps |
| **Method / Technique** | Conceptual synthesis of AI-supported detection and compliance frameworks |
| **Dataset / Tools** | Synthesis of previously published studies and industry reports; no primary data collected |
| **Main Findings** | AI improves flaw identification and adapts to shifting compliance requirements |
| **Limitation** | Conceptual only; cites secondary literature without original experiments |
| **Relevance to Proposed Research** | Further supports Research Gap 3 alongside Abdiukov (2024); reinforces the case for an explainable, empirically-tested alternative |
| **DOI / Link** | https://doi.org/10.15662/IJFIST.2024.0704004 |

---

### 12. Meliala, R., Lim, C., & Andreas, J. (2024)

| Field | Detail |
|---|---|
| **Paper Title** | Integrating Security Testing in CI/CD Pipelines: Current Trends from Literature and Market |
| **Author(s)** | Meliala, R., Lim, C., & Andreas, J. |
| **Year** | 2024 |
| **Research Problem** | Difficulty in standardizing security testing integration into CI/CD pipelines due to disparate toolchains, organizational silos, and developer frictions |
| **Method / Technique** | Mixed-method empirical review combining systematic academic literature analysis with industry market tool benchmarks |
| **Dataset / Tools** | 40 peer-reviewed articles and commercial/open-source CI/CD security market tool reports |
| **Main Findings** | Early integration of security testing (SAST/DAST/SCA) significantly prevents defect leakage into releases, but adoption is hindered by tool integration complexity and noisy alerts |
| **Limitation** | Excludes pre-development and post-deployment stages; lacks real-time build telemetry and fine-grained latency evaluation |
| **Relevance to Proposed Research** | Directly substantiates the problem of developer friction and alert fatigue caused by rigid, uncoordinated automated testing in CI/CD pipelines |
| **DOI / Link** | https://doi.org/10.1109/ICIC64337.2024.10957011 |

---

### 13. Cyril, H. P., & Kumara, S. (2026)

| Field | Detail |
|---|---|
| **Paper Title** | DevSecOps-Driven Security Integration in the Software Development Lifecycle Using CI/CD Pipelines |
| **Author(s)** | Cyril, H. P., & Kumara, S. |
| **Year** | 2026 |
| **Research Problem** | Inconsistent security enforcement and alert triage bottlenecks in automated multi-tool CI/CD deployment pipelines |
| **Method / Technique** | Multi-tool security pipeline integration combined with machine learning (Random Forest) vulnerability classification and prioritization |
| **Dataset / Tools** | Containerized web applications with injected flaw sets; Semgrep, SonarQube, Snyk, OWASP ZAP, and Random Forest classifier |
| **Main Findings** | Achieved 0.75 overall classification accuracy, demonstrating strong detection on CORS issues but revealing high vulnerability triage variance across heterogeneous flaw categories |
| **Limitation** | Low precision (0.38) and moderate F1-score (0.50) on hardcoded secret detection; prone to misclassifications and false alerts on imbalanced flaw datasets |
| **Relevance to Proposed Research** | Proves the necessity of integrating contextual metadata (e.g., test fixtures vs. production paths) and explainable models to improve triage precision and eliminate false alarms |
| **DOI / Link** | https://doi.org/10.1109/ICAIC67076.2026.11395737 |