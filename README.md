# EDA-of-Bank-Telemarketing-Campaign

### About EDA
Exploratory data analysis uses data visualisation techniques to draw inferences and obtain insights from them.
EDA is more about understanding and studying the given data in detail.
Visualisation of data into plots/graphs can be termed one of the tools in the EDA process. 

EDA should be the first step in any data science / machine learning activity. Based on the results of EDA, companies also make business decisions, which can have repercussions later. If not performed properly, EDA can hamper the further steps in the machine learning model building process. If performed well, it may improve the efficacy of all we do in the next steps.


The first task of EDA involves the preparation of data sets for analysis by removing irregularities in the data so that these irregularities do not affect further steps in the process of data analysis and machine learning model building.

 
#### Why EDA?

The major utility of EDA are as follows:

* Maximise the insight in the data set
* Detect outliers and anomalies
* Test underlying assumptions


EDA is majorly carried out with four major topics covered:

1. Data sourcing
2. Data cleaning
3. Univariate analysis
4. Bivariate and multivariate analysis

 ```mermaid
flowchart TD
A[EDA Major Steps] --> B[1. Data sourcing];

A[EDA Major Steps] --> C[2. Data cleaning];


A[EDA Major Steps] --> D[3. Univariate analysis];


A[EDA Major Steps] --> E[4. Bivariate and multivariate analysis];

```




## Data Sourcing
Broadly, data sources can be seen as one of the two types:

* Private data
* Public data
 
 ```mermaid
flowchart TD
A[Data Sourcing] --> B[Private Data];


A[Data Sourcing] --> C[Public Data];


```

**Private data:** Private data majorly belongs to an organisation, and there are certain security and privacy concerns attached to it.
It is used for the companies’ internal analysis purposes in order to gain business and growth insights.
Examples: telecom data, retail data, banking and medical data.

 

**Public data:** Public data are available for public use.
They are offered by many sites such as government websites and public agencies for the purpose of research.
Accessing this data does not require any special permission or approval.
There are many programming techniques that are used to fetch public data through code called Data Mining.


<p align="center">
Public data is not always relevant or useful, and private data is not always easily available.
</p>


### Domain Specific Data
Some Domain Specific data and there uses are as follows:
* **Banking data:** 
  * Banks use data to make credit-related decisions.
  * This data is highly sensitive, as it contains customer transaction details, account details, etc.
  * Security of such data is of topmost importance.
  * Banks can use such data to predict which customer is likely to take a loan in the near future or which customers are interested in investing in term deposits, etc. 
  * With this help of such data, banks can also identify which customers are likely to default on their loans.


* **Telecom data:**
  * Telecom companies use data to optimise plans for customers and predict customer churn.
  * Telecom data can be used to optimise the coverage area based on the customers' calls data and their call performances.


* **HR data:**
  * HR data analytics helps identify and predict employee behaviour. 

* **Retail data:** 
  * Retail data analytics helps drive decisions such as product purchasing, pricing and stocking.


* **Media data:** 
  * The media industry uses data extensively to target viewers.
  * Advertisers use data to identify the best avenues for targeting customers.
  * Journalists use data visualisation to gather relevant information.


