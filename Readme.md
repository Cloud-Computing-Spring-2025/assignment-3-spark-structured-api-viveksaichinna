
# Assignment #3 Spark Structured API: Music Listener Behavior Analysis

## *Prerequisites*

Before starting the assignment, ensure you have the following software installed and configured:

1.⁠ ⁠*Python 3.x*:
   - [Download and Install Python](https://www.python.org/downloads/)
   - Verify installation:
     ⁠ bash
     python3 --version
      ⁠

2.⁠ ⁠*PySpark*:
   - Install using pip:
     ⁠ bash
     pip install pyspark
      ⁠

3.⁠ ⁠*Apache Spark*:
   - Download from the [Apache Spark Downloads](https://spark.apache.org/downloads) page.
   - Verify installation:
     ⁠ bash
     spark-submit --version
      ⁠

4.⁠ ⁠*VS Code or any IDE* for writing scripts and working with CSV files.

---

## *Setup Instructions*

### *1. Project Structure*

Ensure your directory looks like this:

MusicListeningAnalysis/
├── input/
│   ├── listening_logs.csv
│   └── songs_metadata.csv
├── output/
│   ├── user_favorite_genres/
│   ├── avg_listen_time_per_song/
│   ├── top_songs_this_week/
│   ├── happy_recommendations/
│   ├── genre_loyalty_scores/
│   └── night_owl_users/
├── music_analysis.py
└── README.md

---

### *2. Running the Script*

You can run your analysis using the Spark CLI:

#### *a. Navigate to your project directory*

```bash
cd MusicListeningAnalysis/

Run your PySpark script

spark-submit music_analysis.py

Verify Outputs

Check your results using:

ls output/


Overview

This project uses Spark Structured APIs to analyze music listening behavior and trends from a fictional streaming platform. You’ll explore user preferences, song popularity, and engagement patterns using two input datasets.

⸻

Objectives

By completing this assignment, you’ll practice:
	1.	Reading structured data using PySpark
	2.	Performing joins and aggregations
	3.	Generating insights with filtering, grouping, and ranking
	4.	Writing results to CSV files using .write.option("header", True).csv(...)

⸻
Assignment Tasks

1.⁠ ⁠User’s Favorite Genre

Objective:
Identify each user’s favorite genre by counting how many times they played songs from each genre.

Expected Output:
Directory user_favorite_genres/ with most listened genre per user.

⸻

2.⁠ ⁠Average Listen Time per Song

Objective:
Calculate average play duration for each song using listening logs.

Expected Output:
Directory avg_listen_time_per_song/ with song-wise average durations.

⸻

3.⁠ ⁠Top 10 Most Played Songs This Week

Objective:
Get the 10 most played songs in the last 7 days.

Expected Output:
Directory top_songs_this_week/ with top 10 songs and play counts.

⸻

4.⁠ ⁠Recommend “Happy” Songs to Sad Listeners

Objective:
Find users who mostly listen to “Sad” songs and recommend up to 3 new “Happy” songs they haven’t played.

Expected Output:
Directory happy_recommendations/ with user_id and recommended songs.

5.⁠ ⁠Genre Loyalty Score

Objective:
Compute the ratio of plays in a user’s most listened genre. Return users with a loyalty score > 0.8.

Expected Output:
Directory genre_loyalty_scores/ with user_id, genre, and score.

⸻

6.⁠ ⁠Night Owl Users

Objective:
Identify users who frequently listen to music between 12:00 AM and 5:00 AM.

Expected Output:
Directory night_owl_users/ with user_id of late-night listeners.

⸻

📬 Submission Checklist
	•	PySpark script: music_analysis.py
	•	Input datasets in input/ folder
	•	Outputs generated in output/ folder
	•	Completed README.md
	•	Pushed to GitHub
	•	GitHub repo link submitted on Canvas