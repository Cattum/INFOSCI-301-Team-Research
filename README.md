# Data Analysis Report: Unemployment and Mental Health Correlation

## 1. Overview
In this analysis, we examine the relationship between state-level unemployment rates and the prevalence of mental health burdens (measured as the percentage of adults experiencing poor mental health for at least 14 days in a month) across the United States between 2018 and 2021. Our primary aim is to:
- Quantify the strength of this relationship.
- Explore its temporal dynamics, especially potential lag effects.
- Identify states that may be particularly vulnerable.

The dataset integrates unemployment data from the U.S. Bureau of Labor Statistics with mental health indicators from the CDC’s Environmental Public Health Tracking Network.

## 2. Methodology
We conducted the following steps:

### Correlation Analysis:
- Computed Pearson correlation coefficients to measure the strength of association between unemployment rates and mental health burden, both overall and by state.

### Lag Analysis:
- Tested whether unemployment rates from the previous year predict increases in mental health burdens, simulating a possible delayed effect.

### State-Level Sensitivity:
- Identified states where the unemployment-mental health relationship is particularly strong or weak.

All analyses were conducted using Python libraries such as Pandas, SciPy, Matplotlib, and Seaborn.

## 3. Key Findings

### 3.1 Overall Correlation
- **Pearson Correlation Coefficient:** 0.5198  
- **p-value:** < 0.001  
This suggests that higher unemployment rates are associated with increased mental health burdens at the population level.

#### Visualization:
- A scatter plot with a regression line indicated a positive trend between unemployment and mental health burden, albeit with some dispersion, implying that other factors may also influence mental health outcomes.

### 3.2 State-Level Variation
The strength of the unemployment-mental health relationship varied significantly across states:

#### Strongest Positive Correlations (most sensitive states):
- **Nevada** (r = 0.82)
- **New Mexico** (r = 0.79)
- **Alaska** (r = 0.78)
- **West Virginia** (r = 0.76)

These states showed a strong link between unemployment changes and mental health distress.

#### Weakest or Negative Correlations (least sensitive states):
- **Hawaii** (r = -0.05)
- **Vermont** (r = 0.10)
- **New Hampshire** (r = 0.12)

In these states, mental health burdens appeared less directly connected to unemployment fluctuations, suggesting the presence of other mitigating factors (e.g., stronger social safety nets, community resilience).

### 3.3 Lagged Effect Analysis
When considering a one-year lag (i.e., comparing the previous year’s unemployment rate to the current year’s mental health burden):

- **Lagged Pearson Correlation Coefficient:** 0.5621  
- **p-value:** < 0.001  

The lagged relationship was slightly stronger than the contemporaneous one, suggesting that unemployment shocks may take time to fully manifest in population-level mental health statistics. This finding supports the hypothesis of a temporal lag effect between economic distress and psychological outcomes.

## 4. Preliminary Conclusions
- State-level unemployment is moderately associated with mental health burdens, supporting the premise that economic hardship influences population wellbeing.
- There is evidence of a time-lag effect, indicating that the full impact of rising unemployment on mental health may only become apparent after a delay.
- Certain states are particularly vulnerable to the mental health effects of unemployment, possibly due to economic structures, healthcare access, or cultural factors.

### Policy Implications:
- Targeted mental health support may be particularly critical in states with high sensitivity.
- Lag effects highlight the need for proactive intervention strategies following economic downturns, rather than reactive ones.

## 5. Limitations and Future Work
### Limitations:
- **Short Time Frame:** Data spans only 2018–2021. Longer historical windows would provide stronger statistical power.
- **Confounding Variables:** Factors like healthcare access, COVID-19 impacts, and state-level interventions were not controlled for.

### Further Analysis:
- Multivariate regression models controlling for additional socio-economic factors.
- Machine learning models (e.g., LASSO regression) for predictive analysis, as outlined in the proposal.
- Geospatial visualizations using choropleth maps to better illustrate regional differences.

## ✅ Summary Table (optional if you want to attach)

| Analysis                           | Result       |
|------------------------------------|--------------|
| Overall Correlation                | 0.5198       |
| Lagged Correlation (1 year)        | 0.5621       |
| Most Sensitive States             | Nevada, New Mexico, Alaska |
| Least Sensitive States            | Hawaii, Vermont, New Hampshire |
