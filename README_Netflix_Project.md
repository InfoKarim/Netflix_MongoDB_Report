# Netflix MongoDB Analysis Project

This project showcases an end-to-end data analysis pipeline using **MongoDB** and **Docker**, applied to the Netflix Movies & TV Shows dataset from Kaggle.

## 📦 Dataset Overview
- **Source:** [Netflix Movies and TV Shows - Kaggle](https://www.kaggle.com/datasets/shivamb/netflix-shows)
- **Format:** CSV
- **Records:** 8,807 entries
- **Fields:** `type`, `title`, `director`, `cast`, `country`, `date_added`, `release_year`, `rating`, `duration`, `listed_in`, `description`

## 🛠️ Tools & Technologies
- MongoDB (v5)
- Docker
- Mongo Shell
- Aggregation Framework

## 📊 Key Analyses
- 📌 Total number of titles
- 📌 Distinct content types (Movies vs TV Shows)
- 📌 Top 5 producing countries
- 📌 Earliest release year in the dataset
- 📌 Sample document inspection

## 🚀 How It Works

1. **Run MongoDB via Docker:**
```bash
docker run --name mongodb \
  -p 27017:27017 \
  -d \
  -v ~/dsc505:/data/db \
  mongo:5
```

2. **Import the dataset:**
```bash
docker exec mongodb mongoimport \
  --db dsc505 \
  --collection netflix \
  --type csv \
  --headerline \
  --file /data/db/netflix_titles.csv
```

3. **Run aggregation queries in Mongo Shell.**

## 🖼️ Screenshots

Query results and sample document views can be found in the `/screenshots/` folder.

## 📄 Report

The detailed report of the project, including code, queries, and analysis results, is available here:
- [Netflix_MongoDB_Report.pdf](report/Netflix_MongoDB_Report.pdf)

