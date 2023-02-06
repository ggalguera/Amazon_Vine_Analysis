# Amazon Vine Analysis

## Overview of the analysis of the Vine program

The task at hand involves analyzing Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service where manufacturers and publishers receive reviews in exchange for providing products and paying a fee to Amazon. The project includes access to 50 datasets, each containing reviews for a specific product category. The selected dataset will be processed using PySpark for ETL, and the transformed data will be loaded into an AWS RDS instance. The analysis will determine if there is any bias towards favorable reviews from Vine members using PySpark, Pandas, or SQL. A summary of the findings will be written and submitted to the SellBy stakeholders.

### Data Table
We initially need to pull data from Amazon Reviews Datasets allocated in an Amazon s3 bucket and using pyspark we extracted it and convert it to 4 different tables.
![main_table](https://github.com/ggalguera/Amazon_Vine_Analysis/blob/main/main_table.png)

## Results

### Vine reviews vs non-Vine
* A total of 61,724 reviews we counted.
* A total of 585 were Vine paid reviews and 61,139 were Vine unpaid reviews.
* A total of 29,052 were 5 Stars reviews.
* A total of 213 were 5 stars Vine paid reviews out of the 585 Vine paid reviews giving us a 36.41% of Vine paid reviews with 5 stars, on the other side 28,838 were 5 stars Vine unpaid reviews out of the 61,139 Vine unpaid review giving * us a 47.17% of Vine unpaid reviews with 5 stars.

![vine_calculations](https://github.com/ggalguera/Amazon_Vine_Analysis/blob/main/vine_calculations.png)

### Summary

The analysis of the Amazon Vine program revealed that out of the 585 Vine paid reviews, 36.41% received 5 stars, while 47.17% of the 61,139 Vine unpaid reviews received 5 stars. This suggests that there is a positive bias towards Vine unpaid reviews, as they have a higher percentage of 5-star ratings compared to Vine paid reviews.

### Additional Analysis

To further support the statement of a positive bias towards Vine unpaid reviews, we could compare the average rating for Vine paid and Vine unpaid reviews. This would give us a clearer picture of the overall rating distribution and provide additional evidence for any potential positive bias in the Vine program.

