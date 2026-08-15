# Spanish Economic News Sentiment and IBEX 35 Returns

## Overview

This project examines the relationship between sentiment in Spanish economic news and weekly returns of the IBEX 35 during June-August 2026.

The final headline-focused sentiment detector was applied to 18 Spanish economic news articles. The resulting raw sentiment scores were aggregated into weekly measures and compared with IBEX 35 weekly returns across 8 complete weeks.

## Research Question

Is more positive Spanish economic news sentiment associated with higher weekly IBEX 35 returns?

## Final Results

- Observations: 8 complete weeks
- Pearson correlation (r): 0.5198
- R-squared: 0.2702
- Regression slope: 0.001903
- Regression intercept: 0.005471

The results indicate a moderate positive linear association in this sample. The analysis does not establish causation.

## Methodology

The sentiment detector was developed iteratively through four stages:

1. Rule-based detector
2. Event-based detector
3. Headline-focused detector
4. Final headline-first scoring function

The final detector produces a numerical Final Raw Score for each article. Observed scores ranged from -8 to +7.

Raw scores were converted into five sentiment categories:

- -5 or below = -1.0
- -4 to -2 = -0.5
- -1 to +1 = 0.0
- +2 to +4 = +0.5
- +5 or above = +1.0

The categorical scores were manually reviewed for quality control. However, the original Final Raw Scores were retained for the weekly quantitative analysis.

Weekly sentiment was calculated as the mean Final Raw Score for articles published during each Monday-Sunday calendar week.

IBEX 35 weekly return was calculated as:

(Friday Close - Monday Close) / Monday Close * 100

The final comparison contains 8 complete weeks from June 15 through August 9, 2026.

## Limitations

The sample contains only 18 scored articles and 8 complete weekly observations. The detector is a rule-based, headline-focused approach rather than a trained machine-learning model.

The correlation measures association rather than causation. Other factors, including macroeconomic developments, geopolitical events, monetary policy expectations, company-specific news, and international markets may also affect IBEX 35 returns.

Therefore, the findings should be considered exploratory rather than evidence of a stable predictive relationship.
