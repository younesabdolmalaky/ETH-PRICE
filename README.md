# Eth-Price

![ethereum-1](https://user-images.githubusercontent.com/75095471/218719850-1dd5166b-1295-49c4-9b6c-878c13524c89.jpeg)

## what is Ethereum?
Ethereum is a decentralized, open-source blockchain with smart contract functionality. Ether (ETH or Ξ) is the native cryptocurrency of the platform. After Bitcoin, it is the largest cryptocurrency by market capitalization. Ethereum is the most actively used blockchain. Ethereum was proposed in 2013 by programmer Vitalik Buterin.
## dataset description
This dataset provides the history of 5min prices of Ethereum. The data starts from 2018-06-01. All the column descriptions are provided. Currency is USD.
### Open :
Price from the first transaction of a 5min candle
### High : 
Maximum price in a 5min candle

### Low : 
Minimum price in a trading 5min candle

### Close : 
Price from the last transaction of a 5min candle

### Volume :
Number of units traded in a 5min candle

## LSTM
LSTM is an artificial recurrent neural network used in deep learning and can process entire sequences of data. Due to the model’s ability to learn long term sequences of observations, LSTM has become a trending approach to time series forecasting.

The emergence and popularity of LSTM has created a lot of buzz around best practices, processes and more. Below we review LSTM and provide guiding principles that PredictHQ’s data science team has learned.

Typically recurrent neural networks (RNN) have short term memory in that they use persistent previous information to be used in the current neural network. Typical recurrent neural networks can experience a loss in information, often referred to as the vanishing gradient problem. This is caused by the repeated use of the recurrent weight matrix in RNN. In an LSTM model, the recurrent weight matrix is replaced by an identify function in the carousel and controlled by a series of gates. The input gate, output gate and forget gate acts like a switch that controls the weights and creates the long term memory function.

## code

### Data Preparation
The first step is to import and clean the data. The data is in a CSV file and is loaded using the pandas library. Any missing data is removed, and the date column is dropped. The data is then transformed using the MinMaxScaler from the scikit-learn library to bring all the variables to the same scale.
The independent variables are the past 30 candles and the dependent variable is the closing price of the 31st candle. The data is then split into training and testing sets using the train_test_split function from the scikit-learn library.
### Model Building
The model is built using the Sequential class from the tensorflow.keras library. It consists of two layers of LSTM with a dropout layer and batch normalization layer in between to prevent overfitting. The final layer is a dense layer with a single output node to predict the closing price. The model is compiled using the Adam optimizer and the mean squared error loss function.
The model is trained using the fit method and the best model is saved using the ModelCheckpoint callback. The final model is then evaluated using the test set.
### Conclusion
This code provides a basic implementation of a time series forecasting model using LSTM. The model can be further optimized and improved by tuning the hyperparameters and adding more layers to the network. Additionally, the code can be extended to predict other financial time series data, such as stock prices.
