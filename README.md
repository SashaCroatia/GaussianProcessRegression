# Tutorials on Gaussian Process Regression

This repository is a series of notebooks on the study of gaussian process regression (GPR).

## Usage

The following notebooks contain implementations done almost entirely from scratch:
* **1_GPR.ipynb**. This notebook attempts to provide an intuitive introduction to GPR, following chapter 2 in _Gaussian Process for Machine Learning_ by Rasmussen et. al.
* **2_LikelihoodModelSelection.ipynb**. Following chapter 5 of Rasmussen, this notebook introduces the user to the selection of optimum hyperparameters through LOO cross validation and gradient based minimization of the negative log marginal likelihood. Works with 1D observation data and $d$ hyperparameters.
* **3_BayesianModelSelection.ipynb**. This notebook introduces the user to the Bayesian approach of selecting hyperparameters. It covers Bayes Theorem with respect to the marginal likelihood of an hyperparameter with its corresponding prior, introduces Markov Chain Monte Carlo via Metropolis-Hastings algorithm and its application to finding the posterior, and demonstrates adaptive sampling where the original posterior becomes the prior to the next sampling of the posterior from a likelihood with more data points (Bayesian update). Works with 1D observation data and 1 hyperparameter.
* **4_BayesianMS-2Hyperparameters.ipynb**. Same as 3., but with $d$ hyperparameters.
* **5_MultidimensionalGPR.ipynb**. Same as 2., but in $N$ dimensions and $d$ hyperparameters.

<br>

The following notebooks mostly contain reading notes:
* **6_Priors.ipynb**
* **7_CovarianceFunctions.ipynb**

<br>

These notebooks transition the work done in notebooks 1 through 5 to coding implementations with packages like GPy:
* **8_BMS-Package.ipynb** Same as 4., but implemented with GPy.


## License

[MIT](https://choosealicense.com/licenses/mit/)