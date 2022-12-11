# PCA_MDS_US_bankruptcy
# What is this about?

The purpose of this analysis is to conduct a preliminary analysis on a set of US bankruptcy data in order to better understand and potentially categorise different types of bankruptcy. Before this analysis takes place, a brief data description is provided, followed by some data wrangling and exploration to ﬁrst clean the data, and then visualise some of the patterns and characteristics present in it.

The main body of the analysis has been broken down into two parts. The ﬁrst will conduct multidimensional scaling (MDS), a technique that aims to produce a low dimensional representation of a higher dimensional space by attempting to produce pairwise Euclidean distances that are as similar as possible to the original distances. This technique will help visualise which observations are similar from the data and whether any different groups can be observed.

The second stage will involve undertaking a principal components analysis (PCA) which reduces the number of variables by producing a linear combination of the original variables that explains the largest amount of variance. This will provide a good comparison to the results of the MDS while also providing greater insight, as the loadings assigned to each principal component can be examined.

Following this analysis, the results from each will be discussed and compared in the conclusion.

# Motivation of this project

This is a project I did after learning the concepts of high dimensional analysis, where I learnt the concepts of ***MDS (Metric Multidimensional Scaling)* and *PCA (Principal Components Analysis).*** 

So, through this project, I would like to apply what I have learnt into the topic I am interested.

### Why this topic?

With the interest in Economics and Finance, the bankruptcy of the firm situated in the US is an interesting topic to study. 

For example, what is the relationship of each state bankruptcy and econ. activity across year. This analysis explains the implication of economics and finance in US.

# Description of the dataset and Questions of the analysis

We use data on a set of 436 U.S ﬁrms that ﬁled for bankruprcy between the years 1980 and 2000. The data was sourced from [UCLA-LoPucki Brankruptcy Research Database](https://lopucki.law.ucla.edu/). All the information was collected at the time the ﬁrms ﬁled for bankrupcy.

### Description of the dataset

- **Name:** Name of the ﬁrm;
- **Assets:** Total assets (in millions of dollars);
- **CityFiled:** City where ﬁling took place;
- **CPI** U.S CPI at the time of ﬁling;
- **DaysIn:** Length of bankruptcy process;
- **DENYOther:** CityFiled, categorized as Wilmington (DE), New York (NY) or all other cities (OT);
- **Ebit:** Earnings (operating income) at time of ﬁling (in millions of dollars);
- **Employees:** Number of employees before bankruptcy;
- **EmplUnion:** Number of union employees before bankruptcy;
- **FilingRate:** Total number of other bankrupcy ﬁlings in the year of this ﬁling;
- **FirmEnd:** Short description of the event that ended the ﬁrm’s existence;
- **GDP:** Gross Domestic Product for the Quarter in which the case was ﬁled;
- **HeadCityPop:** The population of the ﬁrms headquarters city;
- **HeadCourtCityToDE:** The distance in miles from the ﬁrms headquarters city to the city in which the case was ﬁled;
- **HeadStAtFiling:** The state in which ﬁrms headquarters is located;
- **Liab:** Total amount of money owed (in millions of dollars);
- **MonthFiled:** Categorical variable where numbers from 1 to 12 correspond to months from Jan to Dec;
- **PrimeFiling:** Prime rate of interest on the bankruptcy ﬁling date;
- **Sales:** Sales before bankruptcy (in dollars);
- **SICMajGroup:** Standard industrial clasiﬁcation code;
- **YearFiled:** Year bankruptcy was ﬁled;

### **The full dataset can be found below**

[Bankruptcy.rds](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/008e40c9-0285-45d9-b8e4-fae000d2c663/Bankruptcy.rds)

### General questions of this analysis

- Is the data clean? Are there missing values, outliers or other data credibility issues?
- Can you derive any insights from the data from simple exploratory analysis including summary statistics and basic plots?
- Can the data be easily visualised?
- How can you proﬁle the principal components?
- Do they have some interpretation in terms of the data itself?
- Does the report contain enough information to be reproduced by somebody with knowledge of the techniques used?
- Are all plots clearly presented and correctly explained?
- Is the analysis robust to minor changes in the methodology?
- Are any assumptions made for the analysis or in drawing conclusions. If so, are these clearly explained?
- Does the report focus on a small number of interesting features of the analysis or does the report simply list everything that was attempted (the former is preferable to the latter)?
- Are the limitations of the analysis clearly discussed?
