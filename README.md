# Stock Price Prediction using RNNs (LSTM & GRU)

This project demonstrates the application of Recurrent Neural Networks (RNNs) for time-series forecasting. It compares the performance of two popular RNN architectures, **LSTM (Long Short-Term Memory)** and **GRU (Gated Recurrent Unit)**, in predicting the stock price of IBM.

The models are built using Keras and TensorFlow, and the project includes data preprocessing, model training, and performance evaluation.

## 🚀 Project Overview

The notebook `Stock_Price_Prediction_LSTM_GRU.ipynb` covers the complete end-to-end workflow:

1.  **Data Loading & Preprocessing:**
    * Loads the `IBM_2006-01-01_to_2018-01-01.csv` dataset.
    * Visualizes the training and test splits over time.
    * Applies `MinMaxScaler` to normalize the "High" stock price for model stability.

2.  **Time-Series Data Structuring:**
    * Transforms the sequential data into a supervised learning format by creating sequences of 60 timesteps (e.g., using 60 days of data to predict the 61st day).

3.  **Model Architecture & Training:**
    * **Model 1: LSTM:** A stacked LSTM network with Dropout layers to prevent overfitting.
    * **Model 2: GRU:** A stacked GRU network with a similar architecture for a direct performance comparison.

4.  **Evaluation & Visualization:**
    * The models are trained and then evaluated on the test set (data from 2017 onwards).
    * Predictions are inverse-transformed back to their original dollar value.
    * The results are visualized in a plot comparing the "Real IBM Stock Price" vs. the "Predicted IBM Stock Price".
    * Performance is quantified using **Root Mean Squared Error (RMSE)**.

---

## 🛠️ Setup and Installation

1.  **Clone the Repository**
    ```bash
    git clone [https://github.com/your-username/RNN-Time-Series-Forecasting.git](https://github.com/your-username/RNN-Time-Series-Forecasting.git)
    cd RNN-Time-Series-Forecasting
    ```

2.  **Create a Virtual Environment** (Recommended)
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3.  **Install Required Libraries**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Launch Jupyter**
    ```bash
    jupyter notebook
    ```
    Open the `Stock_Price_Prediction_LSTM_GRU.ipynb` notebook to run the project.

---

## 📊 Dataset

* **IBM Stock Price (2006-2018):** A CSV file containing daily IBM stock data. The model is trained on data up to 2016 and tested on data from 2017-2018. This file is included in the `/data` directory.
