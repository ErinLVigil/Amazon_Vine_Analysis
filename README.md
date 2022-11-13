# Amazon_Vine_Analysis

## Overview

For this project, I used a data set on Amazon to look at reviews of shoes. The ETL process for this allowed us to take large data sets and get it to usable data set and perform the analysls.

Using a data base on AWS and google collab, I was able to take an incredibly large data set and refine it down to something usable for my analysis. This approach allowed me to take the data set, select columns I needed and save them to several different dataframes. It also allowed me to drop dupplicates and null values.

From here, we could connect to PG Admin and write the data to tables that could be easily exportable as CSV for further analysis.

Amazon has a a program that pays for reviews through Vine. We could use one of our csv files to take a closer look at the reviews and the Vine data to see if there was any bias for 5-star reviews from the program.

We looked for only reviews that had more than 20 votes total and where the helpful vote count was at least half of the total vote count in order to look at credible reviews.

## Results

* There weree a total of 27,009 reviews in our data frame. 22 of them were from Vine reviews and 26,987 were from non vine reviews
![vote_count](https://user-images.githubusercontent.com/109319148/201545951-3dedf63a-e079-45b4-9b13-4318aa9c5046.png)

* There were a total of 13 vine paid 5-star reviews and a total of 14,475 non-paid reviews as seen in the screenshot below
![vine_no_vine](https://user-images.githubusercontent.com/109319148/201546730-a8f2a1f4-cfa7-4416-88cb-73b3c8654b17.png)

* As seen above, 59% of reviews that were paid resulted in 5 stars, whereas only 54% percent of non-paid reviews resulted in 5-stars.


## Summary

There is a slight bias for paid reviews to be 5-stars as we saw in the analysis. The bias isn't incredibly strong, as it was only abut 5% more often than the non-paid reviews. If there is not really much positive bias, is there a bias against 1 star reviews if they are paid? I would perform the same analaysis and see if there were less 1-star reviews that were paid versus those that were unpaid? Are people less likely to give incredibly negative reviews if they are paid? This would be an easy check by just switching out the '5' for a '1' in our analysis. 
