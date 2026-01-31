# HackProject
 DelivInsights: Unified Food Delivery Analytics
##📌 Project Overview
DelivInsights is a data integration and analytics project designed to unify fragmented data sources from a food delivery platform. By combining transactional records, user profiles, and restaurant metadata, this project provides a "Single Source of Truth" to analyze customer behavior, membership impact, and restaurant performance.

##❓ Problem Statement
The organization’s data was trapped in format-based silos, preventing a holistic view of the business:

Transactional Data (orders.csv): Contains order IDs, dates, and amounts.

User Profiles (users.json): Semi-structured data containing user locations and membership status (Gold/Regular).

Restaurant Metadata (restaurants.sql): Relational data containing cuisines and star ratings.

The Challenge: Without integrating these files, the business could not identify which cities drive the most revenue from Gold members or which cuisines are the most profitable across different regions.

##🛠️ Technical Stack
Language: Python 3.12

Libraries: Pandas (Data Manipulation), SQLite3 (SQL Parsing), JSON (Data Loading)

Tools: Jupyter Notebook

##📂 Data Architecture & Joins
The project creates a master dataset of 10,000 records using the following logic:

Primary Join: orders.csv + users.json on user_id.

Secondary Join: Merged Result + restaurants.sql on restaurant_id.

##🚀 Key Insights Generated
Membership Impact: Gold members contribute significantly higher Average Order Values (AOV) compared to Regular members.

Top Cuisine: Identified the specific cuisine (e.g., Italian/Indian) generating the highest revenue.

Geography: Chennai and Hyderabad emerged as top-performing cities for premium membership tiers.

Rating Correlation: Higher restaurant ratings (4.5+) directly correlate with higher order frequency.

##📊 Final Dataset Structure
The output file final_food_delivery_dataset.csv includes:

order_id: Unique identifier for each transaction.

user_id: Link to customer profiles.

total_amount: Revenue per order.

membership: Categorization (Gold/Regular).

city: Geographic location of the user.

cuisine: The type of food served.

rating: Restaurant quality score.

rating_range: Binned categories (e.g., 4.1 - 4.5) for trend analysis.

quarter: Temporal tracking of revenue.

##💻 How to Run
Ensure orders.csv, users.json, and restaurants.sql are in the root directory.

Open the provided Jupyter Notebook.

Run the Setup Block to generate the final_food_delivery_dataset.csv.

Run the Analysis Blocks to generate the KPI reports.

Final Output File
You can download the processed master dataset here: Download final_food_delivery_dataset.csv


