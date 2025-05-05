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

