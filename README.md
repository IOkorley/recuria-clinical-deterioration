# RECURIA: Clinical Deterioration Prediction

## Overview

Clinical deterioration rarely occurs instantaneously.

Physiological systems often exhibit subtle changes in stability, variability, and dynamic behavior before adverse events become clinically obvious.

This project evaluates whether RECURIA-derived instability and transition features can provide useful predictive structure for identifying patient deterioration within a 12-hour prediction window.

Rather than focusing solely on predictive performance, this study investigates whether mathematically interpretable representations of instability can characterize biological transitions associated with declining patient status.

---

## Research Question

Can mathematically derived transition features capture clinically meaningful deterioration patterns before adverse events occur?

The central hypothesis is that physiological systems approaching deterioration may exhibit measurable changes in instability, curvature, and transition behavior that can be represented through interpretable mathematical quantities.

---

## Clinical Motivation

In acute care settings, deterioration is often preceded by subtle physiological changes.

Traditional monitoring systems frequently rely on threshold-based alerts that activate after significant changes have already occurred.

RECURIA explores whether transition-oriented features can identify instability patterns before conventional indicators become obvious.

---

## Dataset

### Source

Clinical Deterioration Prediction Dataset

### Domain

Healthcare and Patient Monitoring

### Prediction Task

Predict clinical deterioration within a 12-hour prediction window.

### Features

* Heart Rate
* Respiratory Rate
* Oxygen Saturation
* Blood Pressure
* Temperature
* Laboratory Measurements
* Demographic Variables
* Time-Series Monitoring Data

---

## RECURIA Framework

The framework derives four core mathematical quantities:

### Instability Magnitude

η

Measures the local magnitude of change within the physiological system.

### Oscillatory Transition State

r = η(sinθ + cosθ)

Represents directional transition behavior.

### Curvature

r''

Captures acceleration and structural changes in physiological dynamics.

### Transition Interaction Term

m = ηrr''

Represents interaction between instability and curvature during biological transitions.

---

## Methodology

1. Construct baseline machine learning models.
2. Generate RECURIA-derived features.
3. Train models using conventional and RECURIA feature sets.
4. Evaluate performance on held-out data.
5. Compare predictive behavior and generalization.

---

## Baseline Models

* Logistic Regression
* Random Forest
* XGBoost

---

## Results

| Model   | Baseline F1 | RECURIA F1 |
| ------- | ----------: | ---------: |
| XGBoost |      0.5007 |     0.4979 |

### Interpretation

Performance remained comparable to strong baseline models.

The primary objective of this study was not to maximize predictive performance, but to evaluate whether a common mathematical representation of instability can generalize to physiological monitoring systems.

Maintaining performance while introducing mathematically interpretable transition-oriented features provides evidence that the framework can represent clinically relevant structure without extensive domain-specific engineering.

---

## Key Findings

* Physiological systems exhibit measurable transition behavior before deterioration.
* RECURIA-derived features generalized to patient monitoring data.
* Transition-oriented features remained competitive with strong baseline models.
* Results support further investigation of interpretable feature engineering for healthcare applications.

---

## Research Significance

Clinical deterioration represents a real-world state-transition problem.

Understanding how physiological systems move from stable to unstable states has implications for:

* Early Warning Systems
* Patient Monitoring
* Risk Stratification
* Clinical Decision Support
* Healthcare AI Safety

This study contributes to a broader investigation into whether instability and transition dynamics can be represented through a common mathematical framework across unrelated domains.

---

## Repository Structure

```text
src/
notebooks/
results/
data/
```

---

## Related RECURIA Studies

* Multiple Sclerosis Conversion Prediction
* Autoimmune Disorder Classification
* Solar Activity Prediction
* Groundwater Stress Forecasting
* Retail Demand Forecasting
* Bike-Sharing Demand Forecasting
* Residential Energy Forecasting

---

## Research Themes

* Healthcare AI
* Clinical Monitoring
* Dynamic Systems
* Time-Series Analysis
* Mechanistic Interpretability
* Feature Engineering
* Cross-Domain Generalization

---

## Author

**Ishmaelina Okorley**

Independent researcher exploring mathematically interpretable representations of instability, transition dynamics, and complex system behavior across healthcare, environmental systems, and forecasting applications.

---

## License

Released under the MIT License.
