# 📘 Master Notes: Vectors in Machine Learning

### *Comprehensive Exam Preparation Guide*

---

## 📑 Table of Contents

1. **Conceptual Foundations** (Mental Models, Dot Product, Norm)
2. **Vector Projection** (The Shadow & Formula)
3. **Interpreting the Scalar $k$** (Strength of Contribution)
4. **Similarity vs. Proximity** (Critical Distinction)
5. **Orthogonality & Decomposition** (Independence in Data)
6. **Applications in Machine Learning**
7. **Numerical Examples**
8. **Python Implementation** (Projection, Similarity, Distance Metrics)

---

## 1. Conceptual Foundations

Before building models, we must understand how vectors relate to each other.

| Concept               | Question It Answers                        | Geometric Intuition        |
| --------------------- | ------------------------------------------ | -------------------------- |
| **Dot Product**       | Do two vectors grow in the same direction? | Directional multiplication |
| **Magnitude (Norm)**  | How large is the vector?                   | Length of the arrow        |
| **Cosine Similarity** | Are vectors aligned in angle?              | Direction only             |
| **Projection**        | How much of one vector lies along another? | Shadow on a direction      |
| **Distance (Norm)**   | How close are two vectors?                 | Physical closeness         |

---

### A. Dot Product

$$
\mathbf{v}*1 \cdot \mathbf{v}*2 = \sum_i v*{1i} v*{2i}
$$

* Depends on **direction and magnitude**
* Zero dot product ⇒ orthogonal vectors
* Used in projections, regression, neural networks

---

### B. Magnitude (Norm)

$$
||\mathbf{v}|| = \sqrt{\sum_i v_i^2}
$$

* Measures vector length
* Needed for normalization and cosine similarity

---

## 2. Vector Projection

**Definition:**

> Projection answers: **"How much of vector $\mathbf{v}_1$ lies in the direction of $\mathbf{v}_2$?"**

Geometrically, projection is the **shadow** of one vector onto another.

### Projection Formula

$$
\text{proj}_{\mathbf{v}_2}(\mathbf{v}_1) = \left( \frac{\mathbf{v}_1 \cdot \mathbf{v}_2}{\mathbf{v}_2 \cdot \mathbf{v}_2} \right) \mathbf{v}_2
$$

---

## 3. Interpreting the Scalar $k$

$$
k = \frac{\mathbf{v}_1 \cdot \mathbf{v}_2}{\mathbf{v}_2 \cdot \mathbf{v}_2}
$$

Think of $k$ as **"how strongly this feature speaks for the data point."**

| Value of $k$  | Interpretation                |
| ------------- | ----------------------------- |
| $k \approx 0$ | Orthogonal → no contribution  |
| $0 < k < 1$   | Weak to moderate alignment    |
| $k \approx 1$ | Strong alignment              |
| $k > 1$       | Strong / extreme contribution |
| $k < 0$       | Opposite influence            |

> **Exam Tip:** $k$ is **not bounded** between -1 and 1.

---

## 4. Similarity vs. Proximity

This distinction is crucial in Machine Learning.

### A. Similarity (Cosine Similarity)

**Question:** Do vectors point in the same direction?

$$
\cos(\theta) = \frac{\mathbf{v}_1 \cdot \mathbf{v}_2}{||\mathbf{v}_1|| , ||\mathbf{v}_2||}
$$

* Range: $[-1, 1]$
* Scale-invariant
* Used in NLP, embeddings, recommendation systems

---

### B. Proximity (Distance)

**Question:** How close are the vectors in space?

$$
||\mathbf{v}_1 - \mathbf{v}_2||
$$

* Range: $[0, \infty)$
* Sensitive to magnitude
* Used in KNN, clustering, anomaly detection

---

### C. Summary Rule

> **Normalize for similarity, use distance for proximity, dot product for projection.**

---

## 5. Orthogonality & Decomposition

### Orthogonality

$$
\mathbf{v}_1 \cdot \mathbf{v}_2 = 0
$$

* Means vectors are perpendicular
* In ML: features are independent

---

### Decomposition

Any vector can be decomposed as:

$$
\mathbf{v}*1 = \text{proj}*{\mathbf{v}_2}(\mathbf{v}_1) + \big(\mathbf{v}*1 - \text{proj}*{\mathbf{v}_2}(\mathbf{v}_1)\big)
$$

* Parallel component + residual (error)
* Foundation of least squares and PCA

---

## 6. Applications in Machine Learning

| Algorithm           | Role of Vectors                   |
| ------------------- | --------------------------------- |
| Linear Regression   | Projection onto weight vector     |
| Logistic Regression | Decision score $w \cdot x$        |
| SVM                 | Distance to hyperplane            |
| PCA                 | Orthogonal projections            |
| Neural Networks     | Neuron activation via dot product |

---

## 7. Numerical Examples

### Example 1: Non-Orthogonal

$\mathbf{v}_1 = [6,7], ; \mathbf{v}_2 = [0.9,0.1]$

* Dot product = 6.1
* $||\mathbf{v}_2||^2 = 0.82$
* $k \approx 7.44$
* Projection = $[6.70, 0.74]$

**Interpretation:** Strong contribution along feature direction.

---

### Example 2: Orthogonal

$\mathbf{v}_1 = [3,4], ; \mathbf{v}_2 = [4,-3]$

* Dot product = 0
* Projection = $[0,0]$

**Interpretation:** No shared information.

---

## 8. Python Implementation (Lab Ready)

```python
import math

# --- Basic Operations ---

def dot_product(v1, v2):
    return sum(x*y for x, y in zip(v1, v2))

def magnitude(v):
    return math.sqrt(sum(x**2 for x in v))

def vector_subtract(v1, v2):
    return [x - y for x, y in zip(v1, v2)]

def scale(v, k):
    return [k*x for x in v]

# --- Similarity & Projection ---

def cosine_similarity(v1, v2):
    mag1, mag2 = magnitude(v1), magnitude(v2)
    if mag1 == 0 or mag2 == 0:
        return 0
    return dot_product(v1, v2) / (mag1 * mag2)

def project(v1, v2):
    denom = dot_product(v2, v2)
    if denom == 0:
        raise ValueError("Zero vector projection undefined")
    k = dot_product(v1, v2) / denom
    return scale(v2, k)

# --- Distance Metrics ---

def l1_distance(v1, v2):
    return sum(abs(x) for x in vector_subtract(v1, v2))

def l2_distance(v1, v2):
    return magnitude(vector_subtract(v1, v2))

def lp_distance(v1, v2, p):
    diff = vector_subtract(v1, v2)
    return sum(abs(x)**p for x in diff)**(1/p)
```

---

## ⭐ Final Exam Takeaway

> **Similarity compares direction, proximity compares distance, projection measures contribution.**
