# Classification of Breast Cancer Using Machine Learning

## Dataset source:

Original Wisconsin Breast Cancer Database from: UC Irvine Machine Learning Repository (https://archive-beta.ics.uci.edu/ml/datasets/breast+cancer+wisconsin+original)

## ETL:
1. Data was downloaded manually from UC Irvine Repository and stored locally.
2. Data was transformed first by reading it into a pandas dataframe from its '.data' format using pandas "read_table". Null/NaN values were identified and dropped, additionally, unnecessary columns were dropped as well. Further transformation was done by concatenating all column features into one big dataframe containing just 2 columns (category/feature and score). Both dataframes were saved as csv files.

## Descriptive Statistics:
Pandas functions for description of the data was used to get an idea of how the values are distributed.
Data is categorical so a couple descriptive graphs were made:

