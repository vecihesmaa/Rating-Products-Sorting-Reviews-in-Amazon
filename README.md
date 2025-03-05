# Rating Product & Sorting Reviews in Amazon

## Project Description

One of the most critical problems in e-commerce is accurately calculating post-purchase ratings for products. Solving this issue enhances customer satisfaction for the e-commerce platform, increases visibility for sellers, and ensures a smooth shopping experience for buyers. Another significant challenge is properly ranking product reviews. If misleading reviews appear at the top, they can negatively impact sales, causing both financial losses and customer dissatisfaction. By addressing these two fundamental problems, the e-commerce platform and sellers can boost their sales, while customers can complete their purchasing journey seamlessly.

## Dataset Description

This dataset contains Amazon product data, including various metadata and product categories. It focuses on the most reviewed product in the electronics category and includes user ratings and reviews.

### Variables:
- **reviewerID**: User ID.
- **asin**: Product ID.
- **reviewerName**: User Name.
- **helpful**: Helpfulness rating of the review.
- **reviewText**: The review text.
- **overall**: Product rating.
- **summary**: Summary of the review.
- **unixReviewTime**: Review timestamp.
- **reviewTime**: Raw review date.
- **day_diff**: Number of days since the review was posted.
- **helpful_yes**: Number of upvotes indicating the review was helpful.
- **total_vote**: Total number of votes received by the review.

## Task 1: Calculating the Updated Average Rating and Comparing it to the Existing Average Rating

In the provided dataset, users have given ratings and reviews for a product. The goal of this task is to weight the ratings based on time and compare the initial average rating with the time-weighted average rating.

### Steps:
1. Read the dataset and calculate the product’s initial average rating.
2. Calculate the time-weighted average rating.
3. Compare and analyze the weighted ratings over different time periods.

## Task 2: Selecting the Top 20 Reviews for the Product Page

### Step 1: Creating the **helpful_no** Variable
- **total_vote** represents the total number of upvotes and downvotes a review has received.
- **helpful_yes** represents the number of upvotes.
- Since the dataset does not contain a **helpful_no** variable, it must be derived as:
  
  `helpful_no = total_vote - helpful_yes`

### Step 2: Calculating Review Scores
To rank reviews more effectively, the following scores are computed and added to the dataset:
- **score_pos_neg_diff**
- **score_average_rating**
- **wilson_lower_bound**

For each score:
- Implement the corresponding scoring function.
- Save the calculated values in the dataset under the respective column names.

### Step 3: Selecting the Top 20 Reviews and Analyzing Results
- Rank reviews based on **wilson_lower_bound** scores.
- Select and display the top 20 reviews.
- Interpret the results and discuss the impact of different scoring methods on review ranking.

## Conclusion
This project addresses two major challenges in e-commerce: accurately computing product ratings and ranking reviews effectively. By implementing time-weighted rating calculations and advanced review scoring techniques, we enhance product visibility and customer experience while minimizing the influence of misleading reviews.

