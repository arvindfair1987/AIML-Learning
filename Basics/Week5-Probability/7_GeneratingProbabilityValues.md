# **Probability Approaches in Statistics & Finance**

---

# 🎲 **1. Equal Likelihood Approach (Classical / A Priori Probability)**

### **Definition (Expanded)**

This is used when:

* All outcomes are **symmetrical**,
* No outcome has more "weight" or influence than another,
* There is **no need for historical data**.

It is based purely on **logic** and the physical properties of the system.

---

### **Formula**

If an experiment has **N equal outcomes**, then:

$P(\text{any single outcome}) = \frac{1}{N}$


---

### **More Examples**

* Drawing a card from a **well-shuffled** deck:

  $P(\text{Ace of Hearts}) = \frac{1}{52}$
  
* Choosing a number at random from 1 to 10:
  $
  \frac{1}{10}
  $

---

### **Finance Examples (Expanded)**

1. **Binomial Option Pricing Model (starting assumption)**

   * One period model assumes only **two equally likely states** (up or down) *before* probabilities are adjusted to risk-neutral ones.

2. **Equal weighting in early portfolio modelling**

   * When no information is known, analysts may assume all scenarios (e.g., recessions, expansions, neutral conditions) are equally likely.

3. **Stress Testing (basic version)**

   * Sometimes early versions of stress tests assume equal likelihood across a set of predefined economic scenarios.

---

### **Advantages**

* Simple to use
* No data required
* Works well for fair, symmetric situations

### **Limitations**

* **Rarely realistic in finance**, because markets are not symmetric
* Assumes fairness that often does not exist
* Fails when outcomes have different probabilities

---

---

# 📊 **2. Relative Frequency Approach (Empirical Probability)**

### **Definition (Expanded)**

Probabilities are derived from **observed frequencies** of events over repeated trials or from large historical datasets. The more data we have, the more accurate the probability becomes.

---

### **Formula**

$
P(\text{event}) = \frac{\text{Number of times event occurred}}{\text{Total number of observations}}
$

---

### **More Examples**

* If 30 students out of 200 get an A:
  $
  P(A) = \frac{30}{200} = 0.15
  $

---

### **Finance Examples (Expanded)**

1. **Historical Volatility Estimation**

   * Analysts compute standard deviation of past returns to estimate future volatility.

2. **Expected Return Calculation**

   * Past average returns are used to estimate expected returns in portfolio theory.

3. **Insurance Premium Pricing**

   * Actuaries use historical death rates, accident frequencies, etc.

4. **Default Probability (PD)** in credit risk

   * Banks estimate PD using 5–30 years of default history by rating category.

5. **Market Risk Measures: VaR, CVaR**

   * Based on historical daily losses.

---

### **Advantages**

* Based on real-world data
* Often accurate when large sample sizes exist
* Most widely used in risk management and finance

### **Limitations**

* History **may not repeat itself**
* Not useful for **new products** or **rare events**
* Biased if market conditions change

---

---

# 🤔 **3. Judgemental (Subjective) Approach**

### **Definition (Expanded)**

Probabilities are derived from:

* **Human reasoning**
* **Expert intuition**
* **Experience and knowledge**
* **Qualitative factors**

It is often used when:

* No data exists
* Data is unreliable
* Future conditions differ dramatically from the past

---

### **More Examples**

* Predicting whether a start-up will succeed
* Estimating the chance of a political decision passing
* Evaluating the probability of new technology being adopted globally

---

### **Finance Examples (Expanded)**

1. **IPO Valuation for New Firms**

   * With limited financial history, analysts rely heavily on qualitative judgement.

2. **Mergers & Acquisitions**

   * Judgement is used to estimate synergies that cannot be historically measured.

3. **Forecasting Regulatory Changes**

   * Probabilities depend on political and expert opinion, not data.

4. **Predicting Market Sentiment**

   * Investors often rely on judgement for investor psychology and behavioural shifts.

5. **Black Swan Probability Assignment**

   * Since rare events have limited history, subjective judgement is needed.

---

### **Advantages**

* Useful when history is limited or irrelevant
* Allows incorporation of expert insight, intuition, and qualitative information
* Essential for new markets, emerging technology, policy changes

### **Limitations**

* **Biased opinions** can affect probability
* Different experts may give different probabilities
* Hard to justify or defend
* Not scientific unless structured properly

---

---

# 🔗 **Combining All Three Approaches (Expanded)**

Finance often blends approaches for more reliable forecasts.

---

## **1. Relative Frequency + Judgemental**

**Most common combination in the real world.**

### Example: Analyst Forecasting Stock Returns

* **Start:** Calculate historical average return (relative frequency).
* **Adjust:** Increase or decrease the probability based on new CEO, industry change, or new technology (judgemental).

> **This creates a REALISTIC forecast with both data and expert insight.**

---

## **2. Equal Likelihood + Relative Frequency**

### Example: Monte Carlo Simulations

* Equal likelihood → Each simulated draw from the distribution is random
* Relative frequency → Historical data sets the distribution’s shape (mean & variance)

This creates **mathematically fair simulations grounded in real data**.

---

## **3. Equal Likelihood + Relative Frequency + Judgemental**

### Example: Pricing a Corporate Bond

* **Relative Frequency:** Base default rate = historical rating-based defaults
* **Judgemental:** Analyst adjusts based on recent events (bad management, new risks)
* **Equal Likelihood:** Some valuation models assume equal probability across discrete economic states (e.g., recession, neutral, expansion)

This gives the **most balanced real-world estimate**.

---

---

# 📚 **Extended Summary Table**

| Approach               | Based On         | Good For                                  | Weak For                    | Finance Examples                                             |
| ---------------------- | ---------------- | ----------------------------------------- | --------------------------- | ------------------------------------------------------------ |
| **Equal Likelihood**   | Logic & symmetry | Simple models, games, initial assumptions | Real markets, biased events | Binomial pricing (initial assumptions), equal up/down models |
| **Relative Frequency** | Historical data  | Risk models, trends, common events        | New markets, rare events    | VaR, PD estimates, historical vol, expected returns          |
| **Judgemental**        | Expert opinion   | Unique events, new industries             | Bias, subjectivity          | IPO pricing, geopolitical risk, M&A predictions              |

---

# ⭐ **Final Memory Trick**

To remember the three approaches:

* **Equal = Fair → No data → Theory**
* **Frequency = Past → Lots of data → History**
* **Judgement = Brain → No data → Experience**

-------------------------------------

# 📘 Relationship Between Set Theory and Probability Theory 

Probability theory in the axiomatic framework (Kolmogorov, 1933) uses set theory to define **possible outcomes**, but probability to assign **likelihood**.  
This distinction is essential in financial modelling.

---

## 🏛️ 1. Foundations: Set Theory vs. Probability Theory

| Concept | Role of Set Theory | Role of Probability Theory |
|--------|---------------------|----------------------------|
| **Sample Space $S$** | Lists all possible outcomes. | Must satisfy **$P(S)=1$**. |
| **Event $A$** | A subset of $S$. | Assigned a likelihood **$P(A)\ge0$**. |
| **Set Operations $(\cup,\cap,\complement)$** | Describe structural relationships between events. | Axioms define how probabilities behave under these operations. |

### ✔ Key Principle  
Set theory describes **what can happen**,  
Probability assigns **how likely** each outcome is.

---

## 💰 2. Set Theory in Capital Markets: Defining Sample Spaces

| Capital Market Scenario | Sample Space $S$ | Example Event $A \subseteq S$ |
|------------------------|-----------------|----------------------------------|
| Daily Stock Move | $\{\text{Up},\text{Down},\text{Unchanged}\}$ | $A=\{\text{Up}\}$ |
| Bond Rating Migration | $\{\text{Upgrade},\text{A},\text{BBB},\text{BB},\text{Default}\}$ | $A=\{\text{Default}\}$ |
| Option Expiry | $\{\text{ITM},\text{OTM}\}$ | $A=\{\text{ITM}\}$ |
| Index Return | $\{r \ge -1\}$ | $A=\{r>0\}$ |

> The sample space **does not** reveal whether an outcome is 5%, 10%, or 80% likely.

---

## 🎲 3. Probability Measures: Kolmogorov’s Axioms

### ⭐ Axiom 1: Non-Negativity  
$P(A)\ge 0$

**Finance Example:**  
A probability of default can never be negative: $P(\text{Default}) = 0.05 \ge 0$

### ⭐ Axiom 2: Normalisation  
$P(S)=1$

**Finance Example:**  
For a stock with outcomes Up/Down/Flat:  
$P(\text{Up}) + P(\text{Down}) + P(\text{Flat}) = 1$

### ⭐ Axiom 3: Additivity (Mutually Exclusive Events)

If two events are mutually exclusive, then the probability of their union is the sum of their probabilities.

$$
A \cap B = \varnothing \;\Rightarrow\; P(A \cup B) = P(A) + P(B)
$$

**Finance Example:**

- \(A\): Stock price rises by at least 2%
- \(B\): Stock price falls by at least 2%

Since both events cannot occur simultaneously:

$$ P(A \cup B) = P(A) + P(B) $$
---

## ⚛️ 4. Scientific Example: Radioactive Decay

Sample space: $S=\{\text{Decay},\text{No Decay}\}$

Probability of decay in time $t$:  
$P(\text{Decay}) = 1 - e^{-t/\tau}$

For $t=10$, $\tau=100$:  
$P(\text{Decay}) \approx 0.0952$  
$P(\text{No Decay}) \approx 0.9048$

> Set theory gave us the outcomes; the physics gave us the probabilities.

---

## 💡 5. Capital Market Example: Credit Rating Migration

BBB-rated bond possible outcomes:

| Outcome | Symbol | Probability |
|--------|--------|-------------|
| Upgrade to AA | $R_1$ | 0.02 |
| Upgrade to A | $R_2$ | 0.08 |
| Remain BBB | $R_3$ | 0.70 |
| Downgrade to BB | $R_4$ | 0.15 |
| Default | $R_5$ | 0.05 |

### Complex Events:

- **Investment-grade outcome:** $I = R_1 \cup R_2 \cup R_3$  
- **Distress outcome:** $D = R_4 \cup R_5$

### Apply Additivity:

$P(I)=P(R_1)+P(R_2)+P(R_3)=0.02+0.08+0.70=0.80$

---

## 🧠 6. Why Sets Alone Cannot Describe Probabilities

Sample space: $S=\{\text{Recession},\text{No Recession}\}$

Set theory **does not tell us**:

- $P(\text{Recession})=0.01$  
- $P(\text{Recession})=0.10$  
- $P(\text{Recession})=0.40$  

Probabilities require:  
- **Historical data**  
- **Judgement**  
- **Models**  

---

## 🧮 7. Non-Mutually Exclusive Events: Inclusion–Exclusion Principle

- $A=\{\text{Stock Market Rises}\}$  
- $B=\{\text{Bond Yields Fall}\}$  

These can happen together:

$$
P(A\cup B)=P(A)+P(B)-P(A\cap B)
$$

**Finance Applications:**  
- Portfolio VaR  
- Systemic risk  
- Joint default probability  
- Copula models  

---

## 📝 8. Uniform vs Non-Uniform Probabilities

### Uniform (Classical)  
$S=\{\text{H},\text{T}\}$  
$P(\text{H})=P(\text{T})=0.5$

### Non-Uniform (Finance Analogy)
$P(\text{H}) = 3k$, $P(\text{T}) = k$  
$4k=1 \Rightarrow k=0.25$  
$P(\text{H})=0.75$, $P(\text{T})=0.25$

> Models asymmetric risks and skewed returns.

---

## 🏁 9. Final Conclusion

| Set Theory | Probability Theory |
|------------|------------------|
| Defines all possible outcomes | Assigns numerical likelihood |
| Uses unions, intersections, complements | Uses axioms for consistency |
| Gives structure | Gives meaning |

**In capital markets:**  
- Set theory defines scenarios: up/down/default/upgrade  
- Probability theory assigns likelihood using historical data, judgement, or models (Monte Carlo, Black-Scholes, rating matrices)  
- Together, they form the foundation for risk management, derivative pricing, credit modelling, forecasting, and systemic risk analysis.

-------------------------------

# 📘 Joint, Marginal, and Conditional Probability

Probability helps us **measure the likelihood of events**. When events are related, we need **joint**, **marginal**, and **conditional probabilities**.

---

## 1️⃣ Basic Definitions

### Marginal Probability

* **Definition:** Probability of a single event occurring, ignoring other events.  
* **Notation:** `P(A)`  
* **Example:** Rolling a die, probability of getting an even number:  
  `P(Even) = 3/6 = 0.5`

---

### Joint Probability

* **Definition:** Probability that **two events occur together**.  
* **Notation:** `P(A ∩ B)` or `P(A,B)`  
* **Example:** Rolling a die, probability of **even number AND number >3**:

  * Even numbers: 2, 4, 6  
  * Numbers >3: 4, 5, 6  
  * Common numbers: 4, 6  
  `P(Even ∩ >3) = 2/6 ≈ 0.333`

---

### Conditional Probability

* **Definition:** Probability of **one event given another occurred**.  
* **Notation:** `P(A|B) = P(A ∩ B) / P(B)` (if `P(B) ≠ 0`)  
* **Example:** Probability of getting even **given number >3**:

  * Numbers >3: 4, 5, 6  
  * Even among them: 4, 6  
  `P(Even | >3) = 2/3 ≈ 0.667`

---

### Independence vs Dependence

* **Independent Events:** Occurrence of one event does **not affect** the other.  
  `P(A ∩ B) = P(A) × P(B)`  
  *Example:* Toss a coin twice: first toss heads and second toss heads are independent.  

* **Dependent Events:** Occurrence of one event **affects** the probability of the other.  
  `P(A ∩ B) ≠ P(A) × P(B)`  
  *Example:* Draw two cards without replacement from a deck; probability of second card being red depends on the first draw.  

---

## 2️⃣ Step-by-Step Approach

1. Define events clearly (e.g., `A = Even`, `B = >3`)  
2. Identify sample space `S` (e.g., `{1,2,3,4,5,6}`)  
3. Determine relevant outcomes:

   * Joint: `A ∩ B`  
   * Conditional: `P(A|B) = P(A ∩ B) / P(B)`

4. Compute probability: favorable outcomes / total outcomes  

---

## 3️⃣ Questions: Simple → Advanced

### Simple Questions

**Q1:** Toss a coin twice. Let:

* `A = First toss is Heads`  
* `B = Second toss is Tails`  

* Find joint probability `P(A ∩ B)`  
* Find marginal probabilities `P(A)` and `P(B)`  
* Find conditional probability `P(A|B)`

**Solution:**

* Sample space: `{HH, HT, TH, TT}`  
* `A ∩ B = {HT}` → `P(A ∩ B) = 1/4`  
* `P(A) = 2/4 = 0.5`, `P(B) = 2/4 = 0.5`  
* `P(A|B) = (1/4) / (2/4) = 0.5`  

---

### Medium Questions

**Q2:** A bag has 3 red and 2 blue balls. Pick one randomly:

* `A = Red`  
* `B = First pick is blue`  

Compute joint and conditional probabilities using two-step reasoning.  

*Solution hint:* Use tree diagram or probability multiplication for dependent events.

---

### Advanced Questions

**Q3:** In a company:

|         | Male | Female | Total |
| ------- | ---- | ------ | ----- |
| Manager | 20   | 10     | 30    |
| Staff   | 30   | 40     | 70    |
| Total   | 50   | 50     | 100   |

* Find:

  1. `P(Manager)` (marginal)  
  2. `P(Male and Staff)` (joint)  
  3. `P(Male | Staff)` (conditional)

**Solution:**

1. `P(Manager) = 30/100 = 0.3`  
2. `P(Male and Staff) = 30/100 = 0.3`  
3. `P(Male | Staff) = 30/70 ≈ 0.429`  

---

### Word Problem

**Q4:** A survey shows 60% of people like tea, 50% like coffee, and 30% like both. Find:

1. Probability a person likes **tea or coffee**  
2. Probability a person likes **tea given they like coffee**

**Solution:**

1. `P(Tea ∪ Coffee) = 0.6 + 0.5 − 0.3 = 0.8`  
2. `P(Tea | Coffee) = P(Tea ∩ Coffee)/P(Coffee) = 0.3 / 0.5 = 0.6`  

---

## 4️⃣ Probability Tree Example

Two-step draw from a bag (2 red, 3 blue, no replacement):

First Draw:
Red (2/5) → Second Draw:
Red (1/4)
Blue (3/4)
Blue (3/5) → Second Draw:
Red (2/4)
Blue (2/4)


* Compute `P(Red then Blue) = 2/5 × 3/4 = 3/10`

---

## 5️⃣ Multiple Choice Questions (MCQs)

**Q1:** A die is rolled. `A = Even`, `B = Number >3`. Find `P(A|B)`

* A) 1/2  
* B) 2/3 ✅  
* C) 1/3  
* D) 1/6

**Q2:** Bag has 2 red and 3 blue balls. Pick one. Find `P(Red | Blue not picked)`

* A) 2/5  
* B) 2/4 ✅  
* C) 3/5  
* D) 1/2

**Q3:** Using the company table above, `P(Female | Manager)` = ?

* A) 10/100  
* B) 10/30 ✅  
* C) 10/50  
* D) 10/70

---

## 6️⃣ Analytical Problems

### Problem 1: Joint Probability Table

|       | A   | B   | Total |
| ----- | --- | --- | ----- |
| X     | 0.1 | 0.2 | 0.3   |
| Y     | 0.3 | 0.4 | 0.7   |
| Total | 0.4 | 0.6 | 1     |

* Find `P(X|A)`  
* Find `P(X ∪ A)`

**Solution:**

* `P(X|A) = P(X ∩ A)/P(A) = 0.1 / 0.4 = 0.25`  
* `P(X ∪ A) = P(X) + P(A) - P(X ∩ A) = 0.3 + 0.4 - 0.1 = 0.6`  

---

### Problem 2: Conditional Probability in Finance

* Company A defaults: `P(D_A) = 0.05`  
* Company B defaults: `P(D_B) = 0.10`  
* Both default together: `P(D_A ∩ D_B) = 0.02`

Find `P(A defaults | B defaults)`

**Solution:**  
`P(D_A | D_B) = P(D_A ∩ D_B) / P(D_B) = 0.02 / 0.10 = 0.2`

---

## 7️⃣ Quick Formulas Reference


| Formula | Meaning |
|-------|---------|
| `P(A ∩ B)` | Joint probability |
| `P(A\|B) = P(A ∩ B)/P(B)` | Conditional probability |
| `P(A ∪ B) = P(A) + P(B) − P(A ∩ B)` | Either event |
| `P(A ∩ B) = P(A) × P(B)` | Check for independence |


---

## 8️⃣ Summary Table

| Type        | Notation | Meaning                    | Example                  |
| ----------- | -------- | -------------------------- | ------------------------ |
| Marginal    | P(A)     | Single event probability   | Red ball                 |
| Joint       | P(A ∩ B) | Both events occur together | Even AND >3              |
| Conditional | P(A|B)   | Probability of A given B   | Even given >3            |
