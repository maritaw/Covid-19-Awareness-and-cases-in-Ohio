# Covid-19 Awareness and Covid-19 Cases in Ohio

## Abstract
This study presents a comprehensive analysis of COVID-19’s impact in Ohio, using social media data to capture public awareness and construct a predictive model of the number of cases per day per county. Analyzing over 46 million tweets for topic-related discussions, we discovered patterns correlating social engagement with COVID-19 cases and death counts. Our predictive modeling employed boosting algorithms and achieved an R2 score of 0.924, identifying critical variables such as demographics, social awareness, and number of deaths as key determinants of COVID-19 trends.

## Introduction
In the context of the ongoing COVID-19 pandemic, Ohio faced significant challenges, similar to other states, with escalating numbers of cases, hospitalizations, and fatalities. This project aims to describe and predict the number of Covid-19 cases in Ohio using social awareness data extracted from tweets. The project uses boosting models (AdaBoost and XGBoost) hyperparametarized with Optuna to achieve the best predictive performance.

## Data
Our dataset was collected from over 46,000,000 tweets posted by over 91,000 people in Ohio. Co-occurring hashtags were extracted to manually identify topics related to Covid-19. We employed different similarity measures (Jaccard, Cosine, Intersection) to detect the intensity of discussion on Covid-19-related topics. Key variables include demographics, social awareness metrics, and Covid-19 case and death counts.

## Descriptive Analysis
- **Average Awareness Values:** Sports, core (general Covid-19 awareness), entertainment, illness, and education topics showed the highest levels of discussion.
- **County-Level Awareness:** Delaware county had the highest awareness, while Paulding was at the bottom.
- **Cases and Deaths per Capita:** Pickaway, Franklin, Marion, Lucas, and Mahoning counties had the highest number of per capita cases, while Darke, Miami, Putnam, Shelby, and Mercer counties had the highest number of per capita deaths.
- **Temporal Awareness Trends:** Significant spikes were observed in race topic awareness around day 20 and gender around day 68, with illness and core awareness peaking moderately after day 74.

## Methods
We utilized ensemble boosting methods (AdaBoost and XGBoost) to predict the number of Covid-19 cases in different Ohio counties. Data preprocessing included Label Encoding of categorical variables and the use of Optuna for hyperparameter optimization. The XGBoost model, optimized with a guided hyper-parameter search, achieved the best performance with an R2 score of 0.924.

## Results
The optimal model incorporated 38 critical features, with the number of deaths being the most important predictor. The model effectively used demographic, temporal, spatial, and social awareness factors to predict Covid-19 cases. 

### Key Findings:
- The XGBoost model with optimal hyperparameters (75 boosters, max depth of 4, eta of 0.489, etc.) provided the best predictive performance.
- Social awareness metrics, derived from Twitter data, played a significant role in the model's predictive capabilities.

## Future Work
Possible areas of improvement include more advanced feature engineering, exploration of neural network models, and integration of external datasets such as vaccine availability, vaccination rates, and control measures.

## References
1. T. Akiba et al., “Optuna: A Next-generation Hyperparameter Optimization Framework,” Proceedings of the 25th ACM SIGKDD International Conference on Knowledge Discovery & Data Mining, 2019.
2. K. V. Rashmi and R. Gilad-Bachrach, “Dart: Dropouts meet multiple additive regression trees,” arXiv.org, 2015.
3. Python API reference. Python API Reference - xgboost documentation, 2024.
4. “Covid-19 pandemic in Ohio,” Wikipedia, 2024.
