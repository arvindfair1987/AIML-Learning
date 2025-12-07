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

