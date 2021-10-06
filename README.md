# ML-SentimentClassification
 Machine Learning Assignment 3: Sentiment Classification

This notebook is split up into three phases: The training phase, development phase, and test phase

Training Phase 
First, the three feature representations were read and processed. The goal of this step was to transform the raw input into a format which could be read by the selected machine learning models. For the TFIDF and Count feature sets, this required transforming the raw tuple lists into sparse matrices. The GloVe dataset required no processing as it was already in an acceptable format.

The models used in this analysis were Logistic Regression, Multinomial Naïve Bayes (Gaussian Naïve Bayes for GloVe), Linear Support Vector Classifier, and Multi-layer Perception. Each of these models were trained on each of the processed feature sets. The reason for doing this was to exhaustively compare all models on all feature set combinations, to give the best chance at building an optimal model. 

Development Phase
The goal of this phase was to evaluate each model’s performance on the development data feature representations. To do so, each model was evaluated according to its accuracy, as well as its bias and variance. These evaluation metrics were selected because accuracy allowed overall model performance to be evaluated against baselines, and bias and variance allowed for underfitting and overfitting diagnoses to be made which are vital for model tuning. The baseline selected for this classification task was Weighted Random Baseline. These evaluation metrics mentioned here are visually displayed in the form of confusion matrices and learning curves in the results section.
Once the models had been evaluated on each of the feature representations, the models underwent tuning designed to optimise the model parameters, as well as identify the optimal feature set for each model. This consisted of analysing learning curves to diagnose overfitting and underfitting models, as well as determining which feature set performed the best on each model. 
This processed helped to eliminate underperforming ‘model-feature set’ pairs, and the remaining model was then selected as the classifier to be used in the test phase.

Test Phase
This phase consisted of selecting the best performing model to predict the sentiment of unlabelled tweets from the test dataset.
