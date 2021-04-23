# Udacity+Arvato: Identify Customer Segments
This project is part of the [Udacity Datascience Nanodegree](https://www.udacity.com/course/data-scientist-nanodegree--nd025)

### Table of Contents

1. [Installation](#installation)
2. [Project Motivation](#motivation)
3. [File Descriptions](#files)
4. [Licensing, Authors, and Acknowledgements](#licensing)
5. [Report](#report)

## Installation <a name="installation"></a>

The following Python packages are required: pandas, numpy, pickle, plotly, sklearn, catboost and hyperopt.

## Project Motivation<a name="motivation"></a>

Arvato Financial Solutions is an international financial service provider, offering advanced analytics solutions across the entire customer journey from risk and fraud management to Accounts Receivables Management. For this project, Arvato provides support to a German mail-order company selling organic products by giving them insights on the segmentation of their customers vis a vis general German population, and by delivering a predictive model in order to improve the chances of customers acquisition through mail campaigns.

The problem is two parts. First, understanding what are the key attributes of existing customers vis a vis German general population. Are there segments in the German population which are more or less likely to be customers of the mail-order company given their demographic data ? To answer this question an unsupervised clustering analysis of the general population will be performed and applied to the customers of the company. Due to the importance of categorical variables in the dataset, the Kprototype algorithm is used “Huang, Z.: Clustering large data sets with mixed numeric and categorical values, Proceedings of the First Pacific Asia Knowledge Discovery and Data Mining Conference, Singapore, pp. 21-34, 1997”

Second, how to improve success of mail marketing campaigns by targeting the population with the highest chance of becoming a customer ? To answer this question a supervised model will be applied to predict the probability of a person becoming a customer. The Catboost library is used.
The performance of the model is measured by the AUC as the dataset is extremely imbalanced.
The performance is then submitted to the Kaggle platform https://www.kaggle.com/c/udacity-arvato-identify-customers

As of April 2021, the final model scored an AUC of 0.80612 and ranked 30 out of 361 submissions.

## File Descriptions <a name="files"></a>

1. Datasets

- Udacity_AZDIAS_052018.csv: Demographics data for the general population of Germany; 891 211 persons (rows) x 366 features (columns).
- Udacity_CUSTOMERS_052018.csv: Demographics data for customers of a mail-order company; 191 652 persons (rows) x 369 features (columns).
- Udacity_MAILOUT_052018_TRAIN.csv: Demographics data for individuals who were targets of a marketing campaign; 42 982 persons (rows) x 367 (columns).
- Udacity_MAILOUT_052018_TEST.csv: Demographics data for individuals who were targets of a marketing campaign; 42 833 persons (rows) x 366 (columns).

Each row of the demographics files represents a single person, but also includes information outside of individuals, including information about their household, building, and neighborhood.
The train dataset is used to train and tune the parameters of the predictive model, and the test dataset is the model unseen data on which predictions will be performed and scored on the Kaggle platform.

The other inputs provided are:

- DIAS Information Levels - Attributes 2017.xlsx is a top-level list of attributes and descriptions, organized by informational category.
- DIAS Attributes - Values 2017.xlsx is a detailed mapping of data values for each feature in alphabetical order.

**Please note that these files are not available on the repository due to confidentiality.**

2. Jupyter Notebook

The notebook in which the analysis was performed

## Acknowledgements<a name="licensing"></a>

Must give credit to Udacity and their partner Arvato Financial Solutions for this project.

Must give credit to the Kmodes library https://github.com/nicodv/kmodes for the implementation of the KPrototype algorithm

## Report<a name="report"></a>

PDF file giving more insight on the project.
