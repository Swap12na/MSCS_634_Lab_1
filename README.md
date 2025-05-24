# Lab 1: Data Visualization, Data Preprocessing, and Statistical Analysis Using Python in Jupyter Notebook
## Student Information
**Name:** Vamshidhar Reddy Jonnalagadda
**Course Title:** MSCS 634 - Data Science
**Lab Title:** Lab 1 - Data Exploration and Preparation
---
## Purpose
The purpose of this lab is to perform data exploration, visualization, preprocessing, and statistical analysis using Python in a Jupyter Notebook environment. The dataset used in this lab includes academic, lifestyle, and behavioral data for 1000 students, with variables such as study hours, social media usage, sleep patterns, attendance, and exam scores.
---
## Dataset
- **Name:** Student Academic Lifestyle Dataset
- **Observations:** 1000
- **Features:** 16 (age, gender, study hours, attendance, etc.)
- **Source:** Custom/Manually Provided
- **File Type:** CSV (included in this repository)
---
## Key Steps and Results
### 1. Data Visualization
- **Scatter Plot**: Visualized the relationship between `study_hours_per_day` and `exam_score`. Found a moderate positive correlation—students who studied more tended to score higher.
- **Box Plot**: Compared `exam_score` across different levels of `diet_quality`. Revealed that students with a "Good" diet had a higher median exam score.
### 2. Data Preprocessing
- **Missing Values**: Found 91 missing values in `parental_education_level`. Filled them using mode imputation to maintain data distribution.
- **Outlier Detection**: Used the IQR method to remove extreme outliers from `social_media_hours` and `netflix_hours`. Around 2.5% of entries were affected.
- **Data Reduction**: Dropped columns like `student_id` which were not relevant for analysis. Also sampled 70% of data for a lighter analysis variant.
- **Scaling**: Applied Min-Max Scaling to normalize `study_hours_per_day`, `sleep_hours`, and `exam_score` to a [0, 1] scale.
- **Discretization**: Binned `exam_score` into categorical performance levels: `Low`, `Average`, `High`.
### 3. Statistical Analysis
- **Data Overview**: Used `.info()` and `.describe()` to check for data types, null counts, and summary statistics.
- **Central Tendency**: Calculated mean, median, mode, min, and max for key numeric columns.
- **Dispersion Measures**: Found range, quartiles, variance, and standard deviation for numeric attributes.
- **Correlation Analysis**: Found strong positive correlation between `study_hours_per_day` and `exam_score`, and a weak negative correlation between `social_media_hours` and `exam_score`.
---
## Challenges Faced
- **Imputing Missing Values**: Choosing the right strategy for `parental_education_level` without introducing bias.
- **Outlier Sensitivity**: Some features (like social media usage) had skewed distributions that required careful filtering.
- **Scaling Choices**: Ensuring normalization methods preserved the interpretability of data.
---
