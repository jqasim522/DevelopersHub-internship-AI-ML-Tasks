# DevelopersHub Internship — AI/ML Tasks

| Task | Objective | Model Used | Key Results |
|---|---|---|---|
| Task 2: Stock Prediction | Predict next-day AAPL close price from engineered features | Random Forest Regressor (fallback: Linear Regression) | MAE=0.25, RMSE=0.40, R²=0.85 |
| Task 4: Health Chatbot | Provide safe, factual health information via a chatbot | Gemini 2.5 Flash (google-generativeai) | Safety checks enabled |
| Task 5: Mental Health Chatbot | Offer empathetic support with crisis safeguards | Gemini 2.5 Flash (fallback: DialoGPT-medium) | Crisis routing enabled |
| Task 6: House Price Prediction | Predict CA housing prices with tuning and EDA | Gradient Boosting Regressor (fallback: Random Forest) | MAE=0.35, RMSE=0.55, R²=0.80 |

## Setup

1) Create a free Gemini API key in Google AI Studio.

2) Export the key as an environment variable:

```bash
export GOOGLE_API_KEY="YOUR_KEY_HERE"
```

3) Install dependencies:

```bash
pip install yfinance pandas numpy scikit-learn matplotlib seaborn google-generativeai gradio
```

4) Open and run the notebooks:

- `Task2_Stock_Prediction.ipynb`
- `Task4_Health_Chatbot_Gemini.ipynb`
- `Task5_Mental_Health_Chatbot.ipynb`
- `Task6_House_Price_Prediction.ipynb`
