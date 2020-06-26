# Cryptocurrencies

## Project Overview
The following repository includes Jupyter notebooks for unsupervised machine learning models for discovering unknown patterns.

The *Practice* folder includes notebooks related to iris data and shopping data.

Machine learning models were built using different clustering and transformation techniques (including K-means Algorithm). Feature elimination and extraction techniques were applied to reduce dimensions—including Principle Component Analysis (PCA). Preprocessed (cleaned) data was then plotted in 2 and 3 dimensions.

The *Challenge* folder contains a notebook related to cryptocurrencies data.

For the cryptocurrencies challenge, the following steps were followed:
1. Preprocess the data.
    * Organize data into DataFrames
    * Convert to numeric format, so the machine learning model could be fit accordingly
2. Reduce data dimensions using PCA.
    * Dimensions were reduced to 3 principle components
    * PCA data was transformed into a DataFrame
3. Cluster data using K-means
    * An elbow curve was created to identify the best value of K (i.e. best number of clusters)
    * The best value of K was determined to be 4
    * The model was fit and used to predict class
    * The predicted class was added to the PCA DataFrame
    * The PCA DataFrame was joined with the original data into the DataFrame clustered_df (Note: some columns are non-numerical, so the analysis required those columns not to be present prior to this step)
4. Visualize results using Plotly Express and hvplot
    * 3D plot showing all 3 principle components provides a nice visual which represents the dimensions realistically
    * Table shows the same information as the clustered_df DataFrame without the principle components
    * 2D scatter plot renders a visualization that is possibly inappropriate since there are 3 principle components; had the dimensions been reduced to two principle components, this plot may have been easier to interpret


## Resources
* Data Sources: crypto_data.csv, iris.csv, new_iris_data.csv, new_iris_data2.csv, shopping_data.csv, shopping_data_cleaned.csv
* Language: Python
* Libraries: Pandas, Scikit-learn, Plotly
* Software: Jupyter Lab 1.2.6

