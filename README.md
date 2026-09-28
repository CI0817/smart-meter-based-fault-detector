# Smart-Meter-Based LV Fault Detection & Diagnostics System

## Project Goals

Build a **Smart-Meter-Based LV Fault Detection & Diagnostics System** that:

- simulates a low-voltage distribution network in OpenDSS;
- generates synthetic AMI measurements;
- injects abnormal network conditions;
- detects and classifies those conditions from smart-meter data;
- evaluates detection performance quantitatively;
- presents results through plots or a small dashboard.

## Deliverables

| Week | Main work | Deliverable |
| --- | --- | --- |
| 1 — Network Model | Build a simple LV feeder with transformer, lines and 30–50 customers. Add realistic single/three-phase loads. Verify normal power flow. | Working OpenDSS model + network diagram + baseline voltage/load plots |
| 2 — AMI Dataset Generator | Create 5-minute customer load profiles. Run time-series power flow and record `V, P, Q`. Automate simulation from Python using OpenDSSDirect.py. | Python simulation pipeline + clean AMI dataset + normal-operation plots |
| 3 — Fault/Anomaly Simulation | Implement abnormal scenarios such as transformer overload, undervoltage, overvoltage, customer outage and phase imbalance. Label events automatically. | Labeled dataset containing normal + abnormal operating conditions |
| 4 — Baseline Detection | Implement simple engineering-based detection: voltage thresholds, rolling mean/std, voltage deviation and change detection. | Baseline detector + confusion matrix + precision/recall/F1 |
| 5 — ML Detection | Train one ML method such as Isolation Forest or XGBoost. Compare against baseline detector. Analyse false positives and detection delay. | ML model + baseline-vs-ML comparison + results table |
| 6 — Productisation | Clean repository, create visualisations/dashboard, document architecture, methodology and results. | Finished GitHub project + README + demo + technical report |

By the end, I would aim to have **six tangible outputs**:

1. OpenDSS LV network model
2. Synthetic AMI dataset generator
3. Fault injection framework
4. Rule-based fault detector
5. ML-based anomaly/fault detector
6. GitHub repository with README, results and demonstration

## Metrics to report

Measure:

- Precision
- Recall
- F1 score
- False-positive rate
- Detection latency
- accuracy by fault type

## Tech stack

| Area | Technology | Purpose |
| --- | --- | --- |
| Power-system simulation | OpenDSS | Build and simulate the LV feeder |
| OpenDSS interface | OpenDSSDirect.py | Control simulations from Python |
| Main language | Python | Simulation, processing, detection, evaluation |
| Data processing | Pandas / NumPy | Handle AMI `(V,P,Q)` time-series |
| ML | scikit-learn | Isolation Forest, Random Forest, XGBoost-style baselines |
| Visualisation | Matplotlib + Plotly | Analysis plots and interactive results |
| Development | VS Code + Jupyter | Coding and experimentation |
| Version control | Git + GitHub | Portfolio/repository |
| Environment | uv or venv | Python dependency management |