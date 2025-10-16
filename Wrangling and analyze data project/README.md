
# Wrangle and Analyze Data — WeRateDogs

This project focuses on data wrangling, cleaning, and analysis of the popular **WeRateDogs** Twitter dataset. The analysis involves gathering data from various sources, assessing data quality and structure issues, cleaning the data, and generating visual insights about dog ratings and breed popularity.

## Project Overview

The project demonstrates a full data wrangling workflow:
1. **Data Gathering** — Collect datasets from multiple sources.
2. **Data Assessment** — Detect and document quality and tidiness issues.
3. **Data Cleaning** — Fix, structure, and merge datasets into a single master file.
4. **Data Analysis & Visualization** — Derive insights on tweet ratings and dog breeds.

## Technologies Used
- Python  
- Pandas, NumPy  
- Matplotlib  
- Tweepy, Requests  
- Jupyter Notebook

## Datasets

Three datasets were used in this project:

1. `twitter-archive-enhanced.csv`: Original WeRateDogs tweet archive.
2. `image-predictions.tsv`: Neural network predictions of dog breeds.
3. `tweet_json.txt`: Fetched from Twitter API containing retweet and favorite counts.

## Key Steps and Methods

### 1. Data Gathering
- The first dataset is loaded locally via `pandas.read_csv()`.
- The second dataset is downloaded programmatically using the Requests library.
- The third dataset is collected through the **Twitter API** via Tweepy, using OAuth credentials to fetch JSON data for each tweet and save to file.

### 2. Data Assessment
- Performed both visual and programmatic assessment.
- Found major quality and tidiness issues such as:
  - Missing values and inconsistent datatypes (e.g., `timestamp`, `tweet_id`).
  - Invalid or inconsistent dog names (e.g., lowercase words like "a") and ratings with incorrect denominators.
  - Multiple columns (`doggo`, `floofer`, `pupper`, `puppo`) representing one variable — “dog stage”.
  - Duplicates in image URLs and missing prediction rows.

### 3. Data Cleaning
The cleaning process addressed these issues by:
- Converting data types (`tweet_id` to string, `timestamp` to datetime).
- Combining the four “dog stage” columns into a single one (`dogstage`).
- Filtering out retweets and tweets without images.
- Correcting invalid denominators (setting all to 10).
- Removing duplicates and empty entries.
- Merging all three data sources into one master DataFrame using the `tweet_id` as the key.
- Creating a new column `rating = rating_numerator / rating_denominator`.

## Output and Analysis
### Clean Master Dataset
- Final dataset: 1,994 entries, 22 columns.
- Columns include:
  - `tweetid`, `timestamp`, `text`, `expandedurls`, `ratingnumerator`, `ratingdenominator`, `jpgurl`, `prediction1`, `prediction2`, `prediction3`, `favoritecount`, `retweetcount`, `dogstage`, `rating`, `dogname`.

### Final Storage
- Saved as `twitter_archive_master.csv`.

### Visualization
- A bar chart showing the top five dog breeds by average rating.
- Result: Labrador Retriever ranks highest, followed by Golden Retriever.

## Summary of Findings
This project demonstrates a complete and structured data wrangling workflow with:
- Integration of multiple data sources.
- Identification and correction of messy and inconsistent data.
- Clean, merged dataset ready for analysis.
- Insight that certain breeds consistently receive higher user ratings, reflecting potential social trends in pet popularity.


## License
This project is intended for educational purposes under an open license. Data provided by the Udacity Data Analyst Nanodegree and the WeRateDogs Twitter account.
