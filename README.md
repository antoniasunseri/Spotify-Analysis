# Spotify Top Hits Analysis (1998–2020)

This project investigates trends in popular Spotify tracks from 1998 to 2020, focusing on how song characteristics relate to popularity. The analysis explores how features such as song length, explicit content, featured artists, and edited versions influence a track's success.

## Research Questions

The project is centered around the following key research questions:

1. **Have shorter songs become more popular over time?**
2. **Has the popularity of explicit songs increased in recent years?**
3. **Do songs that feature other artists tend to be more popular than solo performances?**
4. **Are songs with remixes or edited versions more popular than originals?**

## Dataset

- **Source**: [Kaggle - Top Spotify Tracks of 2000–2019](https://www.kaggle.com/datasets/paradisejoy/top-hits-spotify-from-20002019)
- **Dataset**: Contains 1879 top Spotify tracks spanning from 1998 to 2020.
- **Attributes Used**:
  - `artist`: The name of the artist
  - `song`: Song title includes metadata of a featured artist and whether there is a edited version
  - `duration_ms`: Song duration in milliseconds
  - `explicit`: Whether the song has profane lyrics
  - `year`: The year which the song was released
  - `popularity`: Popularity score from 1 to 89, 0 indicates a missing value
  - It also contains additional audio features such as energy, danceability, loudness, speechiness, etc. which were not used directly. 

## Data Cleaning and Preprocessing

- Removed duplicate entries and rows with invalid popularity values (e.g., 0).
- Casted data types (e.g., `duration_ms` to minutes).
- Engineered features:
  - `is_featured`: True if the song contains "feat.", "&", "x", etc.
  - `is_remix_or_edit`: True if the title contains "remix", "edit", "version", etc.
- Normalized some continous variables.
- Cleaned genres to reduce it from 59 categories to 12 categories.

## Methods

- **Exploratory Data Analysis** using pandas, seaborn, and Plotly.
- **Data Cleaning** as disscussed above.
- **Boolean feature engineering** of songs based on explicit lyrics, having collaborations, and alternate versions.
- **Normalization feature engineering** produced plots which transformed the continous variables to normal distributions.
- **Trend analysis** across years and comparison of average popularity by category.
- **Data visualization** through histograms, scatter plots, box plots, and line graphs.
- **Analysis** through static and dynamic visualizations to answer the research questions.

## Key Findings to Research Questions

- **Shorter songs are becoming more popular**, especially in the last 5 to 10 years.
- **Explicit songs** have seen a **steady rise in popularity**, reflecting cultural and industry shifts during recent years.
- **Collaborative tracks** (having featuring artists) tend to perform **better** than solo tracks and have higher popularity scores.
- **Songs with a remixed or edited versions** have a slightly higher threshold for popularity values.

## Technologies Used

- Python 3.13.2 (Versions of remaining packages are present in the requirements text file)
- Pandas and NumPy (for data manipulation and cleaning)
- Seaborn, Matplotlib & WordCloud (for the initial static plots)
- Plotly (for interactive plots embedded in dash)
- Dash (for interactive dashboard with filtering features)

## Acknowledgments

- Instructor Rahim Rasool for constant guidance and support throughout the project.
- Kaggle community for providing the dataset with condensed data of the most popular songs.
- Spotify for publishing the original music metadata.
- Matplotlib and seaborn for static visuals and other python libraries to support these.
- Plotly and Dash for interactive visualizations.
