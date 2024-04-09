# SpaceX Space Race

## Predicting Landing Success of Falcon 9 Rockets
Objective: The objective of this project is to predict the success of landing the first stage of a Falcon 9 rocket, which would provide huge cost saving benefits per launch mission.

## Data Collection
Past launch data is extracted from the [SpaceX API](https://api.spacexdata.com/v4/launches/past).

## Data Wrangling
In order to use machine learning prediction, we must label the data as to whether the launch passed (1) or failed (0). The Landing Outcome column contains this type of information.

## Feature Engineering
To prepare the data for machine learning, important features must be identified and weighted more heavily. The important features were found to be Payload Mass, Orbit Type, Launch Site, and Flight Number.

## Interative Analytics
### Folium
Folium is a powerful library to create inline interactive maps for analyzing distance, location, and other geographical features. We use this to study whether geography or population density plays a role in the success or failure of landings.
### Dash
Dash is a popular dashboarding tool to create interactive dashboards in Python, similar to Power BI or Tableau. It is built on top of the web application framework Flask, which allows to integration with other webpages.
This tool was helpful in visualizing the effect of payload mass and launch site on landing success.

## Machine Learning Prediction
This is a supervised classification problem due to the defined categorical labels. As such, we compare the predictive accuracy of logistic regression, Support Vector Machines, Decision Trees, and K-Nearest Neighbors. 
GridSearchCV is used to optimize the best fit hyperparameters for a given parameter by using a cross-validated grid-search over a parameter grid. Training and testing datasets were created using
an 80/20 split on the data. 

Decision Trees outperformed the other 3 models by over 10% and only misclassified a single landing as a success when it actually failed. The other three models wrongly predicted 3 failed landings as successes.

## Improvements
* A greater number of launch results would be beneficial to increase confidence in our prediction accuracy because there would be more extensive training.
