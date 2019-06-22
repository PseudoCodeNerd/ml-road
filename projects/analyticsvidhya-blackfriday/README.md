# Black-Friday-Practice-Problem

## Introduction

This is my contribution to the Black-Friday Problem competition at:

https://datahack.analyticsvidhya.com/contest/black-friday/

## Problem Statement
A retail company “ABC Private Limited” wants to understand the customer purchase behaviour (specifically, purchase amount) against various products of different categories. They have shared purchase summary of various customers for selected high volume products from last month.
The data set also contains customer demographics (age, gender, marital status, city_type, stay_in_current_city), product details (product_id and product category) and Total purchase_amount from last month.

Now, they want to build a model to predict the purchase amount of customer against various products which will help them to create personalized offer for customers against different products.

### Data contains the following variables.
| Variable |	Definition |
|----------|------------:|
| User_ID | User ID |
| Product_ID | Product ID |
| Gender	| Sex of User |
| Age	| Age in bins |
| Occupation	| Occupation (Masked) |
| City_Category	| Category of the City (A,B,C) |
| Stay_In_Current_City_Years	| Number of years stay in current city |
| Marital_Status	| Marital Status |
| Product_Category_1	| Product Category (Masked) |
| Product_Category_2	| Product may belongs to other category also (Masked) |
| Product_Category_3	| Product may belongs to other category also (Masked) |
| Purchase	| Purchase Amount (Target Variable) |

#### Note: Your model performance will be evaluated on the basis of your prediction of the purchase amount for the test data (test.csv), which contains similar data-points as train except for their purchase amount. Your submission needs to be in the format as shown in "SampleSubmission.csv". We at our end, have the actual purchase amount for the test dataset, against which your predictions will be evaluated. Submissions are scored on the root mean squared error (RMSE). RMSE is very common and is a suitable general-purpose error metric. Compared to the Mean Absolute Error, RMSE punishes large errors:

<hr>

## What I did...

I used <code>SFrame</code> of GraphLab and will continue to do so until I get proficiency with pandas. Here's GraphLab's _extremely helpful_ 
tools for various MachineLearning Application. 
[GraphLab API Docs](https://turi.com/products/create/docs/graphlab.toolkits.html)<br>
__I approached this as a recommender problem and used matrix factorization.__

> [Grpahlab's Documentation on Factorization Recommender](https://turi.com/products/create/docs/generated/graphlab.recommender.factorization_recommender.FactorizationRecommender.html)<br>

My understanding of matrix factorization is that the algo treats the problem as a matrix of the target variable, with user ids and product ids as the two dimensions. It then fills in the blanks in this matrix using factorization. Additionally, it also incorporates features of the users or products such as gender, product category etc. These are called ‘side features’ in recommender jargon.

## Result
### Got Final RMSE: 1925.8
### Score : 2808.78
 
