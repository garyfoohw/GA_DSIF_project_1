# ![](https://www.bloomingtonsouthoptimist.org/wp-content/uploads/2020/04/sat_act.png) Project 1: Market Opportunity for Standardized Test Preparatory Schools


### Problem Statement

Entry into college is a highly competitive affair. Roughly 50% of each year's cohort sits for at least one of the standardized tests. Therefore the business of a private prepatory school for these students can be a lucrative business.  

We wish to explore if there there are geographic concentrations of ACT vs SAT as well as bias in performance in Linguistics vs Formal Sciences so that we can target specific student population and deploy appropriate resources in the right places.

---

### Datasets

#### Provided Data

There are 10 datasets included in the [`data`](./data/) folder for this project. You are required to pick **at least two** of these to complete your analysis. Feel free to use more than two if you would like, or add other relevant datasets you find online.

* [`act_2017.csv`](./data/act_2017.csv): 2017 ACT Scores by State ([source](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows))
* [`act_2018.csv`](./data/act_2018.csv): 2018 ACT Scores by State ([source](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows))
* [`act_2019.csv`](./data/act_2019.csv): 2019 ACT Scores by State ([source](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows))
* [`sat_2017.csv`](./data/sat_2017.csv): 2017 SAT Scores by State ([source](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/))
* [`sat_2018.csv`](./data/sat_2018.csv): 2018 SAT Scores by State ([source](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/))
* [`sat_2019.csv`](./data/sat_2019.csv): 2019 SAT Scores by State ([source](https://blog.prepscholar.com/average-sat-scores-by-state-most-recent))


#### Additional Data
Furthermore, data on latest SAT and ACT (2021) performance breakdown are also sourced.  
`sat_2017_2021.xlsx` and `act_2017_2021.xlsx` are also sourced ([*SAT*](https://nces.ed.gov/programs/digest/d21/tables/dt21_226.40.asp)) ([*ACT*](https://nces.ed.gov/programs/digest/d21/tables/dt21_226.60.asp)).

---
### Data Dictionaries
We use 3 different dataframes here in the study.  

#### Dataframe `df`
|Feature|Type|Dataset|Description|
|---|---|---|---|
|State|object|act_2017, act_2018, act_2019, sat_2017, sat_2018, sat_2019|State which the metric is reported for|
|Year|int|act_2017, act_2018, act_2019, sat_2017, sat_2018, sat_2019|Year which the metric is reported for|
|P_ACT|float|act_2017, act_2018, act_2019|ACT participation rate|
|S_ACT|float|act_2017, act_2018, act_2019|ACT normalized scores|
|P_SAT|float|sat_2017, sat_2018, sat_2019|SAT participation rate|
|S_SAT|float|sat_2017, sat_2018, sat_2019|SAT normalized scores|


#### Dataframe `df_act_bd` (bd means breakdown)
|Feature|Type|Description|
|---|---|---|
|State|object|State which the metric is reported for|
|comp_2021|float|Normalized mean composite score in 2021|
|eng_2021|float|Normalized mean English section score in 2021|
|math_2021|float|Normalized mean Math section score in 2021|
|read_2021|float|Normalized mean Reading section score in 2021|
|sci_2021|float|Normalized mean Science section score in 2021|
|part_2021|float|Normalized participation rate in 2021|


#### Dataframe `df_sat_bd` (bd means breakdown)
|Feature|Type|Description|
|---|---|---|
|State|object|State which the metric is reported for|
|tot_mean_score_2021|float|Normalized mean total score in 2021|
|erw_mean_score_2021|float|Normalized mean ERW section score in 2021|
|math_mean_score_2021|float|Normalized mean mathematics section score in 2021|
|part_2021|float|Normalized participation rate in 2021|

---
#### Observations

We observed that for both ACT and SAT, the scores and particiaption rates are inversely correlated.
This could signify and support the presence of high number of retakes in some states.
We also note the states that prefer ACT are clustered in central USA whereas SAT are preferred on the Eastern/Western seabords.
In general, the Eastern seabord tends to have a better performance in Linguistics over the Formal Sciences.

---

#### Conclusion
There appears to be an opportunity for college prepartory school services at the Eastern seabords to target SAT questions, with increased focus on the Formal Sciences.

---