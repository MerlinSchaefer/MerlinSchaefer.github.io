---
layout: post
title:  "Credit Card Fraud Detection"
date: 2020-10-01 7:00:13 +0200
categories: Projects
---

# Credit card fraud detection using machine learning

I used the Credit Card Fraud Detection dataset as provided on [kaggle](https://www.kaggle.com/mlg-ulb/creditcardfraud).

The code can be found in this [repository](https://github.com/MerlinSchaefer/fraud_dectection)

With this project I wanted to gain some experience with skewed data and outlier detection.
I originally planned to build something interactive, yet I realized that the PCA-features wouldn't be a good fit for any user input etc.
I therefore opted for a more analytic approach with an end-to-end model as the result.


# What I learned doing this project

The first thing I learned was how to handle (highly) skewed data. I was familiar with slightly skewed data and checking whether the data follows certain distributions, but I never worked with a dataset, which was as skewed as this one.
I learned how far reaching these implecations are; from metrics over splitting the data to the actual model selection, highly skewed data can require a strong deviation from the "default" way of handling data.

I also learned to not only check for NAs, which I always did but also to check for possible duplicates, something I missed during my first exploration of the data.

After starting to implement my own solutions for cross validating the data, I realized that the scikit-learn function already had a way of implementing what I was looking for, this taught me to really read the documentation down to the last detail if necessary.

I also realized how quickly GridSearchCV and even RandomSearchCV can require large amounts of computing power. This taught me to be more careful when selecting the hyperparameters to tune.

I learned that anomaly detection might not always be the best choice, even for highly skewed data with a very small number of instances in the target class.

Overall I learned many new things but also used and practiced many existing skills.

Unfortunately I couldn't build a Streamlit app or something interactive as the data was already the product of PCA and the features can't really be given through user input.