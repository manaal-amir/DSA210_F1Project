### DSA210_F1Project  
#### Syeda Manaal Amir  
#### 33550   
#### Spring 2024-25  

__________________________________________________________________________________________________________________________________________________________________________________
# Formula 1 Fan Ratings Analysis 
### Content  
##### Deadline1:  
Project Overview  
Research Questions and Objectives  
Motivation  
Datasets & Data Collection   
Hypothesis  
Dataset Analysis Plan  
Tools and Technologies   
Expected Outcomes  
##### Deadline2:  
Procedure to deduce Findings   
Analysis of Findings  
Hypothesis Tests Results 
##### Deadline3:  
Further Feature Transformation    
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
   - Multiple-way ANOVA evaluated:
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

#### Key Observations from visualized Mean and Median 
![image](https://github.com/user-attachments/assets/bef87aa7-8d6b-4e28-9131-d128281cfea7)
- **Distribution Shape**:  
  - Ratings follow a near-normal distribution, peaking around 6.5–7.  
  - Mild left skew (fewer low ratings) but no significant outliers.  
- **Central Tendency**:  
  - **Mean**: `6.79` | **Median**: `6.81`  
  - Close alignment confirms symmetric distribution.  
- **Range & Spread**:  
  - Majority of ratings fall between 6–8 (positive bias).  
  - Minimal extreme values (low polarization).  
##### Implications for Analysis  
1. Supports use of parametric tests (e.g., ANOVA) due to ~normal distribution.  
2. Consistent mean/median reduces risk of skewed interpretations.
#### Analysis of Most Frequent Winners

#### Key Findings
- **Most Frequent Winning Driver**: `Hamilton`  
- **Most Frequent Winning Constructor**: `Mercedes`  
##### Interpretation
- Dominance of **Hamilton** and **Mercedes** aligns with known F1 trends (2014-2021 era).  
- Useful baseline for comparing fan ratings across top performers.
  #### Comparative Analysis of Mean Fan Ratings

#### By Constructor
| Constructor   | Mean Rating |
|--------------|------------|
| Red Bull     | 7.01       |
| McLaren      | 6.97       |
| Ferrari      | 6.91       |
| Mercedes     | 6.67       |
| Brawn        | 6.32       |
| BMW Sauber   | 5.36       |

##### **Insight**: Red Bull leads with highest average ratings (7.01), while BMW Sauber trails (5.36).

#### By Race Location (Top 5)
| Grand Prix               | Mean Rating |
|-------------------------|------------|
| Azerbaijan              | 8.69       |
| United States           | 7.40       |
| British                 | 7.36       |
| Canadian                | 7.33       |
| Chinese                 | 7.26       |

##### **Key Observation**: Street circuits (Azerbaijan) and North American races score highest.

#### By Year
| Year | Mean Rating |
|------|------------|
| 2012 | 7.37       |
| 2011 | 7.23       |
| 2014 | 7.13       |
| 2010 | 6.76       |
| 2018 | 6.82       |

##### **Trend**: Ratings peaked in 2011-2012, dipped in 2015 (6.33), and rebounded post-2016.

###  Visualization: Average Fan Ratings by Winning Constructor  
![image](https://github.com/user-attachments/assets/cc21fae1-368d-4d08-a886-e201a08958fc)  
##### Key Observations from the Chart
- **Red Bull** leads with the highest average fan rating (~7.0)
- Close competition between **Ferrari** and **McLaren** (~6.9-7.0)
- **Mercedes** underperforms relative to its dominance (~6.7)
- **BMW Sauber** receives the lowest ratings (~5.4)

##### Notable Insights
1. **Performance-Rating Paradox**:  
   - Mercedes' competitive success doesn't translate to top ratings
   - Red Bull's high ratings may reflect fan enthusiasm for their racing style

2. **Historical Context**:  
   - Brawn GP's modest rating (6.3) reflects their single championship season (2009)
   - BMW Sauber's low rating aligns with their limited success period

### Analysis of Fan Ratings by Grand Prix Location  
![image](https://github.com/user-attachments/assets/78ca2d20-57ac-4de8-a25c-0019f516ee66)  

#### Key Observations
- **Top Performing Circuits**:
  - Azerbaijan Grand Prix (8.69)
  - United States Grand Prix (7.40)
  - British Grand Prix (7.36)
  - Canadian Grand Prix (7.33)
  - Chinese Grand Prix (7.26)

- **Lower Rated Circuits**:
  - French Grand Prix (5.22)
  - Russian Grand Prix (5.31)
  - European Grand Prix (5.36)
  - Indian Grand Prix (5.75)
  - Mexican Grand Prix (6.05)

#### Interesting Patterns
1. **Street Circuits Dominate**:
   - Top 3 rated races (Azerbaijan, Canada, Singapore) are all street circuits
   - Suggests fans prefer challenging, unpredictable tracks

2. **Regional Preferences**:
   - North American races consistently score well (USA, Canada, Mexico)
   - Traditional European circuits show more variable ratings

3. **Historical Context**:
   - Lower ratings for newer circuits (Russia, India) may reflect fan attachment to classic tracks
   - French GP's low rating could relate to its temporary return after long absence
##### Clearer in the following visualization  
![image](https://github.com/user-attachments/assets/9a5a9227-f06f-4944-a60f-dc80445d27dd)  

### Analysis of Rating Trends at Top Tracks by Winning Constructor
![image](https://github.com/user-attachments/assets/ba36002b-a59d-43f7-9d3f-790736d3502c)  

#### Key Visual Patterns
- **Temporal Trends**:  
  - Ratings peaked around 2011-2012 (7.5+) across most tracks  
  - Significant dip in 2015 (6.0-6.5) followed by recovery  
  - Mercedes-era (2014-2018) shows stable but lower ratings vs. earlier seasons  

- **Track-Specific Insights**:  
  - **British Grand Prix** maintains consistently high ratings (>7.0)  
  - **Monaco GP** shows widest fluctuations (6.0-8.0)  
  - **Spanish GP** has steepest decline post-2012  

#### Constructor Performance
- **McLaren/Ferrari (2008-2013)**:  
  - Associated with highest ratings at classic tracks  
  - Particularly strong at Belgian GP (~7.8 peak)  

- **Mercedes (2014-2018)**:  
  - Ratings 0.5-1.0 points lower than predecessors at same tracks  
  - Exception: Strong performance at British GP  

- **Red Bull Transition**:  
  - Ratings improve post-2016 as competition increases  

#### Notable Anomalies
- **2015 Drop**:  
  - Corresponds to Mercedes dominance (18/19 wins)  
  - Suggests fan preference for competitive seasons  

- **Brawn's 2009 Spike**:  
  - Brief rating surge during fairytale championship season  

### Analysis of Fan Ratings by Season Segment
 ![image](https://github.com/user-attachments/assets/c048936a-8905-4fd1-95e7-5b9d195e4678)  
#### Key Trends Observed
- **Early Season Peak**:  
  Highest ratings in first 5 races (avg ~6.8)  
  Suggests fan enthusiasm at season start  

- **Mid-Season Dip**:  
  Ratings drop in segments 6-10 and 11-15 (~6.2-6.4)  
  Possible "summer slump" effect  

- **Late Season Recovery**:  
  Final segment (race 16+) rebounds to ~6.6  
  Likely due to championship climaxes  

#### Potential Explanations
1. **Calendar Effects**:
   - Early races often include classic circuits (Australia, Bahrain)
   - Mid-season contains less popular European summer races
   - Late season features title-deciding events

2. **Viewing Patterns**:
   - Fresh excitement at season start
   - Fatigue during mid-season
   - Renewed interest during championship battles

3. **Competitiveness**:
   - Early season often has closer competition
   - Dominant teams may pull ahead mid-season

#### Recommended Actions
- **For Broadcasters**:
  - Boost mid-season coverage with special features
  - Highlight developing storylines to maintain engagement

- **For Teams**:
  - Focus performance spikes on traditionally low-rated segments
  - Analyze if specific circuit types affect segment trends

### Fan Ratings by Winning Driver - Key Findings
![image](https://github.com/user-attachments/assets/eeae3b4e-6e91-4915-951b-1f8d5961bc44)  
#### Top Performers
- **Hamilton/Verstappen/Vettel** dominate (7.5-8.5 ratings)  
#### Rating Distribution  
- **Mean**: 6.81 (±0.87 SD)  
- **Range**: 4.3 (Karthikeyan 2011) → 9.1 (Hamilton 2020)  
- **75th percentile**: 7.4 (only 25% of winners exceed this)

__________________________________________________________________________________________________________________________________________________________________________________  

## 🏎️ Hypothesis Tests Results  

### Seasonal Timing vs. Fan Ratings Analysis  
#### Hypothesis Testing  
- **Null Hypothesis (H₀):** assumes that race ratings are random and not affected by the variables being analyzed.    
- **Alternative Hypothesis (H₁):** suggests that one or more of these factors do impact how fans rate a race.   
  
#### Test Used: Pearson's r correlation (α = 0.05)  
![image](https://github.com/user-attachments/assets/d5b3f947-2f1a-4981-b4dc-27aafce46b40)
#### Key Findings  
| **Metric**       | **Value** | **Interpretation**                   |
|------------------|-----------|--------------------------------------|
| Correlation (r)  | -0.10     | Weak negative relationship           |
| p-value          | 0.1691    | Not statistically significant        |
| Effect Size      | Small     | Negligible practical effect          | 
#### Interpretation     
Weak trend suggests later races may have slightly lower ratings  
Effect is too small to be practically meaningful  
Other factors likely dominate rating differences  

### Statistical Test Results for Fan Ratings using MANOVA

| **Factor**              | **Test Type** | **Statistic** | **p-value** | **Significance**          |
|-------------------------|---------------|---------------|-------------|----------------------------|
| Winning Constructor     | ANOVA         | F = 1.28      | 0.2739      | Not significant           |
| Winning Driver          | ANOVA         | F = 2.04      | 0.0168      | Significant               |
| Track Location          | ANOVA         | F = 1.71      | 0.0243      | Significant               |

> Note: Significance is determined at the p < 0.05 threshold.

#### Key Findings
- **Winning Constructor**: Fan ratings do not significantly differ based on the constructor that won (p = 0.27).
- **Winning Driver**: Fan ratings significantly differ depending on which driver won the race (p = 0.0168).
- **Track Location**: Fan ratings significantly differ depending on where the race was held (p = 0.0243).

#### Dataset Overview
| Metric                | Count |
|-----------------------|-------|
| Total races analyzed  | 202   |
| Unique constructors   | 6     |
| Unique drivers        | 15    |
| Unique tracks         | 26    |

### Final Conclusion
The analysis **rejects the null hypothesis**. While winning constructor has no significant effect on fan ratings, both the **winning driver** and **track location** show statistically significant impacts. This suggests that **who wins** and **where the race takes place** can meaningfully influence how fans rate a race.

### Some other tests were conducted on various other hypotheses:

#### Hypothesis 1: ANOVA Test – Ratings by Winning Constructor  
H₀: The average race ratings are the same across different constructors.  
H₁: At least one constructor has a different average race rating.  
The ANOVA test shows that there is no statistically significant difference in average fan ratings across the six winning constructors (F = 1.280, p = 0.2739). This suggests that which constructor wins a race does not meaningfully impact how fans rate the event.  

#### Hypothesis 2: t-Test – Mercedes vs. Red Bull  
H₀: The average race ratings for races won by Mercedes and Red Bull are the same.  
H₁: The average ratings are different.  
![image](https://github.com/user-attachments/assets/e1b0eebb-68f2-45b6-949e-d96ba852ba07)  
The t-test comparing fan ratings for races won by Mercedes vs. Red Bull shows no statistically significant difference (t = -1.629, p = 0.1055). This indicates that fan ratings are not meaningfully different between races won by these two dominant teams.  

#### Hypothesis 3: t-Test – Ratings for Azerbaijan vs. Turkish Grand Prix  
H₀: Azerbaijan and Turkey have the same average race rating.  
H₁: Their ratings differ.  
![image](https://github.com/user-attachments/assets/642c32ed-e09b-48f1-8199-6587f6c4e6e6)    
The t-test comparing fan ratings for races held in Azerbaijan vs. Turkey reveals a statistically significant difference (t = 3.135, p = 0.0469). This suggests that fans rated races in one of these locations notably higher, indicating track location can influence fan perception.



