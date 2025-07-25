# Estimating Solar Wind Speed and Drag Parameter Using the Drag-Based Model for CME Propagation

## Overview
This repository contains a Python function that estimates two key parameters relevant to the propagation of Coronal Mass Ejections:

- **Solar wind speed (w)**
- **Drag parameter (γ)**

The function works by looping through a range of initial guesses of w and γ and numerically solving for the values that best fit observed CME position (r) and velocity (v) data. 

An example of how to use the function is provided in the example.ipynb notebook.

## Features

- Grid search over user-defined parameter ranges
- Iterative solution using a first order Tayler expansion
- Automatic rejection of unphysical solutions 
- A solution is always found when accurate r and v values are generated using the Drag-Based Model.
- The method remains effective even with small amounts of noise in r and v observations.
- For large measurement noise in r and v, additional filtering of the data is required before applying this method.

## Method

A detailed explanation of the estimation technique used in this repository is presented in the research paper

*Z. Abu-Shaar, T. Podladchikova, A. Veronig, M. Dumbovi\'c, S. Hofmeister, 2025: "Coronal mass ejection arrival forecasting with the drag-based assimilation of satellite observations", Under review*. Under review*.


We recommend referring to this paper for a comprehensive understanding of the methodology.

## Requirements
To use this tool, you need Python 3 and the numpy Python library

## Function
- `get_w_gamma_estimates`
Evaluates estimates of solar wind speed (w) and drag parameter (γ) using values of position (r_at_t) and velocity (v_at_t) of CME at time t.
```
w_estimate, gamma_estimate = get_w_gamma_estimates(t, r0, v0, r_at_t, v_at_t)
```

## License
License: This function is released under the Apache License. You can find the license file in the root directory of the GitHub repository. 

## Contact
For any further assistance or inquiries, please don't hesitate to reach out!

*Zaina Abu-Shaar*
zaina.a.abushaar@gmail.com

## Contributors
* Zaina Abu-Shaar
* Tatiana Podladchikova
