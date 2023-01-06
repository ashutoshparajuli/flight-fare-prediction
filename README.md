# Project Title: Predicting Flight Fares Using Machine Learning

# Summary:

The goal of this project is to build a machine learning model that can predict the fare of a flight based on various input features such as the departure location, destination, time of year, etc. By analyzing a dataset of historical flight prices, I aimed to create a model that can accurately predict the fare of a new flight given certain input features.

# Project Description:

This code is written in Python and is using the pandas library to load and manipulate a dataset containing information about flights. The dataset is read from a URL and stored in a **pandas DataFrame** called **"df"**.

The code then checks for missing values in the dataset using the **isnull()** and **sum()** methods and drops any rows with missing values using the **dropna()** method.

Next, the code extracts and creates new columns for the day, month, hour, and minute of the flight's departure date, departure time, and arrival time using the **to_datetime()** method and the dt attribute. These new columns are created by specifying the appropriate format for the input date or time and extracting the relevant information.

The code then drops the original columns for the date of journey, departure time, and arrival time, as they are no longer needed.

After this, the code checks the format of the duration data and modifies it to a consistent format of hours and minutes if necessary. It then creates separate lists for the hours and minutes of the duration and stores them as integers in separate variables. Finally, it creates new columns for the duration hours and minutes in the DataFrame and drops the original duration column.

The code then encodes the categorical columns in the dataset using the **get_dummies()** method and stores the resulting data in a new DataFrame called **"df_encoded"**.

Finally, the code splits the encoded dataset into training and test sets using the **train_test_split()** method and fits a random forest regression model to the training set. The model is then used to make predictions on the test set and the performance of the model is evaluated using the **mean_absolute_error()** and **r2_score()** functions.
