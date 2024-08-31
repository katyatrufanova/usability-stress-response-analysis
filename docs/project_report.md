# Project Report: Stress Response Analysis in User Interface Usability

## Introduction

This project aims to investigate the relationship between user emotional states, usability, and user experience of interactive systems. The primary goal was to construct a dataset that can be used to explore these connections, focusing on physiological responses during user interaction with different interface designs.

## Experimental Design

### Interactive System Selection

The experiment utilized two versions of an interface based on ["User Inyerface"](https://userinyerface.com/), a web interface intentionally designed to violate usability principles. This choice was motivated by the desire to emphasize the role of usability in user experience and the emotions it can evoke.

Two versions were created:
1. A A "poorly designed" interface, closely mimicking the original "User Inyerface"
2. A "well-designed" interface, correcting the major usability issues

Both interfaces were translated into Italian to accommodate the study participants.

### Usability Testing

Thirty usability tests were conducted with fifteen users, involving students from the Department of Computer Science at the University of Bari Aldo Moro and external volunteers. Each participant interacted with both versions of the interface.

Key aspects of the testing process:

- Participants wore the Empatica E4 wristband to collect physiological data
- Tests were video and audio recorded (for 13 out of 15 users who consented)
- Screen recording was used to capture user interactions
- Users applied the "Thinking Aloud" technique during the tests
- Post-test questionnaires were administered, including SUS, UEQ, and SAM

## Dataset Construction

The constructed dataset includes:

- Physiological data: arterial pulse, heart rate, inter-beat intervals, galvanic skin response, 3-axis accelerometer data, and skin temperature
- Screen recordings of user interactions
- Video and audio recordings of users (where consent was given)
- User information: age group, gender, technology familiarity level
- Results from SUS, UEQ, and SAM questionnaires

## Feature Extraction

Discriminant features were extracted from the physiological data using MATLAB:

### 4.1 Electrodermal Activity (EDA) Features
- Average duration of Skin Conductance Responses (SCRs)
- Average amplitude of SCRs
- Average rise time of SCRs
- Signal mean
- Number of SCRs

### 4.2 Blood Volume Pulse (BVP) and Skin Temperature Features
- Mean of raw signals
- Standard deviation of raw signals
- Mean of absolute values of first differences of raw and normalized signals
- Mean of absolute values of second differences of raw and normalized signals

## 5. Statistical Analysis
Statistical analysis was performed to investigate the relationship between physiological data and usability metrics, with a focus on SUS and UEQ results relative to the interface type.

## 6. Correlation Detection
Correlation indices were calculated to evaluate the relationship between physiological signals and SUS and UEQ scores. Notable findings include:
- Moderate correlation between the number of SCRs and SUS scores
- Moderate correlation between the number of SCRs and some UEQ categories
- Moderate correlation between temperature and one UEQ category

## 7. Classification of Interactive System Based on Physiological Signals
Using MATLAB's Classification Learner tool, various classification algorithms were evaluated to automatically classify the interface version based on extracted physiological features.

Key result: Maximum accuracy of 82.1% achieved using the Ensemble Subspace Discriminant (ESD) algorithm.

## 8. Emotion Classification
The extracted features were used to predict SAM questionnaire results. Maximum accuracies achieved:
- 39.3% for pleasantness (Linear SVM)
- 46.4% for emotional activation (Medium KNN)
- 35.7% for dominance (Gaussian Naive Bayes)

## 9. Usability Prediction
Regression algorithms were used to predict SUS and UEQ scores based on physiological signals:

- **SUS prediction**: Best result with Least Squares Regression Kernel (RMSE: 30.455)
- **UEQ prediction**: Best result for efficiency prediction using Medium Tree and Coarse Tree algorithms (RMSE: 0.48932)

## 10. Conclusion
This study demonstrates the potential of using physiological signals to assess user experience and usability. While some predictions (like SUS scores) were less accurate, others (like interface classification and UEQ score prediction) showed promising results. This research opens up new possibilities in the field of usability engineering and emotion recognition in human-computer interaction.