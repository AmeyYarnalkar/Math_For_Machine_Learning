# T-Test — Complete Detailed Notes


## Why Do We Need a T-Test?

In hypothesis testing, we often test a claim about a population mean.

In Z-test, we assumed:

* Population standard deviation (σ) is known.

But in real life:

* We almost never know the true population standard deviation.
* We only have sample data.
* So we calculate sample standard deviation (s).

Here is the problem:

When we replace σ with s:

* s changes from sample to sample.
* That introduces extra uncertainty.
* The test statistic becomes less stable.

Because of this extra uncertainty, we cannot use the normal (Z) distribution anymore.

So we use the **T-distribution**, which accounts for that extra variability.

---

### Core Idea

> A T-test measures how many estimated standard errors the sample mean is away from the hypothesized population mean.

The word “estimated” is important because we use s instead of σ.

---

## When Do We Use a T-Test?

We use T-test when:

* Population standard deviation (σ) is unknown.
* Sample size is small (especially n < 30).
* Data is approximately normally distributed (important for small samples).
* Sample is random.

Important:

If sample size is large (n ≥ 30), the t-distribution becomes very close to normal distribution.
So Z-test and T-test give almost similar results.

---

## Formula of T-Statistic

$$
t = \frac{\bar X - \mu}{s / \sqrt n}
$$

Where:

* ( \bar X ) = sample mean
* ( \mu ) = hypothesized population mean
* ( s ) = sample standard deviation
* ( n ) = sample size

Denominator:

$$
s / \sqrt n
$$

This is called the **estimated standard error**.

---

## Degrees of Freedom (Very Important)

Degrees of Freedom (df) measure how many independent values are free to vary.

For one-sample t-test:

$$
df = n - 1
$$

Why n − 1?

When we calculate sample mean:

* Once n − 1 values are chosen,
* The last value is fixed to maintain the mean.

So one value is not free.

Example:

If n = 5:

* You can freely choose 4 values.
* The 5th value is forced.

So df = 4.

---

### Relationship Between df and Shape

* Small df → more uncertainty → heavier tails.
* Large df → less uncertainty → distribution approaches normal.
* As df → infinity → t-distribution becomes normal distribution.

---

## Step-by-Step Procedure for T-Test


### Step 1: State Hypotheses

Example:

$
H_0: \mu = 50
$

$
H_1: \mu \ne 50
$

---

### Step 2: Choose Significance Level (α)

Common values:

* 0.05
* 0.01

α represents:

> Probability of making a Type I error (rejecting true null).

Smaller α → stricter test.

---

### Step 3: Compute T-Statistic

$$
t = \frac{\bar X - \mu}{s / \sqrt n}
$$

---

### Step 4: Find Critical T-Value

Critical value depends on:

* α
* One-tailed or two-tailed test
* Degrees of freedom (df)

---

### Step 5: Compare

If:

|t calculated| > t critical → Reject H₀

Otherwise → Fail to reject H₀

---

### Step 6: Write Conclusion Properly

Correct format:

> There is sufficient statistical evidence at α = 0.05 level to reject the null hypothesis.

Never say:

“Null hypothesis is false.”

---

## How to Read a T-Table (Very Important Section)

A typical T-table has:

* Rows → Degrees of Freedom (df)
* Columns → Significance levels (α)

Sometimes columns are divided into:

* One-tailed probability
* Two-tailed probability

---

## Step-by-Step Example

Suppose:

n = 16
α = 0.05
Two-tailed test

---

### Step 1: Find df

$$
df = n - 1 = 16 - 1 = 15
$$

Go to row 15 in the table.

---

### Step 2: Identify Column

For two-tailed α = 0.05.

Look for:

Column labeled 0.05 (two-tailed).

Some tables show:

Two-tailed α = 0.05
or
One-tailed α = 0.025

(Because 0.025 in each tail = 0.05 total)

Be careful here.

---

### Step 3: Read Intersection

At:

Row df = 15
Column α = 0.05 (two-tailed)

You get approximately:

t critical ≈ 2.131

That means rejection region is:

t > 2.131
or
t < -2.131

---

## Important Observations

If df is small (like 5):

Critical value might be around 2.57 (for 0.05 two-tailed).

If df is large (like 100):

Critical value might be around 1.984 (very close to 1.96).

So:

Small df → larger critical value
Large df → approaches 1.96

---



## Z-Test vs T-Test Comparison

| Feature             | Z-Test | T-Test          |
| ------------------- | ------ | --------------- |
| Population σ known? | Yes    | No              |
| Uses sample s?      | No     | Yes             |
| Depends on df?      | No     | Yes             |
| Shape fixed?        | Yes    | Changes with df |
| Heavy tails?        | No     | Yes (small df)  |

---

## Full Example

Given:

Sample mean = 52
Hypothesized mean = 50
s = 4
n = 16
α = 0.05
Two-tailed test

---

Step 1: df

$
df = 16 - 1 = 15
$

---

Step 2: Compute standard error

$
SE = 4 / \sqrt{16} = 4 / 4 = 1
$

---

Step 3: Compute t

$
t = (52 - 50) / 1 = 2
$

---

Step 4: Find critical value

From table:

df = 15
α = 0.05 two-tailed

t critical ≈ 2.131

---

Step 5: Compare

Calculated t = 2
Critical t = 2.131

Since:

2 < 2.131

We fail to reject H₀.

---

Conclusion:

There is not enough evidence at 5% level to conclude that the population mean differs from 50.

---

