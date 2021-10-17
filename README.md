# Amazon Vine Analysis

## Overview of the Analysis Project
This project aims to analyze the Amazon reviews written by Amazon Vine members as they receive products and review them. In this particular instance, we will be analyzing the __musical instruments__ sold on the platform. To carry out this analysis, PySpark will be used to perform the "Extract, Transform, Load" process, where the cleaned-up dataset will be connected to an AWS RDS, and then loaded into pgAdmin. Next, PySpark will be used to determine whether Vine members gave overall positive or negative reviews of the products.

## Results

In the process of this analysis, first, we created a table that contained each review of the musical instrument product, the amount of helpful and total votes, and the rating given. There was also a column indicating whether the user was part of the Vine program. This created an initial dataframe where we further processed to draw conclusions from:

<img width="658" alt="Screen Shot 2021-10-17 at 6 44 32 PM" src="https://user-images.githubusercontent.com/84816495/137647621-ab9be935-83c2-4bd7-bd3b-11b70837a4e7.png">

We filtered the above data to only include reviews that had 20 or more total votes and with 50% or more of them being helpful votes:

<img width="665" alt="Screen Shot 2021-10-17 at 6 50 14 PM" src="https://user-images.githubusercontent.com/84816495/137647777-170a31c0-5fee-48dd-9dff-4a6ad1a5bbf3.png">

The next step was to separate the reviews based on whether they were paid (Yes to the Vine proTogram) or unpaid (No to the Vine program).

The paid reviews include:

<img width="667" alt="Screen Shot 2021-10-17 at 6 51 08 PM" src="https://user-images.githubusercontent.com/84816495/137647790-ba7e5129-5cb0-494d-8dbd-6c392e86b3e8.png">

And the unpaid reviews include:

<img width="664" alt="Screen Shot 2021-10-17 at 6 52 01 PM" src="https://user-images.githubusercontent.com/84816495/137647812-dabc2db1-ed9c-4ef2-909a-5c2525e9c53f.png">

As seen from the above dataframe tables, we can were able to come up with the following numerical figures:
- Total number of Vine reviews: 60
- Total number of non-Vine reviews: 14477
- Number of 5-star Vine reviews: 34
- Number of 5-star non-Vine reviews: 8212


## Summary
