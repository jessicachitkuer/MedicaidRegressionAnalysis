## Affordable-Care-Act

### Linear Regression Analysis: Medicaid’s Effect on U.S. BMI

Regression analysis is an important statistical method for the analysis of medical data. It enables the identification and characterization of relationships among multiple factors. It also enables the identification of prognostically relevant risk factors and the calculation of risk scores for individual prognostication.

#### Summary
A regression analysis of the various types of health insurance offerings and its externalities on the U.S. healthcare system. All regressions are routed to control for heteroskedasticity and empirical models in this study are adjusted for R2 with equally distributed residuals. 

#### Motivation 
Computational social scientists increasingly need to grapple with data that is either too big for a local machine and/or code that is too resource intensive to process on a local machine. In this project, we effectively scale computational methods = local machines. The focus will be social scientific applications, ranging from training machine learning models on large economic time series to processing and analyzing public data in real-time. Several large-scale computing frameworks are used such as MPI, MapReduce, Spark, and OpenCL, with a special emphasis on employing these frameworks using cloud resources and the Python programming language.

Looking at the effects Medicaid has had on United States health is especially important when it provides medical care to four out of ten American children, pays for the care of two thirds of the people in nursing homes, and provides for ten million children and adults with physical and mental disabilities, according to the New York Times. It accounts also for sixty percent of U.S. federal funding. While many assume that Medicaid is expensive in every state, Illinois spending per person was well below the U.S. average for all major eligibility groups and spending per enrollee of $4,682 according to Voices for Illinois Children. If block grants were passed to all the states, Illinois and many other states would have to reduce Medicaid spending, number of programs being covered, and enrollment. With low spending on Medicaid being so prevalent already, it is important to study the impact on low-income, disabled, and children in Illinois. Medicaid is a topic that is of recent interest to this new presidential administration. With the current president threatening to repeal President Obama’s Affordable Care Act (ACA), looking at the results that Medicaid has had on the United States health is important. As one party is discrediting its return on (taxpayer dollars) investment, it is critical to review how government funded health insurance have impacted the well-being of Americans.

#### Data - Variables
While looking at Medicaid’s overall effect on U.S. health, the dependent variable is BMI, an important facet in determining a person’s overall health. BMI is calculated by taking the weight variable in pounds and dividing it by the height variable in inches, squared, then multiplying that number by 703. A BMI score above 30 would be considered obese. Independent variables include Medicaid, health insurance, income, time since last physicians visit, number of dependents, depression, gender, occupation, and education. 

#### Variable Explanation
NLSY79 data is used in this study because it is a cross-sectional representation of individuals. This research study looks at adults aged 25 - 33 for the year 1990 and 45 - 53 for the year 2010, providing the most helpful and efficient way to see the outcome of Medicaid on BMI over time. All variables have a chosen baseline, because if all possibilities are included for a variable, then there would be a problem of perfect multicollinearity. Specific variables, like education and income, were chosen in an attempt to prevent omitted variable bias.

#### Data Specification 
Height is in inches and weight is in pounds, which is how it is typically presented in the data. Dependents is measured by number of children. Income is measured in actual US dollars. Education is broken up into five categories (some high school, high school grad, some college, college grad, graduate). Occupation, gender, and race are binary variables. 
For the dependent variable, height and weight are combined to create BMI. 
For Medicaid, binary dummy variables were created. With health insurance, two dummy variables categorized as private health insurance and no health insurance were created. 
Income is broken up into five categories that include 0, 1-15,000, 15,000-25,000, 25,000-50,000 and 50,000+ (in U.S. dollars). 
The number of dependents is also broken up into four groups ranging from 0 to 3. 
Depression is broken up into four categories that include 0, 1-4,5-9,10+ (in points), which is based on a 7-item Center of Epidemiological Studies Depression (CESD) test. 
Marital status is divided into three categories which include yes, no, and other. 
Gender, urban/rural, and race are treated like binary variables. 
Occupation is broken up into 3 groups that include no jobs, 1 job, 2-3 jobs, and 4+ jobs. 
Number of dependents is also grouped into 3 categories ranging from 2 - 5. 
Finally, number of weeks unemployed are split into 4 categories which include 0 weeks, 4 weeks, 12 weeks, and 26-52 weeks. 

#### Data Cleaning
Analysis was primarily done using SAS, SPSS, and Stata. To analyze data via Python, clean data doing the following:
<li> Split strings containing multiple symptoms into separate columns and apply binary encoding to create a wide dataset with a dummy variable for each
Recode incorrect and null values as NaN. </li>

<li>Ensure that data in each column is in a uniform format (eg. the 'height_inches' column originally contained numeric values encoded as strings as well as '72 inches (capped value for females)', recoded to 72.</li>

<li>Rows containing unhelpful demographic data and codes are dropped.</li>

<li>Set all table values that contain text, excluding headers, to ThisFormat.</li>

<li>Replace all data in the target column with code using more understandable labels; created from the scraped data (eg. 338 becomes OneDep90.) This is done regardless of how the data is prepared. </li>

<p>
Multiple strategies were considered for encoding categorical variables to use with skikit-learn’s Decision Tree module. Because Skikit-learn interprets numerical features as continuous numeric variables, we identified methods to avoid inducing order that does not exist in the data, and determined to use the ‘get_dummies’ function in pandas to convert categorical variables into dummy variables to accomplish this task efficiently. </p>




For a full variable labeling explanation, click [here](https://github.com/jessicachitkuer/MedicaidRegressionAnalysis/blob/main/.github/workflows/NLSY79%20codes.pdf). 

For a summary of the bysort data for 1990 and 2021, click [here](https://github.com/jessicachitkuer/MedicaidRegressionAnalysis/blob/jessicachitkuer-patch-1/Summ%20and%20by%20sort%20for%201990%20and%202010.pdf).

[Wiki for more info. ](https://github.com/jessicachitkuer/MedicaidRegressionAnalysis/wiki).

