# CEBD1260 Project and Final

GITHUB project repository for CEBD1260 class


### Overview of Dataset ###


==*_Under folder Data\_*==


*1. Online Retail.xlsx*

_Dataset Information_

..*The data contains sale transactions between 01/12/2010 and 09/12/2011 for a UK-based and registered non-store online retail company selling many multi-themed gifts. 

..*The dataset format is csv and the variables are: 
    -InvoiceNo (Invoice number)
    -StockCode (Product code)
    -Description (Product name)
    -Quantity (The quantities of each product)
    -InvoiceDate (Invice Date)
    -UnitPrice (Unit price)
    -CustomerID (Customer number): unique for each customer. 
    -Country (Country name)


..*Dataset URL source:  [Online Retail Data Set](http://archive.ics.uci.edu/ml/datasets/online+retail)


For the frequent itemset algorithm , a few transactions where extracted within the file so that the code would not error due to the size of the pyspark data object.




Support: is the percentage of transactions in T that contain all three '21754', '22748' and '22745' together (20% of all orders had the three items together).



The rule X => Y holds with support s if s% of transactions in  D contain X and Y. 

Rules that have a s greater than a user-specified support is said to have minimum support.





Confidence: is the percentage of transactions in T, containing '21754', '22748', that also contain '22745'. 

In other words, the probability of having '22745', given that '21754', '22748' is already in the basket. (65% of orders having products '21754', '22748', also bought '22745'.)



When the resulting confidence is smaller than minimum confidence, in this case .40, the association rule  ['21754', '22748'] => ['22745'] is dropped, otherwise it is added to the result. So, the resulting confidence for this itemset  ['21754', '22748', '22745'] is 1 > .40, meaning that invoices with product '22745' also contained products '21754', '22748'.






The rule X => Y holds with confidence c if c% of the transactions in D that contain X  also contain Y.

Rules that have a c greater than a user-specified confidence is said to have minimum confidence.


Reference: 
https://www.quora.com/What-is-support-and-confidence-in-data-mining

http://wimleers.com/article/fp-growth-powered-association-rule-mining-with-support-for-constraints





*2. Filename '1.csv' and '2.csv'*


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

Assignment 2 is to program in pyspark the algorithm for Frequent Itemsets and Association rules.  It identifies the 

and to decides on the result based on the support and confidence formula.




### K-means Clustering ###







### Assigment #4 ###


Linear_SVM

Decision_Tree_Classifier


Multilayer_Perceptron_Classifier



### Final Assigment ###






