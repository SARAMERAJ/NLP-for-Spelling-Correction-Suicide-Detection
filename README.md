# Spelling Correction using NLP

## Project Overview

This project is a Natural Language Processing project that detects and corrects spelling mistakes in text. The goal is to take user input, identify misspelled words, suggest possible correct words, and generate a corrected sentence.

The project uses the **Million Headlines** dataset from Kaggle to build a custom vocabulary from real news headline text.

Dataset used:  
https://www.kaggle.com/datasets/therohk/million-headlines

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

## Dataset Used

The dataset used in this project is the **Million Headlines** dataset from Kaggle.

Dataset link:  
https://www.kaggle.com/datasets/therohk/million-headlines

The dataset file used is:

```text
abcnews-date-text.csv
