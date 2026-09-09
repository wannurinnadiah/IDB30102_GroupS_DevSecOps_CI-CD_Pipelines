# Adaptive Security Gate: A Context-Aware Framework for Reducing False-Positive Alert Fatigue in DevSecOps CI/CD Pipelines

## Group Information

- **Group Number:** S
- **Assigned Research Area:** DevSecOps Security

### Group Members

| No. | Name | Student ID |
|---|---|---|
| 1 | Wan Nurin Nadiah Binti Wan Mohd Nasir | 52215225059 |
| 2 | Nurul Atiqah Binti Ridzuan | 52215225211 |
| 3 | Muhammad Azamuddin Bin Mohd Shahrid | 52215225175 |
| 4 | Muhammad Qayyum Bin Mohd Syahril | 52215228074 |
| 5 | Nor Arif Haqimi Bin Norazman Halim | 52215124087 |

---

## Research Problem

SAST/SCA tools can produce false-positive and low-relevance security findings, which may contribute to developer alert fatigue and unnecessary CI/CD pipeline interruptions. Traditional security gates that rely mainly on fixed severity thresholds may also overlook contextual factors when deciding whether a security finding should block a pipeline.

---

## Research Aim

To design and develop a context-aware adaptive security gate that prioritises CI/CD security alerts based on contextual risk while minimising false-positive alert fatigue and additional pipeline execution overhead.

---

## Research Objectives

1. To identify contextual risk factors that affect security alert prioritisation in DevSecOps CI/CD pipelines.

2. To design and develop a prototype context-aware adaptive security gate integrated with an open-source SAST/SCA tool.

3. To evaluate the proposed security gate against a conventional non-adaptive gate based on false-positive reduction, detection accuracy, and pipeline execution overhead.

---

## Proposed Solution

The proposed solution is a context-aware adaptive security gate that supplements an existing open-source SAST/SCA tool within a CI/CD pipeline.

The framework considers five contextual factors:

- Code-change criticality
- File-path context
- Deployment environment
- Historical rule reliability
- Security finding severity

These factors are used to calculate a contextual risk score for each security finding. Based on the resulting risk level, findings are classified into three categories:

| Risk Level | Proposed Action |
|---|---|
| **Low Risk** | Suppress the finding and allow the pipeline to continue |
| **Advisory** | Report the finding with a warning without blocking the pipeline |
| **High Risk** | Block the pipeline and raise an alert |

The proposed approach aims to reduce unnecessary security alerts while maintaining effective security detection without introducing substantial additional CI/CD pipeline overhead.

---

## Research Methodology and Development Model

- **Research Methodology:** Experimental Research
- **Development Model:** Iterative Prototyping Model

The experimental methodology will be used to compare the proposed context-aware adaptive security gate with a conventional severity-based security gate under controlled conditions.

The Iterative Prototyping Model will be used to develop, test, and refine the prototype before the final evaluation.

---

## Proposed System Architecture

The proposed architecture consists of five major components:

1. **CI/CD Pipeline**  
   Triggers the security scanning process when code is committed.

2. **SAST/SCA Scanner**  
   Scans the source code and generates security findings.

3. **Context Extraction Module**  
   Collects relevant contextual information for each security finding.

4. **Risk Scoring Module**  
   Calculates the contextual risk score using the identified risk factors.

5. **Adaptive Decision Module**  
   Classifies findings as low-risk, advisory, or high-risk and applies the appropriate pipeline action.

### System Flow

```text
Code Commit
     |
     v
CI/CD Pipeline
     |
     v
SAST/SCA Scanner
     |
     v
Security Findings
     |
     v
Context Extraction
     |
     v
Risk Scoring
     |
     v
Risk Classification
   /      |       \
  /       |        \
Low    Advisory    High
Risk      Risk      Risk
 |         |         |
 v         v         v
Suppress  Notify    Block
 /Pass    /Pass     Pipeline
 Build    Build     / Alert