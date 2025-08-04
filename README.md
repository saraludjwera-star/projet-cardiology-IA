# projet-cardiology-IA
# Intelligent Diagnosis of Heart Failure

Final project for the Building AI course

## Summary

An AI-based tool to assist doctors in diagnosing, stratifying risk, recommending treatment, and following up heart failure patients in low-resource settings.

## Background

Heart failure is a frequent and serious condition, often diagnosed too late in low-resource countries. Health professionals lack adapted decision-support tools, which leads to delayed care, avoidable complications, and high mortality.

My motivation comes from my experience as a physician in Africa, where I saw these challenges firsthand.

This project aims to:
* Support early diagnosis and risk stratification
* Detect silent high-risk profiles without obvious symptoms
* Recommend initial treatment and personalized follow-up
* Gradually integrate telemedicine for remote care

## How is it used?

The user (doctor or health professional) inputs clinical, biological, and ECG data through a simple interface.

The AI system provides:
- a predicted diagnosis,
- risk stratification,
- prognosis estimation,
- an initial treatment proposal (or referral recommendation),
- a personalized follow-up plan.

The tool is designed for health workers in rural or semi-urban areas without easy access to a specialist. It will work on a computer or tablet, even with limited internet connectivity.

## Data sources and AI methods

Input data:
- Clinical data (age, sex, history, symptoms)
- Biological data (creatinine, BNP, etc.)
- ECG features (QRS duration, T wave, heart rate, anomalies...)

AI techniques:
- **Model 1: MFNN (Multi-layer Feedforward Neural Network)**  
   - Input: clinical, biological, and ECG data  
   - Output: diagnosis, risk stratification, prognosis  
   - Technique: supervised learning  

- **Model 2: Therapeutic supervised model**  
   - Input: output of MFNN (dx, risk, prognosis)  
   - Output: recommended treatment (e.g., medication, refer) and follow-up plan  

- **Unsupervised phase (future)**  
   - Goal: identify silent high-risk profiles through clustering  
   - To be added in the future

- **Telemedicine (future)**  
   - Will use reinforcement learning or unsupervised insights for personalized dynamic follow-up and alerts

Tools and libraries:
- Python
- scikit-learn
- XGBoost
- TensorFlow

## Challenges

This project does **not** replace medical expertise. It heavily depends on the quality of input data.

Limitations and considerations:
- Requires clinical validation before deployment
- Needs to be culturally adapted and multilingual
- Doesn’t handle complex comorbidities (e.g., renal failure, diabetes) yet
- Access to real local datasets may be challenging

## What next?

- Build a prototype using simulated or open-access data
- Get access to a real-world database (first in Japan, then Africa)
- Train and validate both the diagnostic and therapeutic models
- Develop the telemonitoring module
- Launch a pilot phase in a hospital in the DRC

## Acknowledgments

* Building AI course by the University of Helsinki and Reaktor
* Open-source tools: scikit-learn, TensorFlow, XGBoost
* Inspired by real medical challenges in under-resourced areas
* Thanks to all researchers and doctors supporting AI for global health equity
