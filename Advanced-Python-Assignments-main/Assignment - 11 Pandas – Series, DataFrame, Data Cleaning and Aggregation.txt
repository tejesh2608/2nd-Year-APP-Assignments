import pandas as pd
import numpy as np

# Create Series with 10 random numbers
ser = pd.Series(np.random.randint(1, 100, 10))
print("Pandas Series:")
print(ser)

# Create DataFrame
data = {
    'Name': ['Amit', 'Rahul', 'Priya', 'Sneha'],
    'Age': [20, 21, 19, 22],
    'City': ['Pune', 'Mumbai', 'Delhi', 'Pune'],
    'Salary': [30000, 40000, 35000, 45000]
}

df = pd.DataFrame(data)

print("\nDataFrame:")
print(df)

# Select column
print("\nName Column:")
print(df['Name'])

# Select rows
print("\nFirst Row:")
print(df.iloc[0])

# Data cleaning
print("\nMissing Values:")
print(df.isnull())

# Remove duplicates
print("\nAfter Removing Duplicates:")
print(df.drop_duplicates())

# Grouping and aggregation
print("\nAverage Salary:")
print(df.groupby('City')['Salary'].mean())

print("\nSalary Statistics:")
print(df['Salary'].agg(['mean', 'sum', 'max', 'min']))
