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

### Notebooks

- **01_data_loading_overview.ipynb**  
  Loads the CIC-IDS2017 datasets and provides an initial overview of features and labels.

- **02_data_cleaning.ipynb**  
  Cleans, standardises, and prepares the raw data for analysis and modelling.

- **03_identify_risk_scoring.ipynb**  
  Implements the **Identify** function of the NIST Cybersecurity Framework by scoring and ranking network services based on risk exposure.

- **04_protect_access_analysis.ipynb**  
  Implements the **Protect** function by defining baseline behaviour and analysing policy violations.

- **05_detect_anomaly_detection.ipynb**  
  Implements the **Detect** function using Isolation Forest and One-Class SVM to identify anomalous network flows.

- **06_respond_incident_summary.ipynb**  
  Implements the **Respond** function by converting detected anomalies into prioritised incident summaries with severity levels.

- **07_recover_post_incident_analysis.ipynb**  
  Implements the **Recover** function by analysing incidents and generating lessons learned and improvement recommendations.

- **08_visual_insights.ipynb**  
  Contains visual summaries and line graphs used for project demonstration and LinkedIn sharing.


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
