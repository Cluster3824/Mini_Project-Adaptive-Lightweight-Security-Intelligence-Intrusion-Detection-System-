# NexusGuard AI

AI-based cloud security system with 10 specialized detection modules, a real-time dashboard, REST API, and automated response engine.

## Features
1. **DDoS Detector**: Isolation Forest based anomaly detection.
2. **IDS Engine**: BiLSTM intrusion detection on sequence sessions.
3. **Zero Trust Scorer**: LightGBM 7-factor trust scorer.
4. **SIEM Log Analyzer**: BERT-tiny NLP multi-stage attack correlation.
5. **Threat Intel**: IOC matching.
6. **Exfiltration Detector**: TCN cumulative data movement monitor.
7. **Vulnerability Manager**: XGBoost CVE prioritization.
8. **Deception System**: Honeypot simulator and TTP logger.
9. **Microsegmentation Firewall**: Connection behavior mapping.
10. **Compliance Checker**: Rule-based index for GDPR/HIPAA/SOC2.

## Setup Instructions
1. **Clone the repository.**
2. **Create virtual environment:** `python -m venv venv && source venv/bin/activate`
3. **Install dependencies:** `pip install -r requirements.txt`
4. **Download datasets (optional):** Place raw datasets (CICIDS2017) in `data/raw/`
5. **Run preprocessing:** `python scripts/preprocess.py`
6. **Train Models:** `python train/train_ddos.py`, etc.
7. **Start the API server:** `uvicorn main:app --reload`
8. **Start Dashboard:** `streamlit run dashboard/app.py`

*(If models are not trained yet, the system runs with rule-based fallbacks by setting `DEMO_MODE=True` in `config.py`)*

## Testing
- Unit tests: `pytest tests/unit/`
- Attack Simulation CLI: `python tests/simulate_attack.py --type all`
- Benchmark Inference Latency: `python tests/benchmark.py`

## Docker
- `docker-compose up -d` to start Redis and the NexusGuard API.
# Mini_Project-Adaptive-Lightweight-Security-Intelligence-Intrusion-Detection-System-
# Mini_Project-Adaptive-Lightweight-Security-Intelligence-Intrusion-Detection-System-
# Mini_Project-Adaptive-Lightweight-Security-Intelligence-Intrusion-Detection-System-
