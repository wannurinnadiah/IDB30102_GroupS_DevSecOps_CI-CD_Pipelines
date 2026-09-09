# Adaptive Security Gate: A Context-Aware Framework for Reducing False-Positive Alert Fatigue in DevSecOps CI/CD Pipelines_Test

## Group Information
* **Group:** S
* **Assigned Research Area:** DevSecOps Security
* **Team Members:**
  * Wan Nurin Nadiah Binti Wan Mohd Nasir (52215225059)
  * Nurul Atiqah Binti Ridzuan (52215225211)
  * Muhammad Azamuddin Bin Mohd Shahrid (52215225175)
  * Muhammad Qayyum Bin Mohd Syahril (52215228074)
  * Nor Arif Haqimi Bin Norazman Halim (52215124087)

## Research Overview
* **Research Problem:** Traditional static security gates in SAST/SCA tools apply uniform pass/fail rules without context, leading to false-positive alert fatigue and pipeline overhead.
* **Research Aim:** To design and develop a context-aware adaptive security gate that prioritizes CI/CD security alerts based on contextual risk while minimizing false-positive alert fatigue and additional pipeline execution overhead.
* **Research Objectives:**
  1. To identify contextual risk factors that affect security alert prioritisation in DevSecOps CI/CD pipelines.
  2. To design and develop a prototype context-aware adaptive security gate integrated with an open-source SAST/SCA tool.
  3. To evaluate the proposed security gate against a conventional non-adaptive gate based on false-positive reduction, detection accuracy, and pipeline execution overhead.

## Methodology & Development
* **Research Methodology:** Experimental Research
* **Development Model:** Iterative Prototyping Model
* **System Architecture:** A 5-component architecture (CI/CD Pipeline, SAST/SCA Scanner, Context Extraction Module, Risk Scoring Module, and Adaptive Decision Module) using a two-stage thresholding logic.

## Technical Execution & Evaluation
* **Expected Tools:** GitHub Actions CI/CD environments, Semgrep, SonarQube.
* **Evaluation Plan:** Baseline scanning without adaptive filtering vs. context-aware scanning using benchmark vulnerable applications. Metrics evaluated will be False Positive Reduction, Detection Accuracy, and Pipeline Overhead.
