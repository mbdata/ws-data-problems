# Title

# Introduction
This task requires us to use a sample dataset of request logs, which contain the geographic locations of the requests and several POIs. The process involves cleaning the dataset by filtering out duplicate requests; assigning these requests to a POI and finding the distances between them; using descriptive statistics to analyze these distances; and to visualize the requests and their respective POIs.

# Steps completed:
1. [Preliminary research](http://htmlpreview.github.com/?https://github.com/mbdata/ws-data-problems/blob/master/notebooks/technical_challenge_preliminary_research.html) was performed in Jupyter Notebook. This involved experimenting with the dataset by trying out various distance calculations - the earth, being an ellipse, is not the simplest surface on which to calculate the distance between two points - and attempting to assign requests to POIs with clustering methods such as K-Means and DBSCAN, which we found did not provide the most accurate assignments to POIs.
2. The data was loaded to Databricks Community Edition and opened in a Spark notebook.
3. [Spark jobs](http://htmlpreview.github.com/?https://github.com/mbdata/ws-data-problems/blob/master/notebooks/EQ%20Works%20Challenge%20-%20Spark%20Jobs.html) which processed the data were created.
4. The cleaned and labeled data was exported and presented in Jupyter Notebook, where the remainder of the [analysis and modeling](http://htmlpreview.github.com/?https://github.com/mbdata/ws-data-problems/blob/master/notebooks/Analysis%20and%20Modeling.ipynb) of the data was performed.

# POI assumptions and hypotheses

# Conclusion

# Cleanup and Labeling
Here is the result of the [cleanup and labeling](http://htmlpreview.github.com/?https://github.com/mbdata/ws-data-problems/blob/master/notebooks/EQ%20Works%20Challenge%20-%20Spark%20Jobs.html).

# Analysis and Modeling
The [analysis and modeling](http://htmlpreview.github.com/?https://github.com/mbdata/ws-data-problems/blob/master/notebooks/technical_challenge_preliminary_research.html).
