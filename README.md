![image](https://github.com/amberwnaushahi/Amazon_Vine_Analysis/blob/main/Images/Header.png)

# Amazon_Vine_Analysis

## Background

The objective of this challenge is to analyze Amazon reviews written by members of the paid Amazon Vine program for Kitchen products. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

PySpark was used to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Next,  using PySpark, I determined if there is any bias toward favorable reviews from Vine members in the dataset so that SellBy stakeholders can assess if membership to the Vine program is going to be beneficial.

## Resources 

* [DataSet - Kitchen Gadgets Reviews](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Kitchen_v1_00.tsv.gz)

* Technologies Used
  * Google Colab (to run PySpark)
  * AWS S3 and RDS
  * PostgreSQL

## Vine Analysis

The following table show the information of the dataset organized into a data-frame exclusively displaying the information we require for our analysis. The data-frame was then filtered to only include relevant data; in this case we are only examining the products which have over 20 reviews, and a ratio of helpful reviews over 50%.

![image](https://github.com/amberwnaushahi/Amazon_Vine_Analysis/blob/main/Images/Filtered_table_all.PNG)

The next two tables filter the previous data-frame even further by splitting the table into two data-frames. One data-frame containing only reviews from paid Vine members, and the other containing only reviews from non-Vine members.

![image](https://github.com/amberwnaushahi/Amazon_Vine_Analysis/blob/main/Images/Filtered_table_vine.PNG)

![image](https://github.com/amberwnaushahi/Amazon_Vine_Analysis/blob/main/Images/Filtered_table_non-vine.PNG)

## Results

![image](https://github.com/amberwnaushahi/Amazon_Vine_Analysis/blob/main/Images/results.PNG)

### Number of Reviews:
* Vine Reviews: 1,158
* Non-vine Reviews: 92,088

### Number of 5-star reviews:
* Vine 5-star Reviews: 489
* Non-vine 5-star Reviews: 43,228

### Percentage of 5-star reviews:
* Percentage of Vine 5-star Reviews: 42.2%
* Percentage of Non-vine 5-star Reviews: 46.9%

## Summary

In summary, 42.4% of the reviews in the Vine program were 5-stars reviews whereas the percentage in the non-Vine reviews is 46.9%. Based on the result of vine vs non-vine review counts, results would suggest that there is no positivity bias in the dataset. The vine program might just not be worth it for the kitchen products category.

However, further analysis can be done to verify this such as statistical distribution (mean, median and mode) of the star rating for the Vine and non-Vine reviews.
