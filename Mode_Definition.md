# 📊 Mode Definition in Statistics

> **Mode** is defined as the value that occurs **most frequently** in a given set of data.  
> It represents the **highest frequency value** — the one that appears the greatest number of times.

---

## 🔹 Definition

A **mode** is the value that appears the most number of times in a data set.

### 🧮 Example
Given the data set:  
`2, 4, 5, 5, 6, 7`  
👉 **Mode = 5**, since it appears twice.

---

## 📘 Understanding Mode in Statistics

Statistics involves the **collection**, **presentation**, and **analysis** of data to extract meaningful insights.  
Data can be represented using:

- Tables  
- Graphs  
- Pie charts  
- Bar graphs  
- Pictorial diagrams  

After organizing data, we identify a **representative value** — a number that summarizes the entire dataset.  
This representative value is known as a **Measure of Central Tendency**.

---

## 📈 Measures of Central Tendency

These are statistical values that describe the center or typical value of a dataset.  
Common measures include:

- **Mean**
- **Median**
- **Mode**

Mode is the value around which most data points are concentrated.

---

## 🔸 Types of Mode in Data Sets

### 🟦 **1. Bimodal**
A data set with **two modes**.  

**Example:**  
Set A = `{2, 2, 2, 3, 4, 4, 5, 5, 5}`  
→ Modes = **2** and **5** (each repeated 3 times).

---

### 🟩 **2. Trimodal**
A data set with **three modes**.  

**Example:**  
Set A = `{2, 2, 2, 3, 4, 4, 5, 5, 5, 7, 8, 8, 8}`  
→ Modes = **2, 5, 8**

---

### 🟨 **3. Multimodal**
A data set with **four or more modes**.

---

## 🧾 Mode Formula for Grouped Data

In **grouped frequency distributions**, the mode cannot be identified by simple observation.  
Instead, it is determined using the **modal class** and the formula below:

\[
\text{Mode} = l + \left( \frac{f_1 - f_0}{2f_1 - f_0 - f_2} \right) \times h
\]

Where:

| Symbol | Meaning |
|:-------:|:--------|
| `l` | Lower limit of the modal class |
| `h` | Size of the class interval |
| `f₁` | Frequency of the modal class |
| `f₀` | Frequency of the class preceding the modal class |
| `f₂` | Frequency of the class succeeding the modal class |

---

## 🧠 Example Calculations

### 🧩 Example 1
Find the mode of the data set:  
`3, 3, 6, 9, 15, 15, 15, 27, 27, 37, 48`

✅ **Solution:**  
The value **15** appears the most times.  
**Mode = 15**

---

### 🧩 Example 2
Find the mode of the data set:  
`4, 4, 4, 9, 15, 15, 15, 27, 37, 48`

✅ **Solution:**  
Both **4** and **15** appear equally frequently.  
**Modes = 4 and 15**  
➡️ Hence, the data set is **bimodal**.

---

### 🧩 Example 3
Find the mode of the data set:  
`3, 6, 9, 16, 27, 37, 48`

✅ **Solution:**  
No number repeats.  
**Hence, there is no mode.**

---

### 🧩 Example 4 — Mode for Grouped Data

In a class of 30 students, the marks obtained in mathematics (out of 50) are tabulated below:

| Class Interval | Frequency |
|----------------|------------|
| 0–10 | 5 |
| 10–20 | 7 |
| 20–30 | 12 |
| 30–40 | 8 |
| 40–50 | 3 |

✅ **Solution:**

- Modal class = **20–30** (highest frequency = 12)  
- \( l = 20 \)  
- \( h = 10 \)  
- \( f_1 = 12 \)  
- \( f_0 = 7 \)  
- \( f_2 = 8 \)

\[
\text{Mode} = 20 + \left( \frac{12 - 7}{2(12) - 7 - 8} \right) \times 10
\]

\[
\text{Mode} = 20 + \left( \frac{5}{24 - 15} \right) \times 10 = 20 + \left( \frac{5}{9} \right) \times 10 = 25.56
\]

📏 **Final Answer:**  
**Mode ≈ 25.56**

---

## 🧾 Summary

| Type | Definition | Example |
|------|-------------|----------|
| **Unimodal** | One mode | {1, 2, 2, 3, 4} → 2 |
| **Bimodal** | Two modes | {1, 1, 3, 3, 4} → 1, 3 |
| **Trimodal** | Three modes | {2, 2, 4, 4, 6, 6} → 2, 4, 6 |
| **No Mode** | No repeating value | {1, 2, 3, 4, 5} |

---

### ✨ Key Takeaways

- Mode = **Most Frequent Value**
- Can be **unimodal**, **bimodal**, or **multimodal**
- For grouped data → use the **mode formula**
- Useful in categorical data where **mean/median** are less meaningful

---

> 💡 **Tip:** Mode helps identify the **most popular** or **common** category in survey and frequency data — often used in business, marketing, and data science analytics.

---

![GitHub Markdown Badge](https://img.shields.io/badge/Markdown-Stylish--GitHub--Note-blue?logo=markdown)
