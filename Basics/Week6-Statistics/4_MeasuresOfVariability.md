# Introduction to Variability

---

## 1. Why Do We Need Variability?

So far, we have studied:
- Measures of central tendency (mean, median, mode)
- Measures of position (quartiles, deciles, percentiles)

These measures describe the *center* or *position* of a data set.  
However, they do not tell us **how spread out the data values are**.

---

## 2. Same Central Value, Different Nature of Data

Consider the heights of three children:

Data Set A: 80, 90, 100  
Data Set B: 90, 90, 90  

Mean of both data sets = 90  
Median of both data sets = 90  

Even though the central values are the same, the two data sets are very different.  
To understand this difference, we need to study **variability**.

---

## 3. What Is Variability?

Variability refers to **how spread out the values in a data set are**.

Other commonly used terms:
- Spread
- Dispersion
- Variation

If values are close to each other, variability is low.  
If values are far apart, variability is high.

---

## 4. Example: Employee Compensation

Suppose we have 10 employees in each of two companies.

### Company A Compensation Data

| Name | Compensation |
|------|--------------|
| A1 | 30000 |
| A2 | 32000 |
| A3 | 31000 |
| A4 | 30500 |
| A5 | 31500 |
| A6 | 32500 |
| A7 | 33000 |
| A8 | 29000 |
| A9 | 34000 |
| A10 | 35000 |

---

### Company B Compensation Data

| Name | Compensation |
|------|--------------|
| B1 | 15000 |
| B2 | 25000 |
| B3 | 40000 |
| B4 | 60000 |
| B5 | 80000 |
| B6 | 100000 |
| B7 | 120000 |
| B8 | 140000 |
| B9 | 160000 |
| B10 | 180000 |

---

## 5. Why Measure Variability?

We want to understand:
- How spread out the compensation values are
- Whether employees earn similar amounts or very different amounts
- How consistent or inconsistent salaries are within a company

Measures of variability help us quantify this spread.

---

## 6. Measures of Variability

Common measures of variability include:
- Range
- Variance
- Standard deviation

We begin with the simplest measure: **Range**.

---

# RANGE

---

## 7. What Is Range?

The range is the simplest measure of variability.

Range = Maximum value − Minimum value

It shows the distance between the smallest and largest values in the data set.

---

## 8. Compensation Values Side by Side

Company A compensation values:
29000, 30000, 30500, 31000, 31500, 32000, 32500, 33000, 34000, 35000

Company B compensation values:
15000, 25000, 40000, 60000, 80000, 100000, 120000, 140000, 160000, 180000

---

## 9. Range of Company A

Maximum compensation = 35000  
Minimum compensation = 29000  

Range of Company A = 35000 − 29000 = 6000

---

## 10. Range of Company B

Maximum compensation = 180000  
Minimum compensation = 15000  

Range of Company B = 180000 − 15000 = 165000

---

## 11. Interpretation of Range

Company A has a small range, indicating salaries are closely grouped.  
Company B has a very large range, indicating large differences in salaries.

Thus, Company B has much higher variability than Company A.

---

## 12. Range Alone Is Not Enough

Range does not consider:
- How values are distributed between minimum and maximum
- The central tendency of the data

For Company A:
- Mean compensation is moderate
- Range is small

For Company B:
- Mean compensation is higher
- Range is very large

To gain deeper insights, we must study additional measures such as variance and standard deviation.

---

## 13. Concept Check (Test Question)

The range of a data set can be negative.

Answer:
False

Explanation:
Range is calculated as maximum minus minimum, and since the maximum is always greater than or equal to the minimum, the range can never be negative.

---

## 14. Test Question: Student Marks

The mathematics test scores of 10 students are given below.

| Name | Marks |
|------|-------|
| S1 | 45 |
| S2 | 52 |
| S3 | 60 |
| S4 | 48 |
| S5 | 75 |
| S6 | 68 |
| S7 | 55 |
| S8 | 80 |
| S9 | 62 |
| S10 | 50 |

---

## 15. Find the Range of the Scores

Maximum marks = 80  
Minimum marks = 45  

Range = 80 − 45 = 35

---

## 16. Key Takeaways

- Measures of central tendency describe the center of data
- Measures of variability describe the spread of data
- Range is the simplest measure of variability
- Range alone is not sufficient for deep analysis
- Variability is essential for meaningful data comparison

---

# Mean Absolute Deviation (MAD)

---

## 1. What Is Deviation?

Deviation indicates **how much a particular data point differs from a fixed value**.  
This fixed value is usually a **measure of central tendency**, such as:
- Mean
- Median

Deviation helps us understand **variability** in the data.

---

## 2. Why Mean Absolute Deviation?

Two data sets may have:
- The same mean
- The same range  

Yet they can differ significantly in how values are distributed.

**Mean Absolute Deviation (MAD)** captures the *average distance* of data points from a central value and hence gives a better picture of spread.

---

## 3. Mean Absolute Deviation About the Mean

Mean Absolute Deviation about the mean measures the **average of absolute deviations from the mean**.

### Algorithm to Calculate MAD About the Mean

1. Calculate the **mean** of the data set  
2. Find the **absolute difference** between each data point and the mean  
3. Calculate the **mean of these absolute differences**

---

## 4. Formula: MAD About the Mean

If  
x₁, x₂, x₃, … , xₙ are n observations  
and their mean is x̄,

Then,

**MAD about Mean**

( |x₁ − x̄| + |x₂ − x̄| + ... + |xₙ − x̄| ) / n
---

## 5. Example: Company A and Company B

### Company A Compensation Data

| Employee | Compensation |
|---------|--------------|
| A1 | 30000 |
| A2 | 32000 |
| A3 | 31000 |
| A4 | 30500 |
| A5 | 31500 |

---

### Step 1: Mean of Company A

\[
\bar{x}_A = \frac{30000 + 32000 + 31000 + 30500 + 31500}{5} = 31000
\]

---

### Step 2: Absolute Deviations (Company A)

| Compensation | Mean | \|Xi − Mean\| |
|-------------|------|---------------|
| 30000 | 31000 | 1000 |
| 32000 | 31000 | 1000 |
| 31000 | 31000 | 0 |
| 30500 | 31000 | 500 |
| 31500 | 31000 | 500 |

---

### Step 3: MAD About the Mean (Company A)

\[
\text{MAD}_A = \frac{1000 + 1000 + 0 + 500 + 500}{5} = 600
\]

---

## 6. Company B Compensation Data

| Employee | Compensation |
|---------|--------------|
| B1 | 20000 |
| B2 | 30000 |
| B3 | 50000 |
| B4 | 70000 |
| B5 | 90000 |

---

### Step 1: Mean of Company B

\[
\bar{x}_B = \frac{20000 + 30000 + 50000 + 70000 + 90000}{5} = 52000
\]

---

### Step 2: Absolute Deviations (Company B)

| Compensation | Mean | \|Xi − Mean\| |
|-------------|------|---------------|
| 20000 | 52000 | 32000 |
| 30000 | 52000 | 22000 |
| 50000 | 52000 | 2000 |
| 70000 | 52000 | 18000 |
| 90000 | 52000 | 38000 |

---

### Step 3: MAD About the Mean (Company B)

\[
\text{MAD}_B = \frac{32000 + 22000 + 2000 + 18000 + 38000}{5} = 22400
\]

---

## 7. Interpretation

- Mean compensation of Company A = 31,000  
- MAD of Company A = 600  

- Mean compensation of Company B = 52,000  
- MAD of Company B = 22,400  

Although Company B has a higher mean, its **mean absolute deviation is much larger**, indicating **greater variability** in salaries.

---

## 8. Formal Definition (MAD About Mean)

The **absolute deviations of data points from the mean** are called absolute deviations about the mean.  
The **mean of these absolute deviations** is called the **mean absolute deviation about the mean**.

---

## 9. Mean Absolute Deviation About the Median

The process is similar, but deviations are calculated from the **median instead of the mean**.

---

### Algorithm: MAD About the Median

1. Calculate the **median**  
2. Find absolute deviations from the median  
3. Take the mean of these deviations

---

## 10. Formula: MAD About the Median

If  
x₁, x₂, … , xₙ are observations  
and median = M,

\[
\text{MAD}_{\text{median}} = \frac{1}{n} \sum_{i=1}^{n} |x_i - M|
\]

---

## 11. Example: MAD About the Median (Company A)

Company A data (sorted):  
30000, 30500, 31000, 31500, 32000  

Median = 31000

| Compensation | Median | \|Xi − Median\| |
|-------------|--------|----------------|
| 30000 | 31000 | 1000 |
| 30500 | 31000 | 500 |
| 31000 | 31000 | 0 |
| 31500 | 31000 | 500 |
| 32000 | 31000 | 1000 |

[
\text{MAD}_{\text{median}} = \frac{1000 + 500 + 0 + 500 + 1000}{5} = 600
]

---

## 12. Mean vs Median in MAD

| Aspect | MAD about Mean | MAD about Median |
|------|----------------|------------------|
| Uses | Mean | Median |
| Sensitive to outliers | Yes | Less |
| Most commonly used | Yes | Sometimes |

In most cases, **MAD about the mean** is preferred because the mean considers **all values including outliers**, giving a more comprehensive measure of dispersion.

---

## 13. Key Takeaways

- MAD measures **average distance from central value**
- Uses **absolute values** to avoid cancellation
- Better than range for understanding spread
- MAD about mean is more commonly used
- Higher MAD ⇒ higher variability

---
# Variance

---

## 1. Introduction to Variance

Another important method to measure the **spread or variability** of a data set is **Variance**.

Variance is similar to **Mean Absolute Deviation (MAD)**, but instead of taking absolute deviations, we **square the deviations** from the mean and then take their average.

Squaring the deviations:
- Removes negative signs
- Gives more weight to extreme values (outliers)
- Makes variance sensitive to dispersion

---

## 2. What Does Variance Measure?

Variance measures **how far the data values are spread around the mean**.

If the variance is:
- **Small** → data points are close to the mean
- **Large** → data points are widely spread

Variance is commonly denoted as **sigma square** or **var**.

---

## 3. Algorithm to Calculate Variance

To calculate variance, follow these steps:

1. Calculate the **mean** of the data set  
2. Calculate the **deviation** of each value from the mean  
3. **Square** each deviation  
4. Calculate the **mean of the squared deviations**

---

## 4. Formula for Variance 

If  
x1, x2, x3, ..., xn are n data values  
and mean = x_bar  

Then,

Variance =  
( (x1 − x_bar)^2 + (x2 − x_bar)^2 + ... + (xn − x_bar)^2 ) / n

This formula is inspired by the concept of **Euclidean distance**, where squared distances are summed to measure dispersion.

---

## 5. Why Deviations About the Mean?

For variance and standard deviation, we always use **deviations about the mean** because:
- The mean uses all data points
- Outliers affect the mean
- Variance captures overall variability more effectively

---

## 6. Example: Compensation Data of Two Companies

Consider the compensation details of **5 employees** from two companies.

### Compensation Data

| Company A | Company B |
|---------|-----------|
| 30000 | 20000 |
| 32000 | 30000 |
| 31000 | 50000 |
| 30500 | 70000 |
| 31500 | 90000 |

---

## 7. Step 1: Calculate the Mean

### Company A

Mean_A = (30000 + 32000 + 31000 + 30500 + 31500) / 5  
Mean_A = 31000

### Company B

Mean_B = (20000 + 30000 + 50000 + 70000 + 90000) / 5  
Mean_B = 52000

---

## 8. Step 2: Deviations from the Mean

### Company A

| Value | Mean | Deviation |
|-----|------|-----------|
| 30000 | 31000 | -1000 |
| 32000 | 31000 | 1000 |
| 31000 | 31000 | 0 |
| 30500 | 31000 | -500 |
| 31500 | 31000 | 500 |

---

### Company B

| Value | Mean | Deviation |
|-----|------|-----------|
| 20000 | 52000 | -32000 |
| 30000 | 52000 | -22000 |
| 50000 | 52000 | -2000 |
| 70000 | 52000 | 18000 |
| 90000 | 52000 | 38000 |

---

## 9. Step 3: Square the Deviations

### Company A

| Deviation | Squared Deviation |
|----------|------------------|
| -1000 | 1000000 |
| 1000 | 1000000 |
| 0 | 0 |
| -500 | 250000 |
| 500 | 250000 |

---

### Company B

| Deviation | Squared Deviation |
|----------|------------------|
| -32000 | 1024000000 |
| -22000 | 484000000 |
| -2000 | 4000000 |
| 18000 | 324000000 |
| 38000 | 1444000000 |

---

## 10. Step 4: Mean of Squared Deviations (Variance)

### Company A

Variance_A =  
(1000000 + 1000000 + 0 + 250000 + 250000) / 5  

Variance_A = 500000

---

### Company B

Variance_B =  
(1024000000 + 484000000 + 4000000 + 324000000 + 1444000000) / 5  

Variance_B = 656800000

---

## 11. Interpretation

- Mean of Company A = 31,000  
- Variance of Company A = 500,000  

- Mean of Company B = 52,000  
- Variance of Company B = 656,800,000  

Although Company B has a higher mean, its variance is **much larger**, indicating **greater variability in compensation**.

---

## 12. Limitation of Variance

Variance is expressed in **squared units**:
- Salary squared
- Marks squared
- Height squared

This makes variance **difficult to interpret directly**.

---

## 13. Why Standard Deviation?

To overcome the limitation of squared units:
- We take the **square root of variance**
- This gives **Standard Deviation**

Standard deviation is expressed in the **same units as the original data**, making interpretation easier.

You will learn about **Standard Deviation** next.

---

## 14. Key Takeaways

- Variance measures spread around the mean  
- Uses squared deviations  
- Sensitive to outliers  
- Large variance indicates high variability  
- Basis for standard deviation  

---

# Standard Deviation

---

## 1. Introduction to Standard Deviation

Variance is an intuitive measure of dispersion inspired by the concept of **Euclidean distance**.  
However, one major issue with variance is that its **units are squared**, which makes interpretation difficult.

To overcome this limitation, we use **Standard Deviation**.

Standard deviation is a **more intuitive measure of spread**, derived directly from variance by taking its **square root**.

---

## 2. What Is Standard Deviation?

Standard deviation measures the **average distance of data values from the mean**, expressed in the **same units as the original data**.

Because of this:
- Standard deviation is easier to understand than variance
- It is widely used in statistics, finance, science, and machine learning

Standard deviation is commonly represented by the symbol **sigma**.

---

## 3. Algorithm to Calculate Standard Deviation

To calculate standard deviation, follow these steps:

1. Calculate the **variance** of the data set  
2. Take the **square root** of the variance  

---

## 4. Formula for Standard Deviation (GitHub Compatible)

If  
Variance = var  

Then,

Standard Deviation = square root of var

That is,

Standard Deviation = sqrt(Variance)

---

## 5. Using the Previous Example (Company A and Company B)

Recall the variances calculated earlier:

- Variance of Company A = 500000  
- Variance of Company B = 656800000  

---

## 6. Standard Deviation Calculation

### Company A

Standard Deviation_A = sqrt(500000)  
Standard Deviation_A ≈ 707.11

---

### Company B

Standard Deviation_B = sqrt(656800000)  
Standard Deviation_B ≈ 25629.67

---

## 7. Interpretation of Results

- Mean compensation of Company A = 31,000  
- Standard deviation of Company A ≈ 707  

- Mean compensation of Company B = 52,000  
- Standard deviation of Company B ≈ 25,630  

This clearly shows that:

- Compensation values in **Company B** are much more spread out  
- Salary deviation in **Company B** is significantly higher than in **Company A**

Although variance provided the same intuition, **standard deviation is easier to read and compare**.

---

## 8. Why Standard Deviation Is Preferred Over Variance

| Aspect | Variance | Standard Deviation |
|------|---------|-------------------|
| Units | Squared units | Same as data |
| Interpretability | Difficult | Easy |
| Usage | Intermediate | Widely used |
| Comparison | Hard | Intuitive |

---

## 9. Population vs Sample Standard Deviation

So far, we have used **n** in the denominator while calculating variance and standard deviation.

This means:
- We are treating the given data as the **entire population**
- The resulting measures are **population variance and population standard deviation**

---

## 10. Why Use n or n − 1?

- If the data represents the **entire population**, divide by **n**
- If the data is only a **sample**, divide by **n − 1**

Using **n − 1** corrects the bias introduced when estimating population variability from a sample.

---

## 11. Sample Variance and Sample Standard Deviation (Reference)

If the data is a sample:

Sample Variance =  
(sum of squared deviations from mean) / (n − 1)

Sample Standard Deviation =  
square root of Sample Variance

---

## 12. Convention Used in This Module

For the remainder of this module:

- Every data set is assumed to be the **entire population**
- Variance and standard deviation formulas will use **n** in the denominator

The distinction between population and sample will be explored further in **inferential statistics**.

---

## 13. Key Takeaways

- Standard deviation is the square root of variance  
- It measures spread in original units  
- Easier to interpret than variance  
- Widely used in real-world data analysis  
- Helps compare variability across data sets  

---

# What Does Standard Deviation Tell Us?

**Standard deviation** tells us **how spread out the data values are from the mean**.

In simple words:

> **It shows how much the values in a data set typically differ from the average.**

---

## What Standard Deviation Tells You

### 1. Closeness to the Mean

- **Small standard deviation** → values are **close to the mean**
- **Large standard deviation** → values are **far from the mean**

---

### 2. Consistency of Data

- Low standard deviation → data is **consistent**
- High standard deviation → data is **inconsistent / highly variable**

---

### 3. Typical Deviation

Standard deviation represents the **average distance of values from the mean**, expressed in the **same units as the data**.

**Example:**

- Mean marks = 70  
- Standard deviation = 5  

👉 Most students score about **5 marks above or below 70**

---

## Simple Example

### Data Set A

```

48, 49, 50, 51, 52

```

- Mean = 50  
- Standard deviation = small  

👉 Scores are tightly grouped

---

### Data Set B

```

20, 35, 50, 65, 80

```

- Mean = 50  
- Standard deviation = large  

👉 Scores are widely spread

---

## Real-Life Meaning

| Context        | What Standard Deviation Tells        |
|---------------|--------------------------------------|
| Exams         | How consistent student scores are    |
| Salaries      | How unequal incomes are              |
| Finance       | How risky an investment is           |
| Manufacturing | Quality consistency                  |

---

## Key Points to Remember

- Measures **spread around the mean**
- Expressed in the **same units as the data**
- Sensitive to **outliers**
- More useful than variance for interpretation

---

## One-Line Exam Answer

> **Standard deviation measures the extent to which data values deviate from the mean.**


