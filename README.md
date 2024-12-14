# Disaster Response Pipeline

This project aims to build a machine learning pipeline for classifying disaster messages. The pipeline enables efficient processing of messages to categorize them into various disaster-related categories, which can help emergency responders prioritize and respond to the most critical cases.

---

## Project Components

### 1. **ETL Pipeline**
The ETL (Extract, Transform, Load) pipeline is implemented in the `process_data.py` script, which:
- **Loads** the messages and categories datasets.
- **Merges** the two datasets into a single unified dataset.
- **Cleans** the data by removing duplicates and handling missing values.
- **Stores** the cleaned data in a SQLite database for further processing.

---

### 2. **ML Pipeline**
The Machine Learning pipeline is implemented in the `train_classifier.py` script, which:
- **Loads** data from the SQLite database.
- **Splits** the dataset into training and testing sets.
- Builds a text processing and machine learning pipeline using **natural language processing (NLP)** techniques.
- **Trains and tunes** a machine learning model using **GridSearchCV** to find the best hyperparameters.
- Outputs the **model's performance** on the test set.
- **Exports** the final trained model as a **pickle file** for use in the web app.

---

### 3. **Flask Web App**
A **Flask-based web application** is included to enable user interaction.  
Key features:
- Users can input a disaster message.
- The app categorizes the message into pre-defined categories, providing actionable insights.

To run the app:
1. Launch the Flask server.
2. Access the web interface to classify messages in real-time.

---

## Installation and Usage

### Prerequisites
- Python 3.x
- Required libraries: `pandas`, `numpy`, `scikit-learn`, `SQLAlchemy`, `nltk`, `Flask`
- Install dependencies via:
  ```bash
  pip install -r requirements.txt
