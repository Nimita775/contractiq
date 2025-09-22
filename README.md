# 📝 ContractIQ – Generative AI Contract Analysis (Mock Demo)

A proof-of-concept showing how **BigQuery Generative AI**–style contract analytics can be built **without Google Cloud** using open-source tools and mock data.  
This repo contains the code and outputs submitted for the **Bolt Hackathon – BigQuery Generative AI Challenge**.

---

## 📂 Repository Contents
| File | Description |
|------|------------|
| `ContractIQ_demo.ipynb` | Kaggle notebook with the full simulation workflow |
| `mock_contracts.csv` | Raw mock contract text |
| `mock_summaries.csv` | AI-generated one-paragraph contract summaries |
| `mock_clauses.csv` | Clause breakdown with clause types & risk tags |
| `mock_risk_scores.csv` | Numeric risk scores (1–10) for each contract |

---

## 🚀 Project Overview
**Goal:** Provide instant contract summaries, identify key clauses, and assign risk scores—mimicking BigQuery’s `AI.GENERATE_*` functions.

### Key Steps
1. **Data Simulation**  
   Created a `mock_contracts.csv` dataset representing four sample contracts.

2. **Generative AI Processing**  
   Used the Hugging Face `transformers` pipeline with a lightweight model  
   (`tiiuae/falcon-7b-instruct`) to:
   * Generate concise summaries  
   * Extract clauses & risk tags  
   * Assign a numeric risk score (1–10)

3. **Output Export**  
   All generated outputs saved as CSVs, mirroring what a real BigQuery pipeline would return.

---

## 🛠️ Tech Stack
- **Python** (Pandas, Regex, Hugging Face Transformers)
- **Kaggle Notebook** (no paid cloud required)
- **Local LLM**: `tiiuae/falcon-7b-instruct` for offline text generation

---

## 📊 Example Output

| contract_id | risk_score | summary (truncated) |
|-------------|-----------|---------------------|
| C001 | 8 | Company A delivers 100 units ... |
| C002 | 6 | Company B pays \$50,000 upon ... |
| C003 | 8 | Confidentiality and data ... |
| C004 | 5 | Company D compensates vendor ... |

---

## ▶️ Reproduce the Demo
1. **Open on Kaggle**  
  [ContractIQ Demo Notebook](https://www.kaggle.com/code/nimitagurjar/contractiq-generative-ai-contract-summarizer)

2. **Install dependencies**  
   ```bash
   pip install transformers pandas
