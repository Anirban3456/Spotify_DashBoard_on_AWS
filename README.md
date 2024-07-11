# Spotify Data Analysis Project

This project leverages AWS services to analyze Spotify data using Excel (CSV) databases for artists, albums, and tracks. The workflow involves storing data in Amazon S3, transforming it with AWS Glue ETL and crawlers, and visualizing insights using AWS Quicksight.

## Table of Contents

- [Project Overview](#project-overview)
- [Architecture](#architecture)
- [Datasets](#datasets)
- [AWS Services Used](#aws-services-used)
- [Setup Instructions](#setup-instructions)
- [Data Analysis](#data-analysis)
- [Visualization](#visualization)
- [Conclusion](#conclusion)
- [License](#license)
- [Acknowledgments](#acknowledgments)

## Project Overview

The goal of this project is to analyze Spotify data to gain insights into artists, albums, and tracks. By using AWS services, we aim to create a scalable and efficient data analysis pipeline.

![image](https://github.com/Anirban3456/Spotify_DashBoard_on_AWS/assets/118114203/b47c8578-adb6-46b1-9d59-a01febd1a441)
The Spotify Dashboard.

![Untitled](https://github.com/Anirban3456/Spotify_DashBoard_on_AWS/assets/118114203/80d503fd-eff5-4213-be42-011718313a3b)

![Screenshot 2024-07-11 131248](https://github.com/Anirban3456/Spotify_DashBoard_on_AWS/assets/118114203/9d00c87f-19b3-4c5d-8af9-1f23c4da3cf4)
AWS glue pipeline.

## Architecture

1. **Data Storage:** Store CSV files in Amazon S3.
2. **Data Cataloging:** Use AWS Glue Crawlers to catalog the data.
3. **ETL Process:** Transform data using AWS Glue ETL jobs.
4. **Data Visualization:** Use AWS Quicksight to create interactive dashboards.

## Datasets

- `artists.csv`: Contains data about artists.
- `albums.csv`: Contains data about albums.
- `tracks.csv`: Contains data about tracks.

![Screenshot 2024-07-10 011543](https://github.com/Anirban3456/Spotify_DashBoard_on_AWS/assets/118114203/2872d7fa-0057-4564-8547-c087daa7a7dc)
The final Database.

## AWS Services Used

- **Amazon S3:** Storage for CSV files.
- **AWS Glue:** ETL and data cataloging.
  - Crawlers to catalog the data.
  - ETL jobs to transform the data.
- **AWS Quicksight:** Visualization and analysis.

## Setup Instructions

### Step-by-Step Guide

1. **Upload CSV files to S3:**
   - Create an S3 bucket.
   - Upload `artists.csv`, `albums.csv`, and `tracks.csv` to the bucket.

2. **Catalog the data with AWS Glue:**
   - Navigate to AWS Glue service.
   - Create a new crawler.
   - Configure the crawler to point to your S3 bucket.
   - Run the crawler to catalog the data.
     
3. **Create AWS Glue ETL jobs:**
   - Create a new Glue job.
   - Define the source as the cataloged tables.
   - Define the transformation logic (if any).
   - Define the target as a new table in the Glue Data Catalog.
   - Run the job to transform and load the data.

4. **Visualize data with AWS Quicksight:**
   - Navigate to AWS Quicksight.
   - Connect to the Glue Data Catalog.
   - Import the transformed data.
   - Create analyses and dashboards based on the data.

## Data Analysis

- Analyze trends in music genres, artist popularity, album releases, etc.
- Use Quicksight to create visual representations such as bar charts, line charts, and tables.

## Visualization

AWS Quicksight allows for creating interactive dashboards to present your findings. Some examples of visualizations you can create include:

- **Artist Popularity:** Chart showing the most popular artists based on track plays.
- **Popular Songs:** Line chart showing the most popular songs.
- **Genre Distribution:** Pie chart showing the distribution of different music genres.
- **Highest number of tracks per album:** Line chart showing the most number of songs per album.
