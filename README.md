# 🧠 FinFluent – An AI-Powered Personalized Financial Advisor

**FinFluent** is a personalized financial advisor built using a multi-agent architecture powered by LLaMA 3.1. It provides dynamic and explainable financial guidance on budgeting, anomaly detection, stock sentiment, and portfolio analysis — all while prioritizing privacy and contextual reasoning.

---

## 🚀 Features

- **Multi-Agent LLM Framework**
  - 🧾 **Budget Agent** – SARIMA-based expense forecasting.
  - ⚠️ **Anomaly Agent** – Isolation Forest to flag irregular transactions.
  - 📈 **Stock Agent** – Combines price data with sentiment from financial news.
  - 📊 **Portfolio Agent** – Analyzes diversification, risk, and sentiment.

- **Realistic Synthetic Dataset**
  - Simulates 5 years of monthly transactions with seasonal trends and outlier injection.
  - Includes seasonlity, real-world factors such as - Inflation, Salary hike, Relocation among others.

- **Dual Interfaces**
  - 💻 **CLI**: Lightweight chat-based terminal interface.
  - 🌐 **Streamlit**: Web UI with conversational financial advising.

- **Security-First Design**
  - AES-based **Fernet encryption** for all uploaded user files.
  - **Local LLM (LLaMA 3.1)** deployment to ensure full data privacy.

---


## 📁 Project Structure

```plaintext
FinFluent/
├── cli/                     # Terminal-based interaction
├── streamlit_ui/           # Streamlit chatbot UI
├── agents/
│   ├── budget_agent.py
│   ├── anomaly_agent.py
│   ├── stock_agent.py
│   └── portfolio_agent.py
├── data/
│   ├── synthetic_data_gen.py
│   └── sample_portfolio.csv
├── llm_controller.py       # Master agent (LLM-based)
├── encryption_utils.py     # File encryption logic
├── requirements.txt
└── README.md
```

---

## 🛠 Tech Stack

- **Python**, **pandas**, **scikit-learn**, **Streamlit**
- **APIs**: Twelve Data, AlphaVantage
- **ML Models**: SARIMA, Isolation Forest
- **LLM**: LLaMA 3.1 (using Ollama)
- **Security**: Fernet encryption from `cryptography`

---

## 📈 Evaluation Metrics

| Task               | Score / Accuracy                      |
|--------------------|----------------------------------------|
| Budget Forecasting | MAPE (Utilities): 12.39%               |
| Anomaly Detection  | Accuracy: 96.4%, F1 Score: 94.6%       |
| LLM Evaluation     | BLEU: 0.286, ROUGE-1: 0.55 (LLaMA 3)   |

---

## 🔐 Privacy First

- All uploads encrypted with **Fernet**; decrypted only at runtime.
- Each sub-agent unlocks data -> uses data for ML models -> deletes the files -> stores aggeregate information from ML models.
- LLMs **never access raw data** – only aggregate summaries.
- **User files are deleted** post-processing to ensure zero data retention.

---

## 👥 Contributors

- **Amit Karanth Gurpur** 
- **Vidya Kalyandurg** 
- **Suraj Patel Muthe Gowda** 
- **Akshata Kumble** 
---

## 📄 Citation & Links

🔗 GitHub Repo: [https://github.com/amitkaranth/FinFluent](https://github.com/amitkaranth/FinFluent)

---

## 🔮 Roadmap

- ✅ Asynchronous agent execution with Celery / asyncio
- ✅ Support for real bank APIs and real-world datasets
- 🔄 Switchable LLMs (GPT-4, Claude 3)
- 🔐 Fernet-secured user-file encryption

---

> _"Empowering financial literacy through explainable AI."_

