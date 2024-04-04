# Email Spam Detection

This project aims to detect spam emails using a Logistic Regression model and TF-IDF vectorization.

## Dataset
The dataset used for this project is stored in "mail_data.csv". It contains two columns:
- **Message**: Email messages
- **Category**: Spam or Ham (1 for Ham, 0 for Spam)

## Dependencies
- pandas
- numpy
- scikit-learn (specifically using train_test_split, TfidfVectorizer, and LogisticRegression)
- Python 3.x

## Project Overview
1. Imported necessary libraries including pandas, numpy, and scikit-learn modules.
2. Loaded the dataset from "mail_data.csv".
3. Preprocessed the data:
   - Checked for null values and filled them with empty strings.
   - Converted the 'Category' column to numerical values (0 for spam, 1 for ham).
4. Separated the data into features (X - messages) and target variable (Y - categories).
5. Split the data into training and testing sets using a 80:20 ratio.
6. Used TF-IDF vectorization to convert text messages into numerical features.
7. Trained a Logistic Regression model using the training data.
8. Evaluated the model's accuracy on the testing data, achieving an accuracy of 96%.
9. Demonstrated the model's prediction capability by testing a sample email.

## Running the Code
1. Ensure you have the required dependencies installed.
2. Place the dataset file "mail_data.csv" in the same directory as the code file.
3. Run the Python code provided.
4. Input your email message in the 'your_mail' list to test if it's categorized as spam or ham.

## Sample Output
If the model predicts '0', it's classified as a spam mail. If it predicts '1', it's classified as a ham mail.

For example:
```
Input: ['this is a sample email']
Output: Ham Mail

Input: ['this is a spam email claiming you won a prize']
Output: Spam Mail
```

## Note
This project assumes the dataset is clean and properly labeled. For real-world applications, additional preprocessing and model tuning may be required.
