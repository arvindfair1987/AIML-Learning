# 📘 Counting Principles – Professor Notes

---

## 1️⃣ Addition Rule (OR Rule)

### 🔹 Statement

If a task can be done **in one of several mutually exclusive (disjoint) ways**, then the total number of ways is the **sum** of the number of ways of each option.

If sets $A_1, A_2, \dots, A_n$ are **pairwise disjoint**, then:

$$
|A_1 \cup A_2 \cup \cdots \cup A_n| = |A_1| + |A_2| + \cdots + |A_n|
$$

---

### ✈️ Example 1: Travel Options

Suppose you need to travel from **Mumbai to New Delhi**.

* Flights available = 14
* Trains available = 12

You can choose **only one mode of transport**.

$$
\text{Total choices} = 14 + 12 = 26
$$

✔️ Flights and trains are **disjoint choices**.

---

### 👕 Generalisation of Addition Rule

Suppose you have:

* 4 shirts
* 3 trousers
* 5 pants

You need to choose **only one garment**.

$$
4 + 3 + 5 = 12
$$

✔️ Shirts, trousers, and pants form **three disjoint sets**.

---

### 🍽️ Example 2: Restaurant Menu

* Veg items = 4
* Non-veg items = 7

You want to order **only one item**.

$$
4 + 7 = 11
$$

✔️ Veg and non-veg items are **distinct and disjoint**.

---

### 📱 Example 3: Buying a Mobile Phone

Available phones:

* Redmi = 7
* Samsung = 11
* iPhone = 12

Choosing **one phone**:

$$
7 + 11 + 12 = 30
$$

✔️ Correct. All phone types form **disjoint sets**.

---

### 🧸 True / False Question

**Statement:** The number of ways to select one item from 6 toys and 7 dolls is 12.

**Solution:**

$$
6 + 7 = 13
$$

❌ Statement is **False**.

---

## 2️⃣ Multiplication Rule (AND Rule)

### 🔹 Statement

If a task consists of **multiple independent stages**, and each stage has a fixed number of choices, then the total number of ways is the **product** of the choices at each stage.

If stage 1 has $m$ choices and stage 2 has $n$ choices, then:

$$
\text{Total ways} = m \times n
$$

---

### 👔 Example 1: Shirt and Trouser

* Shirts = 4 ($s_1, s_2, s_3, s_4$)
* Trousers = 3 ($t_1, t_2, t_3$)

Selecting **one shirt AND one trouser**:

$$
4 \times 3 = 12
$$

✔️ Choice of shirt is **independent** of trouser choice.

---

### 🔑 Important Observations

* Multiplication rule applies to **independent stages**
* Creates **ordered pairs** $(s, t)$
* Order of stages does **not** affect the total count

$$
|S \times T| = |T \times S|
$$

✔️ What matters is the **size of the Cartesian product**, not the order of sets.

---

### 👖 Generalisation of Multiplication Rule

* Shirts = 3
* Pants = 4
* Trousers = 2

Selecting one from each:

$$
3 \times 4 \times 2 = 24
$$

---

### 🔤 Example: Vowel and Consonant

Letters: ${A, B, C, D, E, F, G, H}$

* Vowels = ${A, E}$ → 2
* Consonants = ${B, C, D, F, G, H}$ → 6

$$
2 \times 6 = 12
$$

---

### 🚩 Example: Flag of Two Different Colours

Colours = ${R, B, Y, G}$

Order matters in a flag.

$$
4 \times 3 = 12
$$

Equivalent permutation form:

$$
{}^4P_2 = 12
$$

---

### 🃏 Example: Selecting an Ace and a King

* Aces = 4
* Kings = 4

$$
4 \times 4 = 16
$$

✔️ Independent selections.

---

## 3️⃣ Slot-Label Method

### 🍬 Example 1: Candy and Pen

* Candies = 10
* Pens = 15

Two slots:

$$
10 \times 15 = 150
$$

---

### 👗 Example 2: Product Selection

Sets:

* $S = {\text{Arrow, Peter England, Cambridge}}$ → 3
* $P = {\text{Chanel, Kourse}}$ → 2

$$
3 \times 2 = 6
$$

---

### 🔐 Example 3: Password of 10 Letters

Each slot can be filled in 26 ways.

$$
26^{10}
$$

---

### 🚘 Example 4: Vehicle Number Plate

* Letters = 4 slots → $26^4$
* Numbers = 6 slots → $10^6$

$$
26^4 \times 10^6
$$

---

## 4️⃣ Combining Addition and Multiplication Rules

### 🔑 Password with Letters and Digits

* Letters = 26
* Digits = 10

Each slot:

$$
26 + 10 = 36
$$

Total passwords (10 slots):

$$
36^{10}
$$

---

## 5️⃣ Three-Digit Natural Numbers

* First digit: $1$–$9$ → 9 choices
* Remaining digits: $0$–$9$ → 10 each

$$
9 \times 10 \times 10 = 900
$$

✔️ Numbers like $001$ are **not** three-digit numbers.

---

## 6️⃣ Two-Letter Words (Distinct Letters)

Letters: ${A, B, D, F, H}$

Slot method:

$$
5 \times 4 = 20
$$

✔️ Letters cannot repeat.

---

## 7️⃣ Colouring Squares

* Squares = 8
* Colours = 10

Each square can be coloured independently:

$$
10^8
$$

---

## ⭐ Exam Summary

* **Addition Rule** → OR, disjoint choices
* **Multiplication Rule** → AND, independent stages
* **Slot-Label Method** → Large counting problems
* Leading zeros **do not** create new numbers
* Order matters → **Permutations**

---

✨ *These notes are corrected, structured, and exam-ready.*
