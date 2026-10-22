# Holiday-Package-Purchase-Prediction-Using-Machine-Learning

📌 Project Overview

This project focuses on predicting whether a customer is likely to purchase a holiday package using machine learning classification algorithms. The objective is to help Trips & Travel.com improve its marketing strategy, identify potential customers, and make marketing campaigns more efficient using customer data.

The project uses customer information to train and evaluate multiple classification models, with a final focus on the Random Forest Classifier.

🎯 Problem Statement

"Trips & Travel.Com" company wants to enable and establish a viable business model to expand the customer base.
One of the ways to expand the customer base is to introduce a new offering of packages. Currently, there are 5 types of packages the company is offering  Basic, Standard, Deluxe, Super Deluxe, King. Looking at the data of the last year, we observed that 18% of the customers purchased the packages. However, the marketing cost was quite high because customers were contacted at random without looking at the available information.
The company is now planning to launch a new product i.e. Wellness Tourism Package. Wellness Tourism is defined as Travel that allows the traveler to maintain, enhance or kick-start a healthy lifestyle, and support or increase one's sense of well-being.
However, this time company wants to harness the available data of existing and potential customers to make the marketing expenditure more efficient.

🎯 Project Objectives

Predict whether a customer will purchase a holiday package.

Analyze customer demographics, preferences, and travel behavior.

Clean and preprocess the dataset for machine learning.

Compare multiple classification algorithms.

Optimize the Random Forest model using hyperparameter tuning.

Evaluate model performance using classification metrics and an ROC curve.


📂 Dataset Information

Dataset: Travel.csv

Source: Holiday Package Purchase Prediction – Kaggle

Total Records: 4,888

Original Columns: 20

Target Variable: ProdTaken

The target variable indicates whether a customer purchased a holiday package.

1 – Package purchased

0 – Package not purchased


🛠️ Technologies Used

Python – Programming and data analysis

Pandas – Data manipulation and cleaning

NumPy – Numerical operations

Matplotlib – Data visualization

Seaborn – Exploratory data analysis and visualization

Scikit-learn – Preprocessing, model training, and evaluation

Jupyter Notebook – Development environment



🔄 Project Workflow

1. Data Loading and Understanding

Loaded the travel customer dataset using Pandas.

Examined dataset dimensions, column names, data types, and statistical summaries.

Identified missing values and explored the available features.

2. Data Cleaning

Identified missing values in relevant columns.

Used median imputation for selected numerical features.

Used mode imputation for selected categorical and discrete features.

Checked duplicate records and data types.

3. Feature Engineering

Created the TotalVisiting feature by combining the number of adults/persons visiting and children visiting.

Removed the original columns used to create the combined feature.

Identified numerical, categorical, discrete, and continuous features.

4. Data Preprocessing

Separated the independent variables (X) from the target variable (y).

Applied OneHotEncoder to categorical features.

Applied StandardScaler to numerical features.

Split the data into training and testing sets using an 80:20 ratio, with random_state=42.


5. Model Training and Comparison

The following classification algorithms were evaluated:

Logistic Regression

Decision Tree Classifier

Random Forest Classifier

Gradient Boosting Classifier


6. Hyperparameter Tuning

       Used RandomizedSearchCV with 3-fold cross-validation and 100 parameter combinations to search for suitable Random Forest hyperparameters.

7. Model Evaluation

   Evaluated the trained models using:

Accuracy

Precision

Recall

F1-score

ROC-AUC score

ROC curve



🤖 Final Model: Random Forest Classifier

   The final model was configured using the best hyperparameters identified during the notebook's RandomizedSearchCV process.


📊 Model Performance

  The following are the test-set results recorded in the notebook after hyperparameter tuning.

Performance Interpretation

Accuracy – 93.15%: The model correctly classified approximately 93% of the test records.

Precision – 96.97%: Among the customers predicted to purchase, approximately 97% were actual purchasers in the test set.

Recall – 67.02%: The model identified approximately 67% of actual purchasers.

Weighted F1-score – 92.65%: The weighted F1-score summarizes the balance between precision and recall across the classes.

ROC-AUC – 83.25%: The ROC-AUC score indicates the model's ability to distinguish between the two target classes.

Important observation: Although the model achieves high accuracy and precision, its recall is lower. Further improvements could focus on identifying more potential buyers while maintaining acceptable precision.


💡 Business Benefits

Helps identify customers who are more likely to purchase holiday packages.

Supports data-driven marketing campaign planning.

Can help reduce unnecessary customer outreach.

Provides insights into customer travel behavior and preferences.

Supports more efficient allocation of marketing resources.

These are potential business benefits; actual cost savings would need to be validated in a real marketing campaign.


📁 Repository Structure

Holiday-Package-Purchase-Prediction/
│
├── random-forest-classification-implementation.ipynb
├── Travel.csv
├── README.md
└── auc.png

Note: Update the filenames in this structure to match the actual filenames uploaded to your GitHub repository. The notebook reads Travel.csv; rename your uploaded Travel(1).csv to Travel.csv, or update the notebook's CSV path accordingly. The ROC plot is saved as auc.png when the relevant notebook cell runs.


▶️ How to Run the Project

Step 1: Clone the repository

git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY-NAME.git

Step 2: Navigate to the project folder

cd YOUR-REPOSITORY-NAME

Step 3: Install the required libraries

pip install pandas numpy matplotlib seaborn scikit-learn jupyter

Step 4: Ensure the dataset filename matches the notebook

Place Travel.csv in the same directory as the notebook, or update the file path in the data-loading cell.

Step 5: Launch Jupyter Notebook

jupyter notebook

Open random-forest-classification-implementation.ipynb and run the cells in order.


🚀 Future Improvements

Perform additional feature selection and feature-importance analysis.

Address the difference between precision and recall.

Evaluate class imbalance and experiment with suitable resampling techniques or classification thresholds.

Validate performance using additional cross-validation and test data.

Save the trained model and preprocessing pipeline for reuse.

Develop a simple web application for customer purchase predictions.

Monitor model performance on new customer data.


📚 Learning Outcomes

Through this project, I gained practical experience in:

Data cleaning and exploratory data analysis.

Handling missing values.

Feature engineering and preprocessing.

Encoding categorical variables and scaling numerical features.

Training and comparing classification algorithms.

Hyperparameter tuning using RandomizedSearchCV.

Evaluating classification models using multiple performance metrics.

Applying machine learning to a business-oriented prediction problem.


👨‍💻 Author

Sachin Jadhav

Aspiring Data Analyst | Business Analytics | Machine Learning

Skills: Python | Pandas | NumPy | SQL | Power BI | Machine Learning | Data Analysis


⭐ Acknowledgements

Dataset: Kaggle – Holiday Package Purchase Prediction

Libraries: Pandas, NumPy, Matplotlib, Seaborn, and Scikit-learn

If you find this project useful, feel free to ⭐ the repository!
