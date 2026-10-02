# Zomato Dataset Analysis

## 📌 Project Overview

This project is developed as part of the **InternSpark Data Science Internship**. It focuses on analyzing the Zomato restaurant dataset to identify useful patterns related to restaurant ratings, cuisines, locations, pricing, and other restaurant characteristics.

The project follows this workflow:

**Data Loading → Data Cleaning → EDA → Visualization → Key Findings → Business Recommendations → Reporting**

## 🎯 Project Objective

The main objective is to analyze restaurant data and extract insights related to:

- Restaurant rating distribution
- Restaurant location preferences and hotspots
- Popular cuisines
- Price versus restaurant rating
- Relationships between important numerical variables
- Business opportunities based on the analysis

## 📊 Dataset Description

The Zomato dataset contains restaurant-level information such as:

- Restaurant name
- Address
- Location
- Online ordering availability
- Table booking availability
- Restaurant rating
- Number of votes
- Restaurant type
- Popular dishes
- Cuisines
- Approximate cost for two people
- Listing/category information

Several fields require preprocessing because they contain missing values, text-based ratings, comma-separated costs, and multiple cuisine/dish values.

## 🛠️ Technologies & Tools

- Python 3.x
- Pandas
- NumPy
- Matplotlib
- Seaborn
- WordCloud
- Jupyter Notebook / Google Colab

## 🔄 Project Workflow

```text
Zomato Dataset
      ↓
Data Loading
      ↓
Data Understanding
      ↓
Data Cleaning
      ↓
Exploratory Data Analysis
      ↓
Rating Distribution
      ↓
Location Analysis
      ↓
Cuisine Analysis
      ↓
Price vs Rating
      ↓
Correlation Analysis
      ↓
Visualizations
      ↓
Key Findings
      ↓
5 Business Recommendations
      ↓
PDF Report
```

## 🧹 Data Cleaning

Main cleaning steps include:

1. Load the dataset using Pandas.
2. Inspect rows, columns, data types, and summary statistics.
3. Check missing values.
4. Identify and remove duplicate records.
5. Clean unnecessary spaces from text columns.
6. Convert ratings such as `4.1/5` into numeric values.
7. Convert approximate cost for two people into numeric format.
8. Handle unavailable or invalid values.
9. Clean cuisine and dish fields for frequency analysis.
10. Prepare numerical columns for correlation analysis.

> Missing ratings are treated as unavailable values, not as a rating of zero.

# 📊 Main Analysis

This project focuses only on the five main analysis areas specified in the problem statement:

1. Rating Distribution
2. Location Analysis
3. Cuisine Analysis
4. Price vs Rating
5. Correlation & Heatmap

The project uses **bar charts, line charts, and a correlation heatmap**. A scatter plot is not required.

## ⭐ 1. Rating Distribution

### Objective

Understand how restaurant ratings are distributed across the dataset.

### Analysis

- Average restaurant rating
- Median restaurant rating
- Minimum and maximum rating
- Number of restaurants in different rating ranges
- Overall rating pattern

### Visualization

A **bar chart** shows the number of restaurants in different rating categories.

A **line chart** can also show the progression of restaurant counts across ordered rating levels.

### Business Meaning

Rating distribution helps a platform understand the overall restaurant-rating pattern and identify the most common rating ranges.

## 📍 2. Location Analysis

### Objective

Identify areas with a high concentration of restaurants and understand location-based patterns.

### Analysis

- Number of restaurants by location
- Top restaurant locations
- Restaurant density across major areas
- Average rating by selected locations

### Visualization

A **bar chart** displays the top restaurant locations.

A **line chart** can show changes in restaurant counts or average ratings across selected locations.

### Business Meaning

Location analysis can help improve local restaurant discovery, identify restaurant hotspots, and find potential partnership areas.

## 🍛 3. Cuisine Analysis

### Objective

Identify popular cuisines and examine their rating patterns.

### Analysis

- Most frequently listed cuisines
- Number of restaurants offering each cuisine
- Average rating by cuisine
- Popular cuisine patterns

Because the cuisine column may contain multiple cuisines in one record, the values are split before frequency analysis.

### Visualization

A **bar chart** shows the most popular cuisines.

A **line chart** can show ordered comparisons of average ratings among selected cuisines.

A **WordCloud** can visually highlight frequently occurring cuisine terms.

### Business Meaning

Cuisine analysis can support cuisine-based restaurant collections, personalized recommendations, content, and promotional campaigns.

## 💰 4. Price vs Rating

### Objective

Examine whether restaurant ratings differ across different price ranges.

### Analysis

- Approximate cost for two people
- Price categories
- Number of restaurants in each price category
- Average rating for each price category

The cost field is cleaned by removing commas and converting values to numeric format.

### Visualization

A **bar chart** compares average ratings across price ranges.

A **line chart** can also show the ordered progression from lower-cost to higher-cost categories.

### Business Meaning

This analysis can support budget, mid-range, and premium restaurant segmentation.

> This analysis describes an association between price and rating. It does not prove that price causes ratings to increase or decrease.

## 🔥 5. Correlation & Heatmap

### Objective

Examine statistical relationships between relevant numerical variables.

Main variables include:

- Restaurant rating
- Number of votes
- Approximate cost for two people

### Visualization

A **correlation heatmap** displays the strength and direction of relationships between numerical variables.

It helps identify:

- Positive relationships
- Negative relationships
- Weak relationships
- Stronger relationships

> Correlation shows statistical association, not causation.

## 📈 Visualization Summary

| Analysis | Main Visualization |
|---|---|
| Rating Distribution | Bar Chart / Line Chart |
| Location Analysis | Bar Chart / Line Chart |
| Cuisine Analysis | Bar Chart / Line Chart / WordCloud |
| Price vs Rating | Bar Chart / Line Chart |
| Correlation Analysis | Heatmap |

### Why these charts are used

**Bar Chart:** Used to compare categories such as locations, cuisines, rating groups, and price groups.

**Line Chart:** Used when categories have a meaningful order, such as rating levels or increasing price ranges.

**Heatmap:** Used to visualize correlation values between numerical variables.

**WordCloud:** Used to highlight frequently occurring cuisine terms.

## 💡 Key Findings

The analysis is designed to identify:

- The distribution of restaurant ratings.
- Locations with a high concentration of restaurants.
- The most frequently represented cuisines.
- Differences in average ratings across cuisine categories.
- Differences in ratings across price ranges.
- Relationships between rating, votes, and approximate cost.
- Location and cuisine patterns useful for restaurant discovery.

Exact numerical findings should be taken from the final executed notebook and visualizations.

## 🚀 5 Business Recommendations

### 1. Location-Based Restaurant Discovery

Use restaurant concentration and rating information to improve local restaurant discovery.

### 2. Cuisine-Based Recommendations

Create cuisine-based collections and personalized restaurant recommendations using cuisine popularity and rating patterns.

### 3. Price-Based Restaurant Segmentation

Group restaurants into budget, mid-range, and premium categories using approximate cost information.

### 4. Data-Driven Restaurant Promotion

Use location, cuisine popularity, and rating patterns to identify restaurant categories for platform content and promotional campaigns.

### 5. Partnership Opportunities

Use restaurant density, cuisine demand, price categories, and rating patterns to identify locations and restaurant segments where partnerships may be explored.

## 📁 Project Structure

```text
Zomato-Dataset-Analysis/
│
├── zomato.csv
├── Zomato_Analysis.ipynb
├── README.md
├── Zomato_Dataset_Analysis_Report.pdf
│
└── visualizations/
    ├── rating_distribution.png
    ├── location_analysis.png
    ├── cuisine_analysis.png
    ├── price_vs_rating.png
    └── correlation_heatmap.png
```

## 📓 Notebook Contents

1. Project Introduction
2. Project Objective
3. Import Libraries
4. Load Dataset
5. Dataset Overview
6. Data Types and Summary Statistics
7. Missing Value Analysis
8. Duplicate Analysis
9. Data Cleaning
10. Rating Distribution
11. Location Analysis
12. Cuisine Analysis
13. Price vs Rating
14. Correlation Analysis
15. Correlation Heatmap
16. Key Findings
17. 5 Business Recommendations
18. Conclusion

## ▶️ How to Run

### Google Colab

1. Open Google Colab.
2. Upload `Zomato_Analysis.ipynb`.
3. Upload `zomato.csv`.
4. Check the dataset path.
5. Run the notebook cells from top to bottom.

```python
import pandas as pd

df = pd.read_csv("zomato.csv")
df.head()
```

### Jupyter Notebook

Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn wordcloud
```

Start Jupyter:

```bash
jupyter notebook
```

Open `Zomato_Analysis.ipynb` and execute the cells sequentially.

## 📄 Deliverables

### 1. Jupyter/Google Colab Notebook

Contains data cleaning, the five required analysis areas, visualizations, findings, and recommendations.

### 2. PDF Report

Contains:

1. Introduction
2. Project Objective
3. Dataset Description
4. Data Cleaning
5. Exploratory Data Analysis
6. Cuisine Analysis
7. Location Analysis
8. Price vs Rating
9. Correlation & Heatmap
10. Popular Cuisine/Dish WordCloud
11. Key Findings
12. 5 Business Recommendations
13. Conclusion

### 3. README.md

Explains the project, dataset, workflow, visualizations, analysis, recommendations, and setup instructions.

## 📝 Initial Observations

- The dataset contains multiple restaurant attributes suitable for categorical and numerical analysis.
- Rating values require conversion from text into numeric values.
- Location and cuisine fields are useful for restaurant-discovery analysis.
- Approximate cost can be converted into meaningful price categories.
- Rating, votes, and cost can be examined using correlation analysis.
- Bar charts, line charts, and heatmaps provide suitable visual summaries for the selected analyses.

## ⚠️ Statistical Note

The project focuses on **patterns and associations** in the dataset.

For example, if one price category has a higher average rating than another, this is an observed association and does not prove that price directly causes higher ratings.

## 📌 Project Scope

This Zomato task is primarily an **EDA and business-insight project**.

The requirements emphasize:

- Data cleaning
- Rating distribution
- Location analysis
- Cuisine analysis
- Price vs rating
- Correlation and heatmap
- Visualizations
- Key findings
- Five business recommendations
- Notebook and PDF reporting

**No scatter plot is required for this project.**

Machine learning and deployment should only be added if a separate InternSpark requirement explicitly asks for them.

## 👨‍💻 Internship Information

**Internship:** InternSpark  
**Project:** Zomato Dataset Analysis  
**Domain:** Data Science / Exploratory Data Analysis  
**Level:** Beginner  
**Environment:** Python, Jupyter Notebook / Google Colab

## 📜 Conclusion

The Zomato Dataset Analysis project demonstrates a practical beginner-level Data Science workflow, starting from raw restaurant data and progressing through data cleaning, exploratory analysis, visualization, key findings, and business recommendations.

The project provides practical experience with Python, Pandas, NumPy, Matplotlib, Seaborn, data cleaning, exploratory data analysis, categorical analysis, numerical correlation, visualization, and business-oriented reporting.
