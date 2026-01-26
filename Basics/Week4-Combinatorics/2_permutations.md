# 📘 Permutations – Corrected & Expanded Notes

---

## 1. Review of Counting Principles

### 🔹 Addition Rule (OR Rule)

Use this rule when **only one** of several **mutually exclusive** options can be chosen.

**Example:**

* Choose a snack: chips **or** fruit
* Ways = ways(chips) + ways(fruit)

---

### 🔹 Multiplication Rule (AND Rule)

Use this rule when a task consists of **sequential steps** that all occur together.

**Example:**

* Shirt (3 choices) **and** Pants (2 choices)
* Ways = 3 × 2 = 6

---

## 2. Slot–Label Method

A structured way to apply counting rules:

* Each **slot** represents a position or stage
* Count choices per slot
* Multiply choices across slots

**Example:**
Form a 3-digit number:

| Slot     | Choices  |
| -------- | -------- |
| Hundreds | 9 (1–9)  |
| Tens     | 10 (0–9) |
| Units    | 10 (0–9) |

Total = 9 × 10 × 10 = **900**

---

## 3. Permutations (Order Matters)

A **permutation** is an **arrangement** of objects where **order is important**.

We study **linear permutations** only (arrangements in a row).

---

## 4. Permutations of Distinct Objects (All Objects Used)

### 🔹 Example: Shapes

Objects: Square, Triangle, Circle

| Position | Choices |
| -------- | ------- |
| 1st      | 3       |
| 2nd      | 2       |
| 3rd      | 1       |

Total arrangements = 3 × 2 × 1 = **6**

---

## 5. Permutations Using Product Rule (Seating Example)

Three friends: Gurmeet, Nikita, Sakshi
Seats: 23, 24, 25

| Seat | Choices |
| ---- | ------- |
| 23   | 3       |
| 24   | 2       |
| 25   | 1       |

Total arrangements = 3 × 2 × 1 = **6**

---

## 6. Factorial Notation

For any natural number n:

**n! = n × (n−1) × (n−2) × ... × 1**

Examples:

* 3! = 6
* 5! = 120

---

## 7. General Form of Permutations (All Objects)

If **n distinct objects** are arranged in **n places**:

$$[ P(n,n) = n! ]$$

---

## 8. Permutations of k Objects Out of n Objects

When **order matters** and **not all objects are used**:

$$[ P(n,k) = \frac{n!}{(n-k)!} ]$$

---

### 🔹 Example: Letters

Letters: P, Q, R (n = 3)
Select k = 2

$$[ P(3,2) = \frac{3!}{1!} = 6 ]$$

Arrangements:
(P,Q), (Q,P), (P,R), (R,P), (Q,R), (R,Q)

---

### 🔹 Example: Numbers

Digits: {1,2,3,4}
Form 2-digit numbers without repetition:

$$[ P(4,2) = \frac{4!}{2!} = 12 ]$$

---

## 9. Programming Logic Question (Corrected)

Function: F(A=, B=, C=)

* A → Number
* B, C → Strings

Inputs:

* X → Number
* Y, Z → Strings

Total permutations of X,Y,Z = 3! = 6

Valid permutations (X in position A):

* (X,Y,Z)
* (X,Z,Y)

Invalid permutations = 6 − 2 = **4**

---

## 10. Python Implementation

### 🔹 Using Logic

```python
count = 0
items = ['P','Q','R']
for i in items:
    for j in items:
        if i != j:
            count += 1
print(count)
```

---

### 🔹 Using itertools

```python
from itertools import permutations

list(permutations(['P','Q','R'], 2))
```

---

## 11. Common Mistakes to Avoid

❌ Confusing combinations with permutations
❌ Forgetting order matters
❌ Using n! instead of P(n,k)
❌ Counting numbers with leading zeros

---

## 12. Practice Quiz

### Q1. How many ways can 5 people sit on 3 chairs?

A. 60
B. 120
C. 20
D. 10

✔ Answer: **A (P(5,3) = 60)**

---

### Q2. How many 2-letter codes from A,B,C without repetition?

✔ Answer: **6**

---

### Q3. Is 123 and 321 the same permutation?

✔ Answer: **No (order matters)**

---

## 13. Key Takeaways

* Permutations = **arrangement**
* Order always matters
* Use **factorials** for efficiency
* Apply **slot-label method** for clarity

---

📌 *These notes are exam-ready and conceptually complete.*
