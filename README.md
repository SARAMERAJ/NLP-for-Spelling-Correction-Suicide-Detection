# Spelling Correction using NLP

## Project Overview

This project is a Natural Language Processing project that detects and corrects spelling mistakes in text. The goal is to take user input, identify misspelled words, suggest possible correct words, and generate a corrected sentence.

The project uses the **Million Headlines** dataset from Kaggle to build a custom vocabulary from real news headline text.

Dataset used:  

The dataset used in this project is the **Million Headlines** dataset from Kaggle.

Dataset link:  
https://www.kaggle.com/datasets/therohk/million-headlines

The dataset file used is:


abcnews-date-text.csv

---

## Code Explanation

The notebook starts by importing the required Python libraries for text processing, data handling, spelling correction, grammar checking, and building a simple user interface.

The dataset is then loaded and inspected. The dataset used is `abcnews-date-text.csv`, which contains news headlines. The code mainly uses the `headline_text` column because it contains the text needed to build the spelling correction vocabulary.

After loading the dataset, the code performs text preprocessing. The headlines are cleaned by converting the text to lowercase, removing unnecessary characters, tokenizing the words, removing stopwords, and applying lemmatization. This helps create a cleaner and more useful list of words.

The code then builds a custom vocabulary from the cleaned headline text. This vocabulary is used as the reference list of correct words. When a user enters a sentence, the code checks each word against the vocabulary. If a word is not found, it is treated as a possible spelling mistake.

The spelling correction part suggests possible correct words using word similarity methods such as edit distance and bigram similarity. The system chooses the closest matching word from the vocabulary and uses it to generate a corrected sentence.

The code also includes grammar correction to improve the final sentence after spelling mistakes are fixed.

Finally, a Gradio interface is created so users can type text and see the corrected output in an easy way.

---

## Main Features

- Text preprocessing
- Custom vocabulary creation
- Misspelled word detection
- Spelling correction suggestions
- Corrected sentence generation
- Grammar correction
- Gradio user interface

---
# Suicide Ideation Detection Using NLP and Machine Learning

## Project Overview

This project detects suicide-related intent in tweets using Natural Language Processing and machine learning. The goal is to classify text as either **Not Suicide** or **Potential Suicide** based on the content of the tweet.

The project uses the Suicidal Tweet Detection Dataset from Kaggle and applies text cleaning, exploratory data analysis, feature extraction, model training, model comparison, and a Gradio interface for prediction.

Dataset used:  
https://www.kaggle.com/datasets/aunanya875/suicidal-tweet-detection-dataset

---

## Code Explanation

The notebook starts by importing the required Python libraries for text processing, data analysis, visualisation, machine learning, deep learning, transformer models, spelling correction, grammar correction, and interface development.

The dataset is then loaded and inspected to understand its structure, columns, missing values, and class distribution. The dataset contains tweets and their labels. The main text column is `Tweet`, and the target column is `Suicide`.

After loading the dataset, the code performs exploratory data analysis using different graphs such as label distribution plots, tweet length distribution, word count distribution, sentiment analysis, hashtag and mention analysis, and word clouds. These visualisations help understand the differences between suicide-related and non-suicide tweets.

The code then performs text preprocessing. Tweets are cleaned by removing missing values, unnecessary characters, and noise. The text is prepared for machine learning using TF-IDF vectorisation, which converts the tweet text into numerical features that models can understand.

Several machine learning models are trained and compared, including **Logistic Regression**, **Naive Bayes**, **Random Forest**, **SVM**, and **XGBoost**. Both baseline and tuned versions of these models are tested to compare their performance.

The notebook also trains transformer-based models using **DistilBERT**. DistilBERT is used because it can understand text context better than traditional machine learning models.

After training, all models are evaluated using accuracy, F1-score, classification report, and confusion matrix. The results are saved and compared to identify the best-performing model.

The best-performing model is then used in a Gradio interface. The interface allows users to enter a tweet or short message and receive a prediction. The code also includes spelling and grammar correction before prediction to improve input quality.

Rule-based filters are also added to reduce false positives. For example, phrases like “kill time” or “kill the engine” should not be treated as suicide-related text.

---

## Models Used

- Logistic Regression
- Naive Bayes
- Random Forest
- Support Vector Machine
- XGBoost
- DistilBERT

---

## Results

| Model | Accuracy | F1-Score |
|---|---:|---:|
| DistilBERT Baseline | 98.62% | 98.62% |
| DistilBERT Tuned | 97.00% | 97.00% |
| XGBoost Baseline | 95.85% | 95.85% |
| SVM Tuned | 95.62% | 95.62% |
| Random Forest Tuned | 95.62% | 95.62% |
| Logistic Regression Tuned | 94.01% | 94.01% |
| Naive Bayes Baseline | 90.55% | 90.55% |

The best-performing model was **DistilBERT Baseline**, which achieved the highest accuracy of **98.62%**.

---

## Conclusion

This project shows how NLP and machine learning can be used to detect suicide-related intent from tweet text. The code follows a complete text classification workflow, including data loading, exploratory analysis, text preprocessing, feature extraction, model training, tuning, evaluation, and deployment through a Gradio interface.

DistilBERT was selected as the best model because it achieved the highest accuracy and F1-score. This project is for academic and educational purposes only and should not be used as a real medical or emergency decision system.

---

## Author

**Sara Mohammed Meraj Zaki**
