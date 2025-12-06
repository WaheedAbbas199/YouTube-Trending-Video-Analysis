YouTube Trending Video Analysis 📈
This project delves into a dataset of YouTube trending videos to uncover insights into what makes videos popular in India. By performing comprehensive data preparation, feature engineering, and visualization, we identify key trends and characteristics of high-performing content.

Project Goals
Load and clean the raw video trending dataset.
Engineer new features to enhance analytical depth.
Analyze category performance based on views, likes, dislikes, and comments.
Investigate relationships between key metrics.
Identify trends related to publishing times and channel performance.
Step-by-Step Analysis Summary
1️⃣ Data Preparation and Cleaning
Loaded the dataset: Started by loading the INvideos.csv into a pandas DataFrame.
Handled Missing Values & Duplicates: Ensured data quality by dropping any null values and removing duplicate entries, leading to a clean dataset of (32562, 16) records.
Data Type Conversion: Converted essential columns (category_id, views, likes, dislikes, comment_count) to appropriate numerical types to facilitate calculations and analysis. Date columns (trending_date, publish_time) were converted to datetime objects, and their timezone information was harmonized for accurate date arithmetic.
2️⃣ Feature Engineering
days_to_trend: Calculated the duration (in days) it took for a video to trend by subtracting publish_time from trending_date.
trend_weekday & pub_hour: Extracted the day of the week a video started trending and the hour it was published, providing temporal insights.
like_view_ratio & dislike_view_ratio: Computed ratios of likes/dislikes to views to understand audience sentiment relative to viewership.
engagement Score: Developed an engagement score (likes + comment_count) / views to capture overall audience interaction.
3️⃣ Category Performance Analysis
Average Views by Category: Visualized average views across categories, revealing that Category ID 20 (Gaming/Film & Animation) and 15 (Sports) typically garnered the highest average views. (See Average Views Plot)
Average Likes & Comments by Category: Similar trends were observed for likes and comments, with Category ID 15 and 20 often leading, indicating strong engagement in these content types. (See Average Likes Plot, See Average Comments Plot)
Dislike-to-View Ratio: Category ID 28 (Science & Technology) and 23 (Comedy) exhibited higher dislike-to-view ratios, suggesting potentially more polarizing or niche content. (See Dislike/View Ratio Plot)
Days to Trend: Analysis of days_to_trend showed Category ID 1 (Film & Animation) took the longest to trend on average, while categories like 27 (Education) and 29 (Nonprofits & Activism) trended the fastest, often within 1-2 days. (See Average Days to Trend Plot)
4️⃣ Channel Performance Analysis
Top Channels by Average Views/Likes: Identified top channels based on average views and likes, with
YouTube Spotlight
and
TaylorSwiftVEVO
consistently appearing at the top. (See Top Channels by Avg Views Plot, See Top Channels by Avg Likes Plot)
Worst Channels by Dislike/View Ratio: Highlighted channels with high dislike_view_ratio, such as
Mallika
and
Kamaal R Khan - KRK

, indicating content that might be more controversial or receive negative feedback. (See Worst Channels by Dislike/View Ratio Plot)

5️⃣ Engagement & Temporal Analysis
Engagement Rate by Category: Explored engagement scores, revealing Category ID 28 (Science & Technology) and 23 (Comedy) had strong engagement despite potentially higher dislikes. (See Engagement Rate Plot)
Trending Count by Weekday: Analyzed the distribution of videos trending throughout the week, showing Tuesday and Sunday as peak days for videos appearing on the trending list. (See Trending Count by Weekday Plot)
6️⃣ Content Clustering & Correlation
Text Clustering (KMeans + PCA): Applied TF-IDF vectorization and KMeans clustering on video titles and tags, then used PCA for dimensionality reduction, revealing distinct content clusters. (See Text Clusters Plot)
Correlation Heatmap: Examined correlations between numerical metrics, finding strong positive correlations between views, likes, and comment_count, indicating that popular videos tend to generate more overall interaction. Dislikes also showed a positive correlation, suggesting that highly viewed videos attract both positive and negative feedback. (See Correlation Heatmap Plot)
7️⃣ Data Distribution Overview
Histograms of Numerical Features: Generated histograms for all numerical columns (category_id, views, likes, dislikes, comment_count, like_view_ratio, dislike_view_ratio, days_to_trend, engagement, pub_hour, cluster) to visualize their distributions, ranges, and frequencies, confirming patterns like heavy right-skewness for engagement metrics. (See Histograms)
Conclusion
This analysis provides valuable insights into the dynamics of YouTube trending videos, highlighting the importance of content type, audience engagement patterns, and optimal timing for maximizing visibility. These findings can guide content creators and marketers in developing more effective strategies.

Explore the Notebook 🚀
Feel free to dive into the full Colab notebook for the complete code and detailed visualizations....!
