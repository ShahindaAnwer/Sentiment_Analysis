# IMDB Movie Review

## Objective
Movie reviews are extremely important because of their significant effect on the consumer thought processes, they are not only used as a marketing tool, but also as a predictor as to how a film will perform financially. Review classification is responsible for grouping the reviews into one of the two categories;  positive and negative. This is a binary classification problem.

## Model

<p align="center">
<img src = https://user-images.githubusercontent.com/62629426/228087013-a412c6b0-1520-422a-8cac-59acc59c9d13.png width = 300>
</p>

First off, I used an embedding layer with the GloVe file glove.6B.100d.txt, which is a sentence-transformers model, that maps sentences & paragraphs to a 300 dimensional dense vector space to be used for clustering or semantic search.
<p align="center">
<img src = https://user-images.githubusercontent.com/62629426/228088212-6441a71e-cb84-4eab-8056-5a4663722c72.png width = 500>
</p>

                      The model architecture of GloVe, where the input is a one-hot representation of a word. 
                      The word embedding matrices serve as weight matrices in the model.
                      The output of the model is a vector of inner products of word vectors.

I then used Gated Recurrent Unit (GRU), wich solved my vanishing gradient problem.

<p align="center">
  <img src = https://user-images.githubusercontent.com/62629426/228089859-f7d78c9c-5c91-4d3f-8445-c27d83cc1c9d.png width = 500>
</p>


### Libraries:
- [Tensorflow - Keras](https://www.tensorflow.org/api_docs/python/tf/keras)
- [Keras](https://keras.io/)
- [Numpy](http://numpy.org/)
- [Pandas](https://pandas.pydata.org/)
- [Matplotlib](https://matplotlib.org/)
- [Scikitlearn](https://scikit-learn.org/stable/)
- [seaborn](https://seaborn.pydata.org/)
- [nltk](https://www.nltk.org/)
- [re](https://docs.python.org/3/library/re.html)

### Accuracy:
- Loss: 0.0460
- Accuracy: 0.9927
- Val loss: 0.7226
- Val Accuracy: 0.8560

### Results:

0: `Negative`
1: `Positive`
