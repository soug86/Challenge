# Module 1 Challenge- Deliverable 3

This written analysis contains three sections:

**1. Overview of Project**

**2. Analysis and Challenges**

**3. Results**
 
## 1. Overview of Project


The aim of the analysis was to provide actionable insights to Louise  which would help her determine the optimal time and budget that has historically resulted in successful campaigns. 

The analysis involved looking at historical data from over **4,100** projects from across the world over a nine year period from 2009 to 2017.

## 2. Analysis and Challenges

### **a. Analysis of Outcomes Based on Launch Date:**

The aim of this section of the analysis was to determine the effect of launch timing on the outcome of the project.

Firstly, the dataset had to be filtered so that only the appropriate projects related to 'Theaters' were considered. Next, the format for the launch dates had to be changed into a `Date` format in `MS Excel` so that we can analyze the impact of launch timing on the outcome. Once the format had been decided, the intention was to only focus on the relevant outcomes as a result of which the `Live` projects were not considered. Thus a pivot table was created to capture the impact of outcomes of theaters by month which was finally translated into the chart as below:
![Theater Outcomes based on Launch Date](https://www.github.com/soug86/Resources/Theater_Outcomes_vs_Launch.png) 

### **b. Analysis of Outcomes Based on Goals**

Additionally, Louise wanted to understand the effect of funding goals on outcome of plays. The intent is to provide her with some historical context as to what relationship does funding goal have with project outcome. In order to provide her with the appropriate view, the funding goals were grouped in `$5,000` increments and the number of successful, failed and canceled plays were determined from the dataset using `COUNTIFS` formula with multiple criteria. Consequently, the data was converted to percentage of outcome in each funding category to ensure the comparison was not skewed. A chart was created to provide Louise with a view of the relationship between funding goals and outcome of plays.
![Outcomes based on Goals]

### **c. Challenges and Difficulties Encountered**

For the first analysis, 
- The primary challenge was to ensure the dataset had been setup appropriately, especially ensuring the launch date format was translated from Unix timestamps to `MS Excel` date format. [ref] 
- The other challenge with the first analysis was to ensure the filters were removed from the `PivotChart` to ensure it looked similar to a line chart. This was done by right-clicking the filter on the PivotChart and clicking `Hide All Filters from Chart`.

For the second analysis,
- The first challenge was to use `COUNTIFS` formula instead of a `PivotTable` and to tweak the criteria for each of the categories apprpriately to ensure the correct outcome was caputered. 
- Another challenge was to keep in mind the formula was setup in such a way so that none of the datapoints are missed, e.g. Although the last category was titled "Greater than 50000", it was actually "Greater than or **equal to** 50000" since there were 4 failed plays with a goal of **exactly** $50,000.

## 3. Results

### a. What are two conclusions you can draw about the Outcomes based on Launch Date?

Louise can conclude the following from the analysis of the impact of Launch Date on outcomes,

- Launching a theater in the **summer season** is much more likely to be successful in than winter season. In fact, the month of **May** seems to be the optimal month to launch this project.

- Instances of a theater becoming a failure is pretty consistent throught the year meaning, that there are factors other than Launch date which is the cause of theaters becoming a failure.

### b. What can you conclude about the Outcomes based on Goals?

There are some interesting takeaways when the relationship between outcomes of plays is analyzed with goal funding budget,

- Low buget plays of less than `$5,000` have surprisingly turned out to be successful almost 75% of the time. This is highest success rate across any of the goal categories meaning **plays with good storyline and execution are likely to be successful irrespective of the amount of money spent on big name cast or on a fancy set.** This is borne out by the fact that plays greater than `$45,000` almost always end up being a failed venture. 

### c. What are some limitations of this dataset?

Some of the limitations in the dataset include,

- Presence of bad data in some instances, for eg. `id- 244` has a date in place of the name of the documentary.

- The data doesn't expand on the criteria that is used to determine the outcome of the venture being a success or a failure.

- The data has some significant outliers associated with it which needs to be validated or it risks skewing the analysis.

### d. What are some other possible tables and/or graphs that we could create?

There are some interesting takeaways when other factors are considered to understand the relationship with Outcomes. Some factors like the ones below provide interesting takeaways when we analyze their impact on the final outcome,
- Count of backers
- Average donation
- Duration of the venture
- % Pledged vs Goal funding

Additionally, while the first analysis included `Theaters` while the second analysis included on `Plays`. Analyzing the dataset with a consistent scope will provide more accurate takeaways.

* Open up the activity workbook [07-Stu-OutliersDrawnQuartiled/Outliers_Activity_Unsolved.xlsx](Unsolved/Outliers_Activity_Unsolved.xlsx) and familiarize yourself with the raw data.

