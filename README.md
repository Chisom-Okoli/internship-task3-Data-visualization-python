# Internship-task3-Data-visualization-python
Python project demonstrating basic data visualization of the Iris dataset with bar, line, and scatter plots.

# Task 3: Basic Data Visualization

## Dataset
**Name:** Iris Dataset (`Iris.csv`)  
**Description:** A classic dataset used in machine learning and data analysis. Contains measurements of iris flowers for three species: *setosa*, *versicolor*, and *virginica*.  

**Columns:**
| Column Name    | Description                                   |
|----------------|-----------------------------------------------|
| sepal_length   | Length of the sepal (in cm)                  |
| sepal_width    | Width of the sepal (in cm)                   |
| petal_length   | Length of the petal (in cm)                  |
| petal_width    | Width of the petal (in cm)                   |
| species        | Iris species (*setosa*, *versicolor*, *virginica*) |

---

## Objectives
1. Understand the **distribution of categorical data** (species).  
2. Identify **trends in numerical features** (e.g., sepal length).  
3. Examine **relationships between numerical variables** (e.g., sepal vs petal measurements).  
4. Create visualizations that can be **exported for reports**.

---

## Plots and Visualizations

### 1. Bar Chart
**Name:** Count of Iris Species  

**Description:** Shows the number of samples for each species in the dataset.  

**Objective:** Visualize the distribution of categorical data (*species*).  

**Findings:** All three species have equal representation (50 samples each).  

```python
sns.countplot(data=df, x='species', palette='viridis')
plt.title("Count of Iris Species")
plt.xlabel("Species")
plt.ylabel("Count")
plt.tight_layout()
plt.savefig("bar_plot.png")
plt.show()
```
![Bar Plot](https://github.com/Chisom-Okoli/internship-task3-Data-visualization-python/blob/main/Bar%20chart.png)

### 2. Line Chart
**Name:** Sepal Length Across Samples 

**Description:** Plots sepal length of all samples in order of their index. 

**Objective:** Identify trends or patterns in a numeric feature (sepal_length). 

**Findings:** Sepal lengths vary across samples; no unusual outliers observed. 

```python
plt.plot(df.index, df['sepal_length'], marker='o', linestyle='-', color='blue')
plt.title("Sepal Length Across Samples")
plt.xlabel("Sample Index")
plt.ylabel("Sepal Length")
plt.tight_layout()
plt.savefig("line_chart.png")
plt.show()
```
![Line Chart](https://github.com/Chisom-Okoli/internship-task3-Data-visualization-python/blob/main/Line%20Chart.png)

### 3. Scatter Plot

**Name:** Sepal Length vs Petal Length.

**Description:** Plots the relationship between sepal length and petal length, with points colored by species.

**Objective:** Visualize correlations between two numeric features and compare species.

**Findings:** Clear clusters for each species; strong positive correlation between sepal length and petal length.

```python
sns.scatterplot(data=df, x='sepal_length', y='petal_length', hue='species', palette='deep')
plt.title("Sepal Length vs Petal Length")
plt.xlabel("Sepal Length")
plt.ylabel("Petal Length")
plt.legend(title='Species')
plt.tight_layout()
plt.savefig("scatter_plot.png")
plt.show()
```
![Scatter Plot](https://github.com/Chisom-Okoli/internship-task3-Data-visualization-python/blob/main/Scatter%20plot.png)

## Observations
- Bar plot confirms equal distribution of species.
- Line chart shows trends in sepal length across samples.
- Scatter plot reveals species clusters and strong correlation between sepal and petal lengths, which could be useful for classification.
- These plots can be directly used for analysis, reporting, or presentations.
