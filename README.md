# WordPredict

### ABSTRACT:

We have applied N-gram language modelling with Stupid Backoff algorithm and Recurrent Neural Network LSTM (long-short term memory) model to the Penn Tree Bank dataset which is also known as PTB dataset to perform word prediction. The aim is to determine which algorithm performs best for prediction of words in the N-gram. We implemented N-gram language modelling using a smoothing method called Stupid Backoff which gave average perplexity of just 31 which means the model was just uncertain for 31 alternative predictions. RNN LSTM technique was also used for word prediction using word embedding layers which gave categorical accuracy of 21.76% for 40 epochs. Generally, RNN LSTM outperforms for word prediction when trained for more than 40 epochs but we found that the Stupid Backoff method gives better prediction even for complex data sets and an advantage of being computationally less expensive.

### DATA DESCRIPTION:

Penn Treebank Corpus:
1. ptb.tgz: Zipped file containing full train, test and valid data.
2. ptb.train.txt / ptb.txt: training data set
3. ptb.valid.txt: development set (should be used just for tuning hyper-parameters, but not for training)
4. ptb.test.txt: test set for reporting entropy and perplexity as model evaluation
    
Note: ptb.tgz and ptb.train.txt / ptb.txt dataset is very large and takes longer to be run on local machine. Import the datasets and run the Jupyter Notebooks on Google Collaboratory or GCP for faster implementation. RNN LSTM model took over 4hrs to train 40 epochs on Google Collaboratory.

### ALGORITHMS USED:

N-gram language modelling with Stupid Backoff smoothing technique and Recurrent Neural Network with bi-directional Long Short-Term Memory are the 2 main algorithms used for word prediction. Since predicting a word is a stochastic process and requires memory of words present in the text corpus, these 2 techniques are proven to be best to give better predictions.

### CONCLUSION/RESULT:

On applying the technique of Stupid Backoff, we got average perplexity of around 31 which means the model was just uncertain for 31 alternative predictions. On training the RNN LSTM model for 40 epochs, we get the categorical accuracy to be around 21% on the validation set. But, if LSTM models are trained for over 100 epochs, it outperforms in terms of its prediction. However, if the aim is to predict word with very less computation expense, then Stupid Backoff is the best method which gives good prediction for even a large textual corpus.


### RUN APPLICATION

```git clone <repo>```

```pip install -r requirements.txt```

```python manaye.py runserver```

Visit 127.0.0.1:8000
