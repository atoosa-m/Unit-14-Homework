# Unit-14-Homework
## LSTM Stock Predictor  
![deep-learning](https://user-images.githubusercontent.com/93611442/162126549-f699f374-b204-465d-ab26-6b16260cef65.jpg)
## Background  
Due to the volatility of cryptocurrency speculation, investors will often try to incorporate sentiment from social media and news articles to help guide their trading strategies. One such indicator is the [Crypto Fear and Greed Index (FNG)](https://alternative.me/crypto/fear-and-greed-index/) which attempts to use a variety of data sources to produce a daily FNG value for cryptocurrency. I have been asked to help build and evaluate deep learning models using both the FNG values and simple closing prices to determine if the FNG indicator provides a better signal for cryptocurrencies than the normal closing price data.

In this assignment, I used deep learning recurrent neural networks to model bitcoin closing prices. One model has used the FNG indicators to predict the closing price while the second model has used a window of closing prices to predict the nth closing price.  

In order to complete this assignment I had to prepare the data for training and testing, build and train custom LSTM RNNs and evaluate the performance of each model.  

## About LSTM Models  
The Long Short-Term Memory network or LSTM network is a type of recurrent neural network used in deep learning because very large architectures can be successfully trained. LSTMs are very powerful in sequence prediction problems because they’re able to store past information. This is important in our case because the previous price of Bitcoin is crucial in predicting its future price.  

## Evaluation Summary  
### LSTM Model - Using Closing Prices  
![LSTM_Predictor_Using_Closing_Prices](https://user-images.githubusercontent.com/93611442/162342342-57c2b35a-8a15-45f5-922b-40df7e4e3f2d.jpg)  

### LSTM Model - Using Crypto Fear and Greed Index (FNG)  
![LSTM_Predictor_Using_FNG_Index](https://user-images.githubusercontent.com/93611442/162653861-6257dda0-a438-4759-82e6-25105d937bbd.jpg)

Comparing the two models built in this assignment, we can see that the LSTM model that used the simple closing prices has a lower loss and is able to track the actual values better over time. I also experimented with different window sizes (between 1 to 10) and based on the model performance changes concluded that the lower the window size the better the model performance and the lower the loss. Therefore the window size of 1 day is the one that works best for our model. 


#### Resources

[Keras Sequential Model Guide](https://keras.io/getting-started/sequential-model-guide/)  
[Illustrated Guide to LSTMs](https://towardsdatascience.com/illustrated-guide-to-lstms-and-gru-s-a-step-by-step-explanation-44e9eb85bf21)  
[Stanford's RNN Cheatsheet](https://stanford.edu/~shervine/teaching/cs-230/cheatsheet-recurrent-neural-networks)  
*Time Series Prediction with LSTM Recurrent Neural Networks in Python with Keras by Jason Brownlee on July 21, 2016*  

