# Outlier Detection Techniques
- Scatter plot
- Box plot
- Z-score
- IQR
- DBSCAN clustering: Clustering algorithm. Everything else except core and border points is called noise points. The downside with this method is that the higher the dimension, the less accurate it becomes.
- Isolation forest: Unsupervised learning algorithm. It explicitly isolates anomalies instead of profiling and constructing normal points and regions by assigning a score to each data point. It takes advantage of the fact that anomalies are the minority data points and that they have attribute-values that are very different from those of normal instances. This algorithm works great with very high dimensional datasets and it proved to be a very effective way of detecting anomalies.
- Robust Random Cut Forest: Random Cut Forest (RCF) algorithm is Amazon’s unsupervised algorithm for detecting anomalies. It works by associating an anomaly score as well. Low score values indicate that the data point is considered “normal.” High values indicate the presence of an anomaly in the data. The definitions of “low” and “high” depend on the application but common practice suggests that scores beyond three standard deviations from the mean score are considered anomalous. The details of the algorithm can be found in this paper.
The great thing about this algorithm is that it works with very high dimensional data. It can also work on real-time streaming data (built in AWS Kinesis Analytics) as well as offline data.
