# 📝 ContractIQ — Instant Contract Summaries & Risk Scanner

**Hackathon Proof-of-Concept: BigQuery Generative AI Simulation using Kaggle Notebook**

---

## **Project Overview**

Enterprises and legal teams often review **thousands of contracts** (NDAs, SOWs, vendor agreements). Manual review is **slow, error-prone, and costly**.  

**ContractIQ** automates contract review by:

- Generating **plain-English summaries** of contracts  
- Extracting **clauses with risk tags**  
- Assigning **numeric risk scores** (1–10)  
- Providing **interactive visualizations** for quick analysis  

This notebook demonstrates the **end-to-end workflow** entirely offline using mock data and a local LLM.

---

## **Problem Statement**

Legal teams spend hours or days triaging contracts manually. High-risk clauses can be **overlooked**, delaying deal approvals. ContractIQ **reduces triage time to seconds**, enabling faster deal reviews and automated red-flag alerts.

---

## **Impact**

- **Faster contract analysis** — seconds vs hours/days  
- **Automated red-flag detection** for high-risk clauses  
- **Measurable cost reduction** for legal teams  
- **Visual & interactive outputs** for stakeholders

---

## **Dataset**

- **Mock contracts dataset** (`mock_contracts.csv`) simulates real-world contracts:  
  - `contract_id` – Unique ID  
  - `raw_text` – Contract content  

- **Outputs**:  
  - `mock_summaries.csv` – One-paragraph contract summaries  
  - `mock_clauses.csv` – Extracted clauses with risk levels  
  - `mock_risk_scores.csv` – Overall numeric risk score per contract  

---

## **High-Level Architecture & Workflow**

### **Data Flow**

[Raw Contracts (PDFs/CSV)]
│
▼
[Pre-processing: OCR / Parsing]
│
▼
[Mock Contract Table (contract_id, raw_text)]
│
▼
[Generative AI Simulation (Local LLM)]
├─ Contract Summaries (text)
├─ Clause Extraction & Risk Tags (table)
└─ Contract Risk Scores (numeric)
│
▼
[Visualizations / CSV Export / Dashboard]

## ▶️ Reproduce the Demo
1. **Open on Kaggle**  
  [ContractIQ Demo Notebook](https://www.kaggle.com/code/nimitagurjar/contractiq-generative-ai-contract-summarizer)

2. **Install dependencies**  
   ```bash
   pip install transformers pandas
