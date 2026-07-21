# Ex.No: 01A PLOT A TIME SERIES DATA
###  Name : Sanjay Balaji S
### Reg. No : 212223240149

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
```
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
df = pd.read_csv("AEP_hourly.csv")
df.head()
df.info()
df['Datetime'] = pd.to_datetime(df['Datetime'])
df['decimal_hr'] = [t.hour + t.minute/60 for t in df['Datetime']]
df['Date'] = df['Datetime'].dt.date 
df.head()
plt.plot(df['Date'],df['AEP_MW'], color='blue')
plt.xlabel('Year')
plt.ylabel("Mega Watts")
plt.title("Energy Comsumption Over the years")
plt.show()
```

# OUTPUT:
![alt text](<Screenshot 2026-07-21 143004.png>)

![alt text](<Screenshot 2026-07-21 143010.png>)

# RESULT:
Thus we have created the python code for plotting the time series of given data.