# Analyzing Stress Responses Related to Usability of User Interfaces

## Overview

This repository contains the codebase and documentation for my bachelor thesis project, which investigates the relationship between user interface design, usability, and physiological stress responses. This research combines principles from human-computer interaction, usability engineering, and psychophysiology to provide insights into user experience evaluation.

## Published Research

This work has been published in a peer-reviewed paper:
**Title**: "Analyzing Stress Responses Related to Usability of User Interfaces"
**DOI**: [Link](https://doi.org/10.1145/3605390.3605399)

## Data Collection and Privacy

This project involved extensive user testing with 30 participants, each engaging with two different interface designs. Physiological data was collected using the Empatica E4 wristband, which captured:

- Electrodermal Activity (EDA)
- Blood Volume Pulse (BVP)
- Skin Temperature
- 3-axis Accelerometer data

The dataset collected for this research is proprietary and cannot be shared publicly due to privacy concerns and ethical considerations. The data contains sensitive physiological information and personally identifiable data from participants. As such, the raw data is not included in this repository.

The experiments were conducted with informed consent from all participants, and the data was anonymized and stored securely in compliance with data protection regulations.

## Project Structure

```
usability-stress-response-analysis/
├── scripts/
│   ├── dataset_concatenation.mlx
│   ├── EDA_features_dataset_building_script.mlx
│   ├── EDA_features_SUS_correlation.mlx
│   ├── export_table_to_csv.mlx
│   ├── hrv_hrrange_extraction.mlx
│   ├── merge_eda_temp_bvp_datasets.mlx
│   └── temp_bvp_feature_extraction.mlx
├── interfaces/
│   ├── interface_A/
│   └── interface_B/
├── analysis/
│   ├── classification/
│   └── regression/
├── docs/
│   ├── Presentation.pdf
│   └── project_report.md
└── README.md
```

## Key Features and Findings

- **Innovative Data Collection**: Utilized the Empatica E4 wristband to gather real-time physiological data during user interactions with interfaces.
- **Dual Interface Analysis**: Compared user responses between a poorly designed interface and an optimized version to identify usability impacts.
- **Advanced Signal Processing**: Extracted meaningful features from EDA, BVP, and skin temperature signals using MATLAB.
- **Machine Learning Integration**:
  - Achieved 82.1% accuracy in classifying interface types using physiological signals.
  - Successfully predicted User Experience Questionnaire (UEQ) scores, with the best performance for the efficiency metric.

- **Correlation Analysis**: Identified significant correlations between the number of Skin Conductance Responses (SCRs) and established usability metrics.
- **Comprehensive Usability Evaluation**: Incorporated standard usability questionnaires (SUS, UEQ, SAM) alongside physiological measures.

## Technologies and Tools

- **MATLAB**: Primary tool for data processing, feature extraction, and analysis
- **Empatica E4 wristband**: For physiological data collection
- **HTML/CSS/JavaScript**: Used in creating test interfaces
- **Statistical analysis tools**: For correlation studies and result validation

## Potential Applications and Impact
This research has significant implications for:
- Enhancing user interface design processes
- Developing more accurate and objective usability testing methodologies
- Improving user experience in various digital products and services
- Advancing the field of affective computing in HCI