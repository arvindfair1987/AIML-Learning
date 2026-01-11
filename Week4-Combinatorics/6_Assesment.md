# 📘 Fundamental Counting Principles & Recall Notes

---

## 🔹 Fundamental Counting Principles

### Example 1: 5-digit odd numbers using digits {2,3,4,7,8}

- Digits available = 5
- Repetition allowed (not stated otherwise)
- Last digit must be **odd** → {3, 7} → **2 choices**

Slots:

| Place | Choices |
|-----|--------|
| 1st | 5 |
| 2nd | 5 |
| 3rd | 5 |
| 4th | 5 |
| 5th (odd) | 2 |

$$
5 \times 5 \times 5 \times 5 \times 2 = 1250
$$

✅ **Answer: 1250**

---

### Example 2: Bakery Selection (Addition Rule)

Cupcakes = 30  
Muffins = 35  
Doughnuts = 25  

Since **only one item** is chosen:

$$
30 + 35 + 25 = 90
$$

✅ **Answer: 90**

---

### Example 3: Number Lock (5 rings, 4 numbers each)

- 5 slots
- 4 choices per slot

$$
4^5 = 1024
$$

✅ **Answer: 1024**

---

### Example 4: Tossing a coin twice

Possible outcomes:
$$
\{HH, HT, TH, TT\}
$$

Total outcomes:
$$
2^2 = 4
$$

✅ **Statement is TRUE**

---

### Example 5: 10 Lamps (ON/OFF)

- Each lamp has 2 states
- At least one lamp must be ON

$$
2^{10} - 1 = 1023
$$

✅ **Answer: 1023**

---

### Example 6: Travel Routes via Mumbai

- Mumbai → Kolkata: 3 ways  
- Mumbai → Delhi: 7 ways  

By multiplication rule:

$$
3 \times 7 = 21
$$

✅ **Statement is TRUE**

---

## 🔹 Permutations – Recall Quiz

### Q1: Four-letter words from “GATE” (no repetition)

$$
4! = 24
$$

---

### Q2: Arrange 3 books out of 10 different books

$$
{}^{10}P_3 = \frac{10!}{7!} = 10 \times 9 \times 8 = 720
$$

---

### Q3: Statement

> “The number of arrangements of k objects out of n distinct objects is n!, where k < n.”

❌ **FALSE**

Correct formula:
$$
{}^{n}P_k = \frac{n!}{(n-k)!}
$$

---

### Q4: Seating 26 women and 32 men in a row

Total people:
$$
26 + 32 = 58
$$

All are distinct:
$$
58!
$$

---

### Q5: 5-digit numbers using {1–7}, digits distinct

$$
{}^{7}P_5 = \frac{7!}{2!} = 2520
$$

---

### Q6: Statement

> $P(n,k) = P(n,n-k)$

❌ **FALSE**

Correct identity:
$$
{}^{n}P_k \neq {}^{n}P_{n-k}
$$

---

## 🔹 Permutations with Repetition – Recall Quiz

### Q1: Word “DISCRETE”

Letters:
- E appears twice
- Total letters = 8

$$
\frac{8!}{2!}
$$

---

### Q2: 4-digit even numbers

- Last digit → {0,2,4,6,8} → 5 choices
- First digit ≠ 0 → 9 choices

$$
9 \times 10 \times 10 \times 5 = 4500
$$

---

### Q3: Coin Distribution

Coins:
- 10p ×2
- 20p ×2
- 25p ×3
- 50p ×1

Total coins = 8

$$
\frac{8!}{2!2!3!}
$$

---

### Q4: Statement

> “The number of ways of arranging n identical objects in a row is 1.”

✅ **TRUE**

---

### Q5: 4-letter words from “MISSISSIPPI” (distinct letters)

Distinct letters available:
$$
\{M, I, S, P\}
$$

Choose 4 distinct letters and arrange:

$$
4! = 24
$$

❌ Factorial-division method is **NOT applicable here**

---

### Q6: Statement

> “The number of ways of arranging 5 alphabets in 6 places (repetition allowed) is $6^5$.”

❌ **FALSE**

Correct:
- 6 slots
- 5 choices per slot

$$
5^6
$$

---

## 🔹 Combinations – Recall Quiz

### Q1: Select 7 boys and 4 girls

- Boys: ${}^{12}C_7$
- Girls: ${}^{8}C_4$

$$
{}^{12}C_7 \times {}^{8}C_4
$$

---

### Q2: Eldest always included

- Total members = 10
- Eldest fixed
- Choose remaining 3 from 9

$$
{}^{9}C_3
$$

---

### Q3: Distribute 10 balls into groups of 2,3,5

$$
{}^{10}C_2 \times {}^{8}C_3 \times {}^{5}C_5
$$

Simplifies to:
$$
\frac{10!}{2!3!5!}
$$

---

### Q4: Intersection of 7 lines

Each pair intersects:

$$
{}^{7}C_2 = 21
$$

---

### Q5: 3-letter words with at least one vowel

- Total permutations:
$$
{}^{6}P_3 = 120
$$

- No vowels (only consonants):
$$
{}^{4}P_3 = 24
$$

- At least one vowel:
$$
120 - 24 = 96
$$

---

### Q6: Statement

> “Maximum number of triangles from 40 points is $C(40,37)$.”

Since:
$$
{}^{40}C_3 = {}^{40}C_{37}
$$

✅ **TRUE**

---

## 🔹 Programming Task: Combinations

### Python Code (Correct)

```python
n = int(input())
k = int(input())

def factorial(n):
    if n == 0 or n == 1:
        return 1
    return n * factorial(n - 1)

def calculate_combinations(n, k):
    return factorial(n) / (factorial(k) * factorial(n - k))

print(calculate_combinations(n, k))
