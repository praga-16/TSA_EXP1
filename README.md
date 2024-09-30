# Ex.No: 01 PLOT A TIME SERIES DATA
###  Date: 30-09-2024

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:

## Dataset : https://www.kaggle.com/datasets/jboysen/global-food-prices
## Population:
```
PRAGATHEESVRAN A B
2122212400339
```
```python
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("POPTHM.csv",parse_dates=["DATE"],index_col="DATE")
df.head()
df_filtered = df["2000":"2023"]
annual_mean = df_filtered.resample('Y').mean()
mean = annual_mean.plot(kind='line')
plt.xlabel("Year")
plt.ylabel("Population (in Thousands)")
plt.title("Average Annual Population (2000-2023)")
plt.show()
```
# Market Price:
```python
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("trainset.csv",parse_dates=["Date"],index_col="Date")
df.head()
df.Close.resample('M').mean()
mean=df.Close.resample('M').mean().plot(kind='line')
plt.xlabel("Month")
plt.ylabel("Price")
plt.show()
mean=df.Close.resample('Y').mean().plot(kind='line')
plt.xlabel("Year")
plt.ylabel("Price")
plt.show()
```
# Temperature:
```python
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("DailyDelhiClimateTrain.csv",parse_dates=["date"],index_col="date")
df.head()
mean=df["meantemp"].resample('M').mean().plot(kind='line')
plt.xlabel("Month")
plt.ylabel("Temperature")
plt.show()
```


# OUTPUT:
## Population:

![OUT](https://github.com/JEEVAABI/TSA_EXP1/assets/93427098/fade9281-68b0-4f19-93bc-92660324c9dc)
# Market Price:

![2 (1)](https://github.com/JEEVAABI/TSA_EXP1/assets/93427098/5bccb008-4a74-4afd-b810-224c61675b9c)
# Temperature:

![4 (1)](https://github.com/JEEVAABI/TSA_EXP1/assets/93427098/dbef86e7-56d2-4d1d-be20-36cd57353f62)






# RESULT:
Thus we have created the Python code for plotting the time series of given data.
