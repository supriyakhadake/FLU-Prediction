# FLU-Prediction

## Type of Project: Logistic regression, Decision Tree, Random Forest and KNN-Classifier.

### 1.	Introduction
Our motivation is to predict if a person is infected by FLU or not infected by FLU based on various factors such as symptoms exhibited by the patient.

- Influenza, commonly known as "the flu", is an infectious disease caused by an influenza virus. High fever, runny nose, sore throat, headache, coughing, etc. are the most common symptoms. These symptoms typically begin two days after exposure to the virus and most last less than a week. Complications of influenza may include viral pneumonia, secondary bacterial pneumonia, sinus infections, and worsening of previous health problems such as asthma or heart failure. Once detected at an earlier stage based on the symptoms, the flu can be treated by getting plenty of rest, drinking plenty of liquids and, take medications to relieve the fever and muscle aches associated with the flu if necessary.

- Our model will be created considering the most impactful parameters that can help determine factors that impact people with flu status positive/negative.
In our current project we aim at implementing logistic regression using R and incorporate various data mining tasks to pre-process data. We will build models using different technique for modeling like Classification & Regression Tree(CART) algorithm/ Decision Tress and Random forest to determine important variables. Post comparison we will be able to provide with the best model.

### 2.	Data Sets
Database Selected: Influenza Research Database
Source Website: http://www.fludb.org/brc/staticContent.spg?decorator=influenza&type=FluInfo&subtype=Mission

Dataset Description: Influenza Research Database (IRD) provides a resource for the influenza virus research community that facilitates an understanding of the influenza virus and how it interacts with the host organism, leading to new treatments and preventive actions. This dataset contains influenza surveillance data, human clinical data associated with virus extracts, phenotypic characteristics of viruses isolated from extracts, and all genomic and proteomic data available in public repositories for influenza viruses. The data set has 1700 records and 15 variables

- Dependent Variable: FluTestStatus
- Independent Variables: HostIdentifier, Location, Age, Gender, Temperature, MedicalConditions, Fever, RunningNose, Cough, Myalgia, Headache, ThroatAche, Fatique, Vomiting.

### 3.	Research Problems 
List your research problems, that is, what kinds of the problems you want to solve.
You cannot simply say I want to explore the data and find the patterns
You should provide finer-grained research problems that can be solved by statistical techniques. 

- Considering all the symptoms like running nose, cough, fever, etc. against people who are infected in past, we can determine which of the symptoms impact the most.
- Exploring the Age groups against people who are infected and not to identify age groups most infected.
- Analyze gender with respect to test flu status positive or negative and check if which gender is more susceptible to getting infected.
- Analyze current medical condition for both male and female and check whose condition is bad/good.
- Does having a medical condition affect the likelihood of having flu or not.
- Is Flu only prevalent in one state or it is spread across every state.
- We will check if the symptoms have been correctly identified such as if temperature above 99.2 we can consider fever(mild).
- With respect to prior diagnosis of FLU we can determine how many of them were actually positive in FLU test.

### 4.	Potential Solutions
For each problem you list above, figure out feasible solutions, and introduce your plan to perform experiments.

- The dataset includes missing values which we will take care of using data pre-processing techniques. For example: Missing values in age will be filled with median and if not many can be ignored, temperature data with fever =1 will be inserted as 99.2 and fever=0 as 98.6 which is actual body temperature. We will discretize gender from M/F to 1/0 for simpler evaluation. We will also check if there are any duplicate records and handle the same.
- For all the above-mentioned problem, we will analyze data set by considering all the factors and determining their statistical descriptions like (mean, mode, median, variance, etc.) and finding correlations between the parameters to see how influential they are.
- We will plot bar graphs between different parameters against “flu status” to check their impact on people with flu status as positive/negative.
- We will build and compare different models and determine the best model that helps us determine the odds of FLU status being positive or negative.
- For the problem like 4 and 5 we will check if there is a strong association and correlation between medical condition, gender and person having the fLU. We can decide by regression analysis if there is a strong relation with the FLU status.
- For problem like 6, we can decide by checking the frequency of the people having flu in every state and across the continent and can draw conclusions using clustering, decision tree etc.
- For problem like 8, we can determine if a pre-diagnosis leads to the correct FLU status.

### 5.	Evaluations

- We should always check for missing values in the data before proceeding with the analysis. In our case, we evaluated our data and we observed that there are missing values. So, first we will investigate missing data and deal with it and then go ahead with the EDA.
- We will split our dataset using Hold-out evaluation into train(80%) and test(20%) data.
- We will perform statistical analysis in EDA which will help in describing characteristics of each parameters.
- We will determine correlation between the variables and find the effect of the variables on one another.
- We have identified dependent and independent variables as well as analyzed our categorical data.
- By using random-forest we will have all the important features in descending order.
- Using decision tree, we will be able to have a graphical representation of combinations of decision rules and we get records of the test outcomes as antecedents were the leaf node classification will be the consequence.  
- During regression analysis we will be able to determine which independent variables are most impactful in getting the odds of dependent variable being positive or negative.
- For determining the best model for the system, we will compare the AIC value and the McFadden’s R2 value for the built models.
- We will do predictions on the test data by determining odds of FLU status using the best model.

### 6.	Expected Outcomes
Introduce your expected outcomes for your project

- In view of the model we will have the capacity to decide the elements that most likely lead to correctly determine FLU status. The model is required to help us analyze and decide which gender, location, etc. has more FLU and which symptoms relates to the FLU status positive the most. 
- The model will help us predict if a person has Flu or not as per the rest of the record.
- Our model can help different hospitals to have an idea of how much they need to stock up on medication. For instance, Children Hospital Boston had 10 cases of influenza where as Beth Israel had 10 times more the number of cases. As they had more cases they can stock up accordingly.






