# DA-401

In this project, I am investigating our ability to predict the number of overdoses in census block groups across Allegheny County, Pennsylvania through a time series analysis of overdose EMS data. In this dataset, overdoses are reported by yearly quarters, and we are working to predict the values for Quarter 4 2024. We are doing this analysis using a K Nearest Neighbors (KNN) approach where we use the average of the k past quarters' number of overdose calls to predict the next value in each census block group. To test our model, we split the data into training data (all data from Quarter 1 2015 to Quarter 2 2024) and predicted the Quarter 3 2024 values (testing data). This allows us to assess how well our model is doing, and the code to do that is detailed below.

In this repository, there are 4 main code files of importance:

- Data Manipulation

This contains all of the data manipulation we conducted to get the data in a usable format for the KNN analysis. This requires having the data downloaded (linked below) and ends with creating two CSV files of training and testing data that will be uploaded to be used in the following code files for the analysis.

- BuildingKModel

This file contains the methods we utlized to build the KNN and comparing the predicted values we created through the training data to the actual values in the testing data. It also contains code used to create the heatmap visuals and explore trends in the past data.

- ApplyingKModel

This file contains the running of our KNN model on the full dataset to predict the Quarter 4 2024 values.

- ANOVA Testing

This file contains the code used to run ANOVA testing on the data in order to check for seasonality between the quarters. We did not find conclusive evidence of seasonality in this project

Unfortunately, due to the size of the data, it is unable to be uploaded onto GitHub. The full dataset can be found here: https://catalog.data.gov/dataset/allegheny-county-911-dispatches-ems-and-fire. We utilized the 911 EMS Dispatches data csv as well as the zip file of census block group geographies.
