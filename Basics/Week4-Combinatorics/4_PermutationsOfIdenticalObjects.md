# 📘 Permutations of Identical Objects

---

## 1️⃣ Introduction

So far, we have studied **permutations of distinct objects**.  
Now, we extend this idea to situations where **some objects are identical (repeated)**.

When identical objects are present, simply using $$n!$$ will **overcount** arrangements because swapping identical objects does not create a new permutation.

---

## 2️⃣ General Formula

Suppose there are:

- $$n$$ total objects  
- $$n_1$$ identical objects of type 1  
- $$n_2$$ identical objects of type 2  
- $$\dots$$  
- $$n_k$$ identical objects of type $$k$$  

where:
$$
n = n_1 + n_2 + \dots + n_k
$$

### ✅ Number of distinct permutations:
$$
\boxed{\frac{n!}{n_1! \; n_2! \; \cdots \; n_k!}}
$$

---

## 3️⃣ Example 1: Word **BOOK**

Letters in **BOOK**:
- B → 1 time
- O → 2 times
- K → 1 time

Total letters:
$$
n = 4
$$

### Apply the formula:
$$
\frac{4!}{1! \cdot 2! \cdot 1!} = \frac{24}{2} = 12
$$

### ✅ Number of distinct arrangements = **12**

---

## 4️⃣ Example 2: Forming 7-digit numbers  
Digits given: **1, 1, 2, 2, 4, 4, 4**

Digit counts:
- 1 → 2 times
- 2 → 2 times
- 4 → 3 times

Total digits:
$$
n = 7
$$

### Number of distinct numbers:
$$
\frac{7!}{2! \cdot 2! \cdot 3!}
$$

---

## 5️⃣ Example 3: Word **MATHEMATICS**

Letters:
```

M M A A T T H E I C S

```

Counts:
- M → 2
- A → 2
- T → 2
- Others → 1 each

Total letters:
$$
n = 11
$$

### Number of distinct words:
$$
\frac{11!}{2! \cdot 2! \cdot 2!}
$$

---

## 6️⃣ Example 4: Seating Arrangement Problem

Out of **100 applicants**:
- 21 are named Rajat (identical)
- 33 are named Rahul (identical)
- Remaining 46 are distinct

### Number of seating arrangements:
$$
\frac{100!}{21! \cdot 33!}
$$

(Only identical people need factorial division.)

---

## 7️⃣ Key Observations ⭐

- Division by factorials **removes overcounting**
- Only **identical objects** appear in the denominator
- Order **always matters** in permutations

---

## 8️⃣ Practice Questions

### Q1️⃣ How many unique permutations of the word **LOOSE** exist?

Letters:
- L → 1
- O → 2
- S → 1
- E → 1

Total letters:
$$
n = 5
$$

### ✅ Answer:
$$
\frac{5!}{2!} = 60
$$

---

### Q2️⃣ How many unique permutations of the word **COCOON** exist?

Letters:
- C → 2
- O → 3
- N → 1

Total letters:
$$
n = 6
$$

### ✅ Answer:
$$
\frac{6!}{2! \cdot 3!} = 60
$$

---

### Q3️⃣ True or False

**Statement:**  
> “Given $$n$$ objects, out of which $$x$$ are of type 1, $$y$$ are of type 2, and $$z$$ are of type 3, the total number of permutations is  
> $$\frac{n!}{(x+y+z)!}$$.”

### ❌ Answer: **False**

### ✔ Correct formula:
$$
\frac{n!}{x! \cdot y! \cdot z!}
$$

---

## 9️⃣ Common Exam Mistakes ⚠️

- ❌ Forgetting to divide by factorials of repeated objects
- ❌ Adding factorials instead of multiplying
- ❌ Using combinations instead of permutations

---

## 🔟 Python Connection (Conceptual)

Although mathematics gives the exact count, Python can be used to **generate and verify** permutations using:

- Basic recursion
- `itertools.permutations()` (with filtering for uniqueness)

---

## 🧾 Summary

- Permutations of identical objects correct **overcounting**
- Formula used:
$$
\boxed{\frac{n!}{n_1! n_2! \dots n_k!}}
$$
- This concept is widely used in:
  - Word arrangements
  - Seating problems
  - Number formation
  - Probability and statistics

---

✅ **You are now exam-ready on permutations of identical objects.**
```

