### deep-learning-challenge
#### Overview: 
From Alphabet Soup’s business team, here we have a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization. We have used the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

- EIN and NAME—Identification columns
- APPLICATION_TYPE—Alphabet Soup application type
- AFFILIATION—Affiliated sector of industry
- CLASSIFICATION—Government organization classification
- USE_CASE—Use case for funding
- ORGANIZATION—Organization type
- STATUS—Active status
- INCOME_AMT—Income classification
- SPECIAL_CONSIDERATIONS—Special considerations for application
- ASK_AMT—Funding amount requested
- IS_SUCCESSFUL—Was the money used effectively

## Dependencies

- This code uses Python and relies on several libraries, including:
  - `pandas` for data manipulation
  - `scikit-learn` for machine learning tools
  - `tensorflow` for deep learning
  - `XGBoost` for gradient boosting (optional, if you choose to implement it)
  
## Data

- The data for this project is stored in a CSV file called `charity_data.csv`. It contains information about various funding applications, including features and a target variable indicating whether the funding was successful or not.We loaded the data into panda dataframe and started with dropping the column EIN and NAME as they do not contribute to the predictive power of the model. Next, we looked at APPLICATION_TYPE value count for binnning. Then, chose a cutoff value and create a list of application types to be replaced used the variable name `application_types_to_replace` and replaced in dataframe. We went through the same process for CLASSIFICATION as well. After that, we coverted categorical data to numeric with `pd.get_dummies`. We separated our data into two parts: one with information we'll use to make predictions (like characteristics of funding applications) and another that tells us whether those predictions are right or wrong (if the funding was successful or not). Then, we divided the data into two more parts: one to teach our model (75% of the data) and one to test how well it learned (25% of the data). Finally, we checked the size of these parts to make sure everything was set up correctly.

## Steps taken
1. **Data Preparation:** The data is cleaned, split into training and testing sets (usually 70% train, 30% test), and scaled to help the model learn better.

2. **Model Building:** A deep learning model is created using TensorFlow/Keras. You can adjust the model's architecture.

3. **Model Training:** The model is trained using the training data.

4. **Model Evaluation:** The code calculates accuracy, precision, recall, and ROC-AUC to see how well the model is doing.

  
## Summary : 
This deep learning model did okay but didn't reach our goal. To improve, we suggest trying a different model called XGBoost. It's good at solving problems like this and can be more accurate. It's like switching from one type of car to another because it might be faster and safer. So, we recommend giving XGBoost a try to see if it can do better at predicting funding success for Alphabet Soup.

To use this code, ensure that you have the required dependencies installed. You can adjust hyperparameters and model architecture as needed to improve model performance. After running the code, review the model's performance metrics to make funding decisions.







