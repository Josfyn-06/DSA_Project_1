# DSA_Project_1

This is my application of data analysis concepts learnt during the Data Skillup Africa training taught by the Incubator Hub which include data cleaning, data querying,visualization and insights extraction using Excel, SQL and Power BI.
- - -

## Project Title: Amazon Product Review Analysis
- - -

## Table of Contents 
[Project Overview](#project-overview)

[Dataset](#dataset)

[Data Source](#data-source)

[Tools Used](#tools-used)

[Data Cleaning and Preparation](#data-cleaning-and-preparation)

[Exploratory Data Analysis](#exploratory-data-analysis)

[Data Visuals](#data-visuals)

[Key Insights](#key-insights)

[Recommendation](#recommendation)
- - -

## Project Overview
This project focuses on analysing Amazon product listings and customer review data to generate insights that support:
- Product improvement 
- Marketing strategies
- Enhanced customer engagement 
- - -

## Dataset
The dataset contains product details scraped from Amazon Product pages. It includes:

- **Total Records:** 1,465 rows

- **Total Columns:** 16 fields which include:

  - *Product ID*: This is a unique identifier for each product listing or seller's version of the product
  - *Product Name*: This describes the general product
  - *Product Category*: The group or type the product belongs to
  - *Discounted Price*: The final selling price after discount is applied
  - *Actual Price*: The original or listed price before discount
  - *Discount Percentage*: The percentage deduction from the actual price calculated as:(Actual Price-Discounted Price)/Actual Price*100
  - *Rating*: The average customer rating for the product
  - *Rating Count*: The number of people who rated the product
  - *About Product*: A textual summary or description of the product
  - *User_ID*: A unique identifier for the user who submitted the review
  - *Username*: The name or alias of the person who reviewed the product
  - *Review_ID*: A unique ID assigned  to each review entry
  - *Review Title*: The headline of the review
  - *Review Content*: The full body of the user's review
  - *Img_Link*: URL to the product's image
  - *Product Link*: URL to the product's page on the marketplace
- - -

## Data Source
The dataset was handed to us by the Incubator Hub to practice and showcase what we've learnt so far in the Data Skillup Africa Training. The dataset is available upon request
- - -

## Tools Used
- Microsoft Excel for:
  - Data cleaning
  - Calculated columns
  - Pivot table analysis
  - Dashboard and visualisation
- - -

## Data Cleaning and Preparation
In this phase of my analysis, i performed the following actions to ensure accurate analysis and visualisations:
- **Data loading**: Loaded the data to a blank excel workbook
- **Removal of Irrelevant Columns**: Columns not required for the analysis were removed to reduce noise and improve clarity. They include
  - About Product
  - User_ID
  - User_name
  - Review_Id
  - Review_Title
  - Review_Content
  - Img_Link
  - Product_Link
- **Duplicates Removal**: Removed duplicate rows to ensure unique records. 81 duplicates were found and removed left with 1,384 rows out of 1,465 records that was given in the dataset. I also noticed duplicates in Product Id with same product name with just slight difference in the rating, this showed that the same products were entered twice in the dataset with a difference of 1 or 2 in rating. I first of filtered the rating column in descending order, then i removed duplicates just choosing the product id and product name column in order for the duplicate with the highest rating to be left behind. This brought about 33 more duplicates being found and 1,351 unique values remaining.
- **Blank Value Check**: Verified the dataset for blank values
- **Data Type Conversion**: Standardized data type for:
   - *Prices*: Converted to numeric format
   - *Discount Percentage*: Converted to percentage format
   - *Ratings*: Verified as numbers
- **Column Cleaning**: Cleaned extra spaces and hidden characters from key columns. Cut and trimmed columns that needed cleaning
- **Created Calculated Columns**
  - *Price Range Buckets*: `<₹200`, `₹200–₹500`, `>₹500`
  - *Potential Revenue* = `Discounted Price * Rating Count`
- - -

### Exploratory Data Analysis
After cleaning the dataset and creating calculated columns, i conducted thorough exploration to uncover the product landscape, customer engagement patterns and pricing dynamics on Amazon. Below is how i explored the data:
- **Category Distribution**: Products were spread across multiple categories, with "Electronics" having the highest count followed by "Home and Kitchen" and "Computer and Accessories"
- **Review Activity**: We analyzed the number of reviews and ratings across products and categories.
- **Pricing**: Actual and discounted prices were compared to understand discount trends.
- **Discount Analysis**: We grouped discount percentages to identify heavily discounted product segments.
- **Rating Distribution**: Ratings ranged from 1.0 to 5.0, with the majority of products rated between 3.9 to 4.5.
- **Potential Revenue**: By multiplying actual price with rating count, we estimated potential revenue per product and per category.
- **Unique Products**: We identified and accounted for duplicate product names with different product IDs, and also duplicate product ID with different product names
- **High Performers**: Top 5 products were selected based on a combination of rating score and number of reviews.
- - -

### Data Visuals
<img width="879" height="305" alt="Amazon Pivot" src="https://github.com/user-attachments/assets/1fb8bb19-2589-4f45-9b49-bc930dc2cc71" />




<img width="806" height="296" alt="Amazon Dashboard" src="https://github.com/user-attachments/assets/da422db6-f0f1-4209-b76b-6bd1e21d2ba5" />




### Key Insights
- **Most Reviewed Categories**: Electronics generated the highest review counts followed by "Computer and Accessories and "Home and Kitchen" indicating strong customer engagement in these categories.
- **Actual Price vs. Discount Percentage**: It shows that the higher the price bucket, the lower the discount percentage. And more products are being purchased from the highest price bucket
- **Rating Trends**: Products with higher discounts didn’t necessarily have better ratings — suggesting price cuts don't always reflect quality.
- **Revenue Potential**: Some moderately priced products had very high review counts, showing they contributed significantly to potential revenue.
- **Top Products**: The most successful products combined high ratings (above 4.5) with a large number of reviews (10,000+), mostly in mobile accessories.
- **Duplicates**: Multiple identical product names with different IDs existed — possibly representing different sellers or minor variants. Same with multiple Product ID with different product names
- - -

### Recommendation
- **Focus on High-Performing Categories**: Sellers should invest more in "Electronics" and "Home and Kitchen" and "Computer and Accessories where customer interest is strong.
- **Optimize Discount Strategy**: Rather than large discounts, moderate discounts with quality and strong reviews can drive trust and conversions.
- **Encourage Reviews**: Products with more reviews attract more buyers — sellers can use incentives to gather reviews.
- **Consolidate Listings**: Reduce duplicate listings by ensuring sellers avoid repeating the same product under multiple IDs.
- **Monitor Rating Impact**: Regularly track how ratings fluctuate with price and discount changes to optimize value perception
- **Promote High-Potential Products**: Products with high potential revenue but lower visibility (few reviews) should be promoted more actively.



