# E-Commerce-Product-Range-Analysis
Practicum program final project 
E-Commerce: Product Range Analysis

**Task:**

****Analyze the store's product range.

- Carry out exploratory data analysis
- Analyze the product range
- Formulate and test statistical hypotheses

# Table of Contents:

<div style="height:10px;"></div>

1. [Data Overview and Preprocessing:](#-Preprocessing)
   * [Download the data, Renaming Column Names, Adding necessary column and Study the general information (using info(), describe..)](#-info)
   * [Check for missing values, duplicated rows and other abnormal data (such as: zero and negative values) and choose appropriate ways to deal with them. Chande data type if needed](#-missing)
   * [Study the distribution and dispertion (outliers)](#-dist)
   * [Trying to find color and size traits out of product names](#-color)


<div style="height:5px;"></div>

2. [Product Description Analysis:](#-Analysis)
   * [Create a corpus out of product descriptions.](#-corpus)
   * [Clean up the corpus and removed stopwords etc,Eliminate grammatical variations via stemming](#-clean)
   * [Create a Term-Frequency Inverse Document Frequency (TF-IDF) matrix.](#-tfidf)
   * [Clculate from the TF-IDF the corpus distance matrix comparing the relative similarity.](#-distance)
   * [Use the distance matrix to build a dendrogram from which the number of clusters will be detrmined](#-dendrogram)
   * [Using Kmean to form the clusters](#-kmeans)
   * [Study the term frequencies for each cluster.](#-terms_freq)
   * [Based on the term frequencies, identify product category keywords for each cluster.](#-keywords)
   * [Categorizing the products in the store differently in order to get result that enable better understanding of product range.](#-categorization)
   * [Calculating monthly revenue and monthly cumulating revenue to detect the trend](#-revenue) 
   * [Splitting products by category and finding: 1. the leading categories regarding the number of items in each category 2. the leading categories in sales](#-split)
   * [Finding the top ten selling products](#-selling)
   * [Examining Refunds: by total amount and by frequency](#-refunds)

   
    
<div style="height:5px;"></div>

3. [Product Bundle(Basket) Analysis and Recommender System:](#-recommender)
   * [Create a basket for each transaction (invoice) and study the popullarity for products to appear (in any transaction/invoice) as well as for their different combinations by using Apriori Algorithm](#-basket)
   * [Calculate other Basket metrics using association_rule method in order to realize how to expand sails in the basket level by recommending additional products](#-additional)
   * [Studying product similarities in order to realize how to mantain and increase profits (in a basket level) by recommanding sustitutional/interchangable products](#-interchangable)


<div style="height:5px;"></div> 

4. [Product Market Values Analysis:](#-market)
   * [Calculate product recency-frequency-monetary (RFM Metrics)](#-rfm)
   * [Study product RFM distributions (in order to determine the segmentation split)](#-split)
   * [Categorize products based on K-MEANS](#-categorize)
   * [Charactarize the product clusters based on R, F and M scores](#-RFM_scores)
 
   
<div style="height:10px;"></div>


5. [Conclusions and Suggestions:](#-conclusions)
 
<div style="height:10px;"></div>

**Description of the data:**

The dataset contains the transaction history of an online store that sells household goods.

The file `ecommerce_dataset_us.csv` contains the following columns:

`InvoiceNo` — order identifier

`StockCode` — item identifier

`Description` — item name

`Quantity`

`InvoiceDate` — order date

`UnitPrice` — price per item

`CustomerID`


   * Who is our internal customer?
project managers who are responsible for the relevance of the product range

   * Why do they need that?
they want to determine which products are included in the main and additional assortment in order to competently offer additional products to buyers and optimize purchases (there is no point in purchasing a lot of additional products when the main product is not available)
Classifying or categorization can be one of the options for that


some of the source links: 
http://brandonrose.org/clustering

http://datanongrata.com/2019/04/27/67/

https://realpython.com/k-means-clustering-python/

http://datanongrata.com/2019/04/27/67/

https://medium.com/ssense-tech/unsupervised-product-clustering-exploring-the-cold-start-problem-8053ef04bac9

https://medium.com/web-mining-is688-spring-2021/using-k-means-to-segment-customers-based-on-rfm-variables-9d4d683688c8

https://towardsdatascience.com/rfm-segmentation-using-quartiles-and-jenks-natural-breaks-924f4d8baee1

https://stackabuse.com/association-rule-mining-via-apriori-algorithm-in-python/

https://www.nextlytics.com/blog/machine-learning-in-customer-segmentation-with-rfm-analysis
