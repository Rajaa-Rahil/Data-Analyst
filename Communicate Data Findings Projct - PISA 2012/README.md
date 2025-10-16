## Communicate Data Findings: PISA 2012 Analysis

### Project Overview
This project, *Communicate Data Findings – PISA 2012*, is part of the Data Analyst Nanodegree program from Udacity. It demonstrates end-to-end data exploration, visualization, and communication of insights using the PISA 2012 dataset published by the OECD.

The analysis was performed in two main parts across Jupyter notebooks:
- Part I: Data wrangling, exploration, and preparation.
- Part II: Presentation and visualization of findings.

### Dataset Information
The dataset originates from the **Programme for International Student Assessment (PISA) 2012**, which evaluates the knowledge and abilities of 15-year-old students worldwide in **Math**, **Reading**, and **Science**.

Key statistics:
- Original dataset size: 485,490 students and 636 attributes.
- Cleaned dataset size: 286,907 students and 11 attributes.
- The source of the PISA 2012 datasets is [here](https://www.google.com/url?q=https://s3.amazonaws.com/udacity-hosted-downloads/ud507/pisa2012.csv.zip&sa=D&ust=1581581520574000). Also, you can see the database dictionary [here](https://www.google.com/url?q=https://s3.amazonaws.com/udacity-hosted-downloads/ud507/pisadict2012.csv&sa=D&ust=1554482573645000).

### Selected Variables
After cleaning and shaping the data, the following variables were retained for analysis:
- Country: Student’s country.
- Age: Student’s age.
- Gender: Male or Female.
- StudyExtraHours: Time spent studying beyond classes.
- Internet: Home internet availability.
- Computer: Home computer ownership.
- MotherEduLevel: Mother’s education level.
- FatherEduLevel: Father’s education level.
- MathScoreAvg: Average math performance score.
- ReadingScoreAvg: Average reading performance score.
- ScienceScoreAvg: Average science performance score.

### Project Structure
- Part-I-Communicate-Data-Findings-Projct-PISA-2012.ipynb :  Focuses on data cleaning, wrangling, univariate, bivariate, and multivariate exploration of the PISA 2012 dataset. It includes feature selection, data transformation, and descriptive analysis.
- Part-II-Communicate-Data-Findings-Projct-PISA-2012.ipynb: Contains the final visual presentation of the analysis results focusing on three main aspects: gender differences, parental education impact, and study environment effects.

## Key Findings

1. Gender and Performance
   - Male students outperform female students in Math and Science.
   - Female students outperform males in Reading across most countries.

2. Parental Education Influence
   - Students whose parents hold advanced degrees tend to achieve higher scores across all subjects.
   - The performance gap between students with highly educated vs. less-educated parents is significant.

3. Technology and Study Habits
   - Most students have access to computers and the internet, but ownership alone does not strongly correlate with improved performance.
   - High-achieving students tend to dedicate more time to studying, especially in Math.

4. Country Trends
   - Singapore consistently ranks among the top three countries across all subjects.
   - Canada, Australia, and China-Shanghai also demonstrate strong academic performance distributions.


