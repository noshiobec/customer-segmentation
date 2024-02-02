## Data-Driven Marketing Optimization: Leveraging Customer Segmentation in Online Retail Purchasing

The project focuses on utilizing data-driven marketing strategies through exploratory data analysis conducted with Python programming and visualization using the Microsoft Power BI tool. Specifically, it explores four unsupervised machine learning clustering models (K-means, spectral, agglomerative, and birch clustering) for customer segmentation. These segmented groups are further classified using supervised classification models (logistic regression, random forest, naive Bayes, and support vector machine).

### Problem definition:
Due to the rise in online retailing, many retailers struggle with sales and low conversion rates and this project investigates using machine learning models to help tailor marketing strategies to 
increase campaign effectiveness and improve sales.

### Aim:
This project aims to optimize sales in online retail purchasing through data-driven marketing,
leveraging machine learning models to build an effective customer segmentation strategy.

### DATASET COLLECTION
The data used in this project was obtained from the UCI repository. It's known as the Online Retail II Dataset, and it provides valuable insights into customer behaviour and purchasing patterns in the online retail industry (Chen 2019) . The attribute information of the dataset is shown below. [UCI Repository](https://archive.ics.uci.edu/dataset/502/online+retail+ii).

**Attribute Information:**

* InvoiceNo: The unique Invoice number for purchases made. It is a 6-digit integral number and one starting with 'c' indicates a cancellation.

* StockCode: Unique Product code. Product-specific 5-digit integral numbers.•

* Description: Item name and description. It is nominal.

* Quantity: The quantities of each  item per transaction. It is numeric.

* InvoiceDate: Invoice date and time.

* UnitPrice: Unit price. Numeric. Product price per unit (£).

* CustomerID: A five-digit number uniquely assigned to each customer.

* Country:  The name of the country where a customer resides.

### DATA PREPROCESSING
During data preprocessing, missing values in the dataset were addressed by removing records with missing customer IDs, eliminating duplicates and invoices indicating no sales, and filtering out abnormal numeric values. Feature selection involved adding columns for total price and description length, as well as extracting date-related features for deeper analysis. These steps ensured dataset integrity and enhanced the dataset for subsequent analyses.

### Data Analysis
The data analysis phase involved exploring various columns to extract insights. Summary statistics, like mean, median, counts, etc., were calculated for all columns. Exploratory data analysis (EDA) helps uncover patterns, trends, and issues in the dataset, enabling informed conclusions for analysis or modelling. Key aspects such as missing values, outliers, and variations are identified using descriptive statistics and visual tools like histograms and scatter plots. EDA aids in recognizing relationships, distributions, and anomalies, facilitating pattern detection and hypothesis development 

![image](https://github.com/noshiobec/customer-segmentation/assets/96450822/d3fa42b3-6968-489f-990a-e2a38de1551d)       
**Summary Statistics**

![image](https://github.com/noshiobec/customer-segmentation/assets/96450822/3f713436-195a-43f2-81e8-80e728d1b61f)        
**Word Cloud**


### Model Selection
During the model selection phase, various clustering algorithms, including K-means, Agglomerative Clustering, DBSCAN, Mean Shift, Spectral Clustering, and Birch Clustering, were evaluated for their suitability in market segmentation. These algorithms were assessed based on their ability to identify similar groups within a dataset while minimizing dissimilarity between different groups. For classification model selection, Support Vector Machines (SVM), Logistic Regression, Random Forest, and Naive Bayes Classifier were considered. SVMs are effective for high-dimensional data and aim to maximize the margin between classes, while Logistic Regression is simple and interpretable, suitable for linear relationships between features and outcomes. Random Forest is robust for handling large datasets and preventing overfitting, while Naive Bayes Classifier is efficient in estimating probabilities with a simple structure. Each algorithm was chosen based on factors such as dataset characteristics, model interpretability, and performance requirements

### Clustering Model Implementation and Results Analysis
The clustering model implementation and results analysis phase involved evaluating four clustering models, namely K-means, Agglomerative, Spectral, and Birch clustering, to determine the optimal number of clusters for segmentation. Evaluation metrics such as the elbow method, silhouette score, and Davies-Bouldin Index were used to select the ideal cluster point, with cluster point 3 identified as the most suitable choice. Each model was fitted, and visualizations such as scatter plots were used to understand the clustering results. K-means and Agglomerative clustering emerged as the top choices for segmenting customers, with K-means ultimately selected as the best model due to slightly better silhouette score values for the three clusters. The saved K-means clustering algorithm revealed class 2 with the highest number of customers, followed by class 1 and then class 0, representing distinct customer segments within the dataset.

### Classification Models Implementation and Results Analysis
A comprehensive evaluation of multiple classification models was conducted in this project, utilizing a train/test split methodology. The SVM model demonstrated an accuracy of 96.39%, while Logistic Regression and Random Forest models achieved higher accuracy rates of 99.71%. Logistic Regression notably outperformed other models in precision, recall, and f1 score, indicating a strong balance between precision and recall. However, Naïve Bayes presented the shortest execution time, showcasing its cost-efficiency despite achieving lower metric values. Cross-validation results mirrored those of the train/test split, with Logistic Regression consistently performing the best and Naïve Bayes showing its computational advantage. Logistic Regression emerges as the top-performing model overall, but Naïve Bayes may offer a cost-effective alternative for resource optimization.

![image](https://github.com/noshiobec/customer-segmentation/assets/96450822/4469fa12-c7e1-4c0c-877b-cc9a63eda45c)

![image](https://github.com/noshiobec/customer-segmentation/assets/96450822/1b1ae45a-1a0d-4c09-8f98-7e8b262f808b)



### Power BI Interactive Sales Dashboard Analysis

The Power BI interactive sales dashboard in this project aimed to transform a cleaned dataset into a visually appealing and insightful tool for an online retail business. Key visualizations included top and bottom five countries by total sales, cumulative sales figures across months and years, geospatial visualization of customers and total sales, percentage distribution of segmented customers, and customer segments showing average RMF values. Interactive elements like slicers allowed users to dynamically refine the analysis by altering parameters such as periods, categories, or locations. Key performance metrics (KPIs) provided at-a-glance insights into critical business indicators. The dashboard's effectiveness stemmed from its interactivity, allowing users to tailor their analysis effortlessly and draw meaningful connections between different visualizations. This holistic view empowered stakeholders to glean actionable insights and steer strategic initiatives with precision, making it a versatile decision-making tool adaptable to diverse business scenarios.

![image](https://github.com/noshiobec/customer-segmentation/assets/96450822/d538b6ec-db76-42d8-8e9d-4dcaab600b73)


### ANALYSIS INSIGHT
* Sales Trends:
  * Saturday had significantly lower sales compared to other weekdays.
  * November had the highest sales, followed closely by December.
* Yearly Analysis:
  * 2009 had the lowest total sales, possibly due to records only being available for December.
* Correlation Findings:
  * A correlation plot revealed a high positive correlation between price and quantity.
* Distribution Visualization:
  * Histogram plots were used to visualize the distribution of numerical variables.
* Keyword Identification:
  * A word cloud highlighted frequently appearing keywords in order descriptions, identifying popular items such as "red retrospect," "lunch bag," and "water bottle."
 *Customer Insights:
  * After data cleaning, it was found that there were 5878 unique customers, indicating multiple purchases by many customers.

### Insights from Segmentation Results:
* Group 0:
  * Comprises a smaller number of customers.
  * Exhibits substantial monetary value and high purchase frequency.
  * Represents a prime target for personalized marketing efforts.
  * Higher spending and frequent interactions present an opportunity for further engagement and revenue growth.
* Group 1:
  * Signifies customers with a strong emphasis on recency of purchase.
  * The distinctiveness of this segment is reaffirmed by segmentation results aligning with insights from the box plot.
  * Tailoring strategies to encourage more frequent purchases can lead to sustained sales growth.
* Group 2:
  * Characterized by lower recency, frequency, and monetary values compared to other groups.
  * Offers a unique challenge and opportunity for re-engagement strategies.

### Insights from Machine Learning Algorithm Selection:
* Rigorous comparisons with other prominent models demonstrated K-means' superiority in delivering more meaningful and actionable segmentation outcomes.
* K-means was selected due to its capacity to handle the inherent complexities of customer data.
It could discern distinct patterns even in the presence of noise and variability, allowing for the extraction of coherent customer segments.
* K-means' ability to minimize intra-cluster variance and maximize inter-cluster variance aligned seamlessly with the project's goal of extracting meaningful segments exhibiting substantial differences.
