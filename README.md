# Capstone_2_Spam_Detector
Spam Filtering as a Cybersecurity Measure


# Overview
Cyber-security is the practice of protecting systems and entities from outside forces designed to infiltrate, change, and gleam sensitive information from them. Today, companies have begun to practically invest in professionals and, in larger agencies, entire departments familiar with addressing, preventing, and managing these crises situations. Such professionals can include a team made up of security analysts, IT administrators, and/or a data scientists who work collaboratively to address problems like:

- system cleaning and updating
- problem cleaning, i.e. malware
- internal misuse(access privileges)
- and applying spam and/or phishing filters


# PROPOSAL
The head of Cybersecurity at a prospective company is creating an innovative new software that identifies spam. How can you help them create an effective filter?


# The Data
The data for this project consists of csv file of two folders; each folder containing emails of spam or ham(not spam). Each text file of the folders was iterated through to create a DataFrame, and written to the csv file.


# Methods
For my research, I obtained a public dataset from Kaggle, "spam-mail-dataset", which consisted of a combined csv file of two sets of data; one for spam-labeled email subjects and the other for non-spam-labeled email subjects. They were then written to one large csv file. This was for both ease of accessibility and analysis of both email types. The combined dataset catalogued the categorized emails received by users. Before the model creation, I initially applied a number of exploratory analyses; such as first applying a label to the user column, which - was previously unlabeled - then, the code was further cleaned and the column values were confirmed. I then used one-hot encoding and added a key for the new target variable, so that the variable - which previously held strings in its column - could be fed properly into the model.

I applied some preliminary visualizations to check the initial distribution of the variables; by themselves and in relation to each other. I then built two different models to observe their affect and accuracy on the dataset. The first was built was a Random Forest Classifier to the dataset. After observing the results, I applied some Natural Language Processing(NLP) techniques to the dataset. Specifically, word embedding and word vectorization were used as a better predictive model and to filter user emails. The results are discussed in the next section.


# Results
The random forest ran successfully, but was not always able to detect spam emails. This may be chiefly due to the higher number of 'Ham' variables being in the dataset. A predictive model was able to be created using NLP techniques. Using word embedding, scatter plotting was used to visualize dots annotated with the words from the text. From the second NLP model, a predictive model was successfully created using word vectorization; where each categorization was used to detect and filter new emails.


# Discussion & Recommendation
A closer look at the data indicates that Spam Detection/Spam Filters are best run on NLP word vectorization models. While random forests are very strong performers and work well on both classification and regression, as shown, they can't predict well outside the sample and will only return values within a range already seen before. Drawbacks of the dataset were having an uneven(higher) number of non-spam("Ham") emails; which could also negatively affect other kinds of predictive modeling. This imbalance was overcome for the NLP model, however. Future iterations would implement measures to balance out the dataset by under-sampling the "Ham" variable, and implement cross-validation.
