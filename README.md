# Ex.No: 01 PLOT A TIME SERIES DATA
###  Date: 

# AIM:
To Develop a python program to Plot a time series dataplot of the gold price, I'll use the "Date" and "Price Today" columns.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:

## Dataset : https://www.kaggle.com/datasets/cvergnolle/gold-price-and-relevant-metrics
## Population:
```
PRAGATHEESVRAN A B
2122212400339
```

# Market Price:
```python
import pandas as pd
import matplotlib.pyplot as plt

# Load the CSV file
file_path = 'Gold Price Prediction.csv'  # Replace with your file path
data = pd.read_csv(file_path)

# Convert 'Date' column to datetime format
data['Date'] = pd.to_datetime(data['Date'])

# Set 'Date' as the index
data.set_index('Date', inplace=True)

# Plot the time series of 'Price Today'
plt.figure(figsize=(10, 6))
plt.plot(data.index, data['Price Today'], label='Gold Price Today', color='blue')

# Customize the plot
plt.title('Gold Price Today Over Time')
plt.xlabel('Date')
plt.ylabel('Gold Price')
plt.grid(True)
plt.legend()

# Display the plot
plt.show()

```



# OUTPUT:
## Gold Price Today Over Time:

![image](https://github.com/user-attachments/assets/25fb85f4-e14a-4e8c-af27-333055e76360)






# RESULT:
Thus we have created the Python code for plotting the time series of given data.
