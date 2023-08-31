# Text Sentiment Analysis
## Models used:
1. Logistic Regression
2. Naive Bayes
3. LSTM
## Approach:
### The project is divided into 2 types of approaches:
## Word to Word Approach
- In the first approach, we make term-sentiment frequency matrix. We normalize the results using inverse document frequency or using a similar approach. In this approach each term is given a score that tells us about the associated sentiment. A complete sentence is parsed as a sum of all the scores of the terms present. I trained 2 models using this approach i.e. Logistic Regression and Naive Bayes.

- **Limitations of this approach**
This approach is naive in the sense that it does not consider the sequence in which words appear for prediction. Often times we come across texts that contain both positive and negative words. The model will fail in those cases. These limitations are removed in the second approach.

## Sequence Approach
- In the second approach, we would try to make the model learn the sequence in words appear to learn the associated sentiment. I have used TensorFlow for the implementation but any other similar framework such as PyTorch might be used.
- We first do pre-processing tasks such as train-val-test split, tokenization and padding.
- We then use embeddings(GloVe) to convert the tokens into model trainable form.
- For model. I have used Bi-directional LSTMs because of their ability to see the context on both the directions.
- Let the model run for >10 epochs and it returns an accuracy score of >80%. (Dataset used is [Sentiment140](https://www.kaggle.com/datasets/kazanova/sentiment140) dataset with 1.6 million tweets)








## Live Demo

Sites are currently down, would be up soon!

The application is live on Streamlit [Click Here](https://sentimentanalysisbilstm.streamlit.app/)


If the above link does not work [Click Here](http://ojassharma.pythonanywhere.com/)
