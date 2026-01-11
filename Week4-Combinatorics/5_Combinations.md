# 📘 Combinations

---

## 1️⃣ Introduction to Combinations

The concept of **combinations** deals with the number of ways of **selecting objects**, **without considering the order** of selection.

Until now, you have learned how to **arrange** objects (permutations).  
In combinations, we are only concerned with **which objects are selected**, not their positions.

---

## 2️⃣ Motivating Example (Selection vs Arrangement)

Suppose there are **3 distinct shapes**.

- Number of **arrangements**:
$$
3! = 6
$$

- Number of **selections of all 3 shapes**:
$$
1
$$

Even though the shapes can be arranged in many ways, the **selection remains the same**.

---

## 3️⃣ Definition of Combination

Let:
$$
S = \{a_1, a_2, a_3, \dots, a_n\}
$$

be a set of **n distinct elements**.

The number of ways of selecting **k elements** from this set is denoted by:

$$
{}^{n}C_k \quad \text{or} \quad C(n,k) \quad \text{or} \quad \binom{n}{k}
$$

### Formula:
$$
\boxed{{}^{n}C_k = \frac{n!}{k!(n-k)!}}
$$

---

## 4️⃣ Example: Selecting All Objects

Select **3 objects out of 3 distinct objects**:

$$
{}^{3}C_3 = \frac{3!}{3! \cdot 0!} = 1
$$

✔ Matches the manual observation.

---

## 5️⃣ Relation Between Permutations and Combinations

### Question  
In how many ways can **r balls** be selected from **n distinct balls**?

### Key Relationship:
$$
{}^{n}P_r = {}^{n}C_r \times r!
$$

Equivalently:
$$
\boxed{{}^{n}C_r = \frac{{}^{n}P_r}{r!}}
$$

---

## 6️⃣ Example: Handshake Problem

If there are **12 persons** at a party and each pair shakes hands **exactly once**:

Each handshake is a **selection of 2 people**.

$$
{}^{12}C_2 = \frac{12 \times 11}{2} = 66
$$

### ✅ Answer: **66**

---

## 7️⃣ True / False Question

> “The number of ways of selecting r objects out of n objects is ${}^{n}C_r$.”

### ✅ Answer: **True**

---

## 8️⃣ Combinations Using Python

### Using basic logic

```python
def combination(n, k):
    def factorial(n):
        result = 1
        for i in range(2, n + 1):
            result *= i
        return result

    return factorial(n) // (factorial(k) * factorial(n - k))

print("Number of ways to select 4 volunteers out of 10:", combination(10, 4))
````

---

### Using `itertools`

```python
from itertools import combinations

elements = ['a', 'b', 'c', 'd']
comb = list(combinations(elements, 2))

print(comb)
print("Number of ways to select 2 elements out of 4:", len(comb))
```

Output:

```
[('a', 'b'), ('a', 'c'), ('a', 'd'),
 ('b', 'c'), ('b', 'd'), ('c', 'd')]
Number of ways = 6
```

---

## 9️⃣ Many-One Mapping: Permutations → Combinations

### Example: Select 2 letters from `{a, b, c, d}`

* Permutations:
  $$
  {}^{4}P_2 = 12
  $$

Permutations:
$$
ab, ba, ac, ca, ad, da, bc, cb, bd, db, cd, dc
$$

* Combinations:
  $$
  {}^{4}C_2 = 6
  $$

Combinations:
$$
{a,b}, {a,c}, {a,d}, {b,c}, {b,d}, {c,d}
$$

Each combination corresponds to:
$$
2! = 2
$$
permutations.

Hence, the mapping from permutations to combinations is **many-one**.

---

## 🔟 Important Observations — Part 1

* Valid range:
  $$
  0 \le k \le n
  $$

* Key identity:
  $$
  {}^{n}C_k = \frac{{}^{n}P_k}{k!}
  $$

* Equivalent notations:
  $$
  {}^{n}C_k = C(n,k) = \binom{n}{k}
  $$

* Combinations represent **unordered selections**

---

## 1️⃣1️⃣ Important Observations — Part 2 (Subsets)

The number of **k-element subsets** of an **n-element set** is:
$$
{}^{n}C_k
$$

### Example:

Let:
$$
n = 3,\quad k = 2
$$

Set:
$$
{a,b,c}
$$

Subsets of size 2:
$$
{a,b}, {a,c}, {b,c}
$$

So:
$$
{}^{3}C_2 = 3
$$

---

## 1️⃣2️⃣ Recall Quiz

### Statement:

> “There are 50 subsets of size 3 of a set with 10 elements.”

Compute:
$$
{}^{10}C_3 = \frac{10 \times 9 \times 8}{6} = 120
$$

### ❌ Answer: **False**

---

### Verify identity:

$$
{}^{15}C_5 = \frac{{}^{15}P_5}{5!}
$$

✔ **True**

---

### Many-One Mapping Statement

> “We can always define a many-one function from the permutations of 3 objects out of 6 distinct objects to the combinations of 3 elements out of those 6 objects.”

### ✅ Answer: **True**

---

## 1️⃣3️⃣ Combination Examples

### Example 1: Word **DEPOSIT**

Letters:
$$
D, E, P, O, S, I, T
$$

All distinct → 7 letters

Select **3 letters**:
$$
{}^{7}C_3 = 35
$$

---

### Example 2: Admission Test

* Total questions = 100
* Attempted questions = 40

Number of selections:
$$
{}^{100}C_{40}
$$

---

## 1️⃣4️⃣ Symmetry Property

$$
{}^{n}C_r = {}^{n}C_{n-r}
$$

### Example:

$$
{}^{11}C_8 = {}^{11}C_3
$$

---

## 1️⃣5️⃣ Team Selection Problem

Select:

* 6 batsmen out of 10
* 1 wicket-keeper out of 2
* 4 bowlers out of 8

Total ways:
$$
{}^{10}C_6 \times {}^{2}C_1 \times {}^{8}C_4
$$

Compute:
$$
210 \times 2 \times 70 = 29400
$$

---

## 1️⃣6️⃣ Selecting at Least One Object

Select **at least one object** from **3 distinct objects**:

$$
{}^{3}C_1 + {}^{3}C_2 + {}^{3}C_3
$$

OR directly:
$$
2^3 - 1 = 7
$$

---

## 🔚 Summary

* **Permutations** → order matters
* **Combinations** → order does not matter
* Key formula:
  $$
  \boxed{{}^{n}C_k = \frac{n!}{k!(n-k)!}}
  $$
* Fundamental identity:
  $$
  {}^{n}P_k = {}^{n}C_k \cdot k!
  $$
* Widely used in:

  * Team selection
  * Committees
  * Subsets
  * Probability problems

---

✅ **You are now fully exam-ready on combinations.**

### Generalized Equation: **Selecting *at least one* object out of ( n ) distinct objects**

---

## 🔹 Key idea

“Selecting at least one” means you can select:

[
1,\ 2,\ 3,\ \dots,\ n \text{ objects}
]

Order **does not matter** (this is a *selection*, not an arrangement), so we use **combinations**.

---

## 🔹 Generalized equation

The total number of ways is:

[
\boxed{\sum_{r=1}^{n} \binom{n}{r}}
]

---

## 🔹 Closed-form (important result)

Using the binomial identity:

[
\sum_{r=0}^{n} \binom{n}{r} = 2^n
]

So,

[
\sum_{r=1}^{n} \binom{n}{r}
= 2^n - \binom{n}{0}
= \boxed{2^n - 1}
]

---

## 🔹 Final generalized equation

[
\boxed{\text{Number of ways to select at least one object from } n
= 2^n - 1}
]

---

## 🔹 Why this works (intuition you won’t forget)

* Each object has **2 choices**: selected or not selected
* For ( n ) objects → ( 2^n ) total subsets
* One subset is empty (selecting nothing)
* Remove it → ( 2^n - 1 )

---

## 🔹 Small example (exam-safe)

Let ( n = 3 ), objects = {A, B, C}

Subsets:
[
{A},{B},{C},{A,B},{A,C},{B,C},{A,B,C}
]

Count = **7**

[
2^3 - 1 = 7 \quad \checkmark
]

---

## 🔹 One-line exam answer ⭐

> The number of ways to select at least one object from ( n ) distinct objects is
> [
> \boxed{2^n - 1}
> ]

If you want, I can also give:

* 🔁 **With repetition allowed**
* 🔢 **Order matters version**
* 🧠 **Power-set / binary explanation**
* 📝 **Markdown exam notes**

Just say the word 👍

### Generalized Equation: **Selecting *at least 2* objects out of ( n ) distinct objects**

---

## 🔹 Key idea

“At least 2” means you can select:

[
2,\ 3,\ 4,\ \dots,\ n \text{ objects}
]

Since **order does not matter**, we use **combinations**.

---

## 🔹 Generalized equation (direct form)

[
\boxed{\sum_{r=2}^{n} \binom{n}{r}}
]

---

## 🔹 Closed-form simplification (important)

We use the identity:
[
\sum_{r=0}^{n} \binom{n}{r} = 2^n
]

Subtract the unwanted cases:

* Selecting **0** objects → ( \binom{n}{0} = 1 )
* Selecting **1** object → ( \binom{n}{1} = n )

So,

[
\sum_{r=2}^{n} \binom{n}{r}
= 2^n - \binom{n}{0} - \binom{n}{1}
= \boxed{2^n - 1 - n}
]

---

## 🔹 Final generalized equation

[
\boxed{\text{Number of ways to select at least 2 objects from } n
= 2^n - n - 1}
]

---

## 🔹 Small example (quick check)

Let ( n = 4 )

[
\binom{4}{2} + \binom{4}{3} + \binom{4}{4}
= 6 + 4 + 1 = 11
]

Using formula:
[
2^4 - 4 - 1 = 16 - 5 = 11 \quad \checkmark
]

---

## 🔹 General pattern (very useful)

For **selecting at least ( k )** objects:

[
\boxed{\sum_{r=k}^{n} \binom{n}{r}
= 2^n - \sum_{r=0}^{k-1} \binom{n}{r}}
]

---

## 🔹 One-line exam-ready answer ⭐

> The number of ways to select at least 2 objects from ( n ) distinct objects is
> [
> \boxed{2^n - n - 1}
> ]

If you want, I can:

* Extend this to **at least ( k )** (full generalization)
* Do the **order matters** version
* Add **repetition allowed**
* Convert this into **Markdown exam notes**

Just tell me 😊
