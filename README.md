# DSA210_F1Project  
Syeda Manaal Amir  
33550   
Spring 2024-25  

............

🏎️ Formula 1 Fan Ratings Analysis

............

🏎️ Project Overview  
This project explores whether Formula 1 race ratings are influenced more by the winning driver, the winning constructor, the track location, or the seasonal placement.<br>
By analyzing historical race data (1950-2024), we aim to understand what makes a race more exciting for fans.

.............

🏎️ Research Questions  
Do race winners impact fan ratings? (Do popular or dominant drivers affect engagement?)<br>
Do constructors influence ratings? (Are fans more engaged when underdog teams win?)<br>
Does track location matter? (Are historic venues like Monaco or Silverstone more exciting?)<br>
Does seasonal placement affect ratings? (Do early-, mid-, or late-season races receive different engagement?)<br>
  
.............

🏎️ Datasets & Data Collection  
| Dataset                   | Description                          | Usage                          |
|---------------------------|--------------------------------------|--------------------------------|
| `results.csv`             | Finishing positions of drivers      | Identify the winning driver   |
| `constructor_standings.csv` | Constructor rankings each season  | Find the winning constructor  |
| `races.csv`              | Contains track locations & race dates | Extract track & month info    |
| `fan_ratings.csv`        | Fan ratings for each race           | The dependent variable        |

Fan Ratings Data: compiled from racefans.net <br>
Track Characteristics, Constructor and Driver Popularity: https://www.kaggle.com/datasets/melissamonfared/formula-1?select=circuits.csv <br>
  
.............

🏎️ Analysis Plan  
1️⃣ Data Preprocessing & Merging
Clean and merge fan_ratings.csv with results.csv, constructor_standings.csv, and races.csv.<br>
Extract relevant columns: winner (driver, constructor), track location, seasonal placement.<br>
  
.............

2️⃣ Exploratory Data Analysis (EDA)  
Visualize fan rating trends over time.<br>
Compare race ratings by winner (do certain drivers get higher ratings?).<br>
Analyze constructor impact (does team dominance lower excitement?).<br>
Check location & seasonal trends (do early- or late-season races get better ratings?).<br>
  
.............

3️⃣ Statistical & Machine Learning Models  
Correlation Analysis → Find relationships between race winners, constructors, seasonal placement, track location, and ratings.<br>
Regression Model → Predict fan ratings based on race characteristics.<br>
  
.............

4️⃣ Interpretation & Insights  
Determine whether driver dominance, team success, track uniqueness, or seasonal placement has the biggest impact on race excitement.<br>
Provide visualizations (scatter plots, bar charts, heatmaps) to support findings.<br>
  
.............

🏎️ Expected Outcomes  
By the end of this project, we aim to answer:<br>

Do fans care more about the driver or the team winning?<br>
Are certain tracks or seasonal placements more exciting?<br>
Can we predict fan ratings based on race data?<br>
