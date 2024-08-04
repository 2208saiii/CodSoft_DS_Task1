# Titanic Survival Prediction using Machine Learning

## Project Overview
This project aims to predict the survival of passengers on the Titanic using a machine learning model. The logistic regression model was chosen to perform the predictions, taking into account factors such as passenger class, sex, and age.

## Dataset
The dataset used in this project is the Titanic dataset, which contains detailed information about passengers on the Titanic. The dataset has the following columns:

- `PassengerId`: Unique ID for each passenger
- `Survived`: Survival status (0 = No, 1 = Yes)
- `Pclass`: Ticket class (1 = 1st, 2 = 2nd, 3 = 3rd)
- `Name`: Name of the passenger
- `Sex`: Gender of the passenger
- `Age`: Age of the passenger
- `SibSp`: Number of siblings/spouses aboard the Titanic
- `Parch`: Number of parents/children aboard the Titanic
- `Ticket`: Ticket number
- `Fare`: Passenger fare
- `Cabin`: Cabin number
- `Embarked`: Port of Embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)

## Exploratory Data Analysis (EDA)
Key findings from the EDA include:

- The dataset contains 891 entries with 12 columns.
- 342 passengers survived, while 549 did not.
- There are more male passengers than female passengers.
- The survival rate for female passengers is higher compared to male passengers.
- Passengers in higher classes (1st and 2nd) have a higher survival rate compared to those in the 3rd class.

## Data Preprocessing
The dataset was preprocessed as follows:

- Missing values in the `Age` column were filled with the mean age.
- The `Sex` column was converted to numerical values (0 for female and 1 for male) using Label Encoding.

## Model Training
A logistic regression model was trained to predict the survival of passengers. The data was split into training and testing sets, with 80% used for training and 20% for testing.

### Features
The features used for training the model were:
- `Sex`
- `Pclass`

### Model Evaluation
The model was evaluated using the test data, yielding predictions that can be compared with the actual survival status.

## Prediction
To predict the survival of a specific passenger, use the following code:

```python
res = log.predict([[2, 1]])

if res == 0:
    print("So sorry, Not Survived!")
else:
    print("Survived")
```

### Example Output
```python
So sorry, Not Survived!
```

## Conclusion
This project demonstrates how logistic regression can be used to predict the survival of Titanic passengers based on their sex and class. It provides a straightforward approach to making predictions using machine learning techniques.

## Requirements
- pandas
- numpy
- seaborn
- matplotlib
- scikit-learn

## How to Run
1. Clone the repository.
2. Install the required packages using `pip install -r requirements.txt`.
3. Run the `titanic_survival_prediction.py` script to train the model and make predictions.

## Contributions
Contributions are welcome! Please open issues or submit pull requests to contribute to this project.

Feel free to reach out if you have any questions or need further assistance. Happy coding!
