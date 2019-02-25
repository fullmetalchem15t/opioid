# Opioid Anomaly Detection

# Purpose

The percentage of opioids prescribed by health care providers was examined by clustering  from the 2013 Medicare Part D claims in order to determine anomalous amount of claims given a health care providers specialty and cluster.

# Contents of Repository 

Opioid_Slides.pdf: Presentable slides of an overview of this project. 

opioid.pdf: This is the pdf documentation of this project. This goes into depth into cleaning of the data, describes the data,
the machine learning algoriths used, and the findings.

data_wrangling.ipynb: ipython notebook where databases for the dataset is create and cleaned.

opioid_statistics.ipynb: ipython notebook where both histograms and scatter plots show an overview of the dataset.

opioid_clustering.ipynb: ipython notebook where machine learning is used to create clusters for anomaly detection.

# Method

Clusters were produced for each health care provider specialties in order to account for additional that my explain variation in opioid prescription. This factors are city population, city social economic status (median income), city temperature, location (longitude and lattice).

The data points were standardized with StandardScaler within the scikit-learn module. Then the data was orthogonalized with principal component analysis (PCA). Of the nine orthogonal dimension, six accounted for 90% of the explained variance. For the top ten specialists that prescribed opioids, K-means method was used to create clusters.


# Results

Analysis of the clustering pattern was discussed in the documentation.

# Conclusion


 


