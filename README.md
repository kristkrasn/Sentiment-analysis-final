# Sentiment Analysis of Movie Reviews

## 1. Project Description

This project focuses on developing a sentiment analysis system for movie reviews. The goal is to classify reviews as either positive or negative using machine learning methods.

The project was completed as part of the course DLBAIPNLP01 – Project: NLP.

## 2. Dataset

The project utilizes the IMDb Large Movie Review Dataset, which contains text-based movie reviews labeled with their sentiment.

Dataset source:
https://ai.stanford.edu/~amaas/data/sentiment/

The specific method for loading the data, the file structure, and the preparation of the training and test sets are described in the corresponding cells of the notebook.

## 3. Preprocessing and Text Representation

The text data is prepared for use in machine learning models. Following preprocessing, the text is represented using TF-IDF.

Feature creation is performed using `TfidfVectorizer` with the following parameters:

- `max_features=50000`
- `ngram_range=(1, 2)`
- `min_df=2`

Thus, the model utilizes both unigram and bigram text features.

## 4. Machine Learning Methods

The project compares two classification models:

- Multinomial Naive Bayes
- Logistic Regression

Experiments are conducted using various training set sizes: 1,000, 5,000, 10,000, and 25,000 reviews.

The models are evaluated on a separate test set.

## 5. Model Evaluation

The following metrics are used for evaluation:

- Accuracy
- Precision
- Recall
- F1-score

Model performance is compared across different training set sizes. Additionally, the confusion matrix and examples of reviews misclassified by the model are analyzed.

Based on the experimental results, Logistic Regression was selected for further analysis. The final numerical results are provided in the notebook.

## 6. Project Structure

- `sentiment_analysis.ipynb` — code, experiments, tables, plots, and evaluation results.
- `README.md` — project description.
- `requirements.txt` — list of required Python libraries.
- `sentiment_analysis_report.pdf` — written report.

## 7. Running the Project

The notebook can be opened in Google Colab or Jupyter Notebook.

To re-run the project:

1. Open `sentiment_analysis.ipynb`.
2. Install the required libraries.
3. Prepare the dataset in the format and at the file path expected by the code.
4. Execute the cells sequentially from start to finish.

## 8. Results

The notebook includes a comparison of the models, evaluation results on the test set, plots showing how metrics vary with training set size, and an analysis of misclassifications.

Based on the comparison, the highest F1 Score for Multinomial Naive Bayes was 0.846570, achieved with a training set size of 25000 reviews. For Logistic Regression, the corresponding value was 0.880878, with a training set size of 25000 reviews. The best Accuracy, Precision, and Recall values ​​for each configuration are presented in the table of experimental results in the notebook. Based on the results obtained, the Logistic Regression model was selected for further analysis, as it demonstrated the highest F1 score, higher accuracy and precision, which are balanced with the slightly higher execution time.
