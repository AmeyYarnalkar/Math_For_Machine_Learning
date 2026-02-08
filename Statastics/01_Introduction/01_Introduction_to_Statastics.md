
# Statistics (ML-Oriented Notes)

## What is Statistics?

Statistics is the science of **collecting, organizing, and analyzing data**
to **discover patterns, quantify uncertainty, and make decisions**.

👉 In ML: statistics helps models **learn from data and generalize**.

---

## What is Data?

Data is **any observable or measurable information**
that can be **represented, collected, and analyzed**.

👉 In ML, everything (text, images, audio) is **ultimately converted into numbers**.

---

## Applications of Statistics

1. **Data Exploration & Summarization (EDA)**

   * Understand shape, spread, noise, bias
2. **Statistical Understanding**

   * Distribution, variance, correlation
3. **Model Building**

   * Regression, classification, clustering
4. **Validation & Uncertainty**

   * Error, confidence, overfitting
5. **Optimization & Decision Making**

---

## Types of Statistics

### 1. Descriptive Statistics

**Goal:** Understand and summarize the data you already have

* Mean, median, mode
* Variance, standard deviation
* Tables, charts, plots

👉 Used heavily in **EDA**

---

### 2. Inferential Statistics

**Goal:** Draw conclusions or make predictions about a **population**
using only **sample data**

* Estimation
* Confidence intervals
* Hypothesis testing

👉 Foundation of **generalization in ML**

---

## Population vs Sample

### Population (N)

* **Complete set** of all observations
* Described using **parameters**
* True distribution (usually unknown)

### Sample (n)

* **Subset** of the population
* Described using **statistics**
* What ML models actually see

👉 ML tries to **learn population behavior from samples**

---

## Sampling

Sampling is the **method of selecting samples** from a population.

### Probability Sampling (Unbiased)

1. **Simple Random Sampling**

   * Every member has equal chance
2. **Systematic Sampling**

   * Every nth item after random start
3. **Stratified Sampling**

   * Divide into groups → sample from each
4. **Cluster Sampling**

   * Randomly choose clusters → take all data inside
5. **Multistage Sampling**

   * Combination of multiple methods

---

### Non-Probability Sampling (Biased)

1. **Convenience Sampling**

   * Easiest to collect
2. **Judgemental / Purposive Sampling**

   * Selected based on purpose
3. **Snowball Sampling**

   * Existing samples recruit others
4. **Quota Sampling**

   * Fixed number from each group

👉 Real ML data is often **biased** → causes fairness & generalization issues

---

## Types of Data

### Quantitative Data (Numerical)

* **Discrete:** Countable integers
  (number of users, defects)
* **Continuous:** Measurable real values
  (height, weight, time)

---

### Qualitative Data (Categorical)

* **Nominal:** No order
  (gender, blood group, PIN code)
* **Ordinal:** Order exists, gaps meaningless
  (ratings, feedback levels)

---

## Measurement Scales (Very Important for ML)

### 1. Nominal Scale

* Categories only
* No order
* No arithmetic

Examples:

* Gender, color, city

👉 ML: **One-hot encoding**

---

### 2. Ordinal Scale

* Categories with order
* Unequal or unknown gaps

Examples:

* Poor < Average < Good < Excellent

👉 ML: **Label encoding (use carefully)**

---

### 3. Interval Scale

* Order + equal intervals
* **No true zero**
* Differences meaningful, ratios not

Examples:

* Temperature (°C, °F)

👉 Mean is valid, but “twice as much” is invalid

---

### 4. Ratio Scale

* Everything in interval scale
* **True zero exists**
* All arithmetic valid

Examples:

* Height, weight, age, income

👉 Most ML numerical features belong here

---

## Key ML Insight

> ML models silently assume **interval or ratio scales**
> unless you explicitly handle categorical data.

Wrong scale → wrong model behavior.

---


