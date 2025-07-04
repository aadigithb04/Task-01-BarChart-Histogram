# Task-01-BarChart-Histogram
# Task 01 - Bar Chart / Histogram Visualization
# Dataset: World Population - https://data.worldbank.org/indicator/SP.POP.TOTL

import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Sample population data (you can replace this with actual dataset)
data = {
    'Country': ['India', 'China', 'USA', 'Indonesia', 'Pakistan', 'Brazil', 'Nigeria', 'Bangladesh', 'Russia', 'Mexico'],
    'Population (in Millions)': [1417, 1440, 331, 276, 240, 214, 223, 169, 146, 126]
}

df = pd.DataFrame(data)

# Bar Chart
plt.figure(figsize=(10, 6))
sns.barplot(x='Population (in Millions)', y='Country', data=df, palette='viridis')
plt.title('Population by Country - Bar Chart')
plt.xlabel('Population (in Millions)')
plt.ylabel('Country')
plt.tight_layout()
plt.show()

# Histogram
plt.figure(figsize=(8, 5))
sns.histplot(df['Population (in Millions)'], bins=5, kde=True, color='skyblue')
plt.title('Distribution of Population - Histogram')
plt.xlabel('Population (in Millions)')
plt.tight_layout()
plt.show()
