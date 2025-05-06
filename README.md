 # 🏥Medical Insurance Premium Prediction

Globally, health insurance costs are on the rise, with significant increases projected across Asia-Pacific and North America. This project aims to address this challenge by using a Linear Regression model to predict medical insurance charges based on key demographic and lifestyle factors, including age, sex, BMI, number of children, smoking status, and region.

The workflow begins with setting up and querying the dataset using SQL, followed by exploratory data analysis (EDA) and predictive modeling using Python.

The project leverages widely-used data science libraries such as NumPy, pandas, scikit-learn, seaborn, and matplotlib.

## 🧠Key Features
- Used **MySQL** to structure and preview the dataset
- Performed **data preprocessing and EDA** using **pandas**, **matplotlib**, and **seaborn**
- Created **interaction terms** like `bmi_smoker` and `age_smoker` to capture the impact of smoking on BMI and age in predicting charges
- Built a **Linear Regression model** with **train/test split**
- Evaluated model performance using **R² score**
- Validated predictions on a separate dataset
- Used business rules to cap unrealistic predictions (e.g., minimum charge of $1000)

## 📊Data Description
  
- age: Age of the policyholder
- sex: Gender of the policyholder, either male or female
- bmi: Body Mass Index, a numeric value calculated from weight and height, used to classify underweight, normal, overweight, or obesity. A healthy BMI typically ranges from 18.5 to 24.9
- children: Number of dependents covered under the insurance plan
- smoker: Indicates whether the individual is a smoker (yes or no)
- region: Geographical region in the U.S. where the person resides (northeast, southeast, southwest, northwest)
- charges: Individual medical costs billed by health insurance

## 📊EXPLORATORY DATA ANALYSIS (EDA)
<h3 align="center"> Distribution of Insurance Charges </h3>
<p align="center">
  <img src="Images/distribution.plot.png" width="600"/>
</p>
The distribution of charges is right-skewed, with most charges falling under $15,000 but some reaching beyond $60,000. This suggests the presence of high-cost outliers, associated with specific risk groups (e.g. smokers or high-BMI individuals).

<h3 align="center">  Correlation Heatmap </h3>
<p align="center">
<img src="Images/correlation.plot.png" width="600"/>
</p>
The heatmap shows that smoking status, age and bmi have positive correlation with charges.

### 3. Charges by Smoker Status
Smokers tend to incur significantly higher charges. The median charge for smokers is over 3x higher than for non-smokers, clearly establishing smoking as a strong predictor of medical expenses.

### 4. Charges by Sex
There is no major difference in insurance charges between male and female policyholders. This supports the finding in the correlation matrix where sex_male has almost no relationship with charges.

### 5. Charges by Region
Region does not play a significant role in determining insurance charges. All regions exhibit similar distributions with overlapping medians.

### 6. Charges vs Age (Colored by Smoker)
Insurance charges increase with age, especially for smokers. Smokers tend to face much higher insurance charges as they get older compared to non-smokers, a key justification for creating interaction terms like 'age_smoker'.

### 7. Charges vs BMI (Colored by Smoker)
For people who smoke, their BMI has a significant impact on the amount they are charged for insurance. This means that as a smoker's BMI increases, their insurance costs are likely to rise more noticeably. This interaction validates adding 'bmi_smoker' interaction term in the regression model.


