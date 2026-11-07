# Selfie-Related Injuries Analysis (Python)

Exploratory data analysis of reported selfie-related injuries and deaths around the world, using Python to find where incidents happen, what types are most common, and how they changed over time.

## Business Questions
- Which countries report the most selfie-related incidents and casualties?
- What are the most common types of incidents (falls, drowning, transport, and so on)?
- How do incident types differ between the countries with the most casualties?
- How did reported incidents change between 2011 and 2021?

## Dataset
- **Source:** Selfie-related injuries and deaths dataset (add the link here)
- **Size:** 192 reported incidents, 5 columns (191 after removing one outlier)
- **Period:** October 2011 to August 2021
- **Columns:** Date, Country, Injuries/Casualties, Type, Description

## Tools
Python, Pandas, NumPy, Matplotlib, Seaborn, Plotly Express, Jupyter Notebook

## Workflow

### 1. Data Cleaning
- Converted `Date` to a datetime type.
- Checked for duplicate rows and missing values (none found).
- Reviewed the distribution of casualties per incident and removed one extreme outlier (an incident with 48 casualties, far above the typical 1 to 2), leaving 191 incidents.

### 2. Analysis
- Total casualties by country (top 5 countries).
- Casualties by country and incident type.
- Number of incidents per country.
- Number of incidents per type.

### 3. Visualization
- **Matplotlib and Seaborn:** casualties over time, total casualties by country (bar chart), incident type distribution (pie chart).
- **Plotly (interactive):** world map of casualties by country, pie charts of incident types by number of incidents and by casualties.

## Key Insights

| Metric | Value |
|--------|-------|
| Incidents analyzed | **191** |
| Total casualties | **about 304** |
| Average casualties per incident | **1.6** (median 1) |

1. **India accounts for the largest share:** 70 incidents (37% of all incidents) and 139 casualties (about 46% of the total), far ahead of the United States (18 incidents, 26 casualties), Russia (14 incidents, 19 casualties), Pakistan (8 incidents, 14 casualties), and Indonesia (4 incidents, 12 casualties).
2. **Falls are the most common type of incident:** 75 incidents (39%), followed by drowning (39 incidents, 20%), transport-related incidents (35, 18%), and electrocution (17, 9%). Animal-related and firearm incidents account for 11 each.
3. **Drowning drives casualties in India:** 65 of India's 139 casualties (about 47%) were drownings, followed by falls (29), transport (24), and electrocution (15). Drowning incidents often involve several people at once.
4. **Most incidents involve a single person:** the median is 1 casualty per incident, and only a handful of incidents involve 5 or more people.
5. **Risk comes from dangerous locations:** the leading incident types (falls, water, railways, and electrical structures) all involve people taking photos at heights, near water, or near tracks and power lines.

## Recommendations
- Awareness campaigns should focus on **heights, water, and railway tracks**, where most incidents happen.
- Tourist sites near water and cliffs should have **warning signs and barriers**, especially in countries with the highest casualties.
- Apps and platforms could add **safety warnings** when users share photos taken in high-risk locations.

## Limitations
- The data covers **reported** incidents only, so countries with more media coverage may appear more often.
- The dataset is small (191 incidents), so conclusions are indicative rather than statistical proof.
- One extreme incident (48 casualties) was removed from the analysis.
