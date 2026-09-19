# network-attack-forecasting
ShieldNet — AI-Based Network Attack Forecasting

What it does:
- Analyzes network traffic flow data
- Classifies traffic as Benign or Attack in real time
- Gives an early-warning risk score before threats escalate
- Built for HackDevengers 2.0 (24-hour hackathon)

Problem it solves:
- Networks generate huge traffic volumes every second
- Manual attack detection is slow and difficult
- Traditional security systems often catch attacks too late
- This project flags suspicious traffic before it causes damage

How it works:
- Trained on the CICIDS2017 dataset (78 network flow features)
- Uses a Random Forest Classifier to detect attack patterns
- Streamlit dashboard lets users upload traffic CSVs
- Instantly shows predictions, risk score (0–100%), and risk level (Low/Medium/High)

Tech stack:
- Python
- Pandas
- Scikit-learn (Random Forest Classifier)
- Streamlit
- Joblib

How to run:
1. Install libraries: pip install pandas scikit-learn streamlit joblib
2. Train the model: python train_model.py
3. Launch dashboard: python -m streamlit run app.py
4. Open the link shown in terminal and upload a CSV file

Project files:
- train_model.py — trains and saves the ML model
- app.py — Streamlit dashboard
- data/CICIDS2017_sample_km.csv — training dataset
- network_attack_model.pkl — saved trained model

note:
- We found and fixed a data leakage bug during development (model was accidentally trained using the label column itself)
- After the fix, the model was retrained correctly for real-world accuracy
