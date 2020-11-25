# BayesianOptimizationForceField
This project is my thesis of "Optimize ionic force field with bayesian optimization" at TUDelft. The aim of this research is to optimize ion force field parameters with a probabilistic machine learning technique called Bayesian optimization. This model uses Gaussian Process to model the unknown region in the parameter space and uses the acquisition function to guide the search. Previous work carried the parameter search mainly based on brute force methods which are usually time-consuming. The advantage of this method is that it allows researchers to carry out parameters search without human interaction, thus the tedious force field optimization process can be speeded up. 
The considered ionic properties are:
- Solvation free energy of single ion (thermodynamic integration)
- Size of first hydration shell (ion and oxygen distance)
- Diffusivity 
- Solubility (via contact ion pairs)

The contributions of this project are:
- Train a Bayesian optimization model with normalized data, applied the same model for different ionic properties and ion species. 
- Perform ionic force field search with less human labor involved. 
- Balance the trade-offs between different ionic properties.
- Simultaneously optimize multiple ion species, avoid the misbalanced situation which can be found in the previous studies.

### 1. Normalize parameter space, resulting in smooth contour plot.
### 2. Train a Bayesian Optimization model, kernel function, balance parameters, normalize data, extend to different species, and ionic properties.
![Image text](https://raw.githubusercontent.com/YuchenZhu/BayesianOptimizationForceField/main/img/obs.png)
![Image text](https://raw.githubusercontent.com/YuchenZhu/BayesianOptimizationForceField/main/img/convergence.png)
### 3. MD simulations to compute the target properties.
![Image text](https://raw.githubusercontent.com/YuchenZhu/BayesianOptimizationForceField/main/img/properties.png)
### 4. Find the optimum regions of primary targets: solvation free energy and ion oxygen distances.
![Image text](https://raw.githubusercontent.com/YuchenZhu/BayesianOptimizationForceField/main/img/primaryTgs.png)
### 5. Compute the secondary targets: diffusivity, ion pairing
![Image text](https://raw.githubusercontent.com/YuchenZhu/BayesianOptimizationForceField/main/img/ionPairs.png)
