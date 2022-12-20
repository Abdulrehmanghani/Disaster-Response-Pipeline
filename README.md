# Disaster-Response-Pipeline

The project has three componants which are:

ETL Pipeline: process_data.py file contain the script to create ETL pipline which:
Loads the messages and categories datasets
Merges the two datasets
Cleans the data
Stores it in a SQLite database
ML Pipeline: train_classifier.py file contain the script to create ML pipline which:
Loads data from the SQLite database
Splits the dataset into training and test sets
Builds a text processing and machine learning pipeline
Trains and tunes a model using GridSearchCV
Outputs results on the test set
Exports the final model as a pickle file
Flask Web App: the web app enables the user to enter a disaster message, and then view the categories of the message.
