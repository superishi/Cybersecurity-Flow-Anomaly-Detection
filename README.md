# Cybersecurity-Flow-Anomaly-Detection
Model built to detect anomalous flows in a network.

Used K-means clustering on time series data with Dynamic Time Warping(DTW) as the distance metric to cluster devices according to flow behaviour.

Following this, an ad hoc anomaly detection model was creating using K-nearest-neighbors algorithm with probabilities outputs.

Steps:
1. Pre-process data by aggregating flow data in both hours and 3 hours. (DataPreprocessing.ipynb)
2. Apply SVD dimensionality reduction to flow data. (DataPreprocessing.ipynb)
3. Engineer data into time series format. (weekdayTimeSeriesClustering3hours.ipynb, weekendTimeSeriesClusteringhourly.ipynb)
4. Use K-means clustering with DTW for clustering, hyperparameter testing to find optimal cluster number. (weekdayTimeSeriesClustering3hours.ipynb, weekendTimeSeriesClusteringhourly.ipynb)
5. Use clusters derived from previous step, create K-nearest-neighbors model with probability output to classify flow as anomalous or benign. (WeekendAnomalyClassification.ipynb, WeekdayAnomalyClassification.ipynb)
