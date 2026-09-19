# network-attack-forecasting
AI-based network attack forecasting using Random Forest to classify traffic as Benign or Attack, with a Streamlit dashboard for risk scoring.
# ShieldNet — AI-Based Network Attack Forecasting

An AI-powered system that analyzes network traffic flow data and classifies it as **Benign** or **Attack** in real time, giving security teams an early-warning risk score before threats escalate.

Built for HackDevengers 2.0 (24-hour hackathon).

## Problem Statement
Modern networks generate massive volumes of traffic every second, making manual attack detection difficult and slow. Traditional security systems often flag threats only after damage has occurred. This project aims to provide a lightweight, AI-driven early-warning system that flags suspicious traffic before it escalates.

## How It Works
1. Network flow data (CICIDS2017 dataset, 78 features) is cleaned and preprocessed
2. A Random Forest Classifier is trained to distinguish Benign vs Attack traffic
3. A Streamlit dashboard lets users upload traffic CSVs and instantly view:
   - Predictions (Benign / Attack)
   - Risk score (0–100%)
   - Risk level (Low / Medium / High)
   - Summary metrics (total records, attacks detected, benign traffic)

## Tech Stack
- Python
- Pandas
- Scikit-learn (Random Forest Classifier)
- Streamlit
- Joblib

## How to Run
