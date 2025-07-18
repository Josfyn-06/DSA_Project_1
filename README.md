# DSA_Project_1

This is my application of data analysis concepts learnt during the Data Skillup Africa training taught by the Incubator Hub which include data cleaning, data querying,visualization and insights extraction using Excel, SQL and Power BI.
- - -

## Project Title: Amazon Product Review Analysis
- - -

## 🖇️Table of Contents 
[Project Overview](#project-overview)

[Dataset](#dataset)

[Data Source](#data-source)

[Tools Used](#tools-used)

[Data Cleaning and Preparation](#data-cleaning-and-preparation)

[Exploratory Data Analysis](#exploratory-data-analysis)

[Data Visuals](#data-visuals)

[Insights](#insights)

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
- *Data loading*: Loaded the data to a blank excel workbook
- *Removal of Irrelevant Columns*: Columns not required for the analysis were removed to reduce noise and improve clarity. They include
  - About Product
  - User_ID
  - User_name
  - Review_Id
  - Review_Title
  - Review_Content
  - Img_Link
  - Product_Link
- *Duplicates Removal*: Removed duplicate rows to ensure unique records. 81 duplicates were found and removed left with 1,384 rows out of 1,465 records that was given in the dataset. I also noticed duplicates in Product Id with same product name with just slight difference in the rating, this showed that the same products were entered twice in the dataset with a difference of 1 or 2 in rating. I first of filtered the rating column in descending order, then i removed duplicates just choosing the product id and product name column in order for the duplicate with the highest rating to be left behind. This brought about 33 more duplicates being found and 1,351 unique values remaining.
- *Blank Value Check*: Verified the dataset for blank values
- *Data Type Conversion*: Standardized data type for:
   - Prices (converted to numeric format)
   - Discount Percentage (converted to percentage format)
   - Ratings (verified as numbers)
- *Column Cleaning*: Cleaned extra spaces and hidden characters from key columns. Cut and trimmed columns that needed cleaning
- *Created Calculated Columns*
  - Price Range Buckets: `<₹200`, `₹200–₹500`, `>₹500`
  - Potential Revenue = `Discounted Price * Rating Count
- - -

### Exploratory Data Analysis




