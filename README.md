# CEBD1260 Project and Final

GITHUB project repository for CEBD1260 course


### Overview of Dataset ###
---

Dataset files are saved under the subfolder named 'Data'.  Except for the programs that use the scikit-learn ML library, for example the fetch_20newsgroups method to read data of news articles.


**Online Retail.xlsx**

_Dataset Information_

* The data contains sale transactions between Dec-010-2010 and Dec-09-2011 for a UK-based and registered non-store online retail company selling many multi-themed gifts. 

* The dataset format is csv and the variables are: 
    Attribute | Description
    --------- | ------------
    InvoiceNo | Invoice number
    StockCode | Product code
    Description | Product name
    Quantity | The quantities of each product
    InvoiceDate | Invoice Date
    UnitPrice | Unit price
    CustomerID |Customer number: unique for each customer. 
    Country | Country name)

* Dataset URL source:  [Online Retail Data Set](http://archive.ics.uci.edu/ml/datasets/online+retail)

* The dataset was used on the jupiter notebook program for the Frequent Itemsets and Association Rules, found in the Association_Rule_Mining folder.



**1.csv and 2.cs**

_Dataset Information_

* The data contains measurements of the human body at rest or in movement while walking (through inertial measurement units) with an accelerometer to classify their subjects. The dataset collects data from an Android smartphone accelerometer positioned in the participant's chest pocket, walking in the wild over a predefined path.

* The data are separated by participant (there are 22) and has one file per participant, yet only the first two files were used for the clustering assignment.

* The dataset format is csv and the variables are: time-step, x acceleration, y acceleration, z acceleration

* Dataset URL source:  [User Identification From Walking Activity Data Set](https://archive.ics.uci.edu/ml/datasets/User+Identification+From+Walking+Activity)

* The dataset was used on the jupiter notebook program for the supervised learning model K-means clustering, found in the Clustering folder.



**sample_libsvm_data.txt and sample_multiclass_classification_data.txt from spark mllib 

_Dataset Information_

* The datasets are in fixed column text format.

* Dataset URL source:  [GITHUB (spark/data/mllib)](https://github.com/apache/spark/tree/master/data/mllib)

* The dataset sample_libsvm_data.txt was used in assignment #4 for the jupiter notebook exercises on the Linear Support Vector Machine and Decision Tree Classifier, while the sample_multiclass_classification_data.txt dataset was used on the Multilayer_Perceptron_Classifier.



**cancer_data.csv**

_Dataset Information_

* The dataset format is csv and the variables are: 
    -radius (mean of distances from center to points on the perimeter)
    -texture (standard deviation of gray-scale values)
    -perimeter
    -area
    -smoothness (local variation in radius lengths)
    -compactness (perimeter^2 / area - 1.0)
    -concavity (severity of concave portions of the contour)
    -concave_points (number of concave portions of the contour)
    -symmetry
    -fractal_dimension (coastline approximation)
    -cancer (0 = Benign, 1 = Malignant)  *target*

* Dataset URL source:  [Breast Cancer Wisconsin (Diagnostic) Data Set](http://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnostic%29)

* The dataset was used in the first part of the jupiter notebook program for the K-Nearest Neighbors supervised learning algorithm, found in the Final folder.


**20 newsgroups text dataset**

_Dataset Information_

* The 20 newsgroups dataset comprises around 18000 newsgroups posts on 20 topics split in two subsets: one for training and the other one for testing (or for performance evaluation). 

* Dataset URL source:  [fetch_20newsgroups](http://scikit-learn.org/stable/modules/generated/sklearn.datasets.fetch_20newsgroups.html#sklearn.datasets.fetch_20newsgroups)

* The dataset was used in the second part of the jupiter notebook program for the Supply Vector Machines algorithm, found in the Final folder.



### Frequent Itemsets and Association Rules (Assignment #2) ###
---

In the folder 'Association_Rule_Mining' is an exercise of programming in pyspark the algorithm for Frequent Itemsets and Association rules.  The association algorithm used is pyspark mllib library package FP-Growth (an alternative to Apriori algorithm).

A list of frequent itemsets is listed with a minimum support(percentage of transactions in total transaction that contain an itemset) of .15, and descriptive summary of the output is in the jupiter notebook.



### K-means Clustering (Assignment #3) ###
---

In the folder 'Clustering' is an exercise of applying the unsupervised learning method K-means using pyspark to the 'User Identification From Walking Activity Data Set' dataset. The data is read in through pandas dataframe and saved to text file in which a spark session reads in the text file. 
The model is created with the k=2 to specify the number of clusters the algorithm should find.

Thw K was determined by sqrt(n) because of a simple approach of how to choose k documented in article [A Detailed Introduction to K-Nearest Neighbor (KNN) Algorithm](https://saravananthirumuruganathan.wordpress.com/2010/05/17/a-detailed-introduction-to-k-nearest-neighbor-knn-algorithm/).

Two final clusters are printed at the end of the program to identify the centroid of the three measurements of acceleration in X, Y, Z directions ('xaccel', 'yaccel', 'zaccel').



### Assigment #4 ###
---

In folder 'Assignment4' there are three jupiter notenotebooks exercises for supervised learning classification that is taken from the spark MLlib main guide.
These algorithms are:
1. [Linear Support Vector Machine](https://spark.apache.org/docs/latest/ml-classification-regression.html#linear-support-vector-machine)
2. [Decision Tree Classifier](https://spark.apache.org/docs/2.1.0/ml-classification-regression.html#decision-tree-classifier)
3. [Multilayer Perceptron Classifier](https://spark.apache.org/docs/latest/ml-classification-regression.html#multilayer-perceptron-classifier)



### Final Assigment ###
---
The jupiter notebook under the folder 'Final' (final_assignment.ipynb) has two questions to answer. 

The **_first part_** of the assignmnent is a program classifies data from a cancer diagnostic database to a target variable.  The k-nearest neighbors algorithm was used
for classifying the data and to find/predict a target attribute for a new observation.

In the training phase the dataset is split into train data and its target data. 

In the testing phase the learning model KNeighborsClassifier is applied and fit to the model with the training and target data.


The **_second part_** of the assignment is a program that classifies text to a topic or category.  The support vector machines algorithm was used to classify the data to a target attribute. This exercise also lists corrections to statements in the draft program for five bugs purposely written into the code.

Both of these algorithms are grouped in the supervised learning for classification.


### How to run the jupiter notebook programs ###
---

1. Start a jupter and pyspark session through docker.
2. Run the localhost session in Internet Explorer
3. Upload the jupiter notebooks (in individual folders) to jupier main folder.
4. Upload 'Data folder' containing all the datasets mentioned in README file .
5. Run program statements for each notebook.


