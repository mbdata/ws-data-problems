# Title

# Introduction
This task requires us to use a sample dataset of request logs, which contain the geographic locations of the requests and several POIs. The process involves cleaning the dataset by filtering out duplicate requests; assigning these requests to a POI and finding the distances between them; using descriptive statistics to analyze these distances; and to visualize the requests and their respective POIs.

# Steps completed:
1. [Preliminary research](http://htmlpreview.github.com/?https://github.com/mbdata/ws-data-problems/blob/master/notebooks/technical_challenge_preliminary_research.html) was performed in Jupyter Notebook. This involved experimenting with the dataset by trying out various distance calculations - the earth, being an ellipse, is not the simplest surface on which to calculate the distance between two points - and attempting to assign requests to POIs with clustering methods such as K-Means and DBSCAN, which we found did not provide the most accurate assignments to POIs.
2. The data was loaded to Databricks Community Edition and opened in a Spark notebook.
3. [Spark jobs](http://htmlpreview.github.com/?https://github.com/mbdata/ws-data-problems/blob/master/notebooks/EQ%20Works%20Challenge%20-%20Spark%20Jobs.html) which processed the data were created.
4. The cleaned and labeled data was exported and presented in Jupyter Notebook, where the remainder of the [analysis and modeling](http://htmlpreview.github.com/?https://github.com/mbdata/ws-data-problems/blob/master/notebooks/Analysis%20and%20Modeling.ipynb) of the data was performed.

# POI observations
1. The dataset with the POIs is small, containing only 4 points, but they are widely distant from one another by hundreds of kilometers.
2. Requests are clustered mainly in Canadian cities, but may end up being assigned to a POI in a different city than to which they belong. For example, we found that there was a cluster of points in Ottawa, but they would have been assigned to Montreal given that this was the nearest POI. This forced us to re-evaluate how we assigned requests to POIs, in this task.

# Conclusion
1. Assigning requests to POIs by calculating the distances to all POIs and finding the closest one, by using brute force, is not feasible, even in a Spark environment.
2. Clustering with K-Means, using POIs as starting points, could be a potentially good solution in cases when many POIs are provided.
3. In cases like the one presented in this task, when POIs are centers of distinct geographical locations (cities or provinces), the most efficient solution would be to assign the requests to POIs belonging to the same geographical location, and then to calculate the distances to the assigned POI. This would significantly reduce the amount of irrelevant calculations.


# Cleanup and Labeling
Here is the result of the [cleanup and labeling](http://htmlpreview.github.com/?https://github.com/mbdata/ws-data-problems/blob/master/notebooks/EQ%20Works%20Challenge%20-%20Spark%20Jobs.html).

# Analysis and Modeling
The [analysis and modeling](http://htmlpreview.github.com/?https://github.com/mbdata/ws-data-problems/blob/master/notebooks/technical_challenge_preliminary_research.html).
