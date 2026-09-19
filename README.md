<img width="1916" height="877" alt="Screenshot 2026-09-19 192630" src="https://github.com/user-attachments/assets/68741861-d012-4190-9f36-6816fae2d4db" />
<img width="1902" height="953" alt="Screenshot 2026-09-19 192606" src="https://github.com/user-attachments/assets/964287eb-2827-43e7-8344-2fe9f674bc59" />
<img width="1916" height="1002" alt="Screenshot 2026-09-19 192529" src="https://github.com/user-attachments/assets/13b57997-e6f8-4af1-ba8b-0dba3fa6b992" />
<img width="1905" height="1013" alt="Screenshot 2026-09-19 192510" src="https://github.com/user-attachments/assets/a9aa525a-5a4f-496b-833a-215ba40e69ae" />
<img width="1917" height="1012" alt="Screenshot 2026-09-19 192447" src="https://github.com/user-attachments/assets/4e2a449a-224a-426f-b14c-e0198769a4e5" />
<img width="527" height="555" alt="Screenshot 2026-09-19 192425" src="https://github.com/user-attachments/assets/e48a1c3e-4248-4719-8cf9-87337f9935ee" />
# Network-attack-forecasting
# ShieldNet — AI-Based Network Attack Forecasting

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
