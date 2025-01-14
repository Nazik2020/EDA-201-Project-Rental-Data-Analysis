# EDA-201-Project-Rental-Data-Analysis

## Overview
This project focuses on the Exploratory Data Analysis (EDA) of a rental dataset to uncover insights, handle missing data, detect outliers, and visualize key trends using Python libraries such as pandas, matplotlib, and seaborn.

## Steps and Approach

### 1. Data Import and Initial Exploration
- **File Import:** Imported `rental_data.csv` file.
- **Initial Inspection:** Utilized `df.head()`, `df.tail()`, `df.shape`, `df['cityname'].value_counts()`, `df.describe()`, `df.dtypes`, `df.info(verbose=False)`, and `df.info()` for a quick overview.

### 2. Handling Missing Values
- **Identified Missing Values:** Used `.isnull().sum()` to find missing data.
- **Dropped Columns:** Removed columns with more than 30% missing values (`pets_allowed`, `amenities`, `address`).
- **Filtered Rows:** Dropped rows with more than 1% missing data in `state`, `cityname`, `bathrooms`, `longitude`, `latitude`, `bedrooms`.
- **Validation:** Re-checked missing values to ensure completeness.

### 3. Data Cleaning and Transformation
- **Categorical Conversion:** Converted relevant columns to categorical types (`cityname`, `state`, `source`, `category`, `has_photo`, `price_type`).
- **Dropped Unnecessary Columns:** Removed `currency`, `fee`, `price_type` (single unique value), and `id` (not useful).
- **Data Type Conversion:** Converted `bathrooms` and `bedrooms` to `int` and `time` to `datetime`.
  
### 4. Outlier Detection and Low Variance Columns
- **Outlier Removal:** Used a threshold based on visual inspection of boxplots to filter and remove outliers.
- **Low Variance Columns:** Dropped columns with low variance as they don't contribute significantly to analysis.

### 5. Visualization
- **Price Distribution:** Created histograms to visualize the distribution of prices.
- **Top 10 Cities by Average Price:** Used bar plots to display the average price in the top 10 cities.
- **Price vs. Square Feet:** Created scatter plots to show relationships between price and square footage.
- **Price Over Time:** Used line plots to visualize price trends over time, sorted the time column for better chronological representation, and resampled data monthly to observe the trend.

## Tools Used
- **Pandas:** Data manipulation and analysis.
- **Matplotlib & Seaborn:** Data visualization.

## Conclusion
This project provided insights into the rental market trends, facilitated better understanding of the data structure, and enhanced visualization skills.

