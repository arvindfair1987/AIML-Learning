# 📘 Measures of Position (Quantiles) – Professor Notes

---

## 1️⃣ Introduction to Measures of Position

In many real-world situations, **averages alone are not sufficient** to understand how data is distributed.  
**Measures of position** (also called **measures of location or ranking**) help us understand **where a particular value stands relative to the rest of the data**.

### 📌 Motivating Example: Employee Compensation

Consider a company with **2,000 employees**.  
Employees at the **entry level** receive much lower compensation compared to senior executives such as the **CEO or Managing Director (MD)**.

If we only compute the **mean salary**, it may be misleading because a few very high salaries can distort the average.

👉 To meaningfully analyze such data, we need to:
- Divide salaries into **brackets**
- Identify **low, middle, and high compensation groups**
- Retain information about **how many employees fall into each group**

This is exactly where **measures of position** become useful.

---

## 2️⃣ Concept of Quantiles

To gain insight into a dataset using measures of position, we divide the **ordered data** into **equal-sized parts**.

### 🔹 Definition: Quantile

> A **quantile** is a value that divides a dataset into **equal-sized, adjacent subgroups** after the data has been arranged in ascending or descending order.

- Each subgroup contains (approximately) the **same number of observations**
- Quantiles help us understand **relative standing**, not just central tendency

---

## 3️⃣ Visual Intuition (Conceptual Explanation)

If three dividing points split the data into **four equal parts**, then:
- The data is divided into **four groups**
- The dividing points are called **quantiles**
- These specific quantiles are known as **quartiles**

Thus:
- **Number of parts = 4**
- **Number of quantile cut-points = 3**

> ⚠️ Important: Quantiles refer to the **cut-points**, not the groups themselves.

---

## 4️⃣ Introduction to Quantiles (Corrected)

### ❌ Common Misconception
Quantiles **do NOT** give the total number of observations.

### ✅ Correct Definition

> **Quantiles divide a dataset into equal-sized groups**, based on the **rank or position** of observations.

---

## 5️⃣ Example Dataset: Employee Compensation

Consider the compensation details of employees in a company.

| Employee ID | Name  | Compensation |
|-------------|-------|--------------|
| 101         | Asha  | 25000        |
| 102         | Ravi  | 30000        |
| 103         | Neha  | 35000        |
| 104         | Kiran | 45000        |
| 105         | Meera | 60000        |
| 106         | Arjun | 90000        |


---

## 6️⃣ The Statistical Question

### ❓ Key Questions
- How do we **statistically decide** whether a given compensation is **low or high**?
- Can we **systematically divide** employees into compensation brackets?
- Can we retain information about **how many employees fall in each bracket**?

---

## 7️⃣ Role of the Median (A Special Quantile)

One familiar measure of position is the **median**.

### 🔹 Definition: Median
> The **median** is the value that divides the dataset into **two equal parts** when the data is ordered.

### 📌 Median Calculation (Example)

Ordered compensations:
```

25,000, 30,000, 35,000, 45,000, 60,000, 90,000

```

Since there are **6 observations**, the median is the average of the third and fourth values:

\[
\text{Median} = \frac{35,000 + 45,000}{2} = 40,000
\]

---

## 8️⃣ Interpretation Using the Median

- **50% of employees earn ≤ ₹40,000**
- **50% of employees earn ≥ ₹40,000**

### 📊 Statistical Inference
- Compensation **below the median** → *relatively low*
- Compensation **above the median** → *relatively high*

However, the median only gives **two groups**.  
To gain **finer insights**, we need more quantiles.

---

## 9️⃣ Common Types of Quantiles

Quantiles can divide data into different numbers of equal parts:

| Measure      | Number_of_Parts | Description                           |
|--------------|------------------|---------------------------------------|
| Median       | 2                | Splits data into two equal halves     |
| Tertiles     | 3                | Divide data into three equal parts    |
| Quartiles    | 4                | Divide data into four equal parts     |
| Deciles      | 10               | Divide data into ten equal parts      |
| Percentiles  | 100              | Divide data into a hundred equal parts  |
---

## 🔟 Why Measures of Position Matter

Measures of position help us:
- Identify **low, medium, and high values**
- Compare **relative standing** of individuals
- Understand **income inequality and spread**
- Detect **outliers and skewness**
- Make **fair, data-driven decisions**

---

## ✅ Key Takeaways

- Quantiles divide data into **equal-sized groups**
- Median is the **simplest quantile**
- Higher-order quantiles provide **greater resolution**
- Measures of position are essential for **distributional analysis**

---

📌 **One-Line Summary to Remember**  
> *Quantiles tell us where a value stands relative to the rest of the data, not just what the average is.*

---
# Measures of Position – Quartiles (Complete Notes)

---

## 1. Concept Check Question

### Fill in the blank:

Quantiles are a measure of position that divide a data set into _____.

Correct answer:
Any number of equal parts

Explanation:
Quantiles divide ordered data into equal-sized groups. The number of groups can vary depending on the type of quantile used.

---

## 2. Quartiles

Quartiles are a type of quantile that divide a data set into four equal parts.

---

## 3. Types of Quartiles

The three quartiles are:

1. First quartile (lower quartile)
2. Second quartile (median)
3. Third quartile (upper quartile)

Although the zeroth quartile (minimum value) and the fourth quartile (maximum value) are sometimes mentioned, the standard convention is to work with only three quartiles. We will follow this convention.

---

## 4. Interpretation of Quartiles

The first quartile is the value below which 25 percent of the data lies.  
This is known as the exclusive definition of quartiles.

In the inclusive definition, 25 percent of the data is at or below the first quartile.

In this module, we use the exclusive definition of quantiles.

---

## 5. Visual Understanding of Quartiles

When employee compensation data is divided into four equal parts, three vertical lines divide the histogram into four regions.  
Each region contains an equal number of data points.

The three dividing lines represent:
- First quartile
- Second quartile
- Third quartile

---

## 6. Example: Age of Students

Consider the ages of 21 students in a school.

### Raw Data

| Student Name | Age |
|-------------|-----|
| Tom         | 11  |
| Goutham     | 12  |
| Riya        | 13  |
| Aman        | 14  |
| Sneha       | 13  |
| Kiran       | 15  |
| Neha        | 16  |
| Arjun       | 14  |
| Meera       | 12  |
| Rahul       | 17  |
| Ananya      | 18  |
| Rohit       | 19  |
| Pooja       | 13  |
| Suresh      | 20  |
| Kavya       | 16  |
| Mohan       | 14  |
| Divya       | 15  |
| Sanjay      | 17  |
| Nisha       | 18  |
| Varun       | 16  |
| Aditi       | 13  |

---

## 7. Steps to Find Quartiles

Step 1:
Arrange the data set in ascending or descending order.

Step 2:
Find the median of the entire data set. This is the second quartile.

Step 3:
Divide the data into two parts on either side of the median.

Step 4:
Find the median of each half to obtain the first and third quartiles.

---

## 8. Ordered Data

After arranging the ages in ascending order, we get:

11, 12, 12, 13, 13, 13, 13, 14, 14, 14, 15, 15, 16, 16, 16, 17, 17, 18, 18, 19, 20

---

## 9. Second Quartile (Median)

Since there are 21 observations, the median is the 11th value.

Median (Q2) = 15  
Position = 11th

The median divides the data into two equal parts.

---

## 10. First Quartile (Q1)

The first 10 ages on the left side of the median are:

11, 12, 12, 13, 13, 13, 13, 14, 14, 14

The median of these 10 values is the average of the 5th and 6th values:

(13 + 13) / 2 = 13

First quartile (Q1) = 13

---

## 11. Third Quartile (Q3)

The last 10 ages on the right side of the median are:

15, 16, 16, 16, 17, 17, 18, 18, 19, 20

The median of these values is the average of the 5th and 6th values:

(17 + 17) / 2 = 17

Third quartile (Q3) = 17

---

## 12. Summary of Quartiles

First quartile: Q1  
Second quartile: Q2  
Third quartile: Q3

---

## 13. Interquartile Range (IQR)

The three quartiles are Q1, Q2, and Q3.

The difference between Q3 and Q1 is called the interquartile range.

IQR = Q3 − Q1  
IQR = 17 − 13 = 4

The interquartile range represents the spread of the middle 50 percent of the data.

---

## 14. Outlier Detection Using IQR

Lower bound = Q1 − 1.5 × IQR  
Upper bound = Q3 + 1.5 × IQR

Values below the lower bound or above the upper bound are considered outliers.

---

## 15. Interpretation of Results

- The first 25 percent of students are aged less than 13 years
- The first 50 percent of students are aged less than 15 years
- The first 75 percent of students are aged less than 17 years
- The interquartile range is 4 years

This demonstrates how quartiles help analyze the distribution of a data set.


---

# Measures of Position – Quartiles and IQR (Worked Example)

---

## 1. Given Data

The following table shows employee salary data.  
Only the salary values are used for calculating quartiles.

| EmployeeID | Salary |
|------------|--------|
| 10         | 600752 |
| 12         | 854962 |
| 123        | 711112 |
| 122        | 915606 |
| 145        | 1116282 |
| 134        | 832968 |
| 1345       | 1218716 |
| 12345      | 1019515 |
| 1123       | 754968 |
| 1345       | 847858 |

---

## 2. Arrange the Data in Ascending Order

Salary values arranged in ascending order:

600752  
711112  
754968  
832968  
847858  
854962  
915606  
1019515  
1116282  
1218716  

Total number of observations, n = 10

---

## 3. Second Quartile (Median or Q2)

Since the number of observations is even, the median is the average of the 5th and 6th values.

5th value = 847858  
6th value = 854962  

Median (Q2) = 851410

---

## 4. First Quartile (Q1)

The lower half of the data consists of the first 5 values:

600752  
711112  
754968  
832968  
847858  

The median of these 5 values is the 3rd value.

First Quartile (Q1) = 754968

---

## 5. Third Quartile (Q3)

The upper half of the data consists of the last 5 values:

854962  
915606  
1019515  
1116282  
1218716  

The median of these 5 values is the 3rd value.

Third Quartile (Q3) = 1019515

---

## 6. Interquartile Range (IQR)

The interquartile range measures the spread of the middle 50 percent of the data.

IQR = Q3 − Q1  
IQR = 1019515 − 754968  
IQR = 264547

---

## 7. Summary of Results

| Measure | Value |
|--------|-------|
| Q1 | 754968 |
| Q2 (Median) | 851410 |
| Q3 | 1019515 |
| IQR | 264547 |

---

## 8. Interpretation

- 25 percent of employees earn less than 754968  
- 50 percent of employees earn less than 851410  
- 75 percent of employees earn less than 1019515  
- The middle 50 percent of salaries are spread across a range of 264547  

This shows how quartiles and the interquartile range help in understanding salary distribution and income spread within an organization.

---

## 9. Key Takeaways

- Quartiles divide ordered data into four equal parts  
- The median is the second quartile  
- IQR measures central dispersion and is resistant to outliers  
- Quartiles are widely used in salary analysis and box plots  

---
# Measures of Position – Deciles

---

## 1. What are Deciles?

Deciles are a type of measure of position that divide an ordered data set into ten equal parts.

Each part contains 10 percent of the data.

---

## 2. Number of Deciles

There are nine deciles:

D1, D2, D3, D4, D5, D6, D7, D8, D9

- D1 separates the lowest 10 percent of data
- D5 is the same as the median
- D9 separates the lowest 90 percent of data

---

## 3. Meaning of a Decile

The k-th decile (Dk) is the value below which k × 10 percent of the data lies.

Example:
- D3 means 30 percent of the data lies below it
- D7 means 70 percent of the data lies below it

---

## 4. Steps to Find Deciles

Step 1:
Arrange the data in ascending order.

Step 2:
Find the position of the k-th decile using the formula:

Position of Dk = k × (n + 1) / 10

where n is the number of observations.

Step 3:
Locate the value at the calculated position.
If the position is not a whole number, interpolate between the two nearest values.

---

## 5. Example

Consider the following data set:

2, 4, 6, 8, 10, 12, 14, 16, 18, 20

Number of observations, n = 10

---

## 6. Find the 3rd Decile (D3)

Position of D3 = 3 × (10 + 1) / 10  
Position of D3 = 3.3

The 3.3 position lies between the 3rd and 4th values.

3rd value = 6  
4th value = 8  

D3 = 6 + 0.3 × (8 − 6)  
D3 = 6.6

---

## 7. Find the 7th Decile (D7)

Position of D7 = 7 × (10 + 1) / 10  
Position of D7 = 7.7

7th value = 14  
8th value = 16  

D7 = 14 + 0.7 × (16 − 14)  
D7 = 15.4

---

## 8. Interpretation

- 30 percent of the data values are less than or equal to 6.6
- 70 percent of the data values are less than or equal to 15.4

---

## 9. Relationship with Other Measures

- D5 is equal to the median
- Deciles provide more detail than quartiles
- Deciles are less detailed than percentiles

---

## 10. Uses of Deciles

- Used in income and salary analysis
- Used in education performance ranking
- Used in population and demographic studies

---

## 11. One-Line Summary

Deciles divide ordered data into ten equal parts, each representing 10 percent of the data.

---

# Deciles – Worked Complex Example

---

## Example: Employee Monthly Salaries

The following data represents the monthly salaries of 20 employees in a company.

Salaries (in units):

42000  
38000  
56000  
61000  
47000  
52000  
68000  
45000  
59000  
72000  
81000  
66000  
54000  
49000  
75000  
83000  
91000  
88000  
70000  
64000  

---

## Step 1: Arrange the Data in Ascending Order

After arranging the salaries in ascending order:

38000  
42000  
45000  
47000  
49000  
52000  
54000  
56000  
59000  
61000  
64000  
66000  
68000  
70000  
72000  
75000  
81000  
83000  
88000  
91000  

Number of observations, n = 20

---

## Step 2: Formula for Deciles

Position of the k-th decile:

Position of Dk = k × (n + 1) / 10

---

## Step 3: Find the 2nd Decile (D2)

Position of D2 = 2 × (20 + 1) / 10  
Position of D2 = 4.2

This lies between the 4th and 5th values.

4th value = 47000  
5th value = 49000  

D2 = 47000 + 0.2 × (49000 − 47000)  
D2 = 47000 + 400  
D2 = 47400

---

## Step 4: Find the 5th Decile (D5)

Position of D5 = 5 × (20 + 1) / 10  
Position of D5 = 10.5

10th value = 61000  
11th value = 64000  

D5 = 61000 + 0.5 × (64000 − 61000)  
D5 = 62500

Note:
D5 is equal to the median of the data.

---

## Step 5: Find the 8th Decile (D8)

Position of D8 = 8 × (20 + 1) / 10  
Position of D8 = 16.8

16th value = 75000  
17th value = 81000  

D8 = 75000 + 0.8 × (81000 − 75000)  
D8 = 79800

---

## Step 6: Summary of Deciles

| Decile | Value |
|-------|-------|
| D2 | 47400 |
| D5 | 62500 |
| D8 | 79800 |

---

## Step 7: Interpretation

- 20 percent of employees earn less than 47400  
- 50 percent of employees earn less than 62500  
- 80 percent of employees earn less than 79800  

This gives a detailed picture of salary distribution across different income levels.

---

## Key Observations

- Deciles divide data into ten equal parts  
- D5 represents the median  
- Deciles give more detailed ranking than quartiles  
- Useful for salary, income, and performance analysis  

---

## One-Line Exam Answer

Deciles divide an ordered data set into ten equal parts, each representing 10 percent of the data.

---

# Measures of Position – Percentiles

---

## 1. What are Percentiles?

Percentiles are a type of quantile that divide an ordered data set into 100 equal parts.

There are 99 percentiles:
P1, P2, P3, ..., P99

---

## 2. Meaning of Percentiles

The k-th percentile (Pk) is the value below which k percent of the data lies.

Percentiles tell us:
- What percentage of values lie below a given value
- The relative position of a value within a data set

---

## 3. Simple Interpretation Example

If you scored 62 out of 80 in a test and your score lies in the 90th percentile, it means:

90 percent of students scored less than or equal to 62  
Only 10 percent of students scored higher than you  

This shows your performance relative to others, not just your raw score.

---

## 4. Example 1: Student Test Scores

### Data

| RollNo | Score |
|-------|-------|
| 1 | 35 |
| 2 | 42 |
| 3 | 48 |
| 4 | 50 |
| 5 | 55 |
| 6 | 60 |
| 7 | 62 |
| 8 | 65 |
| 9 | 70 |
| 10 | 78 |

---

### Interpretation Using Percentiles

- If score 50 is at the 40th percentile, then 40 percent of students scored below 50
- If score 65 is at the 80th percentile, then 80 percent of students scored below 65
- If score 78 is at the 95th percentile, then the student performed better than most students

---

## 5. Example 2: Employee Compensation

### Data

| EmployeeID | Compensation |
|------------|--------------|
| 101 | 30000 |
| 102 | 35000 |
| 103 | 42000 |
| 104 | 50000 |
| 105 | 58000 |
| 106 | 65000 |
| 107 | 72000 |
| 108 | 82000 |
| 109 | 95000 |
| 110 | 120000 |

---

### Interpretation Using Percentiles

- If 58000 is the 50th percentile, half of the employees earn less than this amount
- If 82000 is the 75th percentile, 75 percent of employees earn less than this
- If 120000 is the 95th percentile, only a small fraction earns more than this

Percentiles help organizations design fair salary brackets.

---

## 6. Concept Statement (Very Important)

If the 75th percentile of a data set is 87, it means:

75 percent of the data points lie below 87  
25 percent of the data points lie above 87

---

## 7. Example 3: Investment Returns

Suppose an investment company analyzes historical returns.

If the 60th percentile of returns is 3.67, it means:

60 percent of the time, returns were below 3.67  
40 percent of the time, returns were above 3.67  

This helps investors compare investment options and assess risk.

---

## 8. More Everyday Examples

- If your height is at the 90th percentile, you are taller than 90 percent of people
- If a city is at the 10th percentile for rainfall, it receives very low rainfall
- If a product is priced at the 95th percentile, it is more expensive than most products

---

## 9. Relationship with Other Measures

- P50 is equal to the median
- Percentiles give more detail than quartiles and deciles
- Percentiles are widely used in exams, competitive tests, finance, and analytics

---

## 10. One-Line Summary

Percentiles show the relative standing of a value by indicating the percentage of data points that lie below it.

# Relationship between Quartiles, Deciles, and Percentiles

---

## 1. Quantiles – A Unified View

Quartiles, deciles, and percentiles are all types of quantiles.

They differ only in the number of equal parts into which they divide the same ordered data set.

- Quartiles divide data into 4 equal parts
- Deciles divide data into 10 equal parts
- Percentiles divide data into 100 equal parts

Thus, they are different ways of measuring position or ranking in the same data.

---

## 2. Basic Relationship Concept

A given position in a data set can be expressed as:
- a quartile
- a decile
- a percentile

All three represent the same relative location.

---

## 3. Relationship Between Quartiles and Percentiles

| Proportion of Data | Percentile | Quartile |
|-------------------|------------|----------|
| 0.25 | 25th | 1st Quartile (Q1) |
| 0.50 | 50th | 2nd Quartile (Q2 or Median) |
| 0.75 | 75th | 3rd Quartile (Q3) |

---

## 4. Quartiles and Percentiles (Detailed Table)

| Quartile | Equivalent Percentile |
|---------|-----------------------|
| First Quartile (Q1) | 25th Percentile (P25) |
| Second Quartile (Q2) | 50th Percentile (P50) |
| Third Quartile (Q3) | 75th Percentile (P75) |

---

## 5. Relationship Between Deciles and Percentiles

Each decile corresponds to a multiple of 10 percentiles.

| Decile | Equivalent Percentile |
|-------|-----------------------|
| D1 | 10th Percentile |
| D2 | 20th Percentile |
| D3 | 30th Percentile |
| D4 | 40th Percentile |
| D5 | 50th Percentile |
| D6 | 60th Percentile |
| D7 | 70th Percentile |
| D8 | 80th Percentile |
| D9 | 90th Percentile |

---

## 6. Combined Relationship Summary

- Q1 = P25
- Q2 = P50 = D5 (Median)
- Q3 = P75
- D1 = P10
- D9 = P90

Thus, all three measures are consistent and interconnected.

---

## 7. Simple Numerical Example

Suppose in a test:
- Q1 score is 45
- Q2 score is 60
- Q3 score is 75

This means:
- 25 percent of students scored below 45
- 50 percent of students scored below 60
- 75 percent of students scored below 75

Equivalently:
- P25 = 45
- P50 = 60
- P75 = 75

---

## 8. Real-World Applications

- Percentiles are commonly used in student exam results and health growth charts
- Deciles are widely used in income distribution and investment portfolio analysis
- Quartiles are frequently used in descriptive statistics, box plots, and outlier detection

---

## 9. Key Takeaways

- Quartiles, deciles, and percentiles are all quantiles
- They describe relative position, not absolute values
- They are interchangeable representations of the same concept
- Median is the most important connecting point between all three

---

## 10. One-Line Summary

Quartiles, deciles, and percentiles are different but equivalent ways of describing the relative position of data values within a data set.

---
