# 📘 Permutations with Repetition – Corrected & Exam‑Ready Notes

---

## 1. Recap: What You Already Know

Previously, you studied **permutations of distinct elements without repetition**, where:

$$[
P(n,n) = n!
]$$

and more generally,

$$[
P(n,k) = \frac{n!}{(n-k)!}
]$$

These formulas apply **only when repetition is NOT allowed**.

---

## 2. Permutations with Repetition (Core Idea)

When **repetition is allowed**:

* Objects can be reused
* Each position has the **same number of choices**
* The **product rule** applies directly

---

## 3. General Formula: Permutations with Repetition

If:

* `n` = number of **distinct objects**
* `k` = number of **positions (slots)**

Then the number of permutations **with repetition allowed** is:

$$[
\boxed{n^k}
]$$

---

## 4. Slot‑Label Explanation (Very Important)

Think in terms of slots:

```
Slot₁   Slot₂   Slot₃   ...   Slotₖ
 n   ×   n   ×   n   ×  ...  ×  n
```

Since **each slot can take any of the `n` objects**, the total is:

$$[
\underbrace{n \times n \times \cdots \times n}_{k \text{ times}} = n^k
]$$

---

## 5. Simple Visual Example

### Example: Two figures

Objects: {A, B}
Slots: 2

Possible arrangements:

* AA, AB, BA, BB

Total:
$$[
2^2 = 4
]$$

---

## 6. Lottery Example (Corrected)

Three friends: Anil, Sunil, Nikhil

Two lotteries: Lot1, Lot2

* A person **can win more than one lottery**

| Slot | Choices |
| ---- | ------- |
| Lot1 | 3       |
| Lot2 | 3       |

Total ways:
$$[
3^2 = \boxed{9}
]$$

---

## 7. Key Observations ⭐

* Repetition allowed → **same choices for every slot**
* No factorials involved
* Order matters
* Formula depends only on **choices per slot × number of slots**

---

## 8. Recall Quiz – OMR Sheet (Fully Corrected)

### Problem

* 10 questions
* 4 options each
* One option per question

Each question = 4 choices

[
\text{Total ways} = 4^{10}
]

### Slot Method:

```
[ ] [ ] [ ] [ ] [ ] [ ] [ ] [ ] [ ] [ ]
```

Each slot → 4 choices

---

## 9. True / False – 3‑Digit Odd Numbers

Digits: {1,2,3}
Repetition allowed
Must be **odd**

| Slot     | Choices |
| -------- | ------- |
| Hundreds | 3       |
| Tens     | 3       |
| Units    | 2 (1,3) |

$$[
3 \times 3 \times 2 = \boxed{18}
]$$

❌ Given statement (27) is **FALSE**

---

## 10. Applications of Product Rule

### Example: 5‑Digit Numbers

Digits: 0–9
Repetition allowed

| Slot        | Choices |
| ----------- | ------- |
| First       | 9 (1–9) |
| Remaining 4 | 10 each |

$$[
9 \times 10^4
]$$

---

## 11. Word Formation Example

Word: **DEPOSIT** (7 distinct letters)
Form **4‑letter words** (repetition allowed)

$$[
7^4 = \boxed{2401}
]$$

---

## 12. Ordered Selection Example (Array)

Set: {61, 62, ..., 100} → 40 numbers
Slots: 20

$$[
40^{20}
]$$

---

## 13. Quiz: 7‑Digit Odd Numbers

Digits: 0–9

| Slot       | Choices |
| ---------- | ------- |
| First      | 9       |
| Middle 5   | 10 each |
| Last (odd) | 5       |

$$[
9 \times 10^5 \times 5
]$$

---

## 14. True / False Questions

### Q1

> 4‑letter words from X,Y,Z with repetition

$$[
3^4 = 81
]$$

❌ Statement (64) is **FALSE**

---

### Q2

> 3 candidates, 6 voters

Each voter has 3 choices:

$$[
3^6 = 729
]$$

❌ Statement (1024) is **FALSE**

---

## 15. Python Connection

```python
from itertools import product

options = [1,2,3,4]
len(list(product(options, repeat=10)))  # 4^10
```

---

## 16. Final Takeaways ⭐

* **Permutations with repetition = n^k**
* Always identify:

  * number of slots
  * choices per slot
* Slot method avoids mistakes
* Widely used in exams, coding & probability

---
