# 🌍 TravelTriangle Web Scraping & Feature Engineering Project
📌 Project Overview

This project focuses on web scraping travel package data from TravelTriangle, followed by feature engineering, data cleaning, and exploratory data analysis (EDA) to extract meaningful business insights.

The objective is to transform raw, unstructured scraped data into analysis-ready features and understand how pricing, trip duration, itinerary complexity, and destinations influence travel packages.

🎯 Problem Statement

Travel packages vary based on:

Price and discount strategy

Trip duration

Number of locations covered

Destination and stay type

This project aims to:

Convert raw scraped text data into structured features

Analyze pricing patterns and itinerary design

Identify customer preferences and business trends

🌐 Data Source

Website: TravelTriangle

URL:

https://traveltriangle.com/tour-packages/kerala?travelmonth=May%2C%202026


Domain: Travel & Tourism

Region: Kerala Travel Packages

🛠️ Tools & Libraries Used

Python

Requests

BeautifulSoup

Regular Expressions (Regex)

Pandas

NumPy

Matplotlib

Seaborn

Jupyter Notebook

📥 Web Scraping

The following raw fields were scraped from the website:

Package Name

Stay (Days & Nights)

Location

Price (Discounted & Original)

Discount Percentage

Tags (Places & Experiences)

The scraped data was stored in a CSV file for further processing.

🔧 Feature Engineering (Core Part of This Project)

Raw scraped data contained text-heavy and unstructured values, which were transformed into clean, structured features suitable for analysis.

🔹 Raw Columns

Name

Stay

Location

Price

Discount

Tags

🔹 Engineered Features
1️⃣ discount_price

Extracted discounted price from the Price column

Removed currency symbols and commas using regex

Converted to integer

Represents the final selling price

2️⃣ original_price

Extracted original price from the same Price column

Cleaned and converted to numeric format

Used to analyze pricing strategy

3️⃣ Discount_percentage

Extracted numeric discount value from text (e.g., 25% Off)

Converted to integer

Helps understand discount patterns

4️⃣ Total_Days

Extracted trip duration from the Stay column

Combined days and nights into a single numerical value

Enables duration-based analysis

Example:
4 Days & 3 Nights → 4

5️⃣ Location_List1

Extracted and structured multiple locations covered in a package

Represents itinerary coverage

6️⃣ No_of_Locations

Counted the number of locations in Location_List1

Measures itinerary complexity

7️⃣ Tags_List1

Cleaned and structured tags representing attractions and experiences

Used to analyze customer interests

📋 Final Dataset Structure
Numerical Columns

discount_price

original_price

Discount_percentage

Total_Days

No_of_Locations

Categorical Columns

Name

Stay

Location

Location_List1

Tags_List1

📊 Exploratory Data Analysis (EDA)
🔹 Uni-variate Analysis

Histograms & KDE plots for price distribution

Boxplots & violin plots for outlier detection

Count plots & pie charts for categorical variables

🔹 Bi-variate Analysis

Price vs Total Days

Price vs Number of Locations

Price vs Stay Type

Discount vs Original Price

🔹 Categorical vs Categorical

Stay vs Location List using crosstab + heatmap

🔹 Multi-variate Analysis

Correlation heatmap for numerical features

GroupBy and pivot table analysis

Bubble chart for duration, pricing, and itinerary complexity

📈 Key Insights

Most packages are priced in the mid-range, with a few premium offerings.

Trip duration and number of locations strongly influence price.

Discounts are moderate and standardized, not extreme.

Most packages cover 1–2 locations, indicating preference for simple itineraries.

Multi-location trips are less frequent and usually higher value.

📁 Project Structure
├── traveltriangle_webscraping.ipynb
├── traveltriangle_eda.ipynb
├── output.csv
├── README.md

🚀 How to Run

Clone the repository

Install required libraries

Run the web scraping notebook

Load output.csv for feature engineering and EDA

✅ Conclusion

This project demonstrates the complete data science lifecycle:

Web Scraping → Feature Engineering → Data Cleaning → EDA → Business Insights

It highlights how proper feature engineering transforms raw scraped data into valuable analytical insights for the travel domain.

