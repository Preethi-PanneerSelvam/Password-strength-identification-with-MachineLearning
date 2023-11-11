# Password Strength Classifier

## Overview

This Python script utilizes machine learning techniques to classify the strength of passwords into three categories: Weak, Medium, and Strong. It employs the RandomForestClassifier from the scikit-learn library and features the use of Term Frequency-Inverse Document Frequency (TF-IDF) vectorization to convert password strings into numerical representations.

## Requirements

Make sure you have the following libraries installed:

- pandas
- numpy
- scikit-learn

You can install them using the following command:

```bash
pip install pandas numpy scikit-learn
```

## Usage

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/yourusername/your-repository.git
   ```

2. **Navigate to the Project Directory:**
   ```bash
   cd your-repository
   ```

3. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Prepare Data:**
   - Ensure your password data is in a CSV file format with a column named "password" for the passwords and a column named "strength" for the corresponding strength labels (0 for Weak, 1 for Medium, 2 for Strong).

5. **Run the Script:**
   ```bash
   python password_strength_classifier.py
   ```
   Follow the prompts to enter a password and observe the predicted strength.

## Code Structure

- **Importing Libraries:**
  Importing necessary libraries, including pandas, numpy, scikit-learn, and warnings.

- **Data Loading and Cleaning:**
  Loading password data from a CSV file, handling any bad lines, and dropping rows with missing values.

- **Label Mapping:**
  Mapping numerical strength labels to categorical labels (0: "Weak", 1: "Medium", 2: "Strong").

- **Tokenizer Function:**
  Defining a tokenizer function to break down passwords into individual characters.

- **TF-IDF Vectorization:**
  Using scikit-learn's TfidfVectorizer to convert password strings into numerical representations.

- **Train-Test Split:**
  Splitting the data into training and testing sets.

- **Random Forest Classifier:**
  Creating and training a RandomForestClassifier model.

- **Model Evaluation:**
  Printing the accuracy score of the model on the test set.

- **Password Input and Prediction:**
  Taking a password input from the user, transforming it using TF-IDF, and predicting its strength using the trained model.

## Note

This script is a basic example and might need further optimization and customization based on your specific use case and data. Ensure your data is appropriately formatted and representative for training a password strength classifier.

**Disclaimer:** Password strength classification is a complex topic, and this script provides a simplistic approach. Consider consulting security experts for more robust solutions in real-world scenarios.
