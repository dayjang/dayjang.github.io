---
title: "[ML101] Bias-Variance Tradeoff & Regularization"
permalink: /ml1/machine-learning/
header:
  image: 
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

- `Irreducible Error` <br>
= Intrinsic uncertainty/randomness <br>
= exists in even the best possible model<br>

![](bias_var_image2.png)


### What is Regularization?

- Regularization in Machine Learning means reducing overfitting **by punishing model complexity**

<img src="http://www.sciweavers.org/tex2img.php?eq=%0A%0A%0AM%28w%29%20%2B%20%20%5Clambda%20R%28w%29%20%0A%0AM%28w%29%3A%20model%20error%0A%0A%20%5Clambda%20%3A%20%0A%0Aadjustable%20weight%20of%20complexity%20cost%0A%0AR%28w%29%3A%20complexity%20cost%0A&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0" align="left" border="0" alt="M(w) +  \lambda R(w) M(w): model error \lambda : adjustable weight of complexity costR(w): complexity cost" width="308" height="100" />

- Lambda allows us to adjust model complexity

### Ridge vs LASSO Linear Regression? 

- LASSO
= cost function of LASSO Regression: L1 norm 
= <img src="http://www.sciweavers.org/tex2img.php?eq=%5Cmin%20_%7Bw%5Cin%20%5Cmathbb%20%7BR%7D%20%5E%7Bp%7D%7D%7B%5Cfrac%20%7B1%7D%7Bn%7D%7D%5C%7C%7B%5Chat%20%7BX%7D%7Dw-%7B%5Chat%20%7BY%7D%7D%5C%7C%5E%7B2%7D%2B%5Clambda%20%5C%7Cw%5C%7C_%7B1%7D&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0" align="left" border="0" alt="\min _{w\in \mathbb {R} ^{p}}{\frac {1}{n}}\|{\hat {X}}w-{\hat {Y}}\|^{2}+\lambda \|w\|_{1}" width="337" height="43" />

- Ridge
= cost function of Ridge Regression: L2 norm 
= <img src="http://www.sciweavers.org/tex2img.php?eq=%5Cmin%20_%7Bw%5Cin%20%5Cmathbb%20%7BR%7D%20%5E%7Bp%7D%7D%7B%5Cfrac%20%7B1%7D%7Bn%7D%7D%5C%7C%7B%5Chat%20%7BX%7D%7Dw-%7B%5Chat%20%7BY%7D%7D%5C%7C%5E%7B2%7D%2B%5Clambda%20%5C%7Cw%5C%7C_%7B2%7D&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0" align="left" border="0" alt="\min _{w\in \mathbb {R} ^{p}}{\frac {1}{n}}\|{\hat {X}}w-{\hat {Y}}\|^{2}+\lambda \|w\|_{2}" width="337" height="43" />

- L1 vs L2 norm
= L1 regularization can occasionally produce non-unique solutions. 
= A simple example is provided in the figure when the space of possible solutions lies on a 45 degree line. This can be problematic for certain applications 
= <img style="-webkit-user-select: none;cursor: zoom-out;" src="https://upload.wikimedia.org/wikipedia/commons/b/b8/Sparsityl1.png" width="400" height="150">
= can be overcome by combining {\displaystyle L_{1}} L_{1} with {\displaystyle L_{2}} L_{2} regularization in elastic net regularization

- Elastic Net

= <img src="http://www.sciweavers.org/tex2img.php?eq=%5Cmin%20_%7Bw%5Cin%20%5Cmathbb%20%7BR%7D%20%5E%7Bp%7D%7D%7B%5Cfrac%20%7B1%7D%7Bn%7D%7D%5C%7C%7B%5Chat%20%7BX%7D%7Dw-%7B%5Chat%20%7BY%7D%7D%5C%7C%5E%7B2%7D%2B%5Clambda%20%28%5Calpha%20%5C%7Cw%5C%7C_%7B1%7D%2B%281-%5Calpha%20%29%5C%7Cw%5C%7C_%7B2%7D%5E%7B2%7D%29%2C%5Calpha%20%5Cin%20%5B0%2C1%5D%0A%0A&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0" align="left" border="0" alt="\min _{w\in \mathbb {R} ^{p}}{\frac {1}{n}}\|{\hat {X}}w-{\hat {Y}}\|^{2}+\lambda (\alpha \|w\|_{1}+(1-\alpha )\|w\|_{2}^{2}),\alpha \in [0,1]" width="569" height="43" />



