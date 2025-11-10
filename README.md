# Python-SQLite-Google-Drive-Automation
This project is a lightweight ETL pipeline built using Python. It extracts product sales data from a public API, cleans and transforms it, stores it in SQLite, and exports a clean CSV into a Google Drive folder for visualization in Tableau.
# Why I built this
I originally planned to use enterprise tools like Snowflake and Apache Airflow.
But for the scope and scale of this project, I realized:
Snowflake was excessive
Airflow wasn’t compatible with Python 3.13 on Windows
Simple tools could deliver the same value with far less overhead
So I leaned into a lightweight approach. SQLite became my database. A Google Drive folder acted as my trigger mechanism. And a scheduled Python script stitched everything together.
# Tech Stack
Python (Extraction + Transformation)
SQLite (Local storage instead of Snowflake)
Google Drive (Trigger folder + output sync)
Tableau (Visualization)
# Work flow Dia
<img width="1035" height="582" alt="image" src="https://github.com/user-attachments/assets/bb700cd8-2244-4255-a5b6-8c08ef675821" />
# Folder Structure

etl_project/
│
├── etl/
│   ├── extract.py
│   ├── transform.py
│   ├── load.py
│   └── config.py
│
├── main.py
├── requirements.txt
└── README.md

# Pipeline Flow
Extract (API)
     → Transform (pandas)
     → Load (SQLite)
     → Export (CSV)
     → Sync to Google Drive → Tableau Dashboard
# to run 
pip install -r requirements.txt
python main.py
The cleaned CSV will appear in your Google Drive folder automatically.

# Tableau Dashboard output
<img width="1241" height="996" alt="image" src="https://github.com/user-attachments/assets/e32a6978-26f5-4674-9f35-24af965842ce" />

