README
Stock Price Prediction Model Using LSTM
Overview
This project aims to predict future stock prices using historical data of Google's stock prices (GOOG). We use a Long Short-Term Memory (LSTM) neural network, a type of recurrent neural network (RNN), particularly suited for time series prediction.

Dataset
The dataset used in this project is GOOG.csv, which contains historical stock prices of Google. For this model, we specifically utilize the 'Date' and 'Close' columns.

Data Preprocessing
The dataset is preprocessed as follows:

Loading the Data: The dataset is read using pandas and filtered to retain only the 'Date' and 'Close' columns.
Index Conversion: The 'Date' column is converted to datetime format and set as the index.
Sliding Window Approach: We implement a function window_df to create a sliding window of size n (in this case, 3). Each window consists of the stock prices for n days and the target value for the next day.
Splitting Data: The data is split into training (80%), validation (10%), and test (10%) sets.
Model Architecture
The model is built using TensorFlow and Keras with the following architecture:

Input Layer: Takes input shape (3, 1), representing 3 days of stock prices.
LSTM Layer: Contains 64 units.
Dense Layers: Two Dense layers with 32 units each and ReLU activation.
Output Layer: A single unit to predict the stock price.
Compilation and Training
The model is compiled using the Mean Squared Error (MSE) loss function and the Adam optimizer with a learning rate of 0.001. The training is performed over 100 epochs.

Visualization
The stock prices are plotted to visualize the training, validation, and test sets.

Instructions to Run
Install Dependencies:

bash
Copy code
pip install pandas matplotlib numpy tensorflow
Load Data:
Ensure GOOG.csv is in the project directory.

Run the Script:
Execute the script to preprocess the data, build, train, and evaluate the model.
