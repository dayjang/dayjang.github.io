---
title: "[ML101] Bias-Variance Tradeoff"
permalink: /ml1/machine-learning/
header:
  image: "/images⁩/bias_variance_image1.jpg"
sidebar:
  nav: "ml1"
---
### What is Bias-Variance tradeoff?

- a central problem in supervised learning
- when we choose a predictive model, we want to satisfy
    > 1. `Accurately captures the regularities in its training data`
    > 2. `Generalizes well to unseen data` <br>
    Unfortunately, it is typically impossible to do both simultaneously
<br>

- `Variance` <br>
= error from sensitivity to small fluctuations in the training set. <br>
<span style="color:red">High</span> variance -> include <span style="color:red">random noise</span> in the training data <br>
Overfitting
<br>

- `Bias` <br>
= error from erroneous assumptions in the learning algorithm. <br>
<span style="color:red">High</span> bias -> cause an algorithm to <span style="color:red">miss the relevant relations</span> between features and target outputs <br>
Underfitting
