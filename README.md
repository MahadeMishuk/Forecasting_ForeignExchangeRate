# **Forecasting of Foreign Exchange Rate (USD/x)**
Mahade Mishuk


https://github.com/user-attachments/assets/63a5ebd6-ef34-45cf-bf49-3faf56ad7448




**1. Introduction**

Predicting foreign exchange (FX) rates is crucial for various stakeholders, including businesses, financial institutions, and individual traders, as it helps with risk management, investment decisions, and market forecasting. Accurate FX predictions can mitigate risks associated with volatile currency markets, especially in a global economy. The goal of this project is to develop a machine learning (ML) model that can predict future exchange rates with high accuracy, allowing for both short-term and long-term forecasting. The predictions are based on historical data provided by the European Central Bank (ECB).

**2. Data Description**

The dataset used in this project is sourced from www.humdata.org, which contains daily foreign exchange rates against the USD (USD/x) from January 4th, 1999, to the present day.

- Date: The first column represents the date.
- Exchange Rates: The remaining columns represent the exchange rates of various currencies relative to USD. Each number indicates how much 1 USD is worth in terms of another currency.
- Missing Data: Several cells have 0.0 values, either due to missing data or currencies not being available on that date.

  Data Preparation
  
  - To handle missing data, any row containing a 0.0 value was treated by: Forward-filling: Missing exchange rates were filled with the most recent available rate.

**3. Feature Engineering**

- Lagged Features: For Random Forest have been added exchange rates from the previous day as features.

**5. Model Selection and Methodology**

Models Implemented:

Prophet: A deep learning time series forecasting model that handles trends and seasonality. It’s robust to missing data and handles holidays well.

LSTM (Long Short-Term Memory): A deep learning model that is effective for time series predictions, particularly with long-range dependencies.

Random Forest: A machine learning model that excels in capturing simple relationships between features but may not perform as well on highly complex patterns.

**6. Model Evaluation**

The following evaluation metrics were used:

Mean Squared Error (MSE)

Mean Absolute Error (MAE)

Root Mean Squared Error (RMSE)

**7. Future Improvements:**

Ensemble Learning: Combining LSTM and Prophet models to leverage their respective strengths might improve overall accuracy.

Additional Features: Incorporating economic indicators such as interest rates, inflation, and stock indices could further enhance prediction performance.

More Data: Using a larger dataset or different sources (e.g., including more currencies) could improve model robustness.
<img width="1242" alt="Screenshot 2024-10-08 at 12 09 38 AM" src="https://github.com/user-attachments/assets/2623d257-96eb-43ed-84ea-583177eb0c30">

**9. References**

European Central Bank FX Rates

Various Python libraries used, including TensorFlow, Prophet, and Scikit-learn.
