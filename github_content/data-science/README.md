# 📈 Data Science

<p align="center">
  <img src="data-science-cheat-sheet.svg" alt="Data Science Cheat Sheet" width="100%">
</p>

## 📚 Table of Contents

1. [Data Science Pipeline](#data-science-pipeline)
2. [Data Collection](#data-collection)
3. [Data Cleaning](#data-cleaning)
4. [Exploratory Data Analysis](#exploratory-data-analysis)
5. [Feature Engineering](#feature-engineering)

---

## 🔄 Data Science Pipeline

### Complete Workflow

```
Business Understanding → Data Collection → Data Cleaning → 
Feature Engineering → Model Building → Evaluation → Deployment
```

### Key Skills

| Skill | Tools | Importance |
|-------|-------|------------|
| **Statistics** | R, Python | Foundation |
| **Programming** | Python, SQL | Essential |
| **Data Wrangling** | Pandas, NumPy | Critical |
| **Visualization** | Matplotlib, Seaborn | Important |
| **Machine Learning** | Scikit-learn, TensorFlow | Advanced |
| **Communication** | Jupyter, Tableau | Essential |

---

## 📥 Data Collection

### Data Sources

| Source | Type | Tools |
|--------|------|-------|
| **Databases** | Structured | SQL, SQLAlchemy |
| **APIs** | Semi-structured | requests, REST |
| **Web Scraping** | Unstructured | BeautifulSoup, Scrapy |
| **Files** | Various | Pandas, CSV, Excel |
| **Streaming** | Real-time | Kafka, Spark |

### Python for Data Collection

```python
# From CSV
import pandas as pd
df = pd.read_csv('data.csv')

# From Database
import sqlalchemy
engine = sqlalchemy.create_engine('postgresql://user:pass@host/db')
df = pd.read_sql('SELECT * FROM table', engine)

# From API
import requests
response = requests.get('https://api.example.com/data')
data = response.json()

# Web Scraping
from bs4 import BeautifulSoup
soup = BeautifulSoup(html, 'html.parser')
```

---

## 🧹 Data Cleaning

### Common Issues

| Issue | Solution | Code |
|-------|----------|------|
| **Missing Values** | Imputation | `df.fillna()` |
| **Duplicates** | Removal | `df.drop_duplicates()` |
| **Outliers** | Detection & Treatment | IQR, Z-score |
| **Inconsistent Types** | Conversion | `df.astype()` |
| **Invalid Data** | Filtering | `df[df['col'] > 0]` |

### Missing Value Strategies

```python
# Remove rows with missing values
df.dropna()

# Fill with mean/median/mode
df.fillna(df.mean())
df.fillna(df.median())
df.fillna(df.mode().iloc[0])

# Forward/Backward fill
df.fillna(method='ffill')
df.fillna(method='bfill')

# Interpolation
df.interpolate()
```

### Outlier Detection

```python
# IQR Method
Q1 = df['col'].quantile(0.25)
Q3 = df['col'].quantile(0.75)
IQR = Q3 - Q1
lower = Q1 - 1.5 * IQR
upper = Q3 + 1.5 * IQR
df_clean = df[(df['col'] >= lower) & (df['col'] <= upper)]

# Z-score Method
from scipy import stats
z_scores = stats.zscore(df['col'])
df_clean = df[abs(z_scores) < 3]
```

---

## 🔍 Exploratory Data Analysis (EDA)

### EDA Checklist

1. **Understand Structure**
   - Shape, dtypes, head/tail

2. **Univariate Analysis**
   - Distributions, statistics

3. **Bivariate Analysis**
   - Correlations, relationships

4. **Multivariate Analysis**
   - Patterns, clusters

### Python EDA Tools

```python
# Basic info
df.shape
df.info()
df.describe()
df.head()

# Distributions
df['col'].hist()
sns.histplot(df['col'], kde=True)

# Correlations
df.corr()
sns.heatmap(df.corr(), annot=True)

# Relationships
sns.scatterplot(x='col1', y='col2', data=df)
sns.pairplot(df)
```

---

## 🔧 Feature Engineering

### Techniques

| Technique | Description | Example |
|-----------|-------------|---------|
| **Scaling** | Normalize ranges | StandardScaler |
| **Encoding** | Convert categories | OneHotEncoder |
| **Binning** | Group values | pd.cut() |
| **Log Transform** | Reduce skewness | np.log1p() |
| **Polynomial** | Create interactions | PolynomialFeatures |
| **Date Features** | Extract components | year, month, day |

### Encoding Methods

```python
# Label Encoding
from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
df['col_encoded'] = le.fit_transform(df['col'])

# One-Hot Encoding
df_encoded = pd.get_dummies(df, columns=['col'])

# Target Encoding
from category_encoders import TargetEncoder
te = TargetEncoder()
df['col_encoded'] = te.fit_transform(df['col'], df['target'])
```

---

## 📊 Model Building

### ML Workflow

```python
# Import libraries
from sklearn.model_selection import train_test_split
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import accuracy_score, classification_report

# Split data
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)

# Train model
model = RandomForestClassifier()
model.fit(X_train, y_train)

# Predict
y_pred = model.predict(X_test)

# Evaluate
print(f"Accuracy: {accuracy_score(y_test, y_pred):.2f}")
print(classification_report(y_test, y_pred))
```

---

## 🎯 Data Science Tools

### Essential Libraries

| Category | Library | Purpose |
|----------|---------|---------|
| **Data Manipulation** | Pandas | DataFrames |
| **Numerical** | NumPy | Arrays |
| **Visualization** | Matplotlib | Basic plots |
| **Statistical** | Seaborn | Statistical plots |
| **ML** | Scikit-learn | Machine learning |
| **Deep Learning** | TensorFlow/PyTorch | Neural networks |
| **NLP** | NLTK/spaCy | Text processing |

---

## 🔗 Related Resources

| Resource | Link |
|----------|------|
| 📈 Data Science Tutorial | [ChatWhole.com/data-science](https://chatwhole.com/data-science) |
| 🐍 Python for Data Science | [ChatWhole.com/python](https://chatwhole.com/python) |
| 📊 Statistics | [ChatWhole.com/statistics](https://chatwhole.com/statistics) |
| 🤖 Machine Learning | [ChatWhole.com/machine-learning](https://chatwhole.com/machine-learning) |

---

<p align="center">
  <a href="https://chatwhole.com">← Back to ChatWhole.com</a>
</p>
