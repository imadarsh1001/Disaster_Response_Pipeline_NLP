# Disaster Response Pipeline Project

### Project Overview:

In this project, I will apply data engineering to analyze disaster data from [Figure Eight](https://www.figure-eight.com/) to build a model for an API that classifies disaster messages. The initial dataset contains pre-labeled tweets and messages from real-life disasters. This project aims to build a Natural Language Processing tool that categorizes messages.

It is divided into the following sections:

1. Data Processing, ETL Pipeline to extract data from the source, clean data, and save them in a proper database structure.
2. Machine Learning Pipeline to train a model that can classify text messages in 36 categories.
3. Web Application using Flask to show model results and predictions in real-time.

## File Description
~~~~~~~
        disaster_response_pipeline
          |-- app
                |-- templates
                        |-- go.html
                        |-- master.html
                |-- run.py
          |-- data
                |-- disaster_message.csv
                |-- disaster_categories.csv
                |-- DisasterResponse.db
                |-- process_data.py
                |-- ETL Pipeline Preparation.ipynb
                |-- Twitter-sentiment-self-drive-DFE.csv
          |-- models
                |-- classifier_1.pkl
                |-- train_classifier.py
                |-- ML Pipeline Preparation.ipynb
          |-- README
~~~~~~~
### Installation:

This project requires Python 3.x and the following Python libraries:

* Machine Learning Libraries: NumPy, SciPy, Pandas, Sciki-Learn
* Natural Language Process Libraries: NLTK
* SQLlite Database Libraries: SQLalchemy
* Web App and Data Visualization: Flask, Plotly

### Instructions:
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/

### Screenshots:

#### 1. Home Page
!(Homepage.JPG)

#### 2. Classify Messages Page
!(classify_message_page.JPG)

## Licensing, Authors, Acknowledgements
Many thanks to Figure-8 for making this available to Udacity for training purposes. Special thanks to Udacity for the training. Feel free to utilize the contents of this while citing Udacity or figure-8 accordingly.
