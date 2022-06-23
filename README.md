# Classification of Breast Cancer Using Machine Learning

## Dataset source:

Original Wisconsin Breast Cancer Database from: UC Irvine Machine Learning Repository (https://archive-beta.ics.uci.edu/ml/datasets/breast+cancer+wisconsin+original)

## ETL:
1. Data was downloaded manually from UC Irvine Repository and stored locally.
2. Data was transformed first by reading it into a pandas dataframe from its '.data' format using pandas "read_table". Null/NaN values were identified and dropped, additionally, unnecessary columns were dropped as well. Further transformation was done by concatenating all column features into one big dataframe containing just 2 columns (category/feature and score). Both dataframes were saved as csv files.

## Descriptive Statistics:
Pandas functions for description of the data was used to get an idea of how the values are distributed.
Data is categorical so a couple descriptive graphs were made:

 >  ![histograms](https://user-images.githubusercontent.com/80008461/175083521-adec927f-1b6c-4658-af4a-895a62734f89.png) Histograms with counts distribution for each features. With the exception of clump thickness and class, in general, the features are right-skewed.
-----------------

> ![pmf_plots](https://user-images.githubusercontent.com/80008461/175077482-3516d64a-6b53-41de-a184-2f3e52d2ff3e.png) Probability plots for each feature.
-----------------

>  ![cdf_plots](https://user-images.githubusercontent.com/80008461/175077165-c198caac-1868-4578-ac72-1c6cce1f6742.png)Cumulative distribution plots for each feature.
-----------------

>   ![violin_plots](https://user-images.githubusercontent.com/80008461/175077222-50041413-5ea2-498e-90e4-476f16c23fa6.png) Violin plots aggregated by class. For the majority of features the most probable values/categories for the observtions are low numbers between 1 and 3 with the exception of class, which only has 2 values. For class, the most probable value is 2 or benign with about 60% of the data falling into that category. Aggregating the data based on class, each feature shows a more spread distribution when the class is malignant (or 4) while the majority of the values/categories for class 2 tend to be below 5 for all features.
-----------------

>  ![box_plots](https://user-images.githubusercontent.com/80008461/175077647-bb58edb6-8162-41ed-8ecc-f7ace7816b79.png) Given the spread of values, boxplots are fairly difficult to visualize the data properly. Violin plots allow for more effective visualization.
-----------------

> ![poisson_comp_plots](https://user-images.githubusercontent.com/80008461/174682879-8cfe8448-056f-4f46-90b3-1bfd195b657d.png) Comparing distribution of score/values to Poisson distribution for roughly the same amount of randomply generated values.
-----------------

> ![heatmap_counts_plots](https://user-images.githubusercontent.com/80008461/174682970-ff6b1a86-9c5c-4f86-9b83-9c18a87ab937.png) Heatmap of the counts per score for each feature. 1 and 2 appear to be the most common values per feature, except for class since the only possible scores were 2 and 4. In that case, 2 was more frequent than 4.
-----------------

>![kde_class_plots](https://user-images.githubusercontent.com/80008461/175079668-2c6f01da-2629-40ab-9424-26235829029b.png) KDE plots for each feature grouped by class. The distribution of single epithelial_cell_size, uniformity_cell_size, marginal_adhesion and normal_nucleoli are very similar which was already seen in the violin plots.
-----------------

>![ecdf_class_plots](https://user-images.githubusercontent.com/80008461/175080909-b905c13c-65a0-4fbf-9619-2726d6fc9eb8.png) Empirical cumulative distribution plots for each feature grouped by class
-----------------
