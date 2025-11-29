# Netflix Content Analysis (Python EDA Project)

A complete exploratory data analysis (EDA) project on **Netflix titles**, performed entirely using **Python**, **Pandas**, **Matplotlib**, and **Seaborn**.  
This project uncovers insights into Netflix’s catalog across genres, ratings, content types, countries, and freshness.

---

## Project Overview

This project answers key analytical questions about Netflix’s content:

- What types of content dominate the platform?
- Which genres are most popular?
- How has Netflix’s library grown over time?
- How fresh is the catalog?
- How diverse are Netflix’s genres?
- How do Movies and TV Shows differ in structure?

All analysis is performed using **Python only** — no BI tools.

---

## 1. Data Cleaning & Feature Engineering

Key preprocessing steps:

### Date Standardization  
- Cleaned inconsistent `date_added` formats  
- Extracted `year_added`

### Duration Parsing  
Converted `duration` into:
- `duration_value` → numeric minutes (Movies)  
- numeric seasons (TV Shows)

### Genre Engineering  
- Extracted `primary_genre`  
- Converted `genres_list` (string → Python list)  
- Created `is_multi_genre`

### Country Cleaning  
- Extracted `primary_country`  
- Created `is_us_content`

### Freshness Classification  
Mapped titles into categories:
- Ultra Fresh  
- Fresh  
- Recent Catalog  
- Classic  
- Unknown  

Mapped these to a **0–100 freshness score**.

### Audience Segmentation  
Mapped titles into:
- Kids  
- Youth  
- Family  
- General  
- Mature  

---

## 2. Univariate Analysis

Exploration of single variables with visuals:

### **1. Movies vs TV Shows**  
Pie + Bar chart showing content split.

### **2. Top 15 Genres**  
Horizontal bar chart of most common genres.

### **3. Release Year Distribution**  
Histogram showing distribution of release years.

### **4. Addition Timeline**  
Line chart showing titles added per year.

### **5. Ratings Distribution**  
Top rating categories.

### **6. Movie Duration Distribution**  
Histogram + mean line for movie length.

---

## 3. Bivariate Analysis

Exploring how variables relate to each other:

### **1. Genre vs Rating Heatmap**  
Shows how ratings vary across genres.

### **2. Movies vs TV Shows Over Time**  
Growth trends for each content type.

### **3. Movie vs TV Show Duration (Dual Y-Axis Boxplot)**  
- Movies → minutes  
- TV shows → seasons  

### **4. Top Countries**  
Top 10 content-producing countries.

### **5. Freshness by Type**  
Stacked bar showing fresher vs older content split between Movies and TV Shows.

### **6. Audience Segment by Type**  
Compares Kids / Youth / Mature audience splits.

---

## 4. Advanced Analytics (Business KPIs)

High-level metrics commonly used in professional content analytics.

---

### **1. Freshness Index (0–100)**  
Weighted measure of how new Netflix’s catalog is.

Outputs:
- Overall Freshness  
- Movie Freshness  
- TV Show Freshness  

---

### **2. Genre Diversity (Herfindahl Index)**  
Measures how evenly Netflix distributes content across genres.

Diversity = 1 - Σ(genre_share²)
Higher score → more diverse catalog.

---

### **3. Growth Trend (% YoY)**  
Year-over-year growth in titles added to Netflix.

Includes:
- 5-year average growth rate  
- Peak addition year  

---

### **4. Multi-Genre Complexity (%)**  
Percentage of multi-genre titles.

---

### **5. US Content Share (%)**  
Percentage of titles with the USA as primary country.

---

### **Advanced Visualization Grid**
A 2×2 dashboard with:
- Freshness Index  
- Top Genres with diversity score  
- Content growth curve  
- Multi-genre pie chart  

---

## Project Structure

Netflix-Content-Analysis/
│
├── notebooks/
│ └── netflix_analysis.ipynb # Full analysis notebook
│
├── images/
│ ├── univariate_summary.png # 6-in-1 visualization dashboard
│ ├── bivariate_summary.png # 6-in-1 visualization dashboard
│ ├── freshness_pie.png
│ └── advanced_analytics_summary.png
│
├── data/
│ └── netflix_titles.csv # Original dataset
│ └── netflix_cleaned.csv # Cleaned dataset
│ └── netflix_features.csv # Featured dataset
│
└── README.md

---

##  Tech Stack

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Jupyter Notebook  
- GitHub

