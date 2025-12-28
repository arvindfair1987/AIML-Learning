# Measures of Association

---

## 1. Introduction

In earlier sessions, you studied:

- Measures of central tendency (mean, median, mode)
- Measures of variability (range, MAD, variance, standard deviation)

These measures help describe the **distribution of a single variable**.

However, in real-world problems, we are often interested in understanding **how two variables behave together**. This is where **measures of association** become important.

Measures of association help answer questions such as:
- Do two variables increase together?
- Does one variable decrease when another increases?
- How strong is their relationship?

---

## 2. What Are Measures of Association?

Measures of association quantify the **relationship between two or more variables**.

They help determine:
- **Direction** of relationship (positive or negative)
- **Strength** of relationship (weak or strong)

Two important measures of association are:
1. Covariance
2. Correlation (to be studied next)

---

## 3. Real-World Motivation: Financial Analysis Example

Suppose you are a **financial analyst** studying the relationship between company profits and different types of expenditure.

### Company Expenditure and Profit Data

| Month | Marketing | Human Resources | Infrastructure | Profit |
|------|----------|----------------|----------------|--------|
| Jan | 200 | 150 | 300 | 500 |
| Feb | 250 | 160 | 320 | 540 |
| Mar | 300 | 170 | 350 | 600 |
| Apr | 350 | 180 | 380 | 650 |
| May | 400 | 200 | 420 | 720 |

(All values are in thousands)

---

### Question

Do profits increase or decrease with an increase in:
- Marketing expenditure?
- Human resources expenditure?
- Infrastructure expenditure?

To answer such questions, we need **measures of association**.

---

## 4. Another Example: Store Sales Data

Consider the weekly sales data of a stationery store.

| Day | Pencils Sold | Erasers Sold | Pens Sold |
|----|--------------|--------------|-----------|
| Mon | 50 | 45 | 30 |
| Tue | 60 | 55 | 28 |
| Wed | 55 | 50 | 32 |
| Thu | 70 | 65 | 25 |
| Fri | 80 | 75 | 20 |
| Sat | 90 | 85 | 18 |
| Sun | 85 | 80 | 22 |

---

### Key Questions

- Do pencil sales and eraser sales move together?
- Does pen sales move opposite to pencil sales?
- How can we **quantify** these relationships?

---

## 5. Visualising Relationships

A **scatter plot** is a common tool to visualise relationships between two variables.

From scatter plots, we may observe:
- **Positive trend**: both variables increase together
- **Negative trend**: one increases while the other decreases
- **No clear trend**

But visualization alone is **not sufficient**.

---

## 6. Quantifying Relationships: Covariance

To quantify how two variables vary **together**, we use **Covariance**.

Covariance measures the **joint variability** of two variables.

---

## 7. Covariance Formula (GitHub Compatible)

Let:
- Xi be values of variable X
- Yi be values of variable Y
- X_bar be the mean of X
- Y_bar be the mean of Y
- n be the number of observations

Then,

Covariance(X, Y) =  
Sum of (Xi − X_bar) * (Yi − Y_bar) divided by n

---

## 8. Interpretation of Covariance

- Covariance > 0 → Positive relationship
- Covariance < 0 → Negative relationship
- Covariance ≈ 0 → Weak or no linear relationship

Note:
- Covariance magnitude depends on the scale of data
- It does **not** indicate strength clearly (this motivates correlation)

---

## 9. Steps to Calculate Covariance

Given two variables X and Y:

### Step 1
Calculate the mean of X and the mean of Y

### Step 2
Calculate deviations:
- Xi − X_bar
- Yi − Y_bar

### Step 3
Multiply corresponding deviations:
- (Xi − X_bar) * (Yi − Y_bar)

### Step 4
Sum all products and divide by n

---

## 10. Covariance Example: Pencils and Erasers

### Step 1: Mean Values

Mean of pencils sold = 70  
Mean of erasers sold = 65  

---

### Step 2 & 3: Deviations and Products

| Day | Pencils | Erasers | Xi − X̄ | Yi − Ȳ | Product |
|----|--------|---------|--------|--------|--------|
| Mon | 50 | 45 | -20 | -20 | 400 |
| Tue | 60 | 55 | -10 | -10 | 100 |
| Wed | 55 | 50 | -15 | -15 | 225 |
| Thu | 70 | 65 | 0 | 0 | 0 |
| Fri | 80 | 75 | 10 | 10 | 100 |
| Sat | 90 | 85 | 20 | 20 | 400 |
| Sun | 85 | 80 | 15 | 15 | 225 |

---

### Step 4: Covariance

Sum of products = 1450  
n = 7  

Covariance (Pencils, Erasers) = 1450 / 7 ≈ 207.14

---

## 11. Covariance Example: Pencils and Pens

Mean of pens sold = 25

| Day | Pencils | Pens | Xi − X̄ | Yi − Ȳ | Product |
|----|--------|------|--------|--------|--------|
| Mon | 50 | 30 | -20 | 5 | -100 |
| Tue | 60 | 28 | -10 | 3 | -30 |
| Wed | 55 | 32 | -15 | 7 | -105 |
| Thu | 70 | 25 | 0 | 0 | 0 |
| Fri | 80 | 20 | 10 | -5 | -50 |
| Sat | 90 | 18 | 20 | -7 | -140 |
| Sun | 85 | 22 | 15 | -3 | -45 |

Sum of products = -470  

Covariance (Pencils, Pens) = -470 / 7 ≈ -67.14

---

## 12. Conclusions from the Example

- Covariance between **pencils and erasers** is **positive and large**
- Covariance between **pencils and pens** is **negative**

This indicates:
- Strong positive association between pencils and erasers
- Strong negative association between pencils and pens

These results align with real-world logic:
- Pencil users need erasers
- Pen users rely less on pencils

---

## 13. Population vs Sample Covariance

- Divide by **n** → population covariance
- Divide by **n − 1** → sample covariance (unbiased estimate)

In this module, we treat all data as the **population**.

---

## 14. Key Takeaways

- Measures of association study relationships between variables
- Covariance measures joint variability
- Sign of covariance indicates direction
- Magnitude alone is not sufficient to compare strength
- Covariance motivates the need for correlation

---

# Example: Weak Association Using Covariance  
## (Pencils Sold vs Stamps Sold)

---

## 1. Context

So far, you have seen examples where:
- Pencils and erasers showed a **strong positive association**
- Pencils and pens showed a **strong negative association**

Now, let us consider a case where **two variables show a weak relationship**.

---

## 2. Dataset: Weekly Sales of Pencils and Stamps

The following table shows the number of **pencils** and **stamps** sold by a store over one week.

| Day | Pencils Sold | Stamps Sold |
|----|--------------|-------------|
| Mon | 50 | 12 |
| Tue | 60 | 14 |
| Wed | 55 | 11 |
| Thu | 70 | 15 |
| Fri | 80 | 13 |
| Sat | 90 | 16 |
| Sun | 85 | 14 |

---

## 3. Visual Interpretation (Scatter Plot Insight)

If we plot:
- X-axis → Pencils sold
- Y-axis → Stamps sold  

We observe:
- A **slight negative or irregular trend**
- No clear linear pattern
- Points are scattered without a strong direction

This suggests a **weak association**, which we now verify numerically using **covariance**.

---

## 4. Step 1: Calculate the Means

Mean of pencils sold:

(50 + 60 + 55 + 70 + 80 + 90 + 85) / 7  
= 490 / 7  
= 70

Mean of stamps sold:

(12 + 14 + 11 + 15 + 13 + 16 + 14) / 7  
= 95 / 7  
≈ 13.57

---

## 5. Step 2 & 3: Deviations and Products

| Day | Pencils (X) | Stamps (Y) | X − X̄ | Y − Ȳ | Product |
|----|------------|-----------|-------|-------|--------|
| Mon | 50 | 12 | -20 | -1.57 | 31.40 |
| Tue | 60 | 14 | -10 | 0.43 | -4.30 |
| Wed | 55 | 11 | -15 | -2.57 | 38.55 |
| Thu | 70 | 15 | 0 | 1.43 | 0 |
| Fri | 80 | 13 | 10 | -0.57 | -5.70 |
| Sat | 90 | 16 | 20 | 2.43 | 48.60 |
| Sun | 85 | 14 | 15 | 0.43 | 6.45 |

---

## 6. Step 4: Calculate Covariance

Sum of products:

31.40 − 4.30 + 38.55 + 0 − 5.70 + 48.60 + 6.45  
= 115.00

Number of observations (n) = 7  

Covariance (Pencils, Stamps) =  
115.00 / 7  
≈ 16.43

---

## 7. Interpretation of the Result

- Covariance value ≈ **16.43**
- This value is **close to zero** when compared to:
  - Pencils vs Erasers (large positive)
  - Pencils vs Pens (large negative)

---

## 8. Conclusion

- The covariance between **pencils sold** and **stamps sold** is **small in magnitude**
- This indicates **no strong linear association**
- The weak relationship is **logical**, because:
  - Pencils and stamps serve very different purposes
  - Buying more pencils does not strongly influence stamp purchases

---

## 9. Important Insight

| Covariance Value | Interpretation |
|-----------------|----------------|
| Large positive | Strong positive relationship |
| Large negative | Strong negative relationship |
| Close to zero | Weak or no linear relationship |

---

## 10. Final Takeaway

Covariance helps us:
- Identify the **direction** of a relationship
- Recognize when **no strong association exists**

However, because covariance depends on data scale, we need a **standardized measure** to judge strength more clearly.

➡️ This leads us to **Correlation**, which you will study next.

---

# Example: Negative Covariance Close to Zero  
## (Pencils Sold vs Highlighters Sold)

---

## 1. Context

Not all negative relationships are strong.  
Sometimes, two variables may show a **slight negative trend**, but the relationship is **very weak**.

In such cases:
- The **covariance is negative**
- But its **magnitude is close to zero**

---

## 2. Dataset: Weekly Sales of Pencils and Highlighters

| Day | Pencils Sold (X) | Highlighters Sold (Y) |
|----|------------------|-----------------------|
| Mon | 40 | 18 |
| Tue | 50 | 17 |
| Wed | 60 | 19 |
| Thu | 70 | 16 |
| Fri | 80 | 18 |
| Sat | 90 | 17 |
| Sun | 100 | 16 |

---

## 3. Visual Insight (Scatter Plot)

If we draw a scatter plot:
- X-axis → Pencils sold
- Y-axis → Highlighters sold

We observe:
- A **very slight downward tendency**
- Points are scattered
- No strong linear pattern

This suggests a **weak negative association**.

---

## 4. Step 1: Calculate the Means

Mean of pencils sold:

(40 + 50 + 60 + 70 + 80 + 90 + 100) / 7  
= 490 / 7  
= 70

Mean of highlighters sold:

(18 + 17 + 19 + 16 + 18 + 17 + 16) / 7  
= 121 / 7  
≈ 17.29

---

## 5. Step 2 & 3: Deviations and Products

| Day | X | Y | X − X̄ | Y − Ȳ | Product |
|----|---|---|-------|-------|--------|
| Mon | 40 | 18 | -30 | 0.71 | -21.30 |
| Tue | 50 | 17 | -20 | -0.29 | 5.80 |
| Wed | 60 | 19 | -10 | 1.71 | -17.10 |
| Thu | 70 | 16 | 0 | -1.29 | 0 |
| Fri | 80 | 18 | 10 | 0.71 | 7.10 |
| Sat | 90 | 17 | 20 | -0.29 | -5.80 |
| Sun | 100 | 16 | 30 | -1.29 | -38.70 |

---

## 6. Step 4: Calculate Covariance

Sum of products:

-21.30 + 5.80 - 17.10 + 0 + 7.10 - 5.80 - 38.70  
= -70.00

Number of observations (n) = 7  

Covariance (X, Y):

-70.00 / 7  
= -10.00

---

## 7. Interpretation

- Covariance = **-10**
- The sign is **negative**
- The magnitude is **small**

This indicates:
- A **weak negative linear relationship**
- No strong dependence between the two variables

---

## 8. Why This Makes Sense

- Pencils and highlighters are **not substitutes**
- Buying more pencils does not strongly reduce highlighter sales
- Minor variations create a small negative covariance

---

## 9. Key Takeaway

| Covariance Value | Meaning |
|-----------------|--------|
| Negative & large | Strong negative relationship |
| Negative & small | Weak negative relationship |
| Close to zero | Almost no linear relationship |

---

## 10. Final Conclusion

This example shows that:
- Covariance can be **negative**
- Yet still be **close to zero**
- Indicating **very weak association**

This is common in real-world data where variables are only loosely related.

---

# 📘 Properties of Covariance

Covariance is a statistical measure that helps us understand the **direction of the linear relationship** between two variables.

---

## 1. Definition of Covariance

For two variables \(X\) and \(Y\) with \(n\) observations, the covariance is defined as:

$$
\operatorname{Cov}(X, Y) =
\frac{1}{n}
\sum_{i=1}^{n}
(X_i - \bar{X})(Y_i - \bar{Y})
$$

where:
- \( \bar{X} \) is the mean of variable \(X\)
- \( \bar{Y} \) is the mean of variable \(Y\)

---

## 2. Interpretation of Covariance

### ✅ Positive Covariance

$$
\operatorname{Cov}(X, Y) > 0
$$

- Indicates a **positive relationship**
- As \(X\) increases, \(Y\) also tends to increase

---

### ❌ Negative Covariance

$$
\operatorname{Cov}(X, Y) < 0
$$

- Indicates a **negative relationship**
- As \(X\) increases, \(Y\) tends to decrease

---

### ⚠️ Covariance Close to Zero

$$
\operatorname{Cov}(X, Y) \approx 0
$$

- Indicates **lack of strong linear association**
- Variables may still have a non-linear relationship

---

## 3. Core Properties of Covariance

---

### **Property 1: Symmetry (Commutative Property)**

$$
\operatorname{Cov}(X, Y) = \operatorname{Cov}(Y, X)
$$

#### Proof:

Start with the definition:

$$
\operatorname{Cov}(Y, X) =
\frac{1}{n}
\sum_{i=1}^{n}
(Y_i - \bar{Y})(X_i - \bar{X})
$$

Since multiplication is commutative:

$$
(Y_i - \bar{Y})(X_i - \bar{X})
=
(X_i - \bar{X})(Y_i - \bar{Y})
$$

Therefore:

$$
\operatorname{Cov}(X, Y) = \operatorname{Cov}(Y, X)
$$

---

### **Property 2: Covariance of a Variable with Itself**

$$
\operatorname{Cov}(X, X) = \operatorname{Var}(X)
$$

#### Proof:

Using the covariance formula:

$$
\operatorname{Cov}(X, X)
=
\frac{1}{n}
\sum_{i=1}^{n}
(X_i - \bar{X})(X_i - \bar{X})
$$

This simplifies to:

$$
\operatorname{Cov}(X, X)
=
\frac{1}{n}
\sum_{i=1}^{n}
(X_i - \bar{X})^2
$$

Which is exactly the formula for variance.

---

### **Property 3: Effect of Adding a Constant**

If a constant \(c\) is added to a variable:

$$
\operatorname{Cov}(X + c, Y) = \operatorname{Cov}(X, Y)
$$

- Adding a constant does **not change covariance**
- Covariance depends on **deviations from the mean**

---

### **Property 4: Effect of Scaling**

If variables are multiplied by constants \(a\) and \(b\):

$$
\operatorname{Cov}(aX, bY) = ab \cdot \operatorname{Cov}(X, Y)
$$

- Covariance changes with scale
- Units of measurement affect the magnitude

---

## 4. Summary of Properties

| Property | Explanation |
|--------|-------------|
| Sign | Direction of relationship |
| Symmetry | Order of variables does not matter |
| Self-covariance | Equals variance |
| Scale dependent | Changes with units |
| Near zero | Weak or no linear relationship |

---

## 5. Key Insight

A **positive covariance** indicates a positive relationship.  
A **negative covariance** indicates a negative relationship.  
A covariance **close to zero** indicates a lack of strong linear association.

---

## 6. Limitation of Covariance

Covariance has one major limitation:

- It does **not provide a standardized measure**
- Its magnitude depends on units

Because of this limitation, we use **correlation**, which normalizes covariance.

---

➡️ **Next Topic:** Correlation and its advantages over covariance

# 📘 Limitations of Covariance

Although covariance is useful for understanding the **direction** of the relationship between two variables, it has important limitations.

---

## 1. Covariance is Not Scale-Independent

One major limitation of covariance is that its **magnitude depends on the scale (units)** of the variables.

Let us understand this with an example.

---

### Example Data Sets

Consider the following data set:

$$
X = \{1, 2, 3, 4, 5\}
$$

Now, construct another data set by scaling \(X\) by a factor of 10:

$$
Y = \{10, 20, 30, 40, 50\}
$$

---

### Step 1: Mean Values

$$
\bar{X} = 3
$$

$$
\bar{Y} = 30
$$

---

### Step 2: Covariance Between X and Y

$$
\operatorname{Cov}(X, Y)
=
\frac{1}{5}
\sum_{i=1}^{5}
(X_i - \bar{X})(Y_i - \bar{Y})
$$

After calculation:

$$
\operatorname{Cov}(X, Y) = 20
$$

---

### Scaling Further

Now, take another data set obtained by scaling \(X\) by a factor of 100:

$$
Z = \{100, 200, 300, 400, 500\}
$$

Mean of \(Z\):

$$
\bar{Z} = 300
$$

---

### Covariance Between X and Z

$$
\operatorname{Cov}(X, Z)
=
\frac{1}{5}
\sum_{i=1}^{5}
(X_i - \bar{X})(Z_i - \bar{Z})
$$

After calculation:

$$
\operatorname{Cov}(X, Z) = 200
$$

---

## 2. Key Observation

Although:
- \(Y\) is just \(X\) scaled by 10
- \(Z\) is just \(X\) scaled by 100

the covariance values are:

$$
\operatorname{Cov}(X, Y) = 20
$$

$$
\operatorname{Cov}(X, Z) = 200
$$

The **relationship strength has not changed**, but the covariance value has changed **significantly**.

---

## 3. Conclusion: Limitations of Covariance

From this example, we conclude:

- Covariance **depends on the scale** of the variables
- It is **not unit-free**
- Larger units lead to larger covariance values
- Comparing covariance across:
  - different variable pairs, or
  - different data sets  
  is **not meaningful**

---

## 4. Final Takeaway

Covariance is useful for:
- Identifying **direction** of relationship (positive or negative)

But it is **not suitable** for:
- Measuring **strength** of relationship
- Comparing relationships across datasets

---

➡️ **Solution:**  
To overcome these limitations, we use **correlation**, which is a **standardised and scale-independent** measure of association.

# 📘 Pearson’s Correlation Coefficient

So far, you have learnt about **covariance**. You also understood that comparing covariance values across different data sets is difficult because covariance is **not scale-independent**. Hence, we need to **normalise covariance** so that we can meaningfully compare the **strength of association** between different variables.

The statistical measure used to normalise covariance is called **Pearson’s Product-Moment Correlation Coefficient**, commonly known as **Pearson’s correlation coefficient**.

---

## 1. Why Pearson’s Correlation?

Covariance tells us:
- the **direction** of the relationship (positive or negative)

But it does **not** tell us:
- how **strong** the relationship is in a comparable way

This is because covariance depends on the **units and scale** of the variables.

Pearson’s correlation coefficient removes this limitation by **standardising** the covariance.

---

## 2. Definition of Pearson’s Correlation Coefficient

Pearson’s correlation coefficient is defined as:

$$
\rho_{X,Y} = \frac{\operatorname{Cov}(X,Y)}{\sigma_X \, \sigma_Y}
$$

where:
- $$\operatorname{Cov}(X,Y)$$ is the covariance between variables \(X\) and \(Y\)
- $$\sigma_X$$ is the standard deviation of \(X\)
- $$\sigma_Y$$ is the standard deviation of \(Y\)

This normalisation makes correlation **unit-free** and **scale-independent**.

---

## 3. Interpretation of Pearson’s Correlation

The value of Pearson’s correlation coefficient always lies between **−1 and +1**.

- $$\rho = +1$$ → Perfect positive linear relationship  
- $$\rho = -1$$ → Perfect negative linear relationship  
- $$\rho = 0$$ → No linear relationship  

The **closer the value is to ±1**, the **stronger** the linear association.

---

## 4. Steps to Calculate Pearson’s Correlation Coefficient

Suppose two features \(X\) and \(Y\) are given.

### Step 1: Calculate the covariance
$$
\operatorname{Cov}(X,Y)
$$

---

### Step 2: Calculate the standard deviations
$$
\sigma_X
$$

$$
\sigma_Y
$$

---

### Step 3: Divide covariance by the product of standard deviations
$$
\rho_{X,Y} = \frac{\operatorname{Cov}(X,Y)}{\sigma_X \sigma_Y}
$$

This gives the **Pearson’s correlation coefficient**.

---

## 5. Expanded Formula for Pearson’s Correlation

The expanded (population) formula is:

$$
\rho_{X,Y}
=
\frac{
\sum_{i=1}^{n} (X_i - \bar{X})(Y_i - \bar{Y})
}{
\sqrt{
\sum_{i=1}^{n} (X_i - \bar{X})^2
}
\,
\sqrt{
\sum_{i=1}^{n} (Y_i - \bar{Y})^2
}
}
$$

where:
- $$\bar{X}$$ is the mean of \(X\)
- $$\bar{Y}$$ is the mean of \(Y\)
- $$n$$ is the number of data points

---

## 6. Important Observations

- Pearson’s correlation coefficient:
  - does **not depend on units**
  - is **scale-independent**
  - allows **fair comparison** across different datasets
- It measures only **linear relationships**
- A correlation close to zero means **no linear association**, not necessarily no relationship

---

## 7. Final Summary

- Covariance measures **joint variability**
- Pearson’s correlation **normalises covariance**
- Correlation values lie in the range:

$$
-1 \le \rho \le 1
$$

- Pearson’s correlation is widely used in:
  - finance
  - economics
  - data science
  - machine learning

In the next section, you will see **examples of correlation values**, **interpretation using data**, and **Python implementation**.

# 📘 Correlation – Example

Suppose you are given a data set containing the marks scored by a group of students in four different competitive examinations:
- JEE
- CBSE
- GRE
- NEET

We want to study whether there exists any **relationship between JEE scores and the scores of other exams**.

---

## 1. Example Dataset

| Student | JEE (X) | CBSE (Y) | GRE (Z) | NEET (T) |
|--------|---------|----------|---------|----------|
| S1 | 180 | 88 | 315 | 640 |
| S2 | 160 | 82 | 305 | 660 |
| S3 | 200 | 92 | 325 | 610 |
| S4 | 140 | 78 | 295 | 690 |
| S5 | 170 | 85 | 310 | 650 |
| S6 | 155 | 80 | 300 | 675 |

---

## 2. Objective

We will examine the correlation between the following pairs:
- JEE and CBSE
- JEE and GRE
- JEE and NEET

---

## 3. Correlation Formula (Recap)

Pearson’s correlation coefficient between two variables \(X\) and \(Y\) is given by:

$$
\rho_{X,Y} = \frac{\operatorname{Cov}(X,Y)}{\sigma_X \sigma_Y}
$$

---

## 4. Computed Correlation Values

Using the above data:

- Correlation between **JEE and CBSE**:

$$
\rho_{X,Y} \approx +0.95
$$

- Correlation between **JEE and GRE**:

$$
\rho_{X,Z} \approx +0.48
$$

- Correlation between **JEE and NEET**:

$$
\rho_{X,T} \approx -0.88
$$

---

## 5. Interpretation of Results

- The correlation between **JEE and CBSE** scores is **strongly positive**  
  → Students who perform well in JEE also tend to perform well in CBSE.

- The correlation between **JEE and GRE** scores is **moderately positive**  
  → There is some association, but it is not very strong.

- The correlation between **JEE and NEET** scores is **strongly negative**  
  → Students scoring higher in JEE tend to score lower in NEET.

---

## 6. Key Conclusions

- JEE and CBSE measure **similar academic skills**, leading to strong positive correlation.
- JEE and GRE test **partially overlapping abilities**, hence a moderate correlation.
- JEE and NEET focus on **different skill sets**, resulting in a strong negative correlation.

---

## 7. Important Observation

Even though:
- JEE, CBSE, GRE, and NEET scores are on **different scales**

The **correlation values are comparable** because:
- Covariance has been **normalised** using standard deviations.

This makes Pearson’s correlation coefficient a **scale-independent** and **reliable** measure of association.

---

## 8. Final Takeaway

- Correlation measures the **strength and direction** of a linear relationship.
- Values lie in the range:

$$
-1 \le \rho \le 1
$$

- Pearson’s correlation enables **fair comparison** across different variables and datasets.

# 📘 Correlation Using Covariance Examples

In the previous section, you learnt about **covariance** and how it measures the *direction* of the relationship between two variables. However, covariance does not tell us the *strength* of the relationship in a standardised way.

To overcome this limitation, we use **Pearson’s Correlation Coefficient**, which is a **normalised version of covariance**.

In this section, we will use the **same datasets used earlier for covariance** and compute their correlations.

---

## 1. Pearson’s Correlation Coefficient

For two variables \(X\) and \(Y\), Pearson’s correlation coefficient is defined as:

$$
\rho_{X,Y} = \frac{\operatorname{Cov}(X,Y)}{\sigma_X \sigma_Y}
$$

Where:
- \(\operatorname{Cov}(X,Y)\) is the covariance
- \(\sigma_X\) is the standard deviation of \(X\)
- \(\sigma_Y\) is the standard deviation of \(Y\)

The value of correlation always lies between:

$$
-1 \le \rho \le 1
$$

---

## 2. Example 1: Positive Correlation  
### (Pencils vs Erasers)

### Dataset

| Day | Pencils Sold (X) | Erasers Sold (Y) |
|----|-----------------|-----------------|
| Mon | 20 | 15 |
| Tue | 25 | 18 |
| Wed | 30 | 22 |
| Thu | 35 | 25 |
| Fri | 40 | 30 |

### Covariance (from earlier example)

$$
\operatorname{Cov}(X,Y) > 0
$$

### Correlation

After normalising the covariance using standard deviations:

$$
\rho_{X,Y} \approx +0.98
$$

### Interpretation

- Strong **positive correlation**
- As pencil sales increase, eraser sales also increase
- Relationship is **strong and linear**

---

## 3. Example 2: Negative Correlation  
### (Pencils vs Pens)

### Dataset

| Day | Pencils Sold (X) | Pens Sold (Y) |
|----|-----------------|---------------|
| Mon | 20 | 40 |
| Tue | 25 | 35 |
| Wed | 30 | 30 |
| Thu | 35 | 25 |
| Fri | 40 | 20 |

### Covariance (from earlier example)

$$
\operatorname{Cov}(X,Y) < 0
$$

### Correlation

$$
\rho_{X,Y} \approx -0.97
$$

### Interpretation

- Strong **negative correlation**
- As pencil usage increases, pen usage decreases
- Indicates a **substitution effect**

---

## 4. Example 3: Correlation Close to Zero  
### (Pencils vs Stamps)

### Dataset

| Day | Pencils Sold (X) | Stamps Sold (Y) |
|----|-----------------|----------------|
| Mon | 20 | 50 |
| Tue | 25 | 48 |
| Wed | 30 | 51 |
| Thu | 35 | 49 |
| Fri | 40 | 50 |

### Covariance (from earlier example)

$$
\operatorname{Cov}(X,Y) \approx 0
$$

### Correlation

$$
\rho_{X,Y} \approx -0.05
$$

### Interpretation

- Correlation is **close to zero**
- No strong linear relationship
- Changes in pencil sales do **not** affect stamp sales

---

## 5. Summary Table

| Relationship Type | Covariance Sign | Correlation Value |
|------------------|---------------|------------------|
| Strong Positive | Positive | Close to +1 |
| Strong Negative | Negative | Close to −1 |
| No Relationship | Near 0 | Close to 0 |

---

## 6. Key Takeaways

- **Covariance** tells the *direction* of a relationship
- **Correlation** tells both *direction and strength*
- Correlation is:
  - Scale-independent
  - Easy to interpret
  - Bounded between −1 and +1

---

## 7. Final Conclusion

Using the same datasets:
- Pencils & Erasers → **Strong Positive Correlation**
- Pencils & Pens → **Strong Negative Correlation**
- Pencils & Stamps → **No Linear Correlation**

This demonstrates why **correlation is preferred over covariance** when comparing relationships across datasets.

# 📘 Properties of Correlation

Correlation is a **standardised measure of association** that quantifies the **strength and direction of a linear relationship** between two variables.

---

## 1. Definition of Correlation

The Pearson correlation coefficient between two variables \(X\) and \(Y\) is defined as:

$$
\rho(X,Y) = \frac{\operatorname{Cov}(X,Y)}{\sigma_X \sigma_Y}
$$

Where:
- \(\operatorname{Cov}(X,Y)\) is the covariance between \(X\) and \(Y\)
- \(\sigma_X\) and \(\sigma_Y\) are the standard deviations of \(X\) and \(Y\)

---

## 2. Range of Correlation

The value of the correlation coefficient always lies in the interval:

$$
-1 \le \rho(X,Y) \le 1
$$

This bounded range makes correlation **scale-independent** and easy to interpret.

---

## 3. Interpretation of Correlation Values

- Correlation close to **+1**  
  → Strong **positive** linear relationship between features

- Correlation close to **−1**  
  → Strong **negative** linear relationship between features

- Correlation close to **0**  
  → **No strong linear relationship** between features

---

## 4. Symmetry (Commutative Property)

The correlation between \(X\) and \(Y\) is the same as the correlation between \(Y\) and \(X\):

$$
\rho(X,Y) = \rho(Y,X)
$$

### Proof

$$
\rho(X,Y) = \frac{\operatorname{Cov}(X,Y)}{\sigma_X \sigma_Y}
$$

Since:
$$
\operatorname{Cov}(X,Y) = \operatorname{Cov}(Y,X)
$$

and:
$$
\sigma_X \sigma_Y = \sigma_Y \sigma_X
$$

Therefore:

$$
\rho(X,Y) = \rho(Y,X)
$$

---

## 5. Self-Correlation Property

The correlation of a variable with itself is always equal to 1:

$$
\rho(X,X) = 1
$$

### Proof

$$
\rho(X,X) = \frac{\operatorname{Cov}(X,X)}{\sigma_X \sigma_X}
$$

But:
$$
\operatorname{Cov}(X,X) = \operatorname{Var}(X) = \sigma_X^2
$$

Substituting:

$$
\rho(X,X) = \frac{\sigma_X^2}{\sigma_X^2} = 1
$$

---

## 6. Summary of Key Properties

| Property | Mathematical Form |
|--------|-------------------|
| Bounded range | $$ -1 \le \rho \le 1 $$ |
| Positive correlation | $$ \rho \rightarrow +1 $$ |
| Negative correlation | $$ \rho \rightarrow -1 $$ |
| No linear relationship | $$ \rho \approx 0 $$ |
| Symmetry | $$ \rho(X,Y) = \rho(Y,X) $$ |
| Self-correlation | $$ \rho(X,X) = 1 $$ |


---

## 7. Final Takeaway

- Correlation measures **both direction and strength** of linear association
- Unlike covariance, it is:
  - Unit-free
  - Comparable across datasets
  - Easy to interpret
- Correlation does **not imply causation**, only association

## ⚠️ Correlation Does NOT Imply Causation

One of the most important cautions in statistics is:

> **Correlation does not imply causation.**

This means that **even if two variables are strongly correlated**, it does **not** mean that one variable **causes** the other to change.

---

## 1. What Correlation Tells Us

Correlation measures:
- The **direction** of a linear relationship (positive or negative)
- The **strength** of that relationship

Mathematically:

$$
\rho(X,Y) \in [-1,1]
$$

A high magnitude of correlation (close to +1 or −1) only tells us that:
- The variables **move together** in a systematic way

---

## 2. What Correlation Does NOT Tell Us

Correlation does **not** tell us:
- Whether \(X\) causes \(Y\)
- Whether \(Y\) causes \(X\)
- Whether a **third variable** is influencing both

---

## 3. Example 1: Ice Cream Sales and Drowning Incidents

Suppose we observe:
- Ice cream sales increase
- Drowning incidents also increase

The correlation between the two may be:

$$
\rho(\text{Ice Cream Sales}, \text{Drownings}) > 0
$$

### ❌ Incorrect Conclusion
- Eating ice cream causes drowning

### ✅ Correct Explanation
- A **third variable (temperature / summer season)** increases both:
  - People buy more ice cream
  - People swim more

This third variable is called a **confounding variable**.

---

## 4. Example 2: Shoe Size and Reading Ability in Children

We may find a strong positive correlation:

$$
\rho(\text{Shoe Size}, \text{Reading Ability}) > 0
$$

### ❌ Incorrect Conclusion
- Bigger shoe size causes better reading skills

### ✅ Correct Explanation
- **Age** is the hidden variable
- As children grow older:
  - Shoe size increases
  - Reading ability improves

---

## 5. Example 3: JEE Scores and CBSE Scores

We may observe:

$$
\rho(\text{JEE}, \text{CBSE}) \approx +0.95
$$

### What We Can Say
- Students who score high in JEE tend to score high in CBSE

### What We CANNOT Say
- Scoring high in JEE **causes** high CBSE scores

Both exams may be influenced by:
- Academic ability
- Preparation level
- Study habits

---

## 6. Summary Table

| Concept | Meaning |
|------|-------|
| Correlation | Measures association |
| Causation | One variable directly affects another |
| High correlation | Strong relationship |
| High correlation | **Does NOT** guarantee causation |
| Confounding variable | A third variable influencing both |

---

## 7. Final Takeaway

- Correlation is a **descriptive statistical tool**
- It is useful for:
  - Pattern detection
  - Hypothesis generation
- It is **not sufficient** to establish cause-and-effect relationships

To establish causation, we typically need:
- Controlled experiments
- Randomisation
- Domain knowledge
- Causal models

---

### ⭐ One-line Exam Tip

> **Correlation shows association, not causation.**

# 📘 Other Correlation Coefficients

So far, you have learnt about **Pearson’s product-moment correlation coefficient**, which is the most commonly used measure of correlation. However, Pearson’s correlation is not always suitable for all types of data or relationships.

Depending on the nature of the data and the type of relationship, other correlation coefficients such as **Spearman’s rank correlation** and **Kendall’s rank correlation** are also used.

---

## 1. Commonly Used Correlation Coefficients

- Pearson’s Product-Moment Correlation Coefficient  
- Spearman’s Rank Correlation Coefficient  
- Kendall’s Rank Correlation Coefficient  

---

## 2. Pearson’s Product-Moment Correlation Coefficient

### Definition

Pearson’s correlation coefficient measures the **strength and direction of a linear relationship** between two **continuous variables**.

It is generally denoted by:

$$
\rho
$$

### Key Characteristics

- Measures **linear** association
- Sensitive to **outliers**
- Requires numerical, continuous data
- Most widely used correlation measure

### When to Use

- When the relationship between variables is approximately linear
- When data is continuous and normally distributed (or close)

---

## 3. Spearman’s Rank Correlation Coefficient

### Definition

Spearman’s rank correlation coefficient measures the **strength and direction of a monotonic relationship** between two variables.

Instead of using the actual data values, it uses the **ranks** of the data.

### Key Characteristics

- Based on **ranks**, not raw values
- Captures **monotonic** relationships (increasing or decreasing)
- Less sensitive to outliers
- Works well for **ordinal data**

### When to Use

- When the relationship is monotonic but **not linear**
- When data contains outliers
- When variables are ordinal (ranked data)

---

## 4. Kendall’s Rank Correlation Coefficient

### Definition

Kendall’s rank correlation coefficient measures the **strength of association** between two variables based on the number of **concordant** and **discordant** pairs.

### Key Characteristics

- Based on pairwise comparisons
- More **robust to ties**
- Performs better with **small sample sizes**
- Interpretable as probability of agreement between rankings

### When to Use

- When sample size is small
- When data has many tied ranks
- When a more robust rank-based measure is required

---

## 5. Comparison of Correlation Coefficients

| Correlation Type | Data Used | Relationship Type | Sensitivity to Outliers |
|----------------|----------|------------------|------------------------|
| Pearson | Actual values | Linear | High |
| Spearman | Ranks | Monotonic | Moderate |
| Kendall | Ranks | Monotonic | Low |

---

## 6. Important Note

> The **most commonly used correlation coefficient** is **Pearson’s product-moment correlation coefficient**, which is often simply referred to as the **correlation coefficient** and denoted by:

$$
\rho
$$

---

## 7. Final Takeaway

- Use **Pearson’s correlation** for linear, continuous data
- Use **Spearman’s correlation** when relationships are monotonic or data is ordinal
- Use **Kendall’s correlation** for small samples or data with many ties

Choosing the correct correlation coefficient ensures **accurate and meaningful analysis**.

# 📘 Other Correlation Coefficients – Complete Notes

Correlation is not limited to Pearson’s product-moment correlation coefficient.  
When data are **ranked**, **ordinal**, **non-linear**, or contain **outliers**, rank-based correlation coefficients are preferred.

The most important ones are:
- Spearman’s Rank Correlation Coefficient
- Kendall’s Rank Correlation Coefficient

---

## 1️⃣ Spearman’s Rank Correlation Coefficient

### 🔹 Definition
**Spearman’s rank correlation coefficient** measures the **strength and direction of a monotonic relationship** between two variables using their **ranks** instead of actual values.

It is a **non-parametric** measure of correlation.

---

### 🔹 Notation
$$
\rho_s
$$

---

### 🔹 Key Idea
- Convert original data into **ranks**
- Apply Pearson correlation on the ranks
- Detects **monotonic relationships**, not necessarily linear ones

---

### 🔹 Mathematical Definition
$$
\rho_s = \rho\bigl(\text{Rank}(X), \text{Rank}(Y)\bigr)
$$

---

### 🔹 Formula (No Ties Case)
If there are no tied ranks:

$$
\rho_s = 1 - \frac{6\sum_{i=1}^{n} d_i^2}{n(n^2 - 1)}
$$

where:
- $$d_i = \text{difference between ranks of } X_i \text{ and } Y_i$$
- $$n = \text{number of observations}$$

---

### 🔹 Interpretation
| Value of \( \rho_s \) | Meaning |
|---------------------|--------|
| \(+1\) | Perfect increasing monotonic relationship |
| \(-1\) | Perfect decreasing monotonic relationship |
| \(0\) | No monotonic relationship |

---

### 🔹 When to Use Spearman’s Correlation
- Data are **ordinal or ranked**
- Relationship is **monotonic but not linear**
- Presence of **outliers**
- Different measurement scales

---

### 🧠 Example: Spearman’s Rank Correlation

#### Given Data
| Student | Math Score (X) | Rank(X) | Physics Score (Y) | Rank(Y) |
|-------|---------------|--------|------------------|--------|
| A | 90 | 1 | 88 | 2 |
| B | 85 | 2 | 92 | 1 |
| C | 80 | 3 | 78 | 3 |
| D | 70 | 4 | 65 | 4 |
| E | 60 | 5 | 55 | 5 |

#### Rank Differences
| Student | Rank(X) | Rank(Y) | \(d_i\) | \(d_i^2\) |
|-------|--------|--------|-------|----------|
| A | 1 | 2 | -1 | 1 |
| B | 2 | 1 | 1 | 1 |
| C | 3 | 3 | 0 | 0 |
| D | 4 | 4 | 0 | 0 |
| E | 5 | 5 | 0 | 0 |

$$
\sum d_i^2 = 2, \quad n = 5
$$

#### Calculation
$$
\rho_s = 1 - \frac{6 \times 2}{5(25 - 1)} = 1 - \frac{12}{120} = 0.9
$$

#### Conclusion
There is a **strong positive monotonic relationship** between Math and Physics scores.

---

## 2️⃣ Kendall’s Rank Correlation Coefficient

### 🔹 Definition
**Kendall’s rank correlation coefficient** measures the **strength of association** between two variables using **concordant and discordant pairs**.

---

### 🔹 Notation
$$
\tau
$$

---

### 🔹 Key Idea
- Compare all possible pairs of observations
- Count:
  - **Concordant pairs**
  - **Discordant pairs**

---

### 🔹 Formula
$$
\tau = \frac{C - D}{\frac{1}{2}n(n-1)}
$$

where:
- $$C = \text{number of concordant pairs}$$
- $$D = \text{number of discordant pairs}$$
- $$n = \text{number of observations}$$

---

### 🔹 Interpretation
| Value of \( \tau \) | Meaning |
|------------------|--------|
| \(+1\) | All pairs concordant |
| \(-1\) | All pairs discordant |
| \(0\) | No association |

---

## 3️⃣ Concordant and Discordant Pairs

### 🔹 Concordant Pair
Two observations  
$$
(X_i, Y_i), (X_j, Y_j)
$$
are **concordant** if:

$$
(X_i - X_j)(Y_i - Y_j) > 0
$$

➡ Both variables move in the **same direction**.

---

### 🔹 Discordant Pair
A pair is **discordant** if:

$$
(X_i - X_j)(Y_i - Y_j) < 0
$$

➡ Variables move in **opposite directions**.

---

### 🔹 Tied Pair
If:
$$
X_i = X_j \quad \text{or} \quad Y_i = Y_j
$$
the pair is **tied**.

---

### 🧠 Example: Kendall’s Rank Correlation

#### Given Data
| Observation | X | Y |
|-----------|---|---|
| 1 | 1 | 2 |
| 2 | 2 | 3 |
| 3 | 3 | 1 |
| 4 | 4 | 4 |

#### Pairwise Comparison
- Total pairs:
$$
\frac{4(4-1)}{2} = 6
$$

- Concordant pairs = 4  
- Discordant pairs = 2  

#### Calculation
$$
\tau = \frac{4 - 2}{6} = \frac{1}{3}
$$

#### Conclusion
There is a **weak positive association** between X and Y.

---

## 4️⃣ Pearson vs Spearman vs Kendall

| Feature | Pearson | Spearman | Kendall |
|------|--------|----------|---------|
| Data type | Continuous | Ranked | Ranked |
| Relationship | Linear | Monotonic | Monotonic |
| Uses ranks | ❌ | ✅ | ✅ |
| Robust to outliers | ❌ | ✅ | ✅ |
| Handles ties | ❌ | ⚠️ | ✅ |
| Sample size | Large | Medium | Small |

---

## ✅ Key Takeaways
- **Pearson** → Linear relationships on raw data  
- **Spearman** → Monotonic relationships using ranks  
- **Kendall** → Rank association via pair comparisons  

> **Most commonly used correlation coefficient:**  
> **Pearson’s product-moment correlation coefficient**, often denoted by \( \rho \).

---



# 📘 Limitations of Correlation – Complete Notes

Correlation is a powerful statistical tool for measuring **association** between two variables.  
However, correlation has several important **limitations** that must be understood to avoid misleading conclusions.

---

## 1️⃣ Limitation: Need for Adequate Data

Correlation values are **meaningful only when computed on sufficient data**.

With **very small data sets**, correlation values can appear **strong or weak purely by chance**.

---

### 🧠 Example 1: Small Data Set Giving High Correlation

#### Data
$$
X_1 = \{1, 2, 3\}
$$

$$
Y_1 = \{1, 4, 5\}
$$

#### Result
$$
\rho(X_1, Y_1) = 0.96
$$

#### Interpretation
- The correlation value is **very high**
- But the data contains **only 3 observations**
- Such a strong correlation may **not be reliable**

➡ **Conclusion:**  
With insufficient data, correlation values can be **misleading**.

---

### 🧠 Example 2: Larger Data Set with Weaker Correlation

#### Data
$$
X_2 = \{1, 2, 3, 4, 5, 6\}
$$

$$
Y_2 = \{1, 4, 5, 3, 2, 1\}
$$

#### Result
$$
\rho(X_2, Y_2) = -0.26
$$

#### Interpretation
- More data points
- Correlation value closer to zero
- Indicates **weak negative relationship**

➡ **Conclusion:**  
Larger data sets usually give **more stable and trustworthy correlation estimates**.

---

### ✅ Key Takeaway
> You must always ensure that you have **adequate data** to meaningfully interpret correlation values.

---

## 2️⃣ Limitation: Spurious Correlation

A **spurious correlation** occurs when two variables show a **strong correlation**, even though **no meaningful or logical relationship exists** between them.

---

### 🔹 Definition
A correlation that:
- Occurs **by chance**
- Is driven by **noise, coincidence, or hidden factors**
- Does **not imply any real connection**

---

### 🧠 Famous Example of Spurious Correlation

It was observed that:
- The **number of astronauts dying in spacecraft accidents**
- Is strongly correlated with
- The **number of people wearing seat belts in automobiles**

(Data from the 1980s and 1990s)

These two variables are **completely unrelated**, yet the correlation coefficient is **strongly positive**.

➡ This is a classic example of **spurious correlation**.

---

### 🔹 Why Spurious Correlations Occur
- Random chance
- Coincidental trends
- Data collection errors
- Hidden or confounding variables
- Time-based patterns

---

### 🔹 Real-World Reference
A large collection of such examples can be found at:

🔗 https://www.tylervigen.com/spurious-correlations

This website demonstrates how **strong correlations can exist without causation**.

---

## 3️⃣ Correlation Can Be Misleading

You have seen that:
- Small data sets can give **extreme correlation values**
- Unrelated variables can show **strong correlation**

Hence:
> Correlation values must always be interpreted **with context, logic, and domain knowledge**.

---

## 4️⃣ Summary of Limitations of Correlation

| Limitation | Explanation |
|----------|-------------|
| Insufficient data | Small samples can produce misleading correlation values |
| Spurious correlation | Strong correlation may exist without any real relationship |
| No causation | Correlation measures association, not cause–effect |
| Sensitive to outliers | Extreme values can distort correlation |
| Linear focus | Pearson correlation captures only linear relationships |

---

## ✅ Final Takeaways

- Correlation requires **adequate data** for meaningful interpretation
- Strong correlation does **not guarantee a real relationship**
- Spurious correlations are common in real-world data
- Always combine correlation with **logic, visualization, and domain understanding**

---

➡ **Next Topic:**  
Difference between **Correlation and Causation** and why correlation alone is not enough to make decisions.

---
# 📘 Causation and Correlation – Complete Notes

Understanding the difference between **correlation** and **causation** is critical in statistics, data analysis, and machine learning.

---

## 1️⃣ Causation vs Correlation

### 🔹 Definitions

- **Causation** means that one variable directly influences another.
- **Correlation** means that two variables move together in some way, but one may not cause the other.

---

### 🔑 Key Principle

> **Causation implies correlation, but correlation does not necessarily imply causation.**

---

### 🔍 Explanation

- If variable **X causes Y**, then **X and Y will usually be correlated**
- But if **X and Y are strongly correlated**, it does **not** mean that X causes Y

There may be:
- A third hidden variable
- Coincidence
- Measurement errors
- Reverse causation

---

### 📌 Logical Statements

- If **X → Y**, then **Correlation(X, Y)** is expected  
- If **Correlation(X, Y)** is observed, **X → Y is not guaranteed**

Hence, **correlation alone is never proof of causation**.

---

## 2️⃣ When Strong Correlation Requires Further Investigation

If two variables are strongly correlated but the **cause–effect relationship is unknown**, further investigation is required using:
- Domain knowledge
- Controlled experiments
- Causal models
- Additional data

---

## 3️⃣ Real-World Applications of Correlation

---

## 🔬 A. Scientific & Industrial Analysis

In scientific systems, **cause–effect relationships are often known in advance**.  
Correlation is used to **verify whether reality matches theory**.

---

### 🧠 Example: Electronic Circuit Efficiency

**Known fact:**  
Efficiency of electronic circuits **increases when temperature decreases**

So, expected correlation:
$$
\rho(\text{Temperature}, \text{Efficiency}) < 0
$$

---

### 📊 Observed Data

| Ambient Temperature (°C) | Efficiency (%) |
|------------------------|---------------|
| 25 | 76 |
| 22 | 74 |
| 20 | 77 |
| 18 | 72 |
| 14 | 68 |

---

### 📈 Computed Correlation

$$
\rho = +0.83
$$

---

### ❌ Interpretation

- Observed correlation is **strongly positive**
- This **contradicts known physics**
- Efficiency should increase as temperature decreases

---

### ✅ Conclusion

Something is wrong with:
- Circuit design
- Temperature control
- Measurement instruments
- Data collection process

➡ **Correlation here acts as a diagnostic tool**

---

## 🔎 B. Exploratory Data Analysis (EDA)

In EDA, **cause–effect relationships are not known beforehand**.  
Correlation is used to **discover unexpected patterns**.

---

### 🧠 Example: Online Shopping Data

| Day | Laptops Bought | Pillows Bought |
|----|---------------|----------------|
| Mon | 135 | 465 |
| Tue | 174 | 599 |
| Wed | 221 | 845 |
| Thu | 154 | 503 |
| Fri | 141 | 485 |

---

### 📈 Observation

- Strong **positive correlation** between laptops and pillows
- Products appear unrelated

---

### 🔍 Interpretation

Possible explanations:
- Bundle offers
- Festival sales
- Demographic overlap
- Recommendation algorithms
- Checkout suggestions

➡ Correlation **raises questions**, not conclusions

---

### ✅ Role of Correlation in EDA

- Detects hidden relationships
- Suggests hypotheses
- Guides deeper investigation

---

## 🤖 C. Machine Learning Applications

In machine learning:
- Highly correlated features contain **redundant information**
- Redundant features increase:
  - Computation time
  - Model complexity
  - Risk of overfitting

---

### 🧠 Example: Face Recognition Features

| Image | Mean Gray Level (X) | Information Content (Y) | Gray Level Variance (Z) |
|------|-------------------|------------------------|-------------------------|
| Image 1 | 135 | 0.4 | 1324.23 |
| Image 2 | 174 | 1.2 | 1842.49 |
| Image 3 | 221 | 0.6 | 1555.32 |
| Image 4 | 154 | 2.4 | 2009.21 |
| Image 5 | 141 | 5.6 | 2230.15 |

---

### 📊 Correlation Results

$$
\rho(X, Y) = -0.43
$$

$$
\rho(Y, Z) = 0.88
$$

$$
\rho(Z, X) = -0.23
$$

---

### 🔍 Interpretation

- **Information Content (Y)** and **Gray Level Variance (Z)** are strongly correlated
- Both capture similar texture/intensity information

---

### ✅ Feature Selection Decision

One of the features (e.g., **Z**) can be dropped to:
- Reduce redundancy
- Improve training speed
- Simplify the model
- Improve generalization

➡ Correlation helps in **feature engineering**

---

## 4️⃣ Final Summary

- **Causation implies correlation**
- **Correlation does not imply causation**
- Correlation must be interpreted with:
  - Domain knowledge
  - Logic
  - Additional evidence

---

## 📌 Key Takeaways

- Strong correlation is **not proof of cause**
- Correlation can:
  - Detect faults (engineering)
  - Reveal patterns (EDA)
  - Optimize models (machine learning)
- Always ask **why**, not just **how strong**

---

➡ **Next Topic:**  
📘 *How to establish causation: experiments, control variables, and causal inference*


# 📘 Causation and Correlation – Complete Notes

Understanding the difference between **correlation** and **causation** is critical in statistics, data analysis, and machine learning.

---

## 1️⃣ Causation vs Correlation

### 🔹 Definitions

- **Causation** means that one variable directly influences another.
- **Correlation** means that two variables move together in some way, but one may not cause the other.

---

### 🔑 Key Principle

> **Causation implies correlation, but correlation does not necessarily imply causation.**

---

### 🔍 Explanation

- If variable **X causes Y**, then **X and Y will usually be correlated**
- But if **X and Y are strongly correlated**, it does **not** mean that X causes Y

There may be:
- A third hidden variable
- Coincidence
- Measurement errors
- Reverse causation

---

### 📌 Logical Statements

- If **X → Y**, then **Correlation(X, Y)** is expected  
- If **Correlation(X, Y)** is observed, **X → Y is not guaranteed**

Hence, **correlation alone is never proof of causation**.

---

## 2️⃣ When Strong Correlation Requires Further Investigation

If two variables are strongly correlated but the **cause–effect relationship is unknown**, further investigation is required using:
- Domain knowledge
- Controlled experiments
- Causal models
- Additional data

---

## 3️⃣ Real-World Applications of Correlation

---

## 🔬 A. Scientific & Industrial Analysis

In scientific systems, **cause–effect relationships are often known in advance**.  
Correlation is used to **verify whether reality matches theory**.

---

### 🧠 Example: Electronic Circuit Efficiency

**Known fact:**  
Efficiency of electronic circuits **increases when temperature decreases**

So, expected correlation:
$$
\rho(\text{Temperature}, \text{Efficiency}) < 0
$$

---

### 📊 Observed Data

| Ambient Temperature (°C) | Efficiency (%) |
|------------------------|---------------|
| 25 | 76 |
| 22 | 74 |
| 20 | 77 |
| 18 | 72 |
| 14 | 68 |

---

### 📈 Computed Correlation

$$
\rho = +0.83
$$

---

### ❌ Interpretation

- Observed correlation is **strongly positive**
- This **contradicts known physics**
- Efficiency should increase as temperature decreases

---

### ✅ Conclusion

Something is wrong with:
- Circuit design
- Temperature control
- Measurement instruments
- Data collection process

➡ **Correlation here acts as a diagnostic tool**

---

## 🔎 B. Exploratory Data Analysis (EDA)

In EDA, **cause–effect relationships are not known beforehand**.  
Correlation is used to **discover unexpected patterns**.

---

### 🧠 Example: Online Shopping Data

| Day | Laptops Bought | Pillows Bought |
|----|---------------|----------------|
| Mon | 135 | 465 |
| Tue | 174 | 599 |
| Wed | 221 | 845 |
| Thu | 154 | 503 |
| Fri | 141 | 485 |

---

### 📈 Observation

- Strong **positive correlation** between laptops and pillows
- Products appear unrelated

---

### 🔍 Interpretation

Possible explanations:
- Bundle offers
- Festival sales
- Demographic overlap
- Recommendation algorithms
- Checkout suggestions

➡ Correlation **raises questions**, not conclusions

---

### ✅ Role of Correlation in EDA

- Detects hidden relationships
- Suggests hypotheses
- Guides deeper investigation

---

## 🤖 C. Machine Learning Applications

In machine learning:
- Highly correlated features contain **redundant information**
- Redundant features increase:
  - Computation time
  - Model complexity
  - Risk of overfitting

---

### 🧠 Example: Face Recognition Features

| Image | Mean Gray Level (X) | Information Content (Y) | Gray Level Variance (Z) |
|------|-------------------|------------------------|-------------------------|
| Image 1 | 135 | 0.4 | 1324.23 |
| Image 2 | 174 | 1.2 | 1842.49 |
| Image 3 | 221 | 0.6 | 1555.32 |
| Image 4 | 154 | 2.4 | 2009.21 |
| Image 5 | 141 | 5.6 | 2230.15 |

---

### 📊 Correlation Results

$$
\rho(X, Y) = -0.43
$$

$$
\rho(Y, Z) = 0.88
$$

$$
\rho(Z, X) = -0.23
$$

---

### 🔍 Interpretation

- **Information Content (Y)** and **Gray Level Variance (Z)** are strongly correlated
- Both capture similar texture/intensity information

---

### ✅ Feature Selection Decision

One of the features (e.g., **Z**) can be dropped to:
- Reduce redundancy
- Improve training speed
- Simplify the model
- Improve generalization

➡ Correlation helps in **feature engineering**

---

## 4️⃣ Final Summary

- **Causation implies correlation**
- **Correlation does not imply causation**
- Correlation must be interpreted with:
  - Domain knowledge
  - Logic
  - Additional evidence

---

## 📌 Key Takeaways

- Strong correlation is **not proof of cause**
- Correlation can:
  - Detect faults (engineering)
  - Reveal patterns (EDA)
  - Optimize models (machine learning)
- Always ask **why**, not just **how strong**

---

➡ **Next Topic:**  
📘 *How to establish causation: experiments, control variables, and causal inference*


# 📘 Standard Deviation = 0 — Complete Notes

Standard deviation is a measure of **dispersion** or **spread** in a data set.  
It tells us how much the values deviate from the mean.

---

## 1️⃣ When Is Standard Deviation Equal to 0?

> **Standard deviation is equal to 0 if and only if all values in the data set are exactly the same.**

---

## 2️⃣ Mathematical Explanation

Consider a data set:

$$
X = \{x_1, x_2, \dots, x_n\}
$$

The mean is:

$$
\mu = \frac{1}{n} \sum_{i=1}^{n} x_i
$$

The standard deviation is:

$$
\sigma = \sqrt{\frac{1}{n} \sum_{i=1}^{n} (x_i - \mu)^2}
$$

If:

$$
x_1 = x_2 = \dots = x_n = c
$$

then:

$$
\mu = c
$$

and:

$$
(x_i - \mu) = 0 \quad \forall i
$$

So:

$$
\sigma = \sqrt{0} = 0
$$

---

## 3️⃣ Intuitive Understanding

- No variation in data
- Every value equals the mean
- No spread or dispersion

➡ **Perfect consistency → Standard deviation = 0**

---

## 4️⃣ Examples

### Example 1: Constant Values
$$
X = \{10, 10, 10, 10\}
$$

- Mean = 10  
- Standard deviation = **0**

---

### Example 2: Identical Prices
$$
P = \{250, 250, 250\}
$$

- All menu prices are the same
- No variability

---

### Example 3: Same Exam Scores
$$
S = \{75, 75, 75, 75, 75\}
$$

- All students scored the same
- Zero spread

---

## 5️⃣ When Is Standard Deviation NOT Zero?

Standard deviation becomes **greater than 0** if **even one value differs**.

| Data Set | Reason |
|--------|--------|
| $$\{10, 10, 11\}$$ | One value differs |
| $$\{5, 6, 7\}$$ | Clear variation |
| $$\{100, 100, 101\}$$ | Slight spread |

---

## 6️⃣ Important Properties

- Standard deviation is **never negative**
- Minimum possible value is **0**
- Measures **spread, not central value**

---

## 7️⃣ Relation to Correlation

Pearson’s correlation formula:

$$
\rho(X,Y) = \frac{\text{Cov}(X,Y)}{\sigma_X \cdot \sigma_Y}
$$

If:

$$
\sigma_X = 0 \quad \text{or} \quad \sigma_Y = 0
$$

then:

- Correlation is **undefined**
- Division by zero occurs

---

## 8️⃣ Key Takeaways

- **Standard deviation = 0** ⟺ all values are identical
- Indicates **no variability**
- Happens only in **constant data sets**
- Even one different value makes SD > 0

---

## 📝 Exam-Friendly One-Liner

> *Standard deviation is zero when all observations in a data set are equal, indicating no variation.*

---
