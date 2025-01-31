# Testline_Assignment
 Project Overview

This project analyzes quiz performance using historical and current quiz data. It extracts key insights into users' strengths, weaknesses, and trends in scores, accuracy, and speed. The analysis leverages Python, Pandas, and visualization libraries like Matplotlib and Seaborn to generate insights and recommendations for improving quiz performance.

⚙️ Setup Instructions

1. Clone the Repository

  git clone <repository-url>
  cd <repository-folder>

2. Install Dependencies

Ensure you have Python installed. Then install the required packages:

pip install pandas requests matplotlib seaborn

3. Run the Analysis Script

python analysis.py

📂 Approach Description

Data Collection:

Fetches current quiz data from https://www.jsonkeeper.com/b/LLQT.

Fetches historical quiz data from https://api.jsonserve.com/XgAgFJ.

Converts JSON responses into structured Pandas DataFrames.

Code Explanation:

Import Necessary Libraries:

pandas for data manipulation.

requests for fetching JSON data from URLs.

matplotlib.pyplot and seaborn for data visualization.

ast for safely parsing string representations of Python objects.

Load and Process Current Quiz Data:

Fetch JSON data from the current_quiz_url.

Convert the JSON data into a Pandas DataFrame.

Remove unnecessary columns (questions).

Save the cleaned data to a CSV file for further analysis.

Load and Process Historical Quiz Data:

Fetch JSON data from the historical_quiz_url.

Convert dictionaries to strings where necessary to avoid hashability issues.

Remove duplicates and unnecessary columns (response_map).

Save the cleaned data to a CSV file.

Parsing and Flattening Quiz Data:

Convert nested quiz data into structured Pandas DataFrames.

Extract key quiz attributes such as title, topic, and questions_count.

Handle missing values and standardize column data types.

Analysis & Insights Generation:

Topic-wise Performance: Group quizzes by topic and calculate statistics like mean scores, accuracy, and speed.

Time-Based Trends: Aggregate quiz performance over months and track score improvements.

Weak Area Detection: Identify topics with the lowest scores and accuracy for improvement recommendations.

Visualization:

Bar Chart: Display average scores by topic using seaborn.barplot.

Line Plot: Track score trends over time for different topics.

Score Improvement Plot: Display progress across multiple attempts using matplotlib.plot.

Recommendation System:

Identify weak topics and recommend areas of improvement.

Highlight speed issues and suggest pacing improvements.

Detect negative scoring trends and advise strategies to reduce incorrect guesses.

📊 Insights Summary

Weakest Topics: Identified by lowest average score and accuracy.

Score Trends: Highlights areas where performance is improving or declining.

Time Management Issues: Topics with low speed scores suggest areas where users should practice pacing.

Guessing & Negative Scoring: Topics with high negative scores indicate over-reliance on guessing.

Recommendations: Suggests targeted improvements based on historical data trends.

🚀 Future Improvements

Integrate machine learning to predict weak areas dynamically.

Implement a web dashboard for real-time quiz tracking.

Expand data sources to include more quiz platforms.
