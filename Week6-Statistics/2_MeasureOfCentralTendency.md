# 📘 MEASURES OF CENTRAL TENDENCY – COMPLETE PROFESSOR NOTES

---

## 1️⃣ Introduction to Central Tendency

Central tendency is a very useful and fundamental concept in statistics.  
It helps us understand the **typical**, **central**, or **most common behaviour** of data in a dataset.

Instead of analysing every individual data point, we use measures of central tendency to **summarise large datasets into a single representative value**, making it easier to compare and interpret data.

---

## 2️⃣ Business Motivation: Why Central Tendency Matters

Consider the employee specifics of a particular company.

### ❓ Question 1: Departmental Efficiency  
How do we measure **which department is the most efficient** in terms of **revenue generated with the least expenditure**, so that the department can be rewarded?

### ❓ Question 2: Compensation Planning  
How do we calculate a **representative compensation** for designations in a department so that the HR team can offer **competitive salaries** while recruiting new employees?

### ❓ Question 3: Attrition Analysis  
How does the company find the **typical age group most prone to attrition**, so that preventive measures can be taken?

✅ **Answer (Common Explanation):**  
In all the above cases, finding the **central tendency of the data** helps the company take **important managerial decisions**.

---

## 3️⃣ Central Tendency in Practice (HR Dataset Example)

### Given Dataset Fields:
- Employee ID  
- Name  
- Department  
- Compensation  
- Performance Rating  

### ❓ Question:
If the HR head asks:

> *“Find the typical performance rating of employees in the Sales department.”*

### ✅ Solution Steps:
1. Subset the dataset to include **only Sales department employees**
2. Calculate the **mean of their performance ratings**
3. Report this value as a **summary indicator** to management

---

## 4️⃣ Measures of Central Tendency

The three most commonly used measures of central tendency are:

- **Mean**
- **Median**
- **Mode**

We mainly focus on **Mean** and its variations:

- Arithmetic Mean  
- Geometric Mean  
- Harmonic Mean  

---

## 5️⃣ Arithmetic Mean (AM)

### Definition

The Arithmetic Mean is calculated by adding all the values in a dataset and dividing by the total number of observations.

In everyday usage, *average* usually refers to the Arithmetic Mean.  
However, in statistics, *average* may also refer to Median or Mode.

---

### Formula

If we have `n` observations:

$
\mu = \frac{x_1 + x_2 + x_3 + \cdots + x_n}{n}
$

Or,

$
\mu = \frac{\sum x_i}{n}
$

---

### When Arithmetic Mean Works Best
- Data values are similar  
- Data is symmetric  
- No extreme outliers  

---

### Example Dataset

| EmployeeID | Name | Compensation | Department | Performance Rating |
|----------|------|--------------|------------|--------------------|
| 101 | John | 60000 | Sales | 4.5 |
| 102 | Jane | 75000 | Sales | 4.0 |
| 103 | Mike | 50000 | HR | 3.5 |
| 104 | Anna | 80000 | Sales | 4.8 |

---

### ❓ Question:
What is the **mean compensation** of all employees?

### ✅ Solution:
$
\frac{60000 + 75000 + 50000 + 80000}{4} = 66250
$

---

## 6️⃣ Mean Using Frequency Distribution

### Formula

$
\mu = \frac{\sum (x_i f_i)}{N}
$

Where:
- \(x_i\) = value  
- \(f_i\) = frequency  
- \(N = \sum f_i\)

---

### Example: Movie Rating Dataset (Thor)

| Rating | Frequency |
|------|-----------|
| 5 | 10 |
| 4 | 15 |
| 3 | 25 |
| 2 | 30 |

### ❓ Question:
Find the **mean movie rating**.

### ✅ Solution:
1. Total observations:  
   $
   N = 10 + 15 + 25 + 30 = 80
   $

2. Weighted sum:  
   $
   (5×10) + (4×15) + (3×25) + (2×30) = 245
   $

3. Mean rating:  
   $
   \mu = \frac{245}{80} = 3.06
   $

---

## 9️⃣ Geometric Mean (GM)

### Definition

Geometric Mean is used for **multiplicative data**, such as:
- Growth rates  
- Returns  
- Ratios  

### Formula

$
GM = (x_1 x_2 \cdots x_n)^{1/n}
$

---

### Example: Revenue Growth Rates

### ❓ Question:
Revenue growth rates are 10%, 20%, and 30%. Find the **Geometric Mean growth rate**.

### ✅ Solution:
$
(1.10 × 1.20 × 1.30)^{1/3} - 1 = 18.17\%
$

---

## 🔟 Why Arithmetic Mean Fails for Growth Rates

### Example Dataset

| Year | Revenue |
|----|---------|
| 1 | 1000 |
| 2 | 1100 |
| 3 | 990 |

### Arithmetic Mean Growth:
$
\frac{10\% + (-10\%)}{2} = 0\%
$

### Geometric Mean Growth:
$
(1.10 × 0.90)^{1/2} - 1 = -0.501\%
$

✅ GM reflects actual decline.

---

## 1️⃣1️⃣ Doubling Sales in 5 Years

### ❓ Question:
What YoY growth rate is required to **double sales in 5 years**?

### ✅ Solution (Geometric Mean):
$
(2)^{1/5} - 1 = 14.87\%
$

❌ Arithmetic Mean Estimate:
$
100\% / 5 = 20\%
$

---

## 1️⃣2️⃣ Harmonic Mean (HM)

### Definition

Harmonic Mean is used for **rates or ratios** such as speed and efficiency.

### Formula

$
HM = \frac{n}{\sum (1/x_i)}
$

---

### Example: Speed Data (60, 80, 100)

### ✅ Solution:
$
HM = \frac{3}{0.03917} = 76.58 \text{ km/h}
$

---

### Classic Example

Forward speed = 60 km/h  
Return speed = 120 km/h  

- AM = 90 ❌  
- HM = 80 ✅  

---

# 📘 QUIZ – MEASURES OF CENTRAL TENDENCY

---

## ✅ QUIZ 1: Arithmetic Mean (Simple Data)

### Question  
The populations of five countries are given below:

- Cambodia: 16,789,909  
- Indonesia: 17,272,322  
- Malaysia: 3,234,322  
- Maldives: 234,234,324  
- Thailand: 23,323,434  

Find the **mean population** of these five countries.

### Solution  

$
\text{Mean Population} = \frac{16789909 + 17272322 + 3234322 + 234234324 + 23323434}{5}
$

$
= \frac{307108311}{5} = 61,421,662.2
$

**Mean Population = 61,421,662.2**

---

## ✅ QUIZ 2: Arithmetic Mean with Frequency

### Question  
An insurance analyst wants to find the **mean age** of people who purchased a medical insurance policy.  
The age distribution is:

- 13 people are 25 years old  
- 12 people are 28 years old  
- 20 people are 30 years old  

Find the **mean age** of the insurers.  
*(Round your answer to the nearest whole number.)*

### Solution  

$
\text{Mean Age} = \frac{(25 × 13) + (28 × 12) + (30 × 20)}{13 + 12 + 20}
$

$
= \frac{325 + 336 + 600}{45} = \frac{1261}{45} = 28
$

**Mean Age = 28 years**

---

## ✅ QUIZ 3: Geometric Mean (Company Revenue Growth)

### Question  
A company’s revenue grew by:

- 15% in Year 1  
- 25% in Year 2  
- 10% in Year 3  

Find the **geometric mean growth rate** over the three years.

### Solution  

Convert percentages to decimals:

$
0.15,\; 0.25,\; 0.10
$

$
GM = (0.15 × 0.25 × 0.10)^{1/3}
$

$
= (0.00375)^{1/3} ≈ 0.156
$

**Geometric Mean Growth Rate ≈ 15.6%**

---

## ✅ QUIZ 4: Geometric Mean (Portfolio Return)

### Question  
An investor’s portfolio generated the following annual returns:

- 8%  
- 12%  
- 20%  

Find the **geometric mean return** of the portfolio.

### Solution  

Convert percentages to decimals:

$
0.08,\; 0.12,\; 0.20
$

$
GM = (0.08 × 0.12 × 0.20)^{1/3}
$

$
≈ 0.123
$

**Geometric Mean Return ≈ 12.3%**

---

## ✅ QUIZ 5: Harmonic Mean (Car Speed)

### Question  
A car travels the same distance at speeds of:

- 50 km/h  
- 70 km/h  
- 90 km/h  

Find the **harmonic mean speed**.

### Solution  

$
HM = \frac{3}{(1/50 + 1/70 + 1/90)}
$

$
= \frac{3}{0.02 + 0.01429 + 0.01111}
$

$
= \frac{3}{0.0454} ≈ 66.08
$

**Harmonic Mean Speed ≈ 66.08 km/h**

---

## ✅ QUIZ 6: Harmonic Mean (Machine Speed)

### Question  
A machine operates at speeds of:

- 40 units/hour  
- 60 units/hour  
- 80 units/hour  

Find the **harmonic mean speed** of the machine.

### Solution  

$
HM = \frac{3}{(1/40 + 1/60 + 1/80)}
$

$
= \frac{3}{0.025 + 0.01667 + 0.0125}
$

$
≈ 55.42
$

**Harmonic Mean Speed ≈ 55.42 units/hour**

---


## ✅ Final Summary

- Central tendency simplifies large data  
- Mean, Median, Mode serve different purposes  
- Arithmetic Mean → general data  
- Geometric Mean → growth & compounding  
- Harmonic Mean → rates & efficiency  
- **Correct measure = correct decision**

---

# 📘 MEASURES OF CENTRAL TENDENCY  
## ✅ MEDIAN AND MODE — PROFESSOR STYLE NOTES

---

## 🔷 MEDIAN

### 📌 Introduction

Consider any company you are familiar with. The compensation of employees such as an intern, a junior assistant, a senior assistant, a manager, and the CEO usually varies widely. The CEO’s salary is typically much higher than that of other employees.

If we attempt to estimate the *average* salary using the **mean**, the result will be misleading because the extremely high CEO salary pulls the mean upward. In such situations, we require a measure of central tendency that better represents the *typical* value of the dataset.  
This measure is known as the **median**.

---

### 📖 Definition

> **Median** is the middle value of a dataset after arranging the data in ascending or descending order.  
- If the number of observations is **odd**, the median is the middle value.  
- If the number of observations is **even**, the median is the average of the two middle values.

---

### ✍️ Example: Employee Compensation

| Name     | Compensation |
|----------|--------------|
| Anjali   | 30,000       |
| Ravi     | 35,000       |
| Gita    | 32,000       |
| Sita    | 40,000       |
| Vikram  | 45,000       |
| Lalita  | 50,000       |
| Sabaria | 1,000,000    |

**Mean Compensation**

\[
\frac{30,000 + 35,000 + 32,000 + 40,000 + 45,000 + 50,000 + 1,000,000}{7}
= 185,142.86
\]

**Median Compensation**

After sorting:  
30,000, 32,000, 35,000, **40,000**, 45,000, 50,000, 1,000,000

Median = **40,000**

✅ The **median** gives a more realistic idea of typical employee salary than the mean.

---

### 📌 Why Median is Important

- Resistant to **outliers**
- Suitable for **skewed data**
- Represents the **central tendency** more accurately in real-world scenarios

---

### 🧮 Steps to Calculate the Median

1. Arrange the data in ascending order.
2. Let the total number of observations be `n`.
3. If `n` is odd → Median = value at position \((n + 1)/2\).
4. If `n` is even → Median = average of values at positions \(n/2\) and \((n/2)+1\).

---

### ✅ Example (Odd Number of Observations)

Heights (cm): 150, 160, 170, 180, 190  
Sorted: 150, 160, **170**, 180, 190  

Median = **170 cm**

---

### ✅ Example (Even Number of Observations)

Heights (cm): 150, 160, 170, 180, 190, 200  
Median = \((170 + 180)/2 = 175\) cm

---

### 📝 Quiz Question (Solved)

**Problem:**  
Amitabh spends the following amounts (in ₹):  
4000, 1200, 750, 9000, 15600, 4400, 6600

**Solution:**

Sorted data:  
750, 1200, 4000, **4400**, 6600, 9000, 15600  

Number of observations = 7 (odd)

Median position = \((7 + 1)/2 = 4\)

✅ **Median = 4400**

---

### ✅ Concept Check

**Statement:**  
“If all the values of a dataset are increased by 5, the median will also increase by 5.”

✅ **True**  
Adding a constant shifts all values equally without changing their order.

---

## 🔷 MODE

### 📖 Definition

> **Mode** is the value that occurs **most frequently** in a dataset.

A dataset may be:
- **Unimodal** → one mode  
- **Bimodal** → two modes  
- **Multimodal** → more than two modes  
- **No mode** → all values occur only once

---

### ✍️ Example: Preferred Cuisine

| Name    | Cuisine  |
|---------|----------|
| Anjali  | Italian  |
| Ravi   | Indian   |
| Gita   | Italian  |
| Sita   | Mexican  |
| Vikram | Indian   |
| Lalita | Italian  |
| Sabaria| Chinese  |
| Neha   | Indian   |
| Raj    | Mexican  |
| Sonal  | Indian   |

**Frequency Table**

| Cuisine  | Frequency |
|---------|-----------|
| Italian | 3         |
| Indian  | 4         |
| Mexican| 2         |
| Chinese| 1         |

✅ **Mode = Indian**

---

### ✅ Bimodal Distribution Example

| Cuisine | Frequency |
|--------|-----------|
| Italian| 4         |
| Indian | 4         |
| Others | 1 each    |

✅ Modes: **Italian and Indian**  
➡️ Bimodal distribution

---

### ✅ Multimodal Distribution Example

| Number of Athletes | Frequency |
|-------------------|-----------|
| 1000              | 2         |
| 1500              | 2         |
| 2000              | 2         |
| 2500              | 2         |

✅ Modes: 1000, 1500, 2000, 2500  
➡️ Multimodal distribution

---

### ✅ Sports Example: Goals Scored

| Goals | Frequency |
|-------|-----------|
| 0     | 3         |
| 1     | 6         |
| 2     | 4         |
| 3     | 3         |
| 5     | 1         |

✅ **Mode = 1**

---

### ✅ Bimodal Example (Customers)

| Time Slot       | Customers |
|----------------|------------|
| 11–12          | 30         |
| 12–1           | 25         |
| 1–2            | 15         |
| 2–3            | 30         |
| 3–4            | 15         |

✅ Modes at **11–12** and **2–3** → Bimodal distribution

---

### ✅ Multimodal Example: Don Bradman’s Scores

Modes: **83, 85, 87, 111, 134**

➡️ Multimodal distribution  
➡️ Indicates certain scores were repeated frequently.

---

### 📝 Mode Recall Quiz (Solved)

**Data:** 1, 2, 3, 14, 14, 18, 14, 15, 18, 17

| Number | Frequency |
|--------|-----------|
| 14     | 3         |
| 18     | 2         |

✅ **Mode = 14**

---

### ✅ Letter Mode Example

Word: **MATHEMATICS**

| Letter | Frequency |
|--------|-----------|
| M      | 2         |
| A      | 2         |
| T      | 2         |

✅ Modal letters: **M, A, T**

