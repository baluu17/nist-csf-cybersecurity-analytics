# NIST CSF–Aligned Cybersecurity Analytics Platform

This project implements an end-to-end cybersecurity analytics pipeline aligned with the
NIST Cybersecurity Framework (Identify, Protect, Detect, Respond, Recover) using Python
and the CIC-IDS2017 intrusion detection dataset.

The goal of this project is to demonstrate how data analytics and machine learning can be
used to support SOC-style security monitoring and incident handling.

## NIST CSF Mapping

- **Identify**: Asset and service risk scoring based on attack exposure and traffic behaviour
- **Protect**: Baseline policy creation and rule-based violation analysis
- **Detect**: Anomaly detection using Isolation Forest and One-Class SVM
- **Respond**: Incident generation, severity assignment, and analyst-friendly summaries
- **Recover**: Post-incident analysis and recommendations for system improvement

## Data Source

- Dataset: **CIC-IDS2017**
- Raw and processed datasets are not included in this repository due to file size limitations.

All data processing steps can be reproduced by running the notebooks in order,
starting from `01_data_loading_overview.ipynb`.

## Repository Structure

notebooks/
├── 01_data_loading_overview.ipynb
├── 02_data_cleaning.ipynb
├── 03_identify_risk_scoring.ipynb
├── 04_protect_access_analysis.ipynb
├── 05_detect_anomaly_detection.ipynb
├── 06_respond_incident_summary.ipynb
├── 07_recover_post_incident_analysis.ipynb
└── 08_visual_insights.ipynb

## Key Outputs

- Risk-ranked network services (destination ports)
- Policy violation summaries under baseline traffic
- ML-based anomaly detection results
- Prioritised incident queues with severity levels
- Post-incident insights and recovery recommendations

## Visual Highlights

Screenshots and diagrams used for project demonstration and LinkedIn sharing are available
in the project documentation and notebooks.

## Technologies Used

- Python
- Pandas, NumPy
- Scikit-learn
- Jupyter Notebook
- CIC-IDS2017 dataset
