

# Amazon_Vine_Analysis

## Background

The objective of this challenge is to analyze Amazon reviews written by members of the paid Amazon Vine program for Kitchen products. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. 

## Resources 

* Technologies Used
  * AWS S3 and RDS
  * PostgreSQL and pgAdmin
  * Google Colab (to run PySpark)

## Vine Analysis

The following table show the information of the dataset organized into a data-frame exclusively displaying the information we require for our analysis. The data-frame was then filtered to only include relevant data; in this case we are only examining the products which have over 20 reviews, and a ratio of helpful reviews over 50%.

![image](https://github.com/sanjal7137/Amazon_Vine_Analysis/blob/7435a49046edae0a0474917de1d1d3f7eb6c7485/images/vinefiltered.png)

The next two tables filter the previous data-frame even further by splitting the table into two data-frames. One data-frame containing only reviews from paid Vine members, and the other containing only reviews from non-Vine members.

![image](https://github.com/sanjal7137/Amazon_Vine_Analysis/blob/7435a49046edae0a0474917de1d1d3f7eb6c7485/images/paid.png)

![image](https://github.com/sanjal7137/Amazon_Vine_Analysis/blob/7435a49046edae0a0474917de1d1d3f7eb6c7485/images/unpaid.png)

## Results

![image](https://github.com/sanjal7137/Amazon_Vine_Analysis/blob/5fc46ef59d2d7ee4e820fd3171d4e794a9a96288/images/re.png)

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
