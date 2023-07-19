# Final-for-Sebas-Javy
Final Python A Project

We used both Google Colaboration and Jupyter Notebook.

import pandas as pd
import matplotlib.pyplot as plt
import numpy as np

from google.colab import drive
drive.mount('/content/drive')

from google.colab import files
uploaded = files.upload()

pd.read_csv("(YSP) Python A Project - Population-3.csv")

df = pd.read_csv("(YSP) Python A Project - Population-3.csv")

Extract the required columns from the DataFrame (this will be done for each region)
x = df['Year']
y = df['World'] 

m, b = np.polyfit(x, y, 1)
best_fit = m * x + b

Create a scatter plot
plt.scatter(x, y)
plt.plot(x, best_fit, color='red', label='line of best fit')
plt.xlabel('Year')
plt.ylabel('Population')
plt.title('World Population')

Display the plot
plt.show()

Create a plot defining the increasing/decreasing rates of population
plt.plot(x, y, color='black')
plt.scatter(x, y, color='green')
plt.xlabel('Year')
plt.ylabel('Population')
plt.title('Identifying Population Rates')
plt.grid(True)
plt.show()
