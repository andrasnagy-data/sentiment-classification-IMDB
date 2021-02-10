### Sentiment Classification IMDB reviews

**Using Bag of words approach (discrete) and Machine Learning**

I used CountVectorizer to vectorize the text, as the MultinomialNB model "prefers" (from the documentation) integer word counts.

I trained a quick "prototype" of both models (meaning that I did not tune hyper parameters.). The accuracy is not k-fold cross-validated, however it is a good indication of the model's performance. I fit_transformed the train set and only transformed the test set, as to simulate the real-world application (some words may not be present in the document term matrix).

Model accuracy: *Without hyper-parameter tuning*

- Naive_bayes: ~85.6 %
- Logistic Regression: ~88.3 %

These values are plenty better than the 50% base line accuracy.

True Negative:
- NB: 5402
- LR: 5403

False Positives:
- NB: 755
- LR: 754

False Negatives:
- NB: 1040
- LR: 711

True Positives:
- NB: 5303
- LR: 5632

The logistic regression classifier did a better job of identifying positive sentiments.
A better model would include continuous word representation and a deep learning architecture (Recurrent Neural Network).