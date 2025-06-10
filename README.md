# Spotify Top Hits Analysis (1998–2020)

This project investigates trends in popular Spotify tracks from 1998 to 2020, focusing on how song characteristics relate to popularity. The analysis explores how features such as song length, explicit content, featured artists, and edited versions influence a track's success.

## Research Questions

The project is centered around the following key research questions:

1. **Have shorter songs become more popular over time?**
2. **Has the popularity of explicit songs increased in recent years?**
3. **Do songs that feature other artists tend to be more popular than solo performances?**
4. **Are remixes or edited versions of songs more popular than originals?**

## Dataset

- **Source**: [Kaggle - Top Spotify Tracks of 2000–2019](https://www.kaggle.com/datasets)
- **Scope**: Contains over close to 2000 top Spotify tracks spanning from 1998 to 2020.
- **Attributes Used**:
  - `artist`: Artist or band name
  - `song`: Song title
  - `duration_ms`: Song duration in milliseconds
  - `explicit`: Whether the song is marked explicit
  - `year`: Release year
  - `popularity`: Popularity score (0–100)
  - Additional audio features such as energy, danceability, loudness, speechiness, etc.

## Data Cleaning and Preprocessing

- Removed duplicate entries and rows with placeholder popularity values (e.g., 0).
- Casted data types (e.g., `duration_ms` to minutes).
- Engineered features:
  - `is_featured`: True if the song contains "feat.", "&", "x", etc.
  - `is_remix_or_edit`: True if the title contains "remix", "edit", "version", etc.


## Methods

- **Exploratory Data Analysis** using pandas, seaborn, and Plotly.
- **Boolean classification** of songs based on explicit lyrics, collaborations, and alternate versions.
- **Trend analysis** across years and comparison of average popularity by category.
- **Data visualization** through histograms, scatter plots, box plots, and line graphs.

## Key Findings

- **Shorter songs are becoming more popular**, especially in recent years.
- **Explicit songs** have seen a **steady rise in popularity**, reflecting cultural and industry shifts.
- **Collaborative tracks** (featuring artists) tend to perform **better** than solo tracks.
- **Remixed or edited versions** of songs show a slight advantage in popularity, though the effect is less pronounced.

## Technologies Used

- Python 3.12
- Pandas
- Plotly
- Dash (for interactive dashboard)
- NumPy
- Seaborn & Matplotlib (for additional static plots)

## Acknowledgments

- Instructor Rahim Rasool
- Kaggle community for providing the dataset.
- Spotify for the original music metadata.
- Matplotlib and seaborn for static visuals and other python libraries to support these.
- Plotly and Dash for interactive visualizations.
