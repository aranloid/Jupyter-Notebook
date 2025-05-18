### 🌍 **Key Findings from COVID-19 Analysis**

1. **Vaccination Rollout Speed**  
   - *United States* achieved >50% vaccination coverage 5 months faster than India and Kenya.  
   - *Kenya*'s vaccination program started 3 months later than other analyzed countries.

2. **Case Fatality Rates**  
   - *Highest*: United States (1.8%)  
   - *Lowest*: India (1.2%)  
   - Possible factors: Healthcare capacity, age demographics, variant waves.

3. **Infection Waves**  
   - All countries showed 3 distinct case spikes (2020-mid, 2021-start, 2021-end).  
   - *India* had the sharpest surge (April-May 2021 Delta variant wave).

4. **Data Gaps**  
   - Early pandemic records (Jan-Mar 2020) show inconsistent testing.  
   - Vaccination data for Kenya has more missing values than other countries.
  
   - # Detect anomalous case reports
anomalies = covid_df[covid_df['new_cases'] > covid_df['new_cases'].quantile(0.99)]
print(f"Top 1% anomalous case reports ({len(anomalies)} records):")
display(anomalies[['date','location','new_cases']].sort_values('new_cases', ascending=False).head())

### 🔍 **Notable Anomalies**
- **2021-05-01**: India reported 400,000+ cases in one day (world record).  
- **2020-04-15**: US case reporting anomaly (likely data backlog entry).

# COVID-19 Data Analysis

## Project Description
Analysis of global COVID-19 case, death, and vaccination trends using Our World in Data dataset.

## Objectives
1. Explore pandemic trends through visualization
2. Compare country-level responses
3. Analyze vaccination effectiveness
4. Identify data anomalies

## Tools Used
- Python
- Pandas
- Matplotlib/Seaborn
- Plotly
- Jupyter Notebook

## How to Run
1. Install requirements: `pip install pandas matplotlib seaborn plotly jupyter`
2. Launch Jupyter: `jupyter notebook`
3. Open and run `covid_analysis.ipynb`

## Key Insights
- **US**: Fastest vaccination rollout (50% coverage by June 2021)
- **India**: Sharpest case surge (400k/day peak in May 2021)
- **Kenya**: Latest vaccination start (3 months behind others)
- **Data Gaps**: Inconsistent early-pandemic testing records

## Data Source
[Our World in Data](https://ourworldindata.org/covid-cases)



