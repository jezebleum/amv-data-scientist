# Case Application Data Scientist AMV
##  Task
You receive two files:
- cardata.csv: A CSV file containing 10000 cars with an id (AUTO_ID) and its characteristics
- behavior.json: A JSON file containing 106966 cars ids with a two additional columns containing the number of pageviews and contactrequests

Your assignment is to predict interactions (pageviews and contactrequests) based on car characteristics. 

The way you get to the results is more important than the results itself.

## Requirements

1) Python 3.7.4 was used in this repo.
2) The requirements for this project can be found in the requirements.txt. These can be installed in a virtual-env by using `pip install -r requirements.txt`.

## Summary

The notebook consists multiple parts:
1) **Data Exploration** - this part showcases the contents of the original files.
2) **Data Adjustments** - to use the contents of the two files, a column (BOUWJAAR) is transformed to a different column and NaN values were eliminated. The outliers remained within the data, since from a business perspective it makes more sense to leave them in. From there on, the two files were merged into one DataFrame through an inner join. Lastly, a heatmap is generated to gain insight in correlations between numeric values and the target variables.
3) **Model Development** - Two XGB Regressors (pageviews and contactrequests) were made in order to verify whether the dataset was able to produce an accurate regression, however models were not able to generalize extensively. In order to experiment whether the dataset is sufficient for a binary classiification, the target variable contactrequests was adjusted to 0 (no requests) and 1(1 or more requests). To verify whether any model was able to converge a LogisticRegression and a XGBClassifier were trained, however neither of these two was able to converge either.
4) **Conclusion** - The current state of the dataset is not able to converge in neither a regression or a classification function. Further experimentation can be exploited by applying [PCA](https://en.wikipedia.org/wiki/Principal_component_analysis) and [Data binning](https://en.wikipedia.org/wiki/Data_binning). 
