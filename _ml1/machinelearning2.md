---
title: "[ML101] Linear Regression"
permalink: /ml1/machine-learning2/
header:
  image:
sidebar:
  nav: "ml1"
---
### Linear Regression
##### What is Linear Regression?

##### Assumptions of Linear Regression?

Assumption 1: Regression is linear in parameters & correctly specified <br>
Assumption 2: `Error terms`
> Error terms are normally distributed <br>
> Error terms have constant variance for every observation, ->   for every i    
> <img src="http://www.sciweavers.org/tex2img.php?eq=%24Var%28%7B%5Cepsilon_i%7D%29%3D%7B%5Csigma%5E2%7D%24&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0" align="left" border="0" alt="$Var({\epsilon_i})={\sigma^2}$" width="100" height="21" /> 

<br> 

> Error terms are uncorrelated across observations, -> for two observations i and j

> <img src="http://www.sciweavers.org/tex2img.php?eq=%24cov%28%7B%5Cepsilon_i%7D%2C%7B%5Cepsilon_j%7D%29%3D0&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0" align="left" border="0" alt="$cov({\epsilon_i},{\epsilon_j})=0" width="117" height="21" />

> Assumption 3: no perfect multi-collinearity within `independent variables`
