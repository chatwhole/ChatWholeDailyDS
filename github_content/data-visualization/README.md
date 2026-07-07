# 📊 Data Visualization

<p align="center">
  <img src="dataviz-cheat-sheet.svg" alt="Data Visualization Cheat Sheet" width="100%">
</p>

## 📚 Table of Contents

1. [Chart Types](#chart-types)
2. [Matplotlib](#matplotlib)
3. [Seaborn](#seaborn)
4. [Plotly](#plotly)
5. [Best Practices](#best-practices)

---

## 📈 Chart Types

### When to Use Each Chart

| Chart Type | Best For | Data Type |
|------------|----------|-----------|
| **Line Chart** | Trends over time | Continuous |
| **Bar Chart** | Comparing categories | Categorical |
| **Histogram** | Distribution | Continuous |
| **Scatter Plot** | Relationships | Continuous |
| **Pie Chart** | Parts of whole | Categorical |
| **Box Plot** | Distribution & outliers | Continuous |
| **Heatmap** | Correlations | Matrix |
| **Area Chart** | Cumulative trends | Continuous |

### Chart Selection Guide

```
What's your goal?
├── Compare values → Bar Chart
├── Show distribution → Histogram/Box Plot
├── Show relationship → Scatter Plot
├── Show trend over time → Line Chart
├── Show composition → Pie/Stacked Bar
└── Show correlation → Heatmap
```

---

## 🎨 Matplotlib

### Basic Plots

```python
import matplotlib.pyplot as plt

# Line plot
plt.plot(x, y)
plt.title('Title')
plt.xlabel('X Label')
plt.ylabel('Y Label')
plt.show()

# Scatter plot
plt.scatter(x, y, c=colors, s=sizes)
plt.colorbar()
plt.show()

# Bar plot
plt.bar(categories, values)
plt.xticks(rotation=45)
plt.show()

# Histogram
plt.hist(data, bins=30, edgecolor='black')
plt.show()
```

### Subplots

```python
# Create subplots
fig, axes = plt.subplots(2, 2, figsize=(10, 8))

# Plot in each subplot
axes[0, 0].plot(x1, y1)
axes[0, 1].scatter(x2, y2)
axes[1, 0].bar(categories, values)
axes[1, 1].hist(data, bins=30)

plt.tight_layout()
plt.show()
```

### Customization

```python
# Figure size
plt.figure(figsize=(12, 6))

# Colors
plt.plot(x, y, color='#ff6b6b', linewidth=2, linestyle='--')

# Markers
plt.plot(x, y, marker='o', markersize=8)

# Grid
plt.grid(True, alpha=0.3)

# Legend
plt.legend(['Label 1', 'Label 2'])

# Save figure
plt.savefig('plot.png', dpi=300, bbox_inches='tight')
```

---

## 🌊 Seaborn

### Statistical Plots

```python
import seaborn as sns

# Distribution plot
sns.histplot(data, kde=True)

# Box plot
sns.boxplot(x='category', y='value', data=df)

# Violin plot
sns.violinplot(x='category', y='value', data=df)

# Count plot
sns.countplot(x='category', data=df)
```

### Relationship Plots

```python
# Scatter plot with regression
sns.lmplot(x='x', y='y', data=df)

# Pair plot
sns.pairplot(df, hue='category')

# Joint plot
sns.jointplot(x='x', y='y', data=df, kind='hex')
```

### Heatmap

```python
# Correlation heatmap
correlation_matrix = df.corr()
sns.heatmap(correlation_matrix, annot=True, cmap='coolwarm')

# Custom heatmap
sns.heatmap(data, 
            annot=True, 
            fmt='.2f', 
            cmap='viridis',
            center=0,
            square=True)
```

---

## 📊 Plotly

### Interactive Plots

```python
import plotly.express as px
import plotly.graph_objects as go

# Scatter plot
fig = px.scatter(df, x='x', y='y', color='category')
fig.show()

# Line plot
fig = px.line(df, x='date', y='value', color='series')
fig.show()

# Bar chart
fig = px.bar(df, x='category', y='value', color='category')
fig.show()
```

### Subplots

```python
from plotly.subplots import make_subplots

fig = make_subplots(
    rows=2, cols=2,
    subplot_titles=('Plot 1', 'Plot 2', 'Plot 3', 'Plot 4')
)

fig.add_trace(go.Scatter(x=x, y=y), row=1, col=1)
fig.add_trace(go.Bar(x=x, y=y), row=1, col=2)
fig.add_trace(go.Scatter(x=x, y=y), row=2, col=1)
fig.add_trace(go.Bar(x=x, y=y), row=2, col=2)

fig.show()
```

---

## ✅ Best Practices

### Design Principles

| Principle | Description |
|-----------|-------------|
| **Simplicity** | Remove chart junk |
| **Clarity** | Label everything |
| **Accuracy** | Don't mislead |
| **Aesthetics** | Use colors wisely |

### Color Palettes

```python
# Seaborn palettes
sns.color_palette("viridis")
sns.color_palette("plasma")
sns.color_palette("deep")

# Custom colors
colors = ['#ff6b6b', '#4ecdc4', '#45b7d1', '#96ceb4', '#ffeaa7']
```

### Common Mistakes to Avoid

1. **3D charts** - Hard to read, use 2D instead
2. **Pie charts** - Use bar charts for comparison
3. **Truncated axes** - Can be misleading
4. **Too many colors** - Stick to 5-7 colors max
5. **Missing labels** - Always label axes and title

---

## 🔗 Related Resources

| Resource | Link |
|----------|------|
| 📊 Data Visualization Tutorial | [ChatWhole.com/data-visualization](https://chatwhole.com/data-visualization) |
| 🐍 Python for Visualization | [ChatWhole.com/python](https://chatwhole.com/python) |
| 📈 Data Science | [ChatWhole.com/data-science](https://chatwhole.com/data-science) |

---

<p align="center">
  <a href="https://chatwhole.com">← Back to ChatWhole.com</a>
</p>
