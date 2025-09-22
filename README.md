# Parkinson's Disease Telemonitoring - A Clustering Analysis

## 📖 Problem Background

**Parkinson’s disease (PD)** is a chronic, progressive neurodegenerative disorder that primarily affects motor control. It is characterized by symptoms such as tremors, rigidity, bradykinesia (slower movements), and postural instability. Beyond these motor impairments, Parkinson’s disease also affects speech and voice. Patients frequently develop vocal abnormalities such as reduced loudness, monotone speech, breathiness, and imprecise articulation, collectively known as dysphonia. These voice changes often appear early and can serve as non-invasive biomarkers of disease progression.  

**Traditional monitoring of PD progression** relies on in-clinic assessments using the Unified Parkinson’s Disease Rating Scale (UPDRS). While clinically validated, these assessments are costly, time-consuming, and limited to infrequent hospital visits. This creates gaps in continuous disease monitoring and can delay the timely adjustment of treatment plans.  

To address this challenge, researchers have explored remote telemonitoring systems that capture patients’ voice samples in their own homes. Such systems provide frequent, low-cost, and non-invasive monitoring of speech-related symptoms. These systems provide the opportunity to be able to technically assess information on the different *subgroups of patients with similar vocal biomarkers*, *distinct trajectories of disease progression*, *natural groupings of voice recordings that reflect different stages of motor impairment*, etc.  

By identifying these clusters, researchers and clinicians can gain deeper insight into how Parkinson’s manifests across individuals. This may enable personalized treatment strategies, earlier identification of patients at risk of rapid progression, and the development of non-invasive voice-based monitoring tools that complement traditional clinical assessments.  
## 📝 Problem Statement
Parkinson’s disease (PD) progression is typically assessed using the Unified Parkinson’s Disease Rating Scale (UPDRS) during periodic clinical visits. However, these assessments are limited in frequency and often fail to capture the day-to-day fluctuations in patients’ symptoms. Voice impairment is one of the earliest and most consistent symptoms of PD, yet it remains underutilized in clinical monitoring due to the absence of scalable, objective assessment methods.  
Since existing studies primarily focus on predicting UPDRS scores using supervised models, there is a critical gap in understanding whether natural groupings exist among patients or recordings that could represent distinct phenotypes of voice impairment and disease progression. Without such insights, clinicians risk treating PD as a homogeneous condition, overlooking patient subgroups that may require tailored interventions.  
## 🎯 Primary Objective
To identify clinically meaningful subgroups of Parkinson's patients based on various biomedical voice features, with the aim of developing a non-invasive, voice-based stratification system that can enhance clinical decision-making and reduce reliance on infrequent hospital assessments by at least 25%.  

## 📅 Data Description
This dataset contains longitudinal biomedical voice measurements collected from 42 individuals with early-stage Parkinson’s disease over a six-month clinical trial. Participants were monitored remotely using a telemonitoring device that automatically recorded daily or near-daily voice samples in their homes.  
| Variable Name | Type | Description |
|---------------|------|-------------|
| subject# | Integer | Unique identifier for each subject |
| age | Integer | Age of the subject (in years) |
| sex | Binary | Sex of subject (0 = male, 1 = female) |
| test_time | Continuous | Time since recruitment (days) |
| motor_UPDRS | Continuous | Clinician’s motor UPDRS score (interpolated) |
| total_UPDRS | Continuous | Clinician’s total UPDRS score (interpolated) |
| Jitter(%) | Continuous | Variation in fundamental frequency (%) |
| Jitter(Abs) | Continuous | Absolute variation in fundamental frequency |
| Jitter:RAP | Continuous | Relative average perturbation of fundamental frequency |
| Jitter:PPQ5 | Continuous | Five-point period perturbation quotient of fundamental frequency |
| Jitter:DDP | Continuous | Average absolute difference of differences between jitter cycles |
| Shimmer | Continuous | Variation in amplitude |
| Shimmer(dB) | Continuous | Variation in amplitude (decibel scale) |
| Shimmer:APQ3 | Continuous | Three-point amplitude perturbation quotient |
| Shimmer:APQ5 | Continuous | Five-point amplitude perturbation quotient |
| Shimmer:APQ11 | Continuous | Eleven-point amplitude perturbation quotient |
| Shimmer:DDA | Continuous | Average absolute difference of differences between shimmer cycles |
| NHR | Continuous | Noise-to-harmonics ratio |
| HNR | Continuous | Harmonics-to-noise ratio (dB) |
| RPDE | Continuous | Recurrence Period Density Entropy (nonlinear dynamical complexity measure) |
| DFA | Continuous | Detrended Fluctuation Analysis (signal fractal scaling exponent) |
| PPE | Continuous | Pitch Period Entropy (irregularity of pitch variation) |