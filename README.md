# machine_learning_project-unsupervised-learning
### Project Description:

In this project, we will apply unsupervised learning techniques to a real-world data set and use data visualization tools to communicate the insights gained from the analysis.

The data set for this project is the "Wholesale Data" dataset containing information about various products sold by a grocery store.
The project will involve the following tasks:

-	Exploratory data analysis and pre-processing: We will import and clean the data sets, analyze and visualize the relationships between the different variables, handle missing values and outliers, and perform feature engineering as needed.
-	Unsupervised learning: We will use the Wholesale Data dataset to perform k-means clustering, hierarchical clustering, and principal component analysis (PCA) to identify patterns and group similar data points together. We will determine the optimal number of clusters and communicate the insights gained through data visualization.

The ultimate goal of the project is to gain insights from the data sets and communicate these insights to stakeholders using appropriate visualizations and metrics to make informed decisions based on the business questions asked."

## Project Outcomes

1. exploratory data analysis and pre-processing:
- The dataset is made up of a numerical featuers with no missing values
- Inspecting data skewness hint the presence of outliers which are visible in the histogram.
- Another important thing to visualize is the correlation of our dataset, which by the help of the heatmap, we can confirm its presence and intensity. This is further proved by the visual pair plots.
- Z-score is used to detect outliers and determine their significance. The following is done to clip the outliers: Let's go with clipping which will do the following:

* round up anything above 0.95 percentile
* round down anything below 0.5 percentile
- Before applying PCA to the dataset, we need to scale it. StandardScaler() is used. This allows us to see the feature importance in the dataset. 
  
2. . KMeans clustering:
Through the tria-and-error process, 6 clusters are decided.  This interestingly gives a leaves a good chunck of featuers with no cluster, which makes sense because of the nature of our dataset. Features like 'Region' and 'Channel' will nave their separate classification which leaves the products to occupy other clusters. 
   
4. . hierarchical clustering:
The dendogram shows us further information about the clusters. The relationship between trees is visible and there are some clusters that share the same tree node which signifies strong relationship among them. Features like Fresh, Milk, Grocery, and Frozen share the same nodes and it shows that they have strong relationship.
   
6. . PCA:
PCA's plot is crucial in determining the variance of every feature. Now we can see that the how much variance of each feature is found in the original dataset. Clearly, the first 2 features make over 70 percentage while the last two are less significant. We would take this information and combine it with others to learn more about our clusters.

The conclusion below is made by taking Kmeans clustering, Hierarchical clustering, and PCA into account: 

* Products in the Fresh, Milk, and Grocery categories are popular among the customers and they make a big number of the wholesale distributor's sales. The make more than 90 percent of all sales. 
* Fresh and Frozen are found in many clusters compared to other features.We find them in 4 out of 6 clusters.  This means that no matter what buyers are buying, they most likely end up purchasing Fresh and Frozen as well. 
   



