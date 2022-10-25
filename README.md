

(https://github.com/likemycode/codemix/blob/main/Selfnet.pdf)

### Requirements
  Python 3.6 or higher <br>
  Pytorch >= 1.3.0 <br>
  Pytorch_transformers (also known as transformers) <br>
  Pandas, Numpy, Pickle <br>
  Fasttext  <br>

### Dataset
sarcasm dataset for Hinglish language to facilitate further research on code-mix NLP. 

 create a dataset using TweetScraper built on top of scrapy to extract code-mix hindi-english tweets. We pass search tags like #sarcasm, #humor, #bollywood, #cricket, etc., combined with most commonly used code-mix Hindi words as query. All the tweets with hashtags like #sarcasm, #sarcastic, #irony, #humor etc. are treated as positive. Non sarcastic tweets are extracted using general hashtags like #politics, #food, #movie, etc. The balanced dataset comprises of 166K tweets. 
 
preprocess and cleaned the data by removing urls, hashtags, mentions, and punctuation in the data. The respective files can be found here as ```train.csv```, ```val.csv```, and ```test.csv```

### Arguments:

```
--epochs:  number of total epochs to run, default=10

--batch-size: train batchsize, default=2

--lr: learning rate for the model, default=5.16e-05

--hidden_size_lstm: hidden size of lstm, default=1024

--hidden_size_linear: hidden size of linear layer, default=128

--seq_len: sequence lenght of input text, default=56

--clip: gradient clipping, default=0.218

--dropout: dropout value, default=0.198

--num_layers: number of lstm layers, default=1

--lstm_bidirectional: bidirectional lstm, default=False

--fasttext_embed_file: path to fasttext embedding file, default='new_hing_emb'

--train_dir: path to train file, default='train.csv'

--valid_dir: path to validation file, default='valid.csv'

--test_dir: path to test file, default='test.csv'

--checkpoint_dir: path to the saved, default='selfnet.pt'

--test: testing the model, default=False
```
### Train

```python main.py```

### Test

```python main.py --test True```
