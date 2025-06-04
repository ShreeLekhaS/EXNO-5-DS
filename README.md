# EXNO-5-DS-DATA VISUALIZATION USING MATPLOT LIBRARY

# Aim:
  To Perform Data Visualization using matplot python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```
import matplotlib.pyplot as plt
import seaborn as sns
import numpy as np
import pandas as pd
```
### 1. LINE CHART
```
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
plt.plot(x, y, label="Line 1", color='blue', marker='o')
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.title("Simple Line Graph")
plt.legend()
plt.grid(True)
plt.show()
```

![image](https://github.com/user-attachments/assets/863f1eaa-c515-48ad-ac24-2c8eff0dc156)
### 2. MULTI-LINE PLOT

```
x1, y1 = [1,2,3], [2,4,1]
x2, y2 = [1,2,3], [4,1,3]
plt.plot(x1, y1, label='Line A', color='green')
plt.plot(x2, y2, label='Line B', color='red')
plt.title("Multiple Line Plot")
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.legend()
plt.grid(True)
plt.show()
```
![image](https://github.com/user-attachments/assets/8751c998-9d7b-4188-8ea6-487538c79fad)
### 3. FILL BETWEEN LINE CHART

```
x_vals = [0,1,2,3,4,5]
y_vals = [0,1,4,9,16,25]
plt.fill_between(x_vals, y_vals, color="skyblue", alpha=0.4)
plt.plot(x_vals, y_vals, color="Slateblue", alpha=0.6)
plt.title("Line Graph with Fill Between")
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.grid(True)
plt.show()
```
![image](https://github.com/user-attachments/assets/02b35e5c-5138-45f8-8088-6960225c9a6c)

### 4. INTERPOLATED SPLINE PLOT
```
from scipy.interpolate import make_interp_spline
x = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])
y = np.array([2, 4, 5, 7, 8, 8, 9, 10, 11, 12])
x_smooth = np.linspace(x.min(), x.max(), 300)
y_smooth = make_interp_spline(x, y)(x_smooth)
plt.plot(x_smooth, y_smooth, label='Smooth Line', color='purple')
plt.title("Spline Chart")
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.legend()
plt.grid(True)
plt.show()
```
![image](https://github.com/user-attachments/assets/a17a3a93-25be-41a8-8f7e-7fe24d8edb03)
### 5. BAR CHART
```
values = [5, 6, 3, 7, 2]
names = ["A", "B", "C", "D", "E"]
plt.bar(names, values, color='orange')
plt.title("Simple Bar Graph")
plt.xlabel("Categories")
plt.ylabel("Values")
plt.grid(axis='y')
plt.show()
```
![image](https://github.com/user-attachments/assets/1135f585-dc1b-4b19-a9d1-aae223a67ed0)

### 6. STACKED BAR CHART
```
df = sns.load_dataset("tips")
avg_total_bill = df.groupby("day", observed=True)["total_bill"].mean()
avg_tip = df.groupby("day", observed=True)["tip"].mean()
plt.figure(figsize=(8, 6))
plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
plt.show()
```
![image](https://github.com/user-attachments/assets/5df03e69-433d-446a-8521-ad6f397668c9)

### 7. SCATTER PLOT
```
x = [1,2,3,4,5,6,7,8,9,10]
y = [2,4,5,7,6,8,9,11,12,12]
plt.scatter(x, y, label="stars", color="green", marker="*", s=100)
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.title("Custom Scatter Plot")
plt.legend()
plt.grid(True)
plt.show()
```
![image](https://github.com/user-attachments/assets/5ca767e1-6642-480a-b500-08fb9f3ab180)

### 8. PIE CHART
```
activities = ['eat', 'sleep', 'work', 'play']
slices = [3, 7, 8, 6]
colors = ['r', 'y', 'g', 'b']
plt.pie(slices, labels=activities, colors=colors, startangle=90, shadow=True, explode=(0, 0.1, 0, 0), autopct='%1.1f%%')
plt.title("Pie Chart of Daily Activities")
plt.show()
```

![image](https://github.com/user-attachments/assets/28e44df7-b267-492f-a72c-c2945e75d8f3)

# Result:
Thus the code for Data Visualization using matplot successfully executed.
