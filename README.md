# Disaster Response Pipeline Project
This project is to classify disaster response messages through machine learning.

## Content
- Data
  - process_data.py: reads in the data from CSV files, cleans and stores it in a SQL database.
  Basic usage is:
  python process_data.py MESSAGES_DATA CATEGORIES_DATA NAME_FOR_DATABASE
  - disaster_categories.csv and disaster_messages.csv (dataset)
  - DisasterResponse.db: created database from transformed and cleaned data.
  
- Models
  - train_classifier.py: includes the code necessary to load data, transform it using natural language processing, run a machine
  learning model using GridSearchCV and train it.
  Basic usage is python train_classifier.py DATABASE_DIRECTORY SAVENAME_FOR_MODEL  

- App
  - run.py: Flask app and the user interface used to predict results and display them.
  - templates: folder containing the html templates
  Basic usage is python run.py

### Instructions:
1. Run the following commands in theprocess_data project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
       > `python data/.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
       > `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
   > `python run.py`

3. Go to 
   > http://0.0.0.0:3001/

## Screenshots
This is the frontpage:
![Alt text](https://github.com/divvu/DisasterResponsePipeline/blob/master/data_pipeline_ss1.JPG )

![Alt text](https://github.com/divvu/DisasterResponsePipeline/blob/master/data_pipeline_ss2.JPG )

By inputting a word, you can check its category:
![Alt text](https://github.com/divvu/DisasterResponsePipeline/blob/master/data_pipeline_ss3.JPG)

## About
This project was prepared as part of the Udacity Data Scientist nanodegree programme. The data was provided by Figure Eight. 
