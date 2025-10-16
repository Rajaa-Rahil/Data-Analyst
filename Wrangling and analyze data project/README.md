
# Wrangle and Analyze Data — WeRateDogs

This project focuses on data wrangling, cleaning, and analysis of the popular **WeRateDogs** Twitter dataset. The analysis involves gathering data from various sources, assessing data quality and structure issues, cleaning the data, and generating visual insights about dog ratings and breed popularity.

---

## Project Overview

The notebook `wrangle_act.ipynb` demonstrates a full data wrangling workflow:
1. **Data Gathering** — Collect datasets from multiple sources.
2. **Data Assessment** — Detect and document quality and tidiness issues.
3. **Data Cleaning** — Fix, structure, and merge datasets into a single master file.
4. **Data Analysis & Visualization** — Derive insights on tweet ratings and dog breeds.

---

## Datasets

Three datasets were used in this project:

| Source | Description | Format |
|--------|--------------|--------|
| `twitter-archive-enhanced.csv` | Original WeRateDogs tweet archive | CSV |
| `image-predictions.tsv` | Neural network predictions of dog breeds | TSV |
| `tweet_json.txt` | Fetched from Twitter API containing retweet and favorite counts | JSON |

---

## Key Tasks

### Data Gathering
- Downloaded data from local files and the Udacity-provided URL.
- Collected tweet information through the **Twitter API** using **Tweepy**.

### Data Assessment
- Identified inconsistent names, missing values, incorrect rating denominators, and redundant dog stage columns.
- Evaluated both **quality** and **tidiness** aspects of the data.

### Data Cleaning
- Converted data types (e.g., `timestamp` to datetime).
- Combined multiple dog stage columns into one.
- Removed retweets and tweets without images.
- Merged all three datasets into a single clean dataset.

### Analysis
- Calculated ratings per tweet as `rating_numerator / rating_denominator`.
- Visualized average ratings across dog breeds.
- Found that **Labrador Retrievers** and **Golden Retrievers** were among the most consistently high-rated breeds.

---

## Results

- **Final dataset:** `twitter_archive_master.csv`  
  Contains 1,994 entries and 22 columns with integrated and cleaned data.

- **Insightful Findings:**
  - Some dog names were extracted incorrectly from text (e.g., “a”, “this”).
  - Most tweets have ratings above 10/10 — in line with the humorous style of WeRateDogs.
  - Labrador Retrievers received the highest average ratings.

- **Visual Output:**
  - A bar chart showing top 5 dog breeds by average rating.

---

## Technologies Used

- Python  
- Pandas, NumPy  
- Matplotlib  
- Tweepy, Requests  
- Jupyter Notebook

---
