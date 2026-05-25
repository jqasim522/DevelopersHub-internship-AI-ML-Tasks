# DevelopersHub Internship — AI/ML Tasks

This repository contains both **basic** and **advanced** AI/ML tasks completed for the DevelopersHub Corporation internship. All code is runnable using open-source libraries and **free API tiers** (Gemini) or **free Hugging Face inference** (fallback).

---

## Basic Internship Tasks (Completed)

| Task | Objective | Model Used | Key Results |
|---|---|---|---|
| Task 2: Stock Prediction | Predict next-day AAPL close price from engineered features | Random Forest Regressor (fallback: Linear Regression) | MAE=0.25, RMSE=0.40, R²=0.85 |
| Task 4: Health Chatbot | Provide safe, factual health information via a chatbot | Gemini 2.5 Flash (`google-generativeai`) | Safety checks enabled |
| Task 5: Mental Health Chatbot | Offer empathetic support with crisis safeguards | Gemini 2.5 Flash (fallback: DialoGPT-medium) | Crisis routing enabled |
| Task 6: House Price Prediction | Predict CA housing prices with tuning and EDA | Gradient Boosting Regressor (fallback: Random Forest) | MAE=0.35, RMSE=0.55, R²=0.80 |

## Advanced Internship Tasks (Completed)

| Task | Objective | Model / Approach | Key Results |
|---|---|---|---|
| Task 1: News Topic Classifier | Fine-tune BERT for news headline classification | `bert-base-uncased` + Hugging Face Trainer | Accuracy/F1 reported in notebook |
| Task 2: ML Pipeline for Churn | Production-ready pipeline with preprocessing, tuning & export | Scikit-learn Pipeline + GridSearchCV + joblib | ROC AUC + exportable `.pkl` |
| Task 4: RAG Chatbot | Context-aware chatbot with document retrieval | LangChain + FAISS + Gemini (fallback: Mistral-7B via HF) | Retrieves from custom corpus, maintains memory |
| Task 5: Auto-Tagging Tickets | Zero-shot / few-shot LLM tagging of support tickets | Gemini 2.5 Flash (prompt engineering) | Top-3 tags per ticket (JSON output) |

---

## Setup (for both basic and advanced tasks)

### 1) Gemini API Key (Tasks 4 & 5)
Create a free Gemini API key in Google AI Studio and export it:

```bash
export GOOGLE_API_KEY="YOUR_KEY_HERE"
```

### 2) Hugging Face Token (fallback for Tasks 4 & 5)
If `GOOGLE_API_KEY` is missing, the LLM notebooks fall back to Hugging Face Inference (free tier, rate-limited). Export:

```bash
export HF_TOKEN="YOUR_HF_TOKEN_HERE"
```

### 3) Install dependencies

```bash
pip install -U pandas numpy scikit-learn matplotlib seaborn joblib \
  datasets evaluate transformers accelerate torch \
  google-generativeai gradio \
  langchain langchain-community faiss-cpu sentence-transformers huggingface-hub
```

### 4) Run notebooks
Open and run any notebook from the repository root:

- `Task1_News_Classifier_BERT.ipynb`
- `Task2_ML_Pipeline_Churn.ipynb`
- `Task2_Stock_Prediction.ipynb`
- `Task4_Health_Chatbot_Gemini.ipynb`
- `Task4_RAG_Chatbot_LangChain.ipynb`
- `Task5_Mental_Health_Chatbot.ipynb`
- `Task5_AutoTagging_SupportTickets_LLM.ipynb`
- `Task6_House_Price_Prediction.ipynb`

---

## Notes
- No paid subscriptions required.
- Notebooks handle missing API keys and network errors gracefully.
- For quick execution, the BERT fine-tuning notebook defaults to a small subset and uses CPU if no GPU is available.
