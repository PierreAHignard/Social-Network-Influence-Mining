# Bay Area Influencer Targeting

> Identifying the five most influential social network accounts for a targeted
> restaurant marketing campaign in the San Francisco Bay Area.

---

## Overview

This project supports a highly targeted marketing campaign for a new restaurant
in the San Francisco Bay Area. The core challenge was two-fold: accurately
inferring the geographic locations of users with undisclosed information, and
mapping the spread of influence through the network to maximize regional reach.

The analysis was conducted using the **CRISP-DM** framework across a sample of
a professional social network.

---

## Methodology

### 1. Location Prediction
A scoring algorithm analyzes up to **second-degree network connections** to
predict whether a user is located in the San Francisco Bay Area or elsewhere.

### 2. Influence Modeling
Information spread is modeled similarly to an infection propagation model using
a **Mean Field simulation** to estimate the probability of users seeing and
sharing promotional content.

To find the optimal combination of five influencers out of billions of
possibilities, a **Greedy Algorithm** optimized with a **Tabu Search**
metaheuristic is used to avoid local maxima.

---

## Key Findings

| Metric | Result |
|---|---|
| Bay Area users identified | 152 predicted targets |
| Location model accuracy | ~63% (validated against ground-truth) |
| Baseline sharing probability | 10% |
| Campaign exposure rate | **91%** across predicted Bay Area audience |

---

## Recommended Influencers

The following five accounts were identified as the optimal combination for
maximum Bay Area reach :

```
['U7024', 'U22747', 'U27287', 'U16141', 'U3955']
```

> **Note:** Results carry inherent uncertainty due to location prediction
> accuracy and potential false positives. The 91% exposure rate is based on
> simulation under a 10% baseline sharing probability.

<img width="1063" height="837" alt="pred_target" src="https://github.com/user-attachments/assets/a5300e92-2719-498d-8035-be0d08add555" />
