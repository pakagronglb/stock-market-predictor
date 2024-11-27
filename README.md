![image](https://github.com/user-attachments/assets/52b19cb0-fae0-45f5-95b2-b5b9e1fa4324)# 📈 Stock Market Predictor 📊

Welcome to the **Stock Market Predictor**! This project leverages historical S&P 500 data and machine learning to predict stock market movements. Whether you're exploring financial trends or diving into data science, this project serves as a great introduction to stock market analysis with Python. 

---

## 🚀 Features

- **Historical Data Analysis**: Fetches and processes S&P 500 historical data from 1927 to the present using `yfinance`.  
- **Visualization**: Visualizes stock price trends with line plots.  
- **Target Prediction**: Predicts whether the market will close higher or lower the next day.  
- **Machine Learning**: Implements a `RandomForestClassifier` for predictions.  
- **Backtesting**: Evaluates model performance using historical data.  
- **Feature Engineering**: Incorporates rolling averages and trends for better predictions.

---

## 🛠 Installation

1. Clone this repository:  
   ```bash
   git clone https://github.com/pakagronglb/stock-market-predictor.git
   cd stock-market-predictor
   ```
2. Install dependencies:  
   ```bash
   pip install -r requirements.txt
   ```

---

## 📚 How It Works

1. **Data Loading**:  
   Fetch historical S&P 500 data using `yfinance`:
   ```python
   import yfinance as yf
   sp500 = yf.Ticker("^GSPC").history(period="max")
   ```

2. **Feature Engineering**:  
   - Add rolling averages for different time horizons.  
   - Create target labels (`1` for market up and `0` for market down).  

3. **Model Training**:  
   Train a `RandomForestClassifier` with key predictors: `Close`, `Volume`, `Open`, `High`, and `Low`.

4. **Backtesting**:  
   Evaluate the model over historical periods to calculate precision.

---

## 📊 Performance

- **Precision Score**: `54.46%`  
  The model correctly predicts market direction slightly better than random guessing.  
- **Predictions Distribution**:  
  - `1` (Up) Predictions: 1030  
  - `0` (Down) Predictions: 5263  

---

## 🔑 Key Functions

- **`predict(train, test, predictors, model)`**  
  Trains the model and predicts outcomes for the test dataset.  

- **`backtest(data, model, predictors, start, step)`**  
  Simulates historical predictions and evaluates performance.

---

## 🖼 Example Plots

- **Market Trend Visualization**  
  ![Market Trend Line Plot](https://github.com/user-attachments/assets/4447739a-629f-465b-967e-5064a3783ab7)

- **Prediction vs Target**  
  ![Prediction vs Actual](https://github.com/user-attachments/assets/1b741510-b4c4-44d5-ae97-a4f6f5d4c4b5)

---

## 🔍 Future Improvements

- Use more advanced models like `XGBoost` or `LSTM` for time-series predictions.  
- Incorporate sentiment analysis from financial news.  
- Add more sophisticated features, such as volatility and sector performance.

---

## 🏗 Built With

- Python 🐍  
- Pandas 🐼  
- scikit-learn 🤖  
- yfinance 📉  
- Matplotlib 📊  

---

Feel free to contribute or raise issues! 🌟  

Happy Predicting! 🚀
