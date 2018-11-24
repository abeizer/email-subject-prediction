# Email Subject Classification
This project utilizes machine learning concepts to predict the subject of an email body and generate an appropriate subject line for that email.

## Requirements
* __Jupyter Notebook__ (http://jupyter.org/install)
* __Python 3__
* __spaCy__ - an open-source natural language processing library (https://spacy.io/usage/)
* __Enron Corpus__ - over 500,000 emails from emplyees within the Enron corporation (https://www.cs.cmu.edu/~./enron/)

## Getting the dataset ready
1. If the Enron dataset is in a zipped format, unzip it. It should now be a single file in .csv format.
2. Create a folder in the main project directory named `enron`
3. Create a sub-folder in the enron folder, named `initial`
4. Move the unzipped dataset into `/enron/initial`

## Feature-Extraction.ipynb
### Summary
This file is responsible for loading the dataset and changing its structure slightly so that it can be more easily used for our machine learning.

The raw dataset has two features: a filename and an email body. The body contains many features that may hinder natural language processing, such as To: and From: lines.
The feature extraction step separates these lines so that they become their own features within a pandas dataframe. The dataset is then split into training and testing sets, and these sets are saved locally.

### How to Use
Open the file in Jupyter notebook. Run the entire notebook. It may take some time, as the dataset is very large. After running, you should have 3 new files saved locally:
* A .csv containing the entire dataset in its new form in `/enron/unlabeled/enron.csv`
* A .csv containing the training set in `/enron/unlabeled/train.csv`
* A .csv containing the testing set in `/enron/unlabeled/test.csv`

_These sets take a decent chunk of memory. You can optionally shutdown the notebook to free memory for the next steps._

## Pre-processing.ipynb
### Summary
In this file, we load the training set and pre-process the email bodies. 

A clean function is defined which uses
* lemmatization --> a special form of normalization for natural language)
* stopword removal --> the removal of common words in order to focus on less common words which can convey more information

### How to Use
Before running the file, you must have the spaCy library. This can be installed from a terminal/prompt such as anaconda:
```
pip install spacy
python -m spacy download en
```

## Authors:
* [@antakij1](https://github.com/antakij1)
* [@abeizer](https://github.com/abeizer)
