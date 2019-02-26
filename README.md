# Opioid Anomaly Detection

# Purpose

The percentage of opioids prescribed by health care providers was examined by clustering  from the 2013 Medicare Part D claims in order to determine anomalous amount of claims.

# Contents of Repository 

Opioid_Slides.pdf: Presentable slides of an overview of this project. 

opioid.pdf: This is the pdf documentation of this project. This goes into depth into cleaning of the data, describes the data,
the machine learning algoriths used, and the findings.

data_wrangling.ipynb: ipython notebook where databases for the dataset is create and cleaned.

opioid_statistics.ipynb: ipython notebook where both histograms and scatter plots show an overview of the dataset.

opioid_clustering.ipynb: ipython notebook where machine learning is used to create clusters for anomaly detection.

# Method

Clusters were produced for each health care provider specialties in order to account for additional that my explain variation in opioid prescription. This factors are city population, city social economic status (median income), city temperature, location (longitude and lattice).
The data points were standardized with StandardScaler within the scikit-learn module. Then the data was orthogonalized with principal component analysis (PCA). Of the nine orthogonal dimension, six accounted for 90% of the explained variance. For the top ten specialties that prescribed opioids, K-means method was used to create clusters.  Anomaly were determined from the whishers of cluster’s boxplot of opiods claims rate.


# Results

Analysis of the clustering pattern for the top ten specialties was discussed in the documentation. In order to test model, the clusters were used to determined if the opioid claims rate of five health care professionals who were reported to have committed fraudulent opioid and in the dataset were detected as anomalies. Two of the clearly anomalies, two were borderline, and one failed to be detected as anomalies. Due to the two  known cases of fraud being borderline, the criteria to determine if opioid claims rate is anomalous should be reevaluated. 

# Conclusion

Based on results, these clusters can help identify outliers opioid prescribed
by healthcare providers that may be fraudulent. It is recommended that anomalies
within their cluster (and borderline anomalies) should be investigated for possible
cases for fraud. This methodology was found to be more useful for specialties
that have a narrow range of opioid claims rate such as family practice and internal
medicine. 

For future consideration of anomaly detection, it may be beneficial to
focus on the opioids that are commonly abused, such as oxycodone, rather than
all opioids. An addition factor that should be consider is the dollar amount of
claims which may be a strong indicator of fraud. The dollar amount of claims
was considered by Gleb Esman (https://www.splunk.com/blog/2017/09/28/building-a-60-billion-data-model-to-stop-us-healthcare-fraud-with-splunk-and-machine-learning.html) who worked on a similar project and successfully
identified fraudulent claims within the Interventional Pain Management which
our model should struggle with due to the broad range of opioid
claims rate.


 


