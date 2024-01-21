# Mobility Pattern Analysis

### Description 

The project revolves around the analysis of mobility patterns within the Geolife Trajectories dataset using a Python script. Leveraging the KMeans algorithm for spatial clustering, the script identifies distinct clusters, shedding light on specific movement behaviors. Visualization through scatter plots intuitively captures these patterns, complemented by a detailed statistical analysis that provides quantitative insights for each cluster. This holistic approach aims to achieve a comprehensive understanding of mobility dynamics within the dataset.

## Dataset
[Get Dataset] https://www.kaggle.com/datasets/arashnic/microsoft-geolife-gps-trajectory-dataset

[Short Dataset Description] This GPS trajectory dataset was collected in (Microsoft Research) Geolife project by 178 users in a period of over four years (from April 2007 to October 2011). A GPS trajectory of this dataset is represented by a sequence of time-stamped points, each of which contains the information of latitude, longitude and altitude. 

# Data Visualization && Preprocessing

This Python script **DataPreprocessing.ipynb** reads location trajectory data from ".plt" files within a dataset containing 181 folders. It defines functions for reading and visualizing the trajectory, iterates through the dataset, and extracts trajectory data from the first ".plt" file encountered in each subfolder. The trajectory visualization function is included but commented out. It iterates through folders, reads ".plt" files, removes duplicates, handles outliers using the Interquartile Range method, and saves cleaned data in a structured directory. The script ensures data integrity, addresses anomalies, and prepares the dataset for further analysis.

# Elbow Method

This Python script inside of **GPSApplication.ipynb** implements the Elbow Method for determining the optimal number of clusters (k) in KMeans clustering for location trajectory data. It iterates through folders of the Geolife Trajectories dataset, reads ".plt" files, extracts latitude and longitude data, and applies the Elbow Method to evaluate the inertia (within-cluster sum of squares) for various values of k. The resulting plot helps identify an elbow point, aiding in the selection of an appropriate number of clusters for subsequent analysis.

# KMeans

This Python script inside of **GPSApplication.ipynb** utilizes the KMeans algorithm for spatial clustering of cleaned location trajectory data from the Geolife Trajectories dataset. It iterates through folders of preprocessed data, applying spatial clustering with a predefined number of clusters (num_clusters = 2). The results, including a spatial cluster label for each data point, are saved and organized in a dedicated directory ("ClusteringResults_1"). The script incorporates safeguards for handling convergence warnings and skips files with insufficient samples, providing an automated and organized approach to spatial clustering analysis on geospatial data.

# Results
This Python  **Results.ipynb** script analyzes the results of KMeans spatial clustering on cleaned location trajectory data from the Geolife Trajectories dataset. The "Show Result Plots" section generates scatter plots for each clustering result file, visually representing the spatial distribution of data points color-coded by cluster. The subsequent "Extract Statistics" section iterates through the clustering results, extracting and printing essential spatial and altitude statistics for each cluster, including centroid coordinates and the number of points. This comprehensive analysis provides both visual insights into the cluster distribution and quantitative information on the characteristics of each spatial cluster, facilitating a thorough understanding of the clustering outcomes for further interpretation and evaluation.

# Conclusion
This code successfully analyzes mobility patterns within the Geolife Trajectories dataset using spatial clustering. Through KMeans clustering, distinct spatial clusters are identified, visualized, and statistically characterized. The scatter plots offer an intuitive representation of mobility patterns, while the extracted statistics provide quantitative insights.
