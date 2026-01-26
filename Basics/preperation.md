# 📘 Exam & Coding Questions Reference

---

## 1. Integration of Cubic Equation

**Example:**

```python
# Indefinite integral
from sympy import symbols, integrate
x = symbols('x')
expr = 3*x**3 - 5*x**2 + 2*x - 7
integral = integrate(expr, x)
print(integral)  # 3*x**4/4 - 5*x**3/3 + x**2 - 7*x
```

**Definite integral example:**

```python
integrate(x**3 - 2*x**2 + x, (x,1,2))  # 7/12
```

**Substitution example:**

```python
# Integral of (2x+1)^3
u = 2*x + 1
integrate(u**3/2, x)  # (2x+1)^4/8
```

---

## 2. Probability: Dice Combinations

**Problem:** One 10-sided die and one 8-sided die. Count combinations with sum > 12.

**Solution:**

* Use formula: (\sum_{x=1}^{m} \max(0, n - (S - x)))
* Result = 21 combinations.

---

## 3. Probability: Spam Filter

**Given:**

* Spam = 20%
* Filter marks spam correctly = 90%
* Non-spam wrongly marked as spam = 10%

**Find:** P(Not Spam | Marked Spam)

**Solution:**

```python
P_not_spam_given_marked = (0.1*0.8)/(0.9*0.2 + 0.1*0.8)  # 0.308
```

---

## 4. OTP Pattern Count

**4-character OTP:** 3 digits + 1 letter (A-Z, a-z), any order.

**Solution:**

```python
# Choices
digits = 10**3  # 3 digits
letters = 52     # 1 letter
arrangements = 4 # positions of the letter
total = digits * letters * arrangements  # 208000
```

---

## 5. Probability: Balls without Replacement

**Given:** 4 red, 3 blue, 5 green. Pick 2 balls without replacement. Probability none are green.

**Solution:**

```python
P = (7/12) * (6/11)  # 7/22
```

---

## 6. Python String Slicing

```python
S = "ALGORITHM"
result = S[-2:1:-2]  # 'HIO'
```

---

## 7. Dictionary Get Fix

**Original code (incorrect):**

```python
d = {'a':1,'b':2}
s = d.get('c', d.get('a'), d.get('b'))  # Error: too many args
```

**Fixed version:**

```python
d = {'a':1,'b':2}
s = d.get('c', d.get('a', d.get('b')))  # Output: 1
```

**Alternative using or:**

```python
s = d.get('c') or d.get('a') or d.get('b')
```

---

## 8. Coding Problem: Find Z from X and Y

**Given:**
( X = A + B, Y = A - B, Z = A*B )

**Formula:**
( Z = (X^2 - Y^2)/4 )

**Python Code:**

```python
def find_Z(X, Y):
    return (X**2 - Y**2)/4

# Example
X = 10
Y = 4
print(find_Z(X,Y))  # 21.0
```

---

## 9. Set Problem

**Primes < 30:** {2,3,5,7,11,13,17,19,23,29}
**Multiples of 6 < 30:** {6,12,18,24}

* Intersection = ∅
* Union = {2,3,5,6,7,11,12,13,17,18,19,23,24,29}

---

## 10. Operational Units

**Given:** 10 units (0-9), down = {2,4,7}

* Operational units = 10 - 3 = 7
* Operational units numbers = {0,1,3,5,6,8,9}

