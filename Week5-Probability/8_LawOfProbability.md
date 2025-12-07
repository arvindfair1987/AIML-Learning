# 📘 Law of Total Probability — Complete Notes


## 🧠 1. What Is the Law of Total Probability?

The **Law of Total Probability** allows us to find the probability of an event **A**
by considering all the different **cases** (or conditions) under which **A** can occur.

👉 It is essentially a **weighted average of conditional probabilities**.

---

## 🧩 2. Splitting the Sample Space

Suppose the sample space is partitioned into events  

$$
\{ B_1, B_2, \dots, B_n \}
$$

These events must be:

## Mutually Exclusive

Only one event can occur at a time.

$$
B_i \cap B_j = \varnothing,\quad i \ne j
$$

## Collectively Exhaustive

They cover all possibilities.

$$
B_1 \cup B_2 \cup \dots \cup B_n = S
$$


---

## 📐 3. Mathematical Statement

Let **A** be the event of interest.

### Basic form:
$$ P(A) = P(A \cap B_1) + P(A \cap B_2) + \dots + P(A \cap B_n) $$

### Using the Multiplication Rule:
$$
P(A \cap B_i) = P(B_i) \cdot P(A \mid B_i)
$$

### ✅ Final Working Formula:
$$
\boxed{
P(A) = \sum_{i=1}^{n} P(B_i)\, P(A \mid B_i)
}
$$

---

## 🔁 4. The Golden Pattern (Very Important)

### **Split → Multiply → Add**

| Step | What You Do | Meaning |
|----|----|----|
| **Split** | Identify cases $$B_i$$ | Break the situation into disjoint cases |
| **Multiply** | $$P(B_i) \times P(A \mid B_i)$$ | Probability of event happening *in that case* |
| **Add** | Sum all products | Overall probability |

✅ **Memory One-liner:**  
> **Overall chance = sum of (case probability × chance inside that case)**

---

## 📘 5. Worked Examples

---

### ✅ Example 1: Coin from Two Bags

**Scenario**
- Bag A chosen with probability **0.5**, fair coin → $$P(H \mid A)=0.5$$
- Bag B chosen with probability **0.5**, biased coin → $$P(H \mid B)=0.75$$

### Calculation

P(H) = (0.5 × 0.5) + (0.5 × 0.75)  
P(H) = 0.25 + 0.375 = 0.625


✅ Probability of getting Head = **0.625**

---

### ✅ Example 2: Factory Defects

**Scenario**
- Factory A produces **70%**, defect rate **2%**
- Factory B produces **30%**, defect rate **5%**

### Calculation

P(D) = (0.70 x 0.02) + (0.30 x 0.05)

P(D) = 0.014 + 0.015 = 0.029


✅ Probability an item is defective = **2.9%**

---

### ✅ Example 3: Exam Pass Probability

**Scenario**
- Studied well: **40%**, pass rate **90%**
- Did not study well: **60%**, pass rate **30%**

**Calculation**
$$
P(\text{Pass}) = (0.4 \times 0.9) + (0.6 \times 0.3)
$$
$$
= 0.36 + 0.18 = 0.54
$$

✅ Probability of passing = **54%**

---

### ✅ Example 4: Routes to Work

**Scenario**
- Route A chosen **60%**, late **10%**
- Route B chosen **40%**, late **25%**

**Calculation**
$$
P(\text{Late}) = (0.6 \times 0.1) + (0.4 \times 0.25)
$$
$$
= 0.06 + 0.10 = 0.16
$$

✅ Probability of being late = **16%**

---

## 🩺 6. Practical Example: Medical Test (Very Important)

### Blood Test Reliability

**Scenario**
- Disease prevalence:  
  $$
  P(D) = 0.01,\quad P(D^c) = 0.99
  $$
- Test accuracy:
  - $$P(+ \mid D) = 0.95$$ (True Positive)
  - $$P(+ \mid D^c) = 0.10$$ (False Positive)

---

### Step-by-Step Solution

**Split**
- Case 1: Has disease $$D$$
- Case 2: Does not have disease $$D^c$$

**Multiply**
$$
P(D)\times P(+\mid D) = 0.01 \times 0.95 = 0.0095
$$
$$
P(D^c)\times P(+\mid D^c) = 0.99 \times 0.10 = 0.099
$$

**Add**
$$
P(+) = 0.0095 + 0.099 = 0.1085
$$

✅ **Overall Probability of Positive Test = 10.85%**

---

## 🎯 7. Key Takeaways

- The law works **only if cases form a partition**
- It combines **conditional probability** with **weighted averages**
- Used heavily in:
  - Medical testing
  - Machine learning
  - Risk analysis
  - Bayesian inference

---

## 🧠 Final Memory Sentence

> **Split the world into cases, multiply inside each case, then add them up.**

---

