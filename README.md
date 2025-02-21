# Premier Predictor ⚽  

Premier Predictor is a **web scraping and machine learning project** that predicts the winner of English Premier League matches. The project scrapes match data using **BeautifulSoup and requests**, processes the data using **pandas**, and trains a **Random Forest model** to predict match winners.

## Features  
- Scrapes EPL match results, scores, and shooting stats from [FBRef](https://fbref.com/en/)  
- Cleans and structures data using **pandas**  
- Generates **rolling averages** for past match performances  
- Trains a **Random Forest** model to predict match outcomes  
- Evaluates prediction accuracy and iteratively improves precision  

## How It Works  
### 1. Web Scraping  
- Uses **requests** to fetch EPL standings and team URLs.  
- Uses **BeautifulSoup** to parse HTML and extract links to individual team pages.  
- Scrapes **match scores, shooting stats, and team performance history**.  

### 2. Data Processing & Cleaning 
- Converts scraped HTML tables into **pandas DataFrames**.  
- Computes **rolling averages** for key stats like shots, goals, and free kicks.  
- Filters data to include **only Premier League matches**.  

### 3. Machine Learning  
- Defines a **binary classification problem**: predicting if a team will win (1) or not (0).  
- Trains a **Random Forest Classifier** using:  
  - Venue (home/away)  
  - Opponent team  
  - Match hour & day  
  - Rolling averages of past performance  
- Evaluates performance using **precision score** to measure prediction accuracy.  

### 4. Performance Improvements  
- Uses **rolling averages** to capture team **form** in recent matches.  
- Merges **both sides of each match** to improve predictions.  
- Optimizes model parameters for better precision.  

## Results
53% Precision
58% Accuracy


## Future Improvements  
Scrape **more seasons** to improve predictions.  
Use **additional match statistics** (e.g., player injuries, lineups, weather).  
Try **different machine learning models** (e.g., neural networks).  
Analyze **home vs. away performance trends**.  