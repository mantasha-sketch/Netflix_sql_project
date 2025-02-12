# Netflix_sql_project
# 📊 Netflix Data Analysis  

## 🎬 Overview  
This project analyzes Netflix's content catalog using SQL to uncover trends, patterns, and insights about movies, TV shows, genres, directors, actors, and content availability across different countries. The goal is to understand how Netflix structures its content and provide valuable insights for data enthusiasts, content creators, and business strategists.  

## 🚀 Features & Insights  
This analysis answers key questions such as:  

### 📌 **Content Overview**  
- How many **movies vs. TV shows** are on Netflix?  
- What are the **most popular genres**?  
- Which countries produce the **most Netflix content**?  

### ⏳ **Time-Based Trends**  
- How has **content production changed over the years**?  
- What are the **busiest months for new releases**?  
- Which years saw the **highest content release in India**?  

### 🎭 **People Behind the Content**  
- Who are the **top directors with the most Netflix content**?  
- Which **actors appear in the most movies**?  
- How many movies has **Salman Khan starred in over the last 10 years**?  

### 🏆 **Record-Breaking Content**  
- What’s the **longest movie** on Netflix?  
- Which TV shows have **more than 5 seasons**?  
- What’s the **most common rating** for Netflix content?  

### 🔍 **Business Insights & Data Gaps**  
- Categorizing content as **"Good" or "Bad"** based on keywords like "kill" or "violence".  
- Identifying **content without directors or cast information**.  
- Exploring **top actors in Indian-produced movies**.  

## 📂 Dataset  
The dataset used in this analysis includes the following fields:  
- `show_id` – Unique identifier for each content item  
- `type` – Movie or TV Show  
- `title` – Name of the movie/TV show  
- `director` – Director(s) of the content  
- `casts` – List of actors featured  
- `country` – Country where the content was produced  
- `date_added` – When it was added to Netflix  
- `release_year` – The year it was released  
- `rating` – Content rating (e.g., PG-13, TV-MA)  
- `duration` – Duration in minutes (for movies) or seasons (for TV shows)  
- `listed_in` – Genre classification  
- `description` – A brief description of the content  

## 🛠️ Tools & Technologies Used  
- **SQL** – To perform data queries and analysis  
- **PostgreSQL / MySQL** – For database management  
- **Python (Pandas, Matplotlib, Seaborn)** – (Optional) For additional data visualization  
- **Jupyter Notebook** – (Optional) For interactive data exploration  

## 📜 SQL Queries Used
Some key SQL queries used in this project include:

- **Count Movies vs. TV Shows:**
  ```sql
  SELECT type, COUNT(*) AS count FROM netflix GROUP BY type;
  ```

- **Find the Most Common Ratings:**
  ```sql
  SELECT type, rating, COUNT(*) AS count 
  FROM netflix 
  GROUP BY type, rating 
  ORDER BY count DESC 
  LIMIT 1;
  ```

- **List All Movies Released in 2020:**
  ```sql
  SELECT * FROM netflix WHERE type = 'Movie' AND release_year = 2020;
  ```

Find more queries in the [`queries.sql`](queries.sql) file.

## 📊 Data Insights & Business Applications
The findings from this project can help:
- **Content Creators & Streaming Services** – Understand which genres and formats are most popular.
- **Marketers & Business Analysts** – Track content trends and predict future audience preferences.
- **Data Enthusiasts** – Learn how SQL can be used for real-world data analysis.

## 📌 How to Use This Project
1. **Clone the Repository**
   ```sh
   git clone https://github.com/yourusername/netflix-data-analysis.git
   cd netflix-data-analysis
   ```

2. **Load the Dataset into SQL**
   - Open PostgreSQL/MySQL
   - Import the dataset using `COPY` or `LOAD DATA INFILE`
   - Run queries from the [`queries.sql`](queries.sql) file

3. **Explore the Data**
   - Modify SQL queries based on your analysis needs
   - Use Python for data visualization (optional)

## 🏆 Future Work
- Add **data visualization** to showcase trends more effectively.
- Perform **sentiment analysis** on descriptions to classify content mood.
- Explore **machine learning models** for content recommendation.

## 🤝 Contributing
Want to improve this project? Feel free to:
- Fork the repo
- Submit a pull request
- Suggest new queries and business use cases




