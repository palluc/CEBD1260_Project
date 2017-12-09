# CEBD1260 Project and Final

GITHUB project repository for CEBD1260 course


### Overview of Dataset ###
---

==*_ Data files are saved under the subfolder named 'Data' _*==


*	Online Retail.xlsx*

_Dataset Information_

..* The data contains sale transactions between Dec-010-2010 and Dec-09-2011 for a UK-based and registered non-store online retail company selling many multi-themed gifts. 

..* The dataset format is csv and the variables are: 
    Attribute | Description
    InvoiceNo | Invoice number
    StockCode | Product code
    Description | Product name
    Quantity | The quantities of each product
    InvoiceDate | Invoice Date
    UnitPrice | Unit price
    CustomerID |Customer number: unique for each customer. 
    Country | Country name)


..* Dataset URL source:  [Online Retail Data Set](http://archive.ics.uci.edu/ml/datasets/online+retail)


*2.  '1.csv' and '2.csv'*


_Dataset Information_


..*The data contains measurements of the human body at rest or in movement while walking (through inertial measurement units) with an accelerometer to classify their subjects. The dataset collects data from an Android smartphone accelerometer positioned in the participant's chest pocket, walking in the wild over a predefined path.

..*The data are separated by participant (there are 22) and has one file per participant, yet only the first two files were used for the clustering assignment.

..*The dataset format is csv and the variables are: time-step, x acceleration, y acceleration, z acceleration

..*Dataset URL source:  [User Identification From Walking Activity Data Set](https://archive.ics.uci.edu/ml/datasets/User+Identification+From+Walking+Activity)

..*The dataset was used on the supervised learning model K-means clustering

..* K was determined by sqrt(n) because of a simple approach of how to choose k documented in article [A Detailed Introduction to K-Nearest Neighbor (KNN) Algorithm] (https://saravananthirumuruganathan.wordpress.com/2010/05/17/a-detailed-introduction-to-k-nearest-neighbor-knn-algorithm/)





*4. Filename 'sample_libsvm_data.txt' and 'sample_multiclass_classification_data.txt' from spark mllib 



..*The datasets are in fixed column text format.


..*Dataset URL source:  [GITHUB (spark/data/mllib)](https://github.com/apache/spark/tree/master/data/mllib)


..*The dataset sample_libsvm_data.txt was used on the Linear Support Vector Machine and Decision Tree Classifier, while the sample_multiclass_classification_data.txt dataset was used on the
Multilayer_Perceptron_Classifier





*3. Filename 'cancer_data.csv'*




..*The dataset format is csv and the variables are: 
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

..*Dataset URL source:  [Breast Cancer Wisconsin (Diagnostic) Data Set](http://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnostic%29)

..*The dataset was used on the K-Nearest Neighbors supervised learning algorithm.








### Frequent Itemsets and Association rules ###
---

Assignment 2 is to program in pyspark the algorithm for Frequent Itemsets and Association rules.  It identifies the 

and to decides on the result based on the support and confidence formula.




### K-means Clustering ###
---
In this assignment 



### Assigment #4 ###
---

In folder 'Assignment4' there are three jupiter notenotebooks exercises for supervised learning classification that is taken from the spark MLlib main guide.
These algorithms are:
    1.[Linear Support Vector Machine](https://spark.apache.org/docs/latest/ml-classification-regression.html#linear-support-vector-machine)
    2.[Decision Tree Classifier](https://spark.apache.org/docs/2.1.0/ml-classification-regression.html#decision-tree-classifier)
    3.[Multilayer Perceptron Classifier](https://spark.apache.org/docs/latest/ml-classification-regression.html#multilayer-perceptron-classifier)



### Final Assigment ###
---
The jupiter notebook under the folder 'Final' (final_assignment.ipynb) has two questions to answer. 

The **_first part_** of the assignmnent is a program classifies data from a cancer diagnostic database to a target variable.  The k-nearest neighbors algorithm was used
for classifying the data and to find/predict a target attribute for a new observation.

In the training phase the dataset is split into train data and its target data. 

In the testing phase the learning model KNeighborsClassifier is applied and fit to the model with the training and target data.


The **_second part_** of the assignment is a program that classifies text to a topic or category.  The support vector machines algorithm was used to classify the data to a target attribute. This exercise also lists corrections to statements in the draft program for five bugs purposely written into the code.

Both of these algorithms are grouped in the supervised learning for classification.





