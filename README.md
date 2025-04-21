### DSA210_F1Project  
#### Syeda Manaal Amir  
#### 33550   
#### Spring 2024-25  

__________________________________________________________________________________________________________________________________________________________________________________
# Formula 1 Fan Ratings Analysis 
### Content  
Project Overview  
Research Questions and Objectives  
Motivation  
Datasets & Data Collection   
Hypothesis  
Dataset Analysis Plan  
Tools and Technologies   
Expected Outcomes  
Procedure to deduce Findings   
Analysis of Findings  
__________________________________________________________________________________________________________________________________________________________________________________  

## 🏎️ Project Overview 

This project explores **whether Formula 1 race ratings are influenced more by the winning driver, the winning constructor, the track location, or the seasonal placement**.<br>  
By analyzing **historical race data (2008-2018)**, we aim to understand what makes a race more exciting for fans.  

### **Factors Being Analyzed**  
- **Winning Driver** – Do highly rated races feature **popular drivers** like Lewis Hamilton or Max Verstappen? Do **surprise winners** increase fan engagement?  
- **Winning Constructor (Team)** – Do **dominant teams** (e.g., Red Bull, Mercedes, Ferrari) affect ratings? Are fans more excited when an **underdog team** wins?  
- **Track Location** – Are certain circuits (like Monaco, Silverstone, or Spa) consistently rated higher? Do **historic or high-speed tracks** make races more thrilling?  
- **Seasonal Placement** – Does the **timing of the race** within the season (early, mid, or late) impact fan engagement? Do final championship-deciding races get higher ratings?  

To analyze this, we will use **historical race data from 2008 to 2018**, examining how **fan ratings correlate with different race characteristics**.<br>  
By identifying these patterns, we aim to provide insights into what makes a Formula 1 race **truly exciting for fans**.  

__________________________________________________________________________________________________________________________________________________________________________________  


## 🏎️ Research Questions and Objectives 
- Explore how race outcomes are affected by the winning driver, the winning constructor, track location, and seasonal placement, and how these factors influence fan ratings.<br>
- Pinpoint which race characteristics most strongly impact fan engagement, determining whether fans care more about driver performance, team dominance, track uniqueness, or race timing.)<br>
- Leverage race data to identify trends in fan ratings, helping uncover the elements that make a race more exciting and enjoyable for audiences.<br>
- Utilize techniques from the DSA 210 course, including data merging, visualization, and modeling, to apply real-world data science principles in sports analytics.<br>
  
__________________________________________________________________________________________________________________________________________________________________________________  

## 🏎️ Motivation 
I have always been fascinated by **Formula 1**, not just as a sport but also as a cultural phenomenon.<br>  
Recently, I noticed a recurring debate online:  

> *"Do people, especially girls, watch F1 because of the drivers, or because of the sport itself?"*  

Some argue that **drivers have celebrity status**, influencing fan engagement more than the actual racing.<br>  
Others claim that **team performance and race excitement matter more** than individual personalities.<br>  

This debate made me curious:  
- **Do fan ratings depend more on the winning driver or the winning team?**  
- **Are certain tracks or seasons naturally more exciting, or does a popular driver winning boost engagement?**  
- **Can data actually prove whether F1 drivers are more than just athletes—but also celebrities?**  
Through this project, I want to **go beyond opinions and use data to find answers**.<br>  
By analyzing **race results, fan ratings, and track information**, I hope to uncover whether **Formula 1 fandom is driven by the sport itself or the personalities of its stars**.<br>  

Additionally, this project gives me the chance to apply **real-world data science skills** from my **DSA 210 course**, allowing me to explore how data-driven insights can shape our understanding of sports and entertainment.  

__________________________________________________________________________________________________________________________________________________________________________________  


## 🏎️ Datasets & Data Collection 
The following table contains the datasets I will be exploiting along wiht thier description and usage.  
| Dataset                   | Description                          | Usage                          |
|---------------------------|--------------------------------------|--------------------------------|
| `results.xlsx`             | Finishing positions of drivers      | Identify the winning driver   |
| `constructor_standings.xlsx` | Constructor rankings each season  | Find the winning constructor  |
| `races.xlsx`              | Contains track locations & race dates | Extract track & month info    |
| `fan_ratings.xlsx`        | Fan ratings for each race           | The dependent variable        |

### The variables being analyzed are:
- The fan ratings, Winning Drivers; compiled from previously released records on racefans.net  
- Track name  
- Seasonal Placement of Race    
- Winning constructor;  
  - previously mentioned data (except ratings, and winning drivers) all taken from a publicly avaiable dataset on kaggle: https://www.kaggle.com/datasets/melissamonfared/formula-1?select=circuits.csv <br>
  
The Excel file (.xlsx) containing fan ratings and winning drivers will serve as the primary dataset. It will be enriched by merging additional .xlsx files, incorporating relevant independent variables from the remaining datasets to create a comprehensive dataset for analysis.

__________________________________________________________________________________________________________________________________________________________________________________  

## 🏎️ Hypothesis  

- **H₀ (Null Hypothesis):** The **race winner, winning constructor, track location, and seasonal placement** have **no significant impact** on fan ratings.  
    - assumes that race ratings are random and not affected by the variables being analyzed.  
- **H₁ (Alternative Hypothesis):** At least one of these factors **significantly influences** fan ratings, meaning that race excitement is affected by **who wins, where the race is held, or when it takes place**.  
    - suggests that one or more of these factors do impact how fans rate a race.  

__________________________________________________________________________________________________________________________________________________________________________________  

## 🏎️ Dataset Analysis Plan 
- Data Collection
- Visualization
- Hypothesis Testing
- Trend Analysis  

__________________________________________________________________________________________________________________________________________________________________________________  

## 🏎️ Tools and Technologies  

To analyze and visualize the data effectively, I will utilize the following tools:  

- **Python** → The core programming language for handling datasets, performing statistical analysis, and running models, either through Google Colab or Visual Studio Code.  
- **Pandas** → Essential for **data preprocessing, filtering, and transformation** to prepare insights.  
- **Matplotlib & Seaborn** → Used for generating **graphs, heatmaps, and trend visualizations** to better understand the relationship between variables.  

__________________________________________________________________________________________________________________________________________________________________________________  

## 🏎️ Expected Outcomes  
By the end of this project, the aim is to answer:<br>

Do fans care more about the driver or the team winning?<br>
Are certain tracks or seasonal placements more exciting?<br>
Can we predict fan ratings based on race data?<br>  

__________________________________________________________________________________________________________________________________________________________________________________  

## 🏎️ Procedure to deduce Findings   
The analysis pipeline executed the following steps:

1. **Data Preparation**
   - Four key datasets (race ratings, constructor standings, race details, constructor info) were loaded from Excel files
   - Column names were standardized and winning constructors (position=1) were identified
   - Datasets were merged to connect fan ratings with race winners
   - Results were sorted chronologically by season and race number

2. **Data Quality Assurance**
   - Missing value checks were performed
   - Merge success was verified by examining matched records
   - Column structures and data samples were inspected

3. **Exploratory Analysis**
   - Rating distributions were visualized via histograms with density curves
   - Central tendency metrics (mean, median, mode) were computed
   - Group averages were compared across:
     - Constructors (winning teams)
     - Race locations (circuits)
     - Seasonal years

4. **Statistical Testing**
   - Pearson correlation assessed seasonal timing effects (race number vs ratings)
   - One-way ANOVAs evaluated:
     - Constructor-based rating differences
     - Driver-based rating differences  
     - Track-based rating differences
   - Results included F-statistics, p-values, and significance flags (p<0.05)

5. **Visualization**
   - Multiple plot types (histograms, bar charts, scatter plots) were generated
   - Visualizations highlighted relationships between ratings and:
     - Temporal factors (season progress, year)
     - Performance factors (winning teams/drivers)
     - Geographical factors (race locations)

The pipeline transformed raw Formula 1 data into an analysis-ready format and systematically investigated potential drivers of fan ratings through both statistical testing and visual exploration.  
__________________________________________________________________________________________________________________________________________________________________________________  

## 🏎️ Analysis of Findings  
