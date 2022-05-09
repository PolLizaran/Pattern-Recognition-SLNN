# Pattern-Recognition-SLNN

## Introduction

The aim of this project was to be capable of recognizing the numbers in a sequence of blurred digits by making a binary classification. Given a target number, we wanted to determine whether the number contained in the image was the target one. 

To make that study, three well-known unconstrained optimization algorithms were used: Gradient Method (`GM`), Quasi-Newton Methods (`QNM`), specifically `BFGS` & Stochastic Gradient Method (`SGM`). 
The procedure to achieve that goal was to formulate a Single Layer Neural Network (`SLNN`) that was trained to recognize the different numbers with First Derivative Optimization methods.

The output signal of the SLNN, assumed to be binary, was obtained through Ridge Regression, thus being the function to minimize: $\~{L}(X^{TR}, y^{TR}, \lambda) = L(w; X^{TR}, y^{TR}) + \lambda \cdot \dfrac{\|w\|^2}{2}$

## Parameters

* $X^{TR}$ -> Training data set
* $y^{TR}$ -> Output signal resulting from $X^{TR}$
* $\lambda$ -> Regularization parameter for Ridge regression (also known as Tikhonov regularization)
* $w$ -> Output of the Single Layer sigmoids (activation function)

## Steps to follow

1. Open the file `uo_nn_batch.m` and configure the parameters you want to use for optimization. 
2. Run the file.
3. Wait for the results that will be redirected into the `.csv` file. 

`uo_nn_batch.m` calls the function `uo_nn_solve`, that is the main function of the project. Firstly it generates training and test datasets by calling to the function `uo_nn_dataset.m`. Secondly it defines the Loss function and later on it calls to the correspondant algorithm that has been selected. 
Once the optimization algorithms end, the results obtained are verified to work with a different data set (test). By last, if desired, the last line of the code can be uncommented and `uo_nn_Xyplot.m` will be called and a graphical interface with the results will be displayed.

## Objectives

- Recognize numbers and its patterns.
- Understanding which algorithms give better results for minimizing the error of classification.
- Study which combinations of $\lambda$-algorithms give better performance


In order to study the results obtained in a more in-depth way, we decided to import the data file (.csv) to `R` and plot several results. By that, we were able of analyzing the different outcomes generated by the three algorithms (`GM, QNM, SGM`).

## Requirements

[Mathjax](https://chrome.google.com/webstore/detail/mathjax-plugin-for-github/ioemnmodlmafdkllaclgeombjnmnbima/related) extension for Chrome is needed to properly visualize the formulas in the Markdown.

- - -

## Authors

Copyright © 2022 Pol Lizaran Campano (https://github.com/PolLizaran) & Clàudia Mur Planchart (https://github.com/claudiamur)

This project is available under the terms of the GNU General Public License v3. See [LICENSE.md](LICENSE.md) for more information.

Data Science and Engineering, UPC, 2022
