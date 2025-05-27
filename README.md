📈 Next-Day Stock Price Prediction using Random Forest
This project predicts the next-day closing price of a stock using historical data and a Random Forest Regressor. The model is trained on technical features such as Open, High, Low, Close, Volume, and a 5-day moving average.

📂 Dataset
Format: CSV file (individual stock data from the NIFTY 50 dataset)

Required Columns: Date, Open, High, Low, Close, Volume

Source: Nifty50 Stock Market Data on Kaggle

🛠️ Setup & Usage (Google Colab)
Open this project in Google Colab.

Run the first cell to upload a single CSV stock file from the NIFTY50 dataset.

The model will preprocess the data, train a Random Forest Regressor, and evaluate it.

🔍 Project Workflow
1. Import Libraries
Essential Python libraries like pandas, numpy, matplotlib, and scikit-learn are imported for data handling, model training, and evaluation.

2. Upload CSV File
A single CSV file is uploaded using Google Colab's files.upload() function. The file should contain daily stock data.

3. Preprocessing
Converts Date to datetime and sorts chronologically.

Creates a new target column Next_Close, which is the close price shifted by one day.

Calculates a 5-day moving average (5day_MA) of the close price as an additional feature.

Drops any rows with missing values.

4. Feature Selection
The following features are used to train the model:

Open

High

Low

Close

Volume

5day_MA (5-day moving average of the Close price)

Target variable: Next_Close

5. Model Training
A Random Forest Regressor with 100 estimators is trained on 80% of the data. The remaining 20% is used for testing.

6. Evaluation Metrics
MAE (Mean Absolute Error): Measures average magnitude of errors.

RMSE (Root Mean Squared Error): Penalizes large errors more than MAE.

R² Score: Represents the proportion of variance in the target variable explained by the model.

7. Visualization
The actual vs predicted next-day closing prices are plotted to visualize the model's prediction quality.

📊 Example Output (RELIANCE.NS)
mathematica
Copy
Edit
📊 Model Evaluation (Random Forest):
MAE   (Mean Absolute Error)       : 10.35
RMSE  (Root Mean Squared Error)   : 14.28
✅ Model Accuracy (R² Score)       : 92.67%
🚀 Future Improvements
Include more technical indicators (e.g., RSI, MACD).

Use models like LSTM or XGBoost for time series modeling.

Tune hyperparameters for better performance.

📄 License
This project is for educational purposes and is open to modification and experimentation.
