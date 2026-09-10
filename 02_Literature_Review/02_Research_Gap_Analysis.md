# Research Gap Analysis

*This corresponds to Section 2.5 of the Research Proposal and must remain consistent with that section.*

Three gaps emerge from the literature synthesis:

## Gap 1: Context-Blindness
Static security gates apply uniform pass/fail rules regardless of commit risk, generating high false-positive volumes that drive gate bypass — particularly in SMEs (Cheenepalli et al., 2025; Ebert & Hochstein, 2023).

## Gap 2: Security Coverage vs. Pipeline Velocity Trade-off
Multi-scanner pipelines improve vulnerability detection but severely degrade deployment speed, introducing up to 41.8% execution overhead (Rida, 2026). Existing frameworks lack an adaptive mechanism to dynamically adjust scanning intensity based on a commit's specific risk profile, forcing teams to choose between speed and security.

## Gap 3: Explainability and Evaluation Bias in AI/ML Triage
AI and ML approaches show strong benchmark performance in vulnerability triage (Kandadi et al., 2026; Kalwani, 2026; Nagvekar, 2025) but suffer from:
- **Synthetic evaluation bias** — models trained on synthetic traffic data (e.g., CICIDS-2017) rather than real CI/CD execution logs
- **Black-box explainability gap** — predictions given without transparent reasoning (Abdiukov, 2024; Gangina, 2024), reducing developer trust
- **Lack of inline adaptability** — current models function as offline diagnostic tools rather than dynamic gate controllers

## How This Research Addresses the Gaps

| Research Gap | How the Proposed Framework Addresses It |
|---|---|
| Context-blindness | Context Extraction Module scores findings using code-change criticality, file-path context, deployment environment, historical rule reliability, and severity — not severity alone |
| Coverage vs. velocity trade-off | Two-stage thresholding (advisory + blocking) allows low-risk findings to be suppressed or logged instead of always halting the pipeline, targeting reduced overhead without sacrificing detection |
| Explainability & evaluation bias | Uses a transparent, rule-based contextual scoring approach (not a black-box ML model) and is evaluated on real benchmark application scans rather than synthetic network traffic |

Together, these gaps justify a **context-aware, explainable, inline-adaptive security gate** — the direction pursued in this study (Adaptive Security Gate: A Context-Aware Framework for Reducing False-Positive Alert Fatigue in DevSecOps CI/CD Pipelines).
