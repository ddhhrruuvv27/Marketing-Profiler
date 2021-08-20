The **US Adult Census dataset** is a repository of 32,560 entries extracted from the **1994 US Census database**.

The data was cleaned and pre processing was done, by removing all the rows containing one or more missing values from the **"adult.data"** file.
All the rows containing “?” was marked as NaN (not a number) and finally dropped to obtain the **"preprocessed_data.csv"**.

The Census Income dataset has 32,560 entries. Each entry contains the following information
about an individual: <br />
* **age:** the age of an individual <br />
* **workclass:** a general term to represent the employment status of an individual <br />
* **fnlwgt:** final weight <br />
* **education:** the highest level of education achieved by an individual. <br />
* **education-num:** the highest level of education achieved in numerical form. <br />
* **marital-status:** marital status of an individual. <br />
* **occupation:** the general type of occupation of an individual <br />
* **relationship:** represents what this individual is relative to others. <br />
* **race:** Descriptions of an individual’s race <br />
* **sex:** the biological sex of the individual <br />
* **capital-gain:** capital gains for an individual <br />
* **capital-loss:** capital loss for an individual <br />
* **hours-per-week:** the hours an individual has reported to work per week <br />
* **native-country:** country of origin for an individual <br />
* **income:** whether or not an individual makes more than $50,000 annually. <br />

**Preliminary Exploratory Data Analysis** 
Exploratory data analysis was performed by plotting a correlation heatmap of each factor with every other factor.

Based on the matrix, it is quite evident that:
* Native countries, Race, and the Working-class do not seem to have any impact.
* Education-num (sorted in increasing order) is better than Education.
* At first glance, age, education-num, sex, capital gain and hours-per-week seem to be most prominent.

**Data Visualization** 

**1. Age**

It is evident from the visualization that people who earn more than $50k per year are on average about 43-44 years old and the people who earn less than $50k per year are around 34-37 years old. 

**2. Working Class**

A majority of the people are employed in the private sector. Also, there are almost negligible numbers of people in the without-pay category.
From the above visualization, we can see that all the working class except self-employed earn less than $50k per year. This is a clear indication that can help the model to predict the income category for unseen data.

**3. Final weight**

It represents continuous data with an integer value given by the Census Bureau. This weight assigned is what the Census Bureau feels the entry represents. For example, if there are two entries with a similar fnlwgt value they have more chance to contain similar characteristics. This could be a combination of factors like race, education, etc. However, the biggest disadvantage of this factor after the analysis was that it was not standardized for different regions, and using it directly was not that informative in predicting the income when compared to other factors. Due to this reason this factor was dropped for further consideration.

**4. Education and education-num**

The analysis of Education was done initially by understanding the distribution using the Pie-chart. To further understand the relationship between education and income the distribution of entries and its associated percentage above 50K and less than equal to 50K was plotted using stacked and group bar charts. The final observation was that the income increased when the education was higher. This can be observed from the instances below as Preschool does not have any entry above 50K while higher education fields like Masters, Doctorate, Prof-school and Assoc-acdm have many 50k income entries. Education-num is the numbering which can be used for predictive models.

**5. Marital Status**

It can be observed from the pie and bar charts that the Married-civ-spouse category has the highest fraction of the people whose salary is more than 50K, while the never married category has the highest fraction of people whose salary is less than 50K.

**6. Occupation**

It can be observed that there is an inclination that positions requiring profoundly qualified experts with school or college degrees are paid better compared to occupations that are most certainly not. This observation appears to be sensible and mirrors the present world job market.

**7. Relationship**

The incomes across different relationship categories are distributed unevenly. Married couples earn more than unmarried or not in the family. This data is a bit unbalanced, and that is the reason why wives category plot is higher. Those who are not-in-family such as the one who earn more than those who are their own-child or are unmarried. The Other and Not-In-Family attribute is not much derived as the income level is not highly available for these categories.

**8. Race**

The incomes across different races are distributed unevenly. More Asian-Pac Islander earn higher incomes(greater than $50k) as compared to all the other races. The white race comes next with a slightly lesser proportion of the population earning greater than $50k. In terms of these two races, the Black, Amer-Indian-Eskimo and Other races earn more in the lower income range and are distributed in the graph which shows that a higher percentage of race belonging to this population earns lower income wages as compared to Asian-Pac Islander and White.

**9. Race**

The visualization shows that out of the total data available 33% are Female and 67% are Male. Further comparison of the data with income, it shows that nearly 30% of the total male population earns a salary more than 50K while about less than 15% of the total females earn more than 50K.

**10. Capital Gain and Capital Loss**

Capital-gain and Capital-loss is continuous data. Based on the distribution of the data it shows that the Capital-gain of the data is mostly left skewed and data has a long left tail. While the Capital-loss of the data is distributed normally. Hence it is mostly distributed normally. Most of the data has 0 value which means the data is mostly missing and is being replaced by the 0 value. Thus it will be not advisable to have these two columns for the future analysis of the data.

**11. Hours per week and native country**

Hours per week is a continuous feature whereas native countries are a discrete feature. The visualization depicts the dependence of hours per week on deciding the income. It is clearly evident that if the number of hours worked per week is greater than 40, then the probability of the income being greater than 50K is much higher. The same trend can be observed for all the countries.

**Tools**

For the analysis of the data, we have used **“Jupyter Notebook”** and **“Google Colab”** for web-based interactive computational environments. The programming language **“Python”** is used to make all the data manipulations and creating data-visualization plots. The data manipulation libraries used throughout the project are **“Pandas”** and **“Numpy”**. The data visualization libraries used throughout the project are **“Matplotlib”** and **“Seaborn”** .

**Predictive Models**
Having performed the preliminary research on various factors using promising visualizations, the features were used to train a predictive model that predicts on unseen test data.
The results of experimentation with various different machine learning models are enumerated below:
| Score Metric   | SVM (RBF kernel)| SVM (Linear kernel)| Random Forest (Gini) | Random Forest (Entropy) |
| :------------- | :-------------: | -----------------: | -------------------: | ----------------------: |












 
