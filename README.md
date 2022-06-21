# Classification of Breast Cancer Using Machine Learning

## Dataset source:

Original Wisconsin Breast Cancer Database from: UC Irvine Machine Learning Repository (https://archive-beta.ics.uci.edu/ml/datasets/breast+cancer+wisconsin+original)

## ETL:
1. Data was downloaded manually from UC Irvine Repository and stored locally.
2. Data was transformed first by reading it into a pandas dataframe from its '.data' format using pandas "read_table". Null/NaN values were identified and dropped, additionally, unnecessary columns were dropped as well. Further transformation was done by concatenating all column features into one big dataframe containing just 2 columns (category/feature and score). Both dataframes were saved as csv files.

## Descriptive Statistics:
Pandas functions for description of the data was used to get an idea of how the values are distributed.
Data is categorical so a couple descriptive graphs were made:

 > ![histograms](https://user-images.githubusercontent.com/80008461/174682516-e2228b23-9919-4b4e-a1a0-aae0b1b5a5bf.png) Histograms with density distribution for each features. With the exception of clump thickness and class, in general, the features are right-skewed.


> ![pmf_plots](https://user-images.githubusercontent.com/80008461/174682607-4b30b886-d297-4106-a3c9-8ec6584497a9.png) Probability plots for each feature.

> ![cdf_plots](https://user-images.githubusercontent.com/80008461/174682689-1ebdd3a9-d37a-44af-8cfb-0b0ac9bc8303.png) Cumulative distribution plots for each feature.

>  ![violin_plots](https://user-images.githubusercontent.com/80008461/174850993-de25c925-c6b5-4a91-ad41-edf046cef6e3.png) Violin plots aggregated by class. For the majority of features the most probable values/categories for the observtions are low numbers between 1 and 3 with the exception of class, which only has 2 values. For class, the most probable value is 2 or benign with about 60% of the data falling into that category. Aggregating the data based on class, each feature shows a more spread distribution when the class is malignant (or 4) while the majority of the values/categories for class 2 tend to be below 5 for all features.
>  ![box_plots](https://user-images.githubusercontent.com/80008461/174851065-7befccff-7da4-44e0-b75b-74649ea151df.png) Given the spread of values, boxplots are fairly difficult to visualize the data properly. Violin plots allow for more effective visualization.

> ![poisson_comp_plots](https://user-images.githubusercontent.com/80008461/174682879-8cfe8448-056f-4f46-90b3-1bfd195b657d.png) Comparing distribution of score/values to Poisson distribution for roughly the same amount of randomply generated values.

> ![heatmap_counts_plots](https://user-images.githubusercontent.com/80008461/174682970-ff6b1a86-9c5c-4f86-9b83-9c18a87ab937.png) Heatmap of the counts per score for each feature. 1 and 2 appear to be the most common values per feature, except for class since the only possible scores were 2 and 4. In that case, 2 was more frequent than 4.

