# Credit-Card-Segmentation-ML-Project-
We have identified different segments in the existing customer based on their spending patterns as well as past interaction with the bank.

Data Description: 

Data is of various customers of a bank with their credit limit, the total number of credit cards the customer has, and different channels through which customer has contacted the bank for any queries, different channels include visiting the bank, online and through a call.

Customer key - Identifier for the customer
Average Credit Limit - Average credit limit across all the credit cards
Total credit cards - Total number of credit cards
Total visits bank - Total number of bank visits
Total visits online - total number of online visits
Total calls made - Total number of calls made by the customer.

Key Questions:

How many different segments of customers are there?
How are these segments different from each other?
What are your recommendations to the bank on how to better market to and service these customers?


Steps to follow:

Perform univariate analysis on the data to better understand the variables at your disposal and to get an idea about the no of clusters. Perform EDA, create visualizations to explore data. 
Properly comment on the codes, provide explanations of the steps taken in the notebook and conclude your insights from the graphs. 
Execute K-means clustering use elbow plot and analyse clusters using boxplot 
Execute hierarchical clustering (with different linkages) with the help of dendrogram and cophenetic coeff. Analyse clusters formed using boxplot 
Calculate average silhouette score for both methods. 
Compare K-means clusters with Hierarchical clusters. 
Analysis the clusters formed, tell us how is one cluster different from another and answer all the key questions. 

Part One: Exploratory Data Analysis

Average credit limit:
The majority of records do not have credit or have a low limit.

![image](https://user-images.githubusercontent.com/96012606/202175935-6ef85fcc-e39d-487e-8d11-86e54925b8c8.png)

Total credit cards:
Looks to be normally distributed. I can't help but wonder, why do some many users have more than one credit card?

![image](https://user-images.githubusercontent.com/96012606/202176071-ce9fe953-512a-4b17-baa6-c84567999c89.png)


Total bank visits:
Once again, normally distributed variable.

![image](https://user-images.githubusercontent.com/96012606/202176158-e2a44249-36ef-47da-a480-94b6a9054b03.png)


Part Two: K-means

First, we want to iterate through and view the performance of each value of K for K-means, then using a linegraph to find the elbow of the plot we can select the optimal number of clusters.

![image](https://user-images.githubusercontent.com/96012606/202176311-c7b806dd-046a-4a2d-9ccb-02fd8f04dfb7.png)

Part Three: Hierarchical Clustering

For hierarchical clustering, we begin by evaluating the cophenetic coefficients for each linkage type and also each affinity/metric. Below is a list of said outcomes, ignoring any combination that scores poorly, and ignoring any combination that will result in an error. It's worth noting that scipy has more options than sklearn does for metrics and linkages. While there are several good combinations, I will pick euclidean for the metric and average for linkage as these are options in both scipy and sklearn.

![image](https://user-images.githubusercontent.com/96012606/202176568-a34c9deb-4c15-4948-8021-54b5b53a6285.png)

Part Four: Key Questions

How many different segments of customers are there?
How are these segments different from each other?
What are your recommendations to the bank on how to better market to and service these customers?

Arguably, there are three distinct categories of customers:

In-person users: prefer to handle bank transactions in person. They have the fewest credit cards and the lowest available credit. They are also the most active users.
Phone users: prefer verbally handling transactions remotely.
Online users: prefer digital transactions. They also have the most credit cards and the highest available credit.


We can tailor contact methods to these customer preferences. Online/phone users will probably prefer email/text notifications, while in-person users mail prefer mail notifications and upselling (when at the bank location). Since online users tend to have (and presumably use) the most credit, these may be the demographic we want to target with our next ad campaign, focusing on digit recruiting.





