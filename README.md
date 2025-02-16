# Analysis of Olympic sports and medals (1896 - 2012)

Data link: [Olympic Summer Data](https://www.kaggle.com/datasets/the-guardian/olympic-games?select=summer.csv)

## An overview

The analysis examines Olympic Games data stored in 'summer.csv' using Python's pandas, matplotlib, and seaborn libraries. Here are the main findings and analyses performed:

Individual Athlete Analysis
- The code specifically looked at notable athletes like Jesse Owens and Carl Lewis
- A comprehensive analysis of medal counts (Gold, Silver, Bronze) by athletes shows top performers across different Olympic years
- The analysis includes visualisation of top medal winners using horizontal bar charts

Country-Specific Analysis
- Detailed examination of USA performance, particularly gold medals by gender over time
- Analysis of China's (CHN) performance in 2008 Olympics, breaking down medals by gender
- Comparative analysis of Italy, France, and Germany's medal performances using stacked bar charts
- Creation of a heatmap for the 2008 Olympics showing medal distribution across countries

Temporal Analysis
- The dataset spans multiple Olympic years
- Total medal counts were analyzed and visualised across years using stacked bar charts
- Trend analysis of medal distributions over time using line plots
- The code tracks the evolution of participation and performance metrics over different Olympic years

USA-Specific Deep Dive
- Created a detailed analysis of top USA winners for each Olympic year
- Combined athlete names with years to create comprehensive performance summaries
- Visualised USA's top performers across different Olympic years

Technical Aspects
- The analysis makes extensive use of pandas' groupby operations
- Multiple visualisation techniques are employed including:
  - Countplots for medal and gender distribution
  - Heatmaps for country-wise medal performance
  - Bar charts (both horizontal and vertical) for comparative analysis
  - Stacked bar charts for showing composition of medals

The analysis examines both individual and national performance at the Olympics, with a particular focus on medal counts and gender distribution. It employs various data manipulation techniques and visualization methods to present the findings effectively.

## Analysis techniques and a more detailed overview of the analysis process

I'll provide a more detailed analysis focusing on the key technical approaches and findings:

Detailed Data Manipulation Techniques:

1. Data Filtering and Selection
- Multiple complex filtering operations using boolean conditions, for example:
```python
df[(df.Gender == 'Men') & (df.Medal == 'Gold') & (df.Event == '100M Freestyle')]
```
- Event-specific analysis, particularly for swimming events like 100M and 200M Freestyle
- Time-based filtering for records after 1984: `df[df.Year >= 1984]`

2. Advanced Aggregation Methods
- Multilevel grouping operations:
```python
df.groupby(['Athlete','Medal']).size().unstack().fillna(0)
```
- Complex aggregation with multiple metrics:
```python
df.groupby('Country').agg({'Year':['count','min','max']})
```
- Creation of pivot-style tables for medal counts across different dimensions

Specific Findings:

1. Gender Distribution Analysis
- For China in 2008:
  - Used specialized visualization comparing medal distribution between genders
  - Implemented custom color coding (RdBu palette) for gender distinction
  - Shows gender balance in medal achievements

2. USA Performance Trends
- Created a sophisticated analysis tracking top performers over time
- Constructed a custom dataframe showing best performers per year:
```python
usa_winners = usa.groupby(['Year','Athlete','Medal']).size().unstack(fill_value=0)
usa_winners['Total'] = usa_winners['Gold'] + usa_winners['Silver'] + usa_winners['Bronze']
```
- Generated a 'Brief' field combining athlete names with years for better visualization

3. Medal Distribution Patterns
- Total medals analysis across years shows historical trends
- Created stacked visualizations showing the proportion of Gold, Silver, and Bronze medals
- Implemented specialized sorting to identify top performers in each medal category

4. Country Comparisons
- Detailed analysis of Italy, France, and Germany using custom color coding:
  - Gold: gold color
  - Silver: silver color
  - Bronze: brown color
- Created heatmap visualization for 2008 Olympics showing relative performance of all participating countries

5. Data Structure and Organization
- Utilized index manipulation for better data access
- Implemented various data cleaning techniques including:
  - Handling missing values with fillna()
  - Data type conversions (e.g., converting Year to string for visualization)
  - Complex data reshaping using unstack() operations

6. Visualization Techniques
- Multiple specialized plots:
  - Horizontal and vertical bar charts for different comparative analyses
  - Heat maps for dense data representation
  - Line plots for temporal analysis
  - Custom sized plots using figsize parameter
- Consistent use of meaningful color schemes:
  - Medal-appropriate colors (gold, silver, bronze)
  - Gender-specific colors (red/blue)
  - Custom palettes for specific visualizations

Would you like me to elaborate on any of these aspects or explore another dimension of the analysis?

