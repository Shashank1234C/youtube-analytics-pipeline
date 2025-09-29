# YouTube Analytics Pipeline

## Overview
A simple **ETL pipeline** that fetches YouTube video and channel data via the **YouTube API**, transforms it, and loads it into **PostgreSQL** for analysis.

---

## Tech Stack
- Python (pandas, SQLAlchemy, google-api-python-client)  
- PostgreSQL  
- YouTube Data API  

---

## Setup
1. Clone repo:  
   git clone https://github.com/Shashank1234C/youtube-analytics-pipeline.git 
   cd youtube-analytics-pipeline

2. Create and activate venv:  
   python -m venv venv  
   # Windows  
   .\venv\Scripts\Activate  
   # Mac/Linux  
   source venv/bin/activate

3. Install dependencies:  
   pip install -r requirements.txt

4. Create `config.env` from `config.env.example` and add your credentials:  
   YOUTUBE_API_KEY=your_api_key_here  
   POSTGRES_URL=postgresql+psycopg2://username:password@localhost:5432/youtube_analytics

---

## Run ETL
python etl_pipeline.py

---

## Database Schema
- **dim_channels:** channel info  
- **dim_videos:** video info  
- **fact_video_stats:** video stats (views, likes, comments)  

---

## License
MIT License
