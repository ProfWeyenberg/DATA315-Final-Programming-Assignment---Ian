## Problem 1: Inferring the Bias of a Coin

**Data:** 8 heads and 4 tails in 12 coin flips

**Prior:** Uniform distribution on (0, 1)

**Questions and Answers:**

1. **What is the posterior mean of p?**
   - **Answer:** 0.6418

2. **What is the posterior standard deviation of p?**
   - **Answer:** 0.1236

**Interpretation:** Given the observed data of 8 heads and 4 tails, the probability of the coin landing heads is estimated to be approximately 64.2%. The standard deviation of 0.124 indicates moderate uncertainty around this estimate. The true probability is likely between approximately 0.39 and 0.87 (within ±2 standard deviations).

---

## Problem 2: Estimating the Rate of an Exponential Process

**Data:** Waiting times in minutes: 2.1, 0.9, 1.7, 3.2, 2.8

**Prior:** Gamma(2, 1) distribution for lambda

**Questions and Answers:**

1. **What is the posterior mean of lambda?**
   - **Answer:** 0.1703

2. **What values of lambda form the middle 90% of the posterior distribution?**
   - **5th percentile:** 0.0288
   - **95th percentile:** 0.3978

**Interpretation:** The rate parameter lambda is estimated at approximately 0.17 events per minute. This corresponds to an average waiting time of about 1/0.17 ≈ 5.9 minutes between orders. The 90% credible interval [0.029, 0.398] shows considerable uncertainty in the rate estimate, which is expected given the small sample size of only 5 observations.

---

## Problem 3: Normal Mean with Known Variance

**Data:** 5.2, 4.8, 5.5, 5.0, 5.3

**Known standard deviation:** delta = 1

**Prior:** Normal distribution with mean 0 and standard deviation 10

**Questions and Answers:**

1. **What is the posterior mean of mu?**
   - **Answer:** 5.138
   - **True theoretical posterior mean:** 5.150

**Interpretation:** The mean mu is estimated at 5.138, which is very close to both the sample mean (5.16) and the theoretical posterior mean (5.150). This close agreement validates our Metropolis sampler implementation. The posterior distribution shows high precision due to the known variance and relatively large sample size.

---

## Summary of Results

| Problem | Parameter | Posterior Mean | Additional Statistics |
|---------|-----------|----------------|----------------------|
| 1 - Coin Bias | p | 0.6418 | SD = 0.1236 |
| 2 - Exponential Rate | lambda | 0.1703 | 90% CI: [0.029, 0.398] |
| 3 - Normal Mean | mu | 5.138 | True mean = 5.150 |

---
