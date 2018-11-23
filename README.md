# Email Subject Classification
This project utilizes machine learning concepts to predict the subject of an email body and generate an appropriate subject line for that email.

## Requirements
* Jupyter Notebook (http://jupyter.org/install)
* Python 3
* Enron email dataset (https://www.cs.cmu.edu/~./enron/)

## Instructions for using this Project
### Getting the dataset ready
1. If the Enron dataset is in a zipped format, unzip it. It should now be a single file in .csv format.
2. Create a folder in the main project directory named `enron`
3. Create a sub-folder in the enron folder, named `initial`
4. Move the unzipped dataset into `/enron/initial`

### Feature-Extraction.ipynb
#### Summary
This file is responsible for loading the dataset and changing its structure slightly so that it can be more easily used for our machine learning.

The raw dataset has two features: a filename and an email body. The body contains many features that may hinder natural language processing, such as To: and From: lines.
The Data Manipulation step separates these lines so that they become their own features. The dataset is then split into training and testing sets, and these sets are saved locally.

#### How to Use
Open the file in Jupyter notebook. Run the entire file. It may take some time, as the dataset is very large. After running the file, you should have 3 new files saved locally:
* A .csv containing the entire dataset in its new form (/enron/unlabeled/enron.csv)
* A .csv containing the training set (/enron/unlabeled/train.csv)
* A .csv containing the testing set (/enron/unlabeled/test.csv)

These sets take a decent chunk of memory. You can optionally shutdown the notebook to free memory for the next steps.

### Pre-processing.ipynb
#### Summary
In this file, we load the training set and start looking at how we can define possible email topics.


### Authors:
* @antakij1
* @abeizer
