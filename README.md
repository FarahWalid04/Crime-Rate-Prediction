🧠 Crime Pattern Analysis — Data Mining Final Project

📖 Overview

This project applies Data Mining techniques to analyze crime patterns in San Francisco using real-world data.
By combining unsupervised learning (Hierarchical Clustering) and supervised learning (K-Nearest Neighbors - KNN),
the goal is to uncover hidden crime patterns, cluster similar incidents, and classify new data points based on learned structures.

The project demonstrates how clustering can reveal geographical and behavioral relationships in crime data,
while classification helps predict which cluster new incidents belong to — a valuable approach for public safety and urban planning.

🎯 Objectives

Identify natural crime groupings within San Francisco using Hierarchical Clustering

Use KNN classification to categorize new crimes based on discovered clusters

Visualize crime distributions by category, time, and geography

Evaluate model performance using Silhouette Score and Accuracy metrics

📊 Dataset

Source: San Francisco Crime Dataset (Kaggle)

Records: ~800,000 incidents (sampled down to 15,000 for analysis)

Timeframe: January 2003 – May 2015

Key Features:

X, Y: Geographical coordinates

DayOfWeek: Temporal information

PdDistrict: Police district

Category: Type of crime

🧹 Data Preprocessing

Steps performed before modeling:

Sampling: Randomly selected 15,000 records for computational efficiency

Feature Selection: Focused on relevant spatial, temporal, and categorical attributes

Encoding: Label-encoded DayOfWeek and PdDistrict

Scaling: Standardized only X and Y coordinates for clustering accuracy

Train-Test Split: 70% training / 30% testing

🧩 Methodology

🔹 Hierarchical Clustering

Performed agglomerative clustering using Ward linkage and Euclidean distance

Built a dendrogram to visualize cluster hierarchy

Selected 5 clusters as the optimal cutoff

Cluster labels assigned to training samples

🔹 K-Nearest Neighbors (KNN) Classification

Treated cluster labels as pseudo-classes

Trained KNN classifier to predict cluster membership for new records

Evaluated model on unseen data to test generalization

📈 Evaluation Metrics

Metric	Description	Result

Silhouette Score	Measures cluster separation and cohesion	Indicated well-defined clusters

KNN Accuracy	Classification accuracy on test data	~84%

🎨 Visualizations

Several visual tools were used to interpret patterns:

Bar Plot: Number of incidents by crime category

Scatter Plot: X vs Y coordinates colored by cluster

Bar Plot: Number of incidents by hour of the day

Dendrogram: Visualization of hierarchical cluster formation

These visualizations helped confirm spatial crime hotspots and temporal crime trends.

⚙️ Tools & Libraries

Python

NumPy, Pandas

Matplotlib, Seaborn

Scikit-learn

💡 Challenges Faced

Handling imbalanced and noisy data

Selecting the optimal number of clusters

Managing scaling of geospatial features without losing interpretability

Avoiding data leakage between training and test sets

Balancing computational efficiency with model accuracy

👩‍💻 Team Members

Farah Walid:	Visualizations & Report Documentation

Nour Essam:	Hierarchical Clustering & Notebook Markdowns

Basmala Hossam El-Din:	Data Collection & Preprocessing

Rodina Mohamed:	Evaluation Metrics

Mariam Ahmed: KNN Classification

🧠 Conclusion

This project successfully demonstrated how Hierarchical Clustering and KNN classification
can be combined to detect, analyze, and predict crime patterns from real-world datasets.
The integration of clustering and supervised learning provides meaningful insights into urban safety trends
and highlights the power of data mining for decision-making in public security.
