# 🐍 Python for Data Science

<p align="center">
  <img src="python-cheat-sheet.svg" alt="Python Cheat Sheet" width="100%">
</p>

## 📚 Table of Contents

1. [Python Basics](#python-basics)
2. [Data Structures](#data-structures)
3. [NumPy](#numpy)
4. [Pandas](#pandas)
5. [Data Visualization](#data-visualization)

---

## 🚀 Python Basics

### Variables & Data Types

```python
# Variables
name = "ChatWhole"      # str
age = 25                 # int
height = 5.9            # float
is_student = True       # bool

# Type checking
type(name)               # <class 'str'>
```

### Operators

| Operator | Description | Example |
|----------|-------------|---------|
| `+` | Addition | `5 + 3 = 8` |
| `-` | Subtraction | `5 - 3 = 2` |
| `*` | Multiplication | `5 * 3 = 15` |
| `/` | Division | `5 / 3 = 1.67` |
| `//` | Floor Division | `5 // 3 = 1` |
| `%` | Modulus | `5 % 3 = 2` |
| `**` | Power | `5 ** 3 = 125` |

### Control Flow

```python
# If-else
if condition:
    # do something
elif other_condition:
    # do something else
else:
    # default

# For loop
for i in range(10):
    print(i)

# While loop
while condition:
    # do something
```

---

## 📦 Data Structures

### Lists

```python
# Creating lists
fruits = ["apple", "banana", "cherry"]
numbers = [1, 2, 3, 4, 5]

# Methods
fruits.append("date")      # Add to end
fruits.insert(1, "blue")   # Insert at index
fruits.remove("banana")    # Remove item
fruits.pop()               # Remove last
fruits.sort()              # Sort list
```

### Dictionaries

```python
# Creating dictionaries
student = {
    "name": "John",
    "age": 25,
    "grade": "A"
}

# Methods
student.get("name")        # Get value
student.keys()             # Get keys
student.values()           # Get values
student.items()            # Get key-value pairs
```

### Tuples & Sets

```python
# Tuple (immutable)
coordinates = (10, 20)

# Set (unique values)
unique_numbers = {1, 2, 3, 4, 5}
```

---

## 🔢 NumPy

```python
import numpy as np

# Array creation
arr = np.array([1, 2, 3, 4, 5])
matrix = np.array([[1, 2], [3, 4]])

# Operations
np.mean(arr)           # Mean
np.std(arr)            # Standard deviation
np.sum(arr)            # Sum
np.dot(arr, arr)       # Dot product

# Array manipulation
arr.reshape(5, 1)      # Reshape
np.concatenate([a, b]) # Concatenate
```

### NumPy Functions

| Function | Description |
|----------|-------------|
| `np.array()` | Create array |
| `np.zeros()` | Array of zeros |
| `np.ones()` | Array of ones |
| `np.eye()` | Identity matrix |
| `np.linspace()` | Evenly spaced numbers |
| `np.random.rand()` | Random numbers |

---

## 🐼 Pandas

```python
import pandas as pd

# DataFrame creation
df = pd.DataFrame({
    'name': ['Alice', 'Bob', 'Charlie'],
    'age': [25, 30, 35],
    'city': ['NYC', 'LA', 'Chicago']
})

# Reading data
df = pd.read_csv('data.csv')
df = pd.read_excel('data.xlsx')

# Basic operations
df.head()              # First 5 rows
df.info()              # DataFrame info
df.describe()          # Statistics
df.shape               # Dimensions
```

### Data Selection

```python
# Select columns
df['name']             # Single column
df[['name', 'age']]    # Multiple columns

# Select rows
df.iloc[0]             # First row
df.loc[df['age'] > 25] # Conditional

# Filtering
df[df['city'] == 'NYC']
```

### Data Manipulation

```python
# Add column
df['salary'] = [50000, 60000, 70000]

# Drop column
df.drop('salary', axis=1)

# Group by
df.groupby('city').mean()

# Merge
pd.merge(df1, df2, on='id')
```

---

## 📊 Data Visualization

```python
import matplotlib.pyplot as plt
import seaborn as sns

# Line plot
plt.plot(x, y)
plt.show()

# Scatter plot
plt.scatter(x, y)
plt.show()

# Bar plot
plt.bar(categories, values)
plt.show()

# Histogram
plt.hist(data, bins=30)
plt.show()
```

---

## 🔗 Related Resources

| Resource | Link |
|----------|------|
| 🐍 Python Tutorial | [ChatWhole.com/python](https://chatwhole.com/python) |
| 📊 Statistics | [ChatWhole.com/statistics](https://chatwhole.com/statistics) |
| 🤖 Machine Learning | [ChatWhole.com/machine-learning](https://chatwhole.com/machine-learning) |

---

<p align="center">
  <a href="https://chatwhole.com">← Back to ChatWhole.com</a>
</p>
