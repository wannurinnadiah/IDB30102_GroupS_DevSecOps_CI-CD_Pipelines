# System Architecture

The proposed architecture consists of five major components:
* **CI/CD Pipeline**
* **SAST/SCA Scanner**
* **Context Extraction Module**
* **Risk Scoring Module**
* **Adaptive Decision Module**

## Workflow

When code is committed, the CI/CD pipeline triggers the selected SAST/SCA scanner, which generates security findings. The Context Extraction Module then collects relevant contextual information, such as code-change criticality, file-path context, deployment environment, historical rule reliability, and finding severity. These factors are passed to the Risk Scoring Module to calculate a contextual risk score for each finding.

## Decision Logic

The Adaptive Decision Module classifies each finding as:
- **Low-risk:** May be suppressed.
- **Advisory:** Reported without blocking the pipeline.
- **High-risk:** Blocks the pipeline.
