# 📊 Statistics in Data Science

> **Statistics** is the science of **collecting, analyzing, interpreting, and presenting data** to uncover meaningful patterns and make informed decisions.  
> In **Data Science**, statistics serves as the **backbone** for understanding data, validating models, and making reliable predictions.



# ⚖️ Measures of Central Tendency

> These measures describe the **center** or **typical value** of a dataset.  
> The three main measures are **Mean**, **Median**, and **Mode**.

---

## 🧮 1. Mean (Arithmetic Average)

**Definition:**  
The arithmetic mean is the simplest and most widely used measure of a mean, or average. It simply involves taking the sum of a group of values and then dividing by the total number of values.
The formula for the arithmetic mean is:

$$ \bar{x} = \frac{x_1 + x_2 + \dots + x_n}{n} = \frac{1}{n} \sum_{i=1}^{n} x_i $$
\[ 
\text{Mean } (\mu) = \frac{\sum X}{n}
\]

**Example:**
```text
Data: 10, 15, 20, 25, 30  
Mean = (10 + 15 + 20 + 25 + 30) / 5 = 20
```

**Key Points:**
- Represents the average value.
- Sensitive to **outliers**.
- Commonly used for **average income, temperature, or marks**.

---

## ⚖️ 2. Median

**Definition:**  
The **median**, in statistics, is the middle value of the given list of data when arranged in an order. The order of data or observations can be made either in ascending order or descending order. .

- **Odd number of values:** Middle value  
- **Even number of values:** Average of two middle values  

**Examples:**
```text
Odd Data: 12, 14, 18, 20, 22 → Median = 18  
Even Data: 10, 20, 30, 40 → Median = (20 + 30)/2 = 25
```

**Key Points:**
- Not affected by **extreme values**.
- Ideal for **skewed datasets** (e.g., income, property prices).

---

## 🔁 3. Mode

**Definition:**  
A **mode** is defined as the value that has a higher frequency in a given set of values. It is the value that appears the most number of times. 

**Example:**
```text
Data: 4, 5, 6, 6, 7, 8, 9 → Mode = 6
```

**Key Points:**
### Bimodal, Trimodal & Multimodal (More than one mode)
  - When there are two modes in a data set, then the set is called bimodal
     For example, The mode of Set A = {2,2,2,3,4,4,5,5,5} is 2 and 5, because both 2 and 5 is repeated three times in the given set.

- When there are three modes in a data set, then the set is called trimodal
    For example, the mode of set A = {2,2,2,3,4,4,5,5,5,7,8,8,8} is 2, 5 and 8

- When there are four or more modes in a data set, then the set is called multimodal

### 📊 Mean, Median, and Mode Comparison

| **Measure** | **Description** | **Example** |
|:-------------|:----------------|:-------------|
| **Mean** | Mean is the average value obtained by dividing the sum of all values by the total number of values.<br><br>**Formula:**<br>Mean = (Sum of Observations) / (Number of Observations) | For the dataset **{2, 2, 3, 4, 5}**:<br>Mean = (2 + 2 + 3 + 4 + 5) / 5 = **3.2** |
| **Median** | The median is the central value of a dataset when arranged in ascending or descending order. | For the dataset **{2, 2, 3, 4, 5}**:<br>Median = **3** |
| **Mode** | The mode is the value that appears most frequently in a dataset. | For the dataset **{2, 2, 3, 4, 5}**:<br>Mode = **2** |


---

# 🌈 Measures of Dispersion

> While central tendency tells us where data centers, **dispersion** tells us how much it **varies** or **spreads out**.

---

## 📏 1. Range

**Definition:**  
Difference between the **maximum** and **minimum** values.

\[
\text{Range} = \text{Max} - \text{Min}
\]

**Example:**
```text
Data: 10, 12, 18, 20, 25 → Range = 25 - 10 = 15
```

⚠️ *Highly affected by outliers.*

---

## 🔢 2. Variance (σ²)

**Definition:**  
Variance measures how far each value is from the mean — it’s the **average squared deviation**.

\[
σ^2 = \frac{\sum (X - \mu)^2}{n}
\]

**Example:**
```text
Data: 2, 4, 6  
Mean = 4  
Variance = [(2−4)² + (4−4)² + (6−4)²] / 3 = 2.67
```

📖 *Higher variance = greater spread of data.*

---

## 📉 3. Standard Deviation (σ)

**Definition:**  
Square root of variance — indicates the **average distance** of data points from the mean.

\[
σ = \sqrt{\frac{\sum (X - \mu)^2}{n}}
\]

**Example:**
```text
From the previous example:  
σ = √2.67 ≈ 1.63
```

✅ *Widely used in finance, education, and research.*

---

## 📊 4. Interquartile Range (IQR)

**Definition:**  
The range of the **middle 50%** of data. Less sensitive to extreme values.

\[
\text{IQR} = Q3 - Q1
\]

**Steps:**
1. Sort data.  
2. Find Q1 (25th percentile).  
3. Find Q3 (75th percentile).  
4. Subtract Q1 from Q3.

**Example:**
```text
Data: 5, 7, 8, 12, 13, 14, 18, 21, 23  
Q1 = 8, Q3 = 18  
IQR = 18 − 8 = 10
```

---

## 🧭 5. Quartiles

| Quartile | Meaning | Percentile |
|-----------|----------|-------------|
| Q1 | Median of lower half | 25th |
| Q2 | Median of full dataset | 50th |
| Q3 | Median of upper half | 75th |

**Example:**  
If student scores are sorted,  
Q1 = score below which 25% of students scored.

---

## 📐 6. Mean Absolute Deviation (MAD)

**Definition:**  
Average of the absolute deviations from the mean.

\[
\text{MAD} = \frac{\sum |X - \mu|}{n}
\]

**Example:**
```text
Data: 3, 6, 9  
Mean = 6  
MAD = (|3−6| + |6−6| + |9−6|)/3 = 2
```

💡 *Easier to interpret than variance and less affected by extreme values.*

---

# 🧾 Summary Table

| Measure | Formula | Description | Outlier Sensitivity |
|----------|----------|-------------|----------------------|
| **Mean** | ΣX / n | Arithmetic average | ✅ Yes |
| **Median** | Middle value | Resistant to extremes | ❌ No |
| **Mode** | Most frequent value | Useful for categorical data | ❌ No |
| **Range** | Max − Min | Simplest measure of spread | ✅ Yes |
| **Variance** | Σ(X−μ)² / n | Average squared deviation | ✅ Yes |
| **Standard Deviation** | √Variance | Avg. distance from mean | ✅ Yes |
| **IQR** | Q3 − Q1 | Spread of middle 50% | ❌ No |
| **MAD** | Σ|X−μ| / n | Avg. absolute deviation | ❌ No |

---

### 🎯 Key Takeaway

> 📌 **Central tendency** gives you the *typical value*,  
> while **dispersion** tells you how *consistent or variable* your data is.  
> Together, they form the foundation of **descriptive statistics** — a core skill in data science.

---

**💻 Next Step:**  
Want to visualize these concepts?  
Try plotting them in Python using libraries like **NumPy**, **Pandas**, and **Matplotlib** to see how data distribution affects these measures.

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

data = [10, 15, 20, 25, 30]
print("Mean:", np.mean(data))
print("Median:", np.median(data))
print("Mode:", pd.Series(data).mode()[0])
plt.hist(data, bins=5, color='skyblue', edgecolor='black')
plt.title("Data Distribution")
plt.xlabel("Values")
plt.ylabel("Frequency")
plt.show()
```

---

✨ *By mastering these measures, you build the foundation for advanced data science techniques like machine learning, predictive modeling, and statistical inference.*
