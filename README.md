# Eth-Price
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

