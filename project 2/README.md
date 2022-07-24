# Disaster Response Pipeline Project
## Table of Contents
 * [Project Motivation](#project-motivation)
 * [File Descriptions](#file-descriptions)
 * [Instructions](#Instructions)
 * [Licensing, Authors, Acknowledgements, etc.](#licensing-authors-acknowledgements-etc)
 
### Project Motivation
This project serves as crucial part of my journey in udacity data scientist nanodegree.
We create an ETL pipeline for provided disaster data to build and serve machine learning that will categorize real messages sent during disaster event model from a front end in FLASK web app. The purpose of web app is to simulate situation where end user can input a new message and get classification results in several categories along with couple of helpful visualizations.

### File Descriptions
app    

| - template    
| |- master.html # main page of web app    
| |- go.html # classification result page of web app    
|- run.py # Flask file that runs app    


data    

|- disaster_categories.csv # data to process    
|- disaster_messages.csv # data to process    
|- process_data.py # data cleaning pipeline    
|- YourDatabaseName.db # database to save clean data to     


models   

|- train_classifier.py # machine learning pipeline     
|- classifier.pkl # saved model     

README.md    

### Components
There are three components I completed for this project.

#### 1. ETL Pipeline
A Python script, `process_data.py`, writes a data cleaning pipeline that:

 - Loads the messages and categories datasets
 - Merges the two datasets
 - Cleans the data
 - Stores it in a SQLite database
 
 
#### 2. ML Pipeline
A Python script, `train_classifier.py`, writes a machine learning pipeline that:

 - Loads data from the SQLite database
 - Splits the dataset into training and test sets
 - Builds a text processing and machine learning pipeline
 - Trains and tunes a model using GridSearchCV
 - Outputs results on the test set
 - Exports the final model as a pickle file
 

#### 3. Flask Web App
The project includes a web app where end user can input a new message and get classification results in several categories. 

### Instructions
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/YourDatabaseName.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/

### Licensing, Authors, Acknowledgements, etc.
Thanks to Udacity for starter code for the web app. 
