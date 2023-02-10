# kaggle_comp_nlp_disaster_tree
The solve of kaggle competition of binary classification
## Pipeline
1. Generate features with EDA
2. Create data proccesing based on finded features
3. RoBERTa embeddings fine-tuned by tweets 
4. Create NeuralNetwork
5. It fit on 20 epochs 
### Features
The main problem of this dataset is dirty text data. There are many a lot of jargon.
I created next things:
- length of text (in official texts used more length of text than in public text)
- count of dog, hashtag symbols and links
- availability of keyword, location and link
- calculate sentiment score of keyword 
- get style of text (procent of probability accessories public style)
- drop duplicates
- lemmatization text
- clear data off dirt
- create RoBERTa embeddings for tweet-text
### Model
I use neural network with dropout and normalize layers, output model is probability of accessories two classes 
- optimizer: AdamW
- sheduler: linear sheduler
- loss function: cross entropy loss
### Metric
**F1-score** was used in competition
### Conclusion
I have score **0.798** in valid data and take 402/800 place.
