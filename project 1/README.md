# Boston Airbnb Data Analysis

## Installations
 - NumPy
 - Pandas
 - Seaborn
 - Matplotlib
 - scikit-learn
 - PrettyPrinter
 
No additional installations beyond the Anaconda distribution of Python and Jupyter notebooks.

## Project Motivation
For this project I was interested in conducting exploratory data analysis from end user's perspective using boston airbnb dataset found on kaggle
([link to kaggle dataset](https://www.kaggle.com/datasets/airbnb/boston)):
 - Which Neighbourhoods are popular to live amongst customers coming to boston?
    *   Based on number of listings in the neighbourhood
    *   Based on average ratings given
    *   Based on number of reviews
 - Types of Airbnbs offered in boston
    *   Whats the popular property type that gets posted?
 - What factors affect ratings the most?
    *   can we predict ratings given to an airbnb listing based on different factors identified
    *   Performing feature selection and predicting user ratings for a given airbnb listing with random forest regressor algorithm

## File Descriptions
* Please find jupyter notebook "boston_airbnb.ipynb" which includes code for data cleaning, handling missing/categorical columns, Data visualization,Modeling and Feature Selection using Random Forest Regressor implementation in scikit-learn
* All datasets are available in 'data' folder in ".csv" format

## Result Summary
  - Jamaica Plain and Dorchester are top two neighbourhoods based on number of listings and average ratings combined. But if we just look at the average ratings then Leather District, Roslindale are the neighbourhoods where ratings are higher even though not a lot of listings are available in the area
  - Airbnb listings are offered in "entire home", "private room" and "shared room" types. "Entire home" is majorly available in apartments,rather than bunglows. As we go to private room and shared room, houses start seeing a increased listings but still leaded by apartments.
  - we trained a random forest regressor to perform feature selection for predicting user ratings as well as modeling for user ratings.<br>
As we had over 27 features, the ones that are found to be most useful to having good user ratings is "number of ratings", "host listings count","monthly price" and "superhost"<br>
We can conclude that superhosts tend to have great ratings with multiple listings and large number of ratings.

## Licensing, Authors, and Acknowledgements

Licensing for the data and other descriptive information at the [Kaggle link available here].

[Kaggle link available here]: https://www.kaggle.com/airbnb/boston
