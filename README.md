# Tutorials on Gaussian Process Regression

This repository is a series of notebooks on the study of gaussian process regression (GPR). It's intended for educational purposes.

## Usage

### GPR from Sratch

The following notebooks contain implementations done almost entirely from scratch:
* **1_GPR.ipynb**. Attempts to provide an intuitive introduction to GPR, following chapter 2 in _Gaussian Process for Machine Learning_ by Rasmussen et. al.
* **2_LikelihoodModelSelection.ipynb**. Following chapter 5 of Rasmussen, this notebook introduces the user to the selection of optimum hyperparameters through _leave-one-out cross validation_ and _gradient-based minimization_ of the _negative log marginal likelihood_.
Implementation: 1D observation data and $d$ hyperparameters.
* **3_BayesianModelSelection.ipynb**. Introduces the user to the Bayesian approach of selecting hyperparameters. Covers _Bayes Theorem_ with respect to the marginal likelihood of a hyperparameter and its corresponding prior. Introduces _Markov Chain Monte Carlo_ via _Metropolis-Hastings algorithm_ and its application to finding the _posterior_. Demonstrates _adaptive sampling_ where the original posterior becomes the prior to the next sampling of the posterior from a likelihood with added data points (_Bayesian update_). Implementation: 1D observation data and 1 hyperparameter.
* **4_BayesianMS-2Hyperparameters.ipynb**. Same as 3., but with $d$ hyperparameters.
* **5_MultidimensionalGPR.ipynb**. Same as 2., but in $N$ dimensions and $d$ hyperparameters.

<br>

### Notes (no code)

The following notebooks contain reading notes and little to no code:
* **6_Priors.ipynb** Information on different priors used for sampling from the posterior distribution of hyperparameters. Used in Bayesian optimization and adaptive sampling.
* **7_CovarianceFunctions.ipynb** Information on different covariance functions used for the kernel in a GP.
* **10_HMC.ipynb** Since we use HMC sampling of the hyperparameter posterior, this notebook provides background on HMC.
* **14_InverseProb.ipynb** Notes are from _Parameter Estimation and Inverse Problems_ 3rd ed by Aster et al. Introduces the inverse problem and linear regression.

<br>

### GPR using GPy package

These notebooks transition the work done in notebooks 1 through 5 to coding implementations with the package GPy:
* **8_BMS-Package.ipynb** Same as 4., but implemented with GPy. DO NOT USE THIS ONE. It was simply to introduce the package, but improvements on its functionality are done in the 9th notebook.
* **9_BMS-1D.ipynb** This program builds 1D GPRs with gradient-based and Bayesian-based optimization.
* **11_BMS-2D.ipynb** Same as notebook 9, except in 2D (code without graphics works for higher dimensions). Includes variations of the rbf kernel such as ADR and off-diagonal terms of the lengthscale.
* **12_MultiRespGP-1D.ipynb** Introduces _Latin Hypercube Sampling_ and 1-D multi-output GPRs via _ICM_.
* **13_MultiRespGP-2D.ipynb** Study of multi-output GPRs of 2D observational data. Introduces _IMC_ and _LMC_. Code also works for higher dimensional data (without graphics).



## License

[MIT](https://choosealicense.com/licenses/mit/)