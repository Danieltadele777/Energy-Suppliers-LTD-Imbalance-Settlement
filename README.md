# Energy-Suppliers-LTD-Imbalance-Settlement
### Introduction
In this analysis, I focused on reconciling energy imbalances for Energy Suppliers Ltd(name modified to keep privacy). The task was to identify and analyze discrepancies between ES's internal metered data from individual Points of Delivery (PODs) and the allocation data reported by Distribution System Operators (DSOs). By exploring these imbalances, I aimed to provide actionable insights to optimize energy supply, prevent financial discrepancies, and improve the accuracy of energy reporting between EES and its network partners. 

The analysis involved data cleaning, exploratory analysis, hypothesis testing, and visualization to identify patterns and areas requiring intervention.

### KPIs Used
The following Key Performance Indicators (KPIs) were used to measure and assess the energy imbalances and operational performance:

1. **Imbalance Rate (%)**:  
   - The percentage difference between ES's internal metered data (POD) and the DSO allocation data
   - This KPI highlights the extent of discrepancies in energy reporting.

2. **Total Energy Discrepancy (kWh)**:  
   - The total difference in energy reported by the DSOs versus the PODs over a specific period (e.g., daily, weekly, monthly).  
   - Helps quantify the overall imbalance and its potential financial impact.

3. **Peak Imbalance Time Period**:  
   - Identifies the time period (specific hours or days) when the highest imbalance occurs.  
   - Useful for pinpointing operational inefficiencies during high-demand periods.

4. **POD Compliance Rate (%)**:  
   - The percentage of PODs that report energy usage within an acceptable range of variance compared to the DSO data.  
   - A lower compliance rate may indicate systemic reporting issues.

5. **DSO Reporting Accuracy (%)**:  
   - The ratio of accurate energy allocations reported by DSOs compared to EES's internal data.  
   - This KPI is crucial for assessing the reliability of third-party data.
## Table of contents
 - [Task Overview](#task-overview)
 - [Data Source](#data-source)
 - [Tools Used](#tools-used)
 - [Data cleaning](#data-cleaning)
 - [Exploratory data analysis](#exploratory-data-analysis)
 - [Hypothesis Testing](#hypothesis-testing)
 - [Data Analysis](#data-analysis)
 - [Findings](#findings)
 - [Python Visualization](#python-visualization)
 - [Recommendations](#recommendations)
 - [Limitations](#limitations)
 - [References](#references)
 - [Presentation Video](#presentation-video)

### Task Overview
In this analysis, I performed a reconciliation of imbalances between energy supply and demand for Energy Suppliers Ltd. The goal was to analyze discrepancies between the company's internal metered data (POD data) and the allocation data reported by various DSOs (Distribution System Operators). By identifying these imbalances, the analysis provided valuable insights into energy management and operational efficiency.

### Data Source
- **Mapping File**: Contains DSO and POD mappings, identifying which of the 100 PODs belong to which of the 6 DSOs.
- **DSO Data File**: Contains energy allocation data from DSOs, timestamped.
- **POD Data File**: Contains metered energy data for each of the 100 PODs, timestamped.

### Tools Used
- Python (Pandas, NumPy, Matplotlib, Seaborn)
- Jupyter Notebook

### Data Cleaning
- Handled missing or inconsistent data, ensuring PODs and DSOs had properly aligned timestamps.
- Removed duplicate records and filtered out any irrelevant data points, such as those outside the desired time range.
- Applied functions to normalize data formats across different files (e.g., ensuring consistency in timestamp formats).

### Exploratory Data Analysis
- Visualized energy imbalances over time using line charts and histograms to observe patterns in energy supply and demand.
- Grouped data by DSOs and PODs to understand discrepancies across different locations.
- Created summary statistics (mean, median, variance) to measure energy imbalances.

### Hypothesis Testing
- Performed a hypothesis test to check whether the internal POD data significantly differs from the allocation data reported by the DSOs.
- The null hypothesis (H0): The mean of POD and DSO data is the same.
- The alternative hypothesis (H1): There is a significant difference between the POD and DSO data.

### Data Analysis
- Detected significant differences in energy allocation between internal metered data and DSO-reported data.
- Identified peak imbalance periods and major sources of discrepancies at the DSO and POD level.
- Quantified the impact of discrepancies on operational costs and energy management efficiency.

### Findings
- The largest differences between metered data and DSO allocations occur during the evening (19:00 - 22:00) and midday (11:00 - 14:00). These periods are likely critical for investigating the causes of the imbalances.

- The absolute difference has a higher mean of 161.35 units, with a standard deviation of 207.3 units. This suggests that while some differences are small, others can be quite significant. The maximum difference reaches up to 799.23 units, indicating potential outliers or significant imbalances.

DSO-Level Differences:

- DSO 3 and DSO 6 show the highest total absolute differences, each with over 6.63 million units, followed by DSO 4. These DSOs likely contribute the most to the discrepancies observed in the imbalance invoices. DSO 5 and DSO 2 show negligible differences, indicating minimal or no significant discrepancies for these operators.
  
- Imbalances in energy allocation were more prevalent during specific periods, especially during high-demand seasons.
  
- Certain DSOs consistently reported lower energy usage compared to the internal measurements, indicating possible underreporting.
  
- Discrepancies could lead to financial losses if not addressed, particularly in reconciling energy transactions.

### Python Visualization
<img width="1430" alt="1" src="https://github.com/user-attachments/assets/3341d16a-4d08-4b9c-a02c-a56439a18195">
<img width="1467" alt="2" src="https://github.com/user-attachments/assets/38431359-b6a8-4d82-900d-c34ff4ce7738">
<img width="1470" alt="3" src="https://github.com/user-attachments/assets/cff4a6d1-4345-4b18-bf08-cd307eeb1dfa">
<img width="1430" alt="4" src="https://github.com/user-attachments/assets/50185907-5803-4f16-8ab7-50d9fde436ed">
<img width="1429" alt="5" src="https://github.com/user-attachments/assets/baacf80b-797e-47af-88b9-d58abf41746b">
<img width="1455" alt="6" src="https://github.com/user-attachments/assets/648ab416-3a0c-45b0-a60a-654787f5b1df">
<img width="1398" alt="7" src="https://github.com/user-attachments/assets/df14dc31-dcb2-4c6e-8290-12fb24975db0">
<img width="1192" alt="8" src="https://github.com/user-attachments/assets/86da7bb5-14ca-4fd9-a6bb-0310c44494a1">
<img width="1222" alt="9" src="https://github.com/user-attachments/assets/121818a4-fea3-4413-88e3-59707662ddb5">
<img width="886" alt="10" src="https://github.com/user-attachments/assets/f19eef95-c582-401c-95f9-2f499cff775f">
<img width="1009" alt="11" src="https://github.com/user-attachments/assets/cf771406-1cbd-4d48-b443-9a92b8dec740">
<img width="1348" alt="12" src="https://github.com/user-attachments/assets/c0c3678d-3a99-4ce0-881c-bef0324e3e81">
<img width="1097" alt="13" src="https://github.com/user-attachments/assets/f1eba906-9118-471b-aa53-b9092665d83c">
<img width="1010" alt="14" src="https://github.com/user-attachments/assets/ecb9a6b6-7faa-43be-9655-29ed2e451b4e">
<img width="941" alt="15" src="https://github.com/user-attachments/assets/d5b6c631-2e15-4243-83f5-e4f194b91249">

### Recommendations
1. Improve communication and data sharing between EES and DSOs to minimize discrepancies.
   
2. Considering the hours periods of interest where discrepancies were particularly high might be necessary to investigate if there were any known events (e.g., outages, maintenance, high usage, production) during these hours that could explain the differences.

3. During the period of 2020 day 03 and 04, a high peak registered specifically in DSO 1 and DSO 6. Does the COVID-19 outbreak disrupt the normal procedure, usage, production or if there were any outages or maintenance were taken place at those days? By investigating especially the DSO 1 dramatic increase, we can find out the real cause.

4. It is also important to investigate the reporting style to undersand if it is the root cause of discrepancey.The DSOs might aggregate or report the data differently than how it's processed internally at EES. Or there might be differences in how imbalances are calculated between the TSO and EES.
5. Implement automated data reconciliation tools to flag imbalances in real-time.

6. Further investigation into DSO reporting practices during high-demand periods.

### Limitations
- The analysis was limited to the data available for 100 PODs, which may not fully represent all energy distribution points.
- The project focused on historical data; real-time analysis would provide better insights into current operations.
- Assumptions made during data cleaning (such as filling in missing data) may introduce some bias into the analysis.

### References
- Data from Energy Suppliers Ltd (Internal metered POD data and DSO allocation data).
- Python libraries: pandas, NumPy, Matplotlib.

### Presentation Video
- [presentation video]
