---
layout: page
title: Software and Tools
description: >
  A list of software contributed by Dr. Neeraj Dhanraj Bokde
hide_description: true
accent_image: 
  background: url('/images/kailash.jpg') center/cover
  overlay: false
sitemap: false
permalink: /software/
---

# R Packages

### 1. PSF: Forecasting of Univariate Time Series Using the Pattern Sequence-Based Forecasting (PSF) Algorithm
* Pattern Sequence Based Forecasting (PSF) takes univariate time series data as input and assist to forecast its future values.
* This algorithm forecasts the behavior of time series based on similarity of pattern sequences.
* Initially, clustering is done with the labeling of samples from database.
* The labels associated with samples are then used for forecasting the future behaviour of time series data.

![w1](https://user-images.githubusercontent.com/10669836/134778693-f4c2acf8-0124-44db-af3f-c11f8076f8eb.jpg)
#### CRAN
* [https://cran.r-project.org/package=PSF](https://cran.r-project.org/package=PSF)
#### Publication/Manual
* Bokde N., Asencio-Cortés G., Martínez-Alvarez F., and Kulat K. D. (2017). [PSF: Introduction to R Package for Pattern Sequence Based Forecasting Algorithm](https://journal.r-project.org/archive/2017/RJ-2017-021/index.html). _The R Journal_ (IF 3.984), 9(1), 324-333. 

---

### 2. imputeTestbench: Test Bench for the Comparison of Imputation Methods
* Provides a test bench for the comparison of missing data imputation methods in uni-variate time series.
* Imputation methods are compared using different error metrics.
* Proposed imputation methods and alternative error metrics can be used.
![w2](https://user-images.githubusercontent.com/10669836/134777727-14e5799a-0bde-49c2-b9c1-336cb3a22a0f.PNG)
#### CRAN
* [https://cran.r-project.org/package=imputeTestbench](https://cran.r-project.org/package=imputeTestbench)
#### Publication/Manual
* **Bokde N.**, Kulat K. D., Beck M. W., and Asencio Cortés G. (2018). [R package imputeTestbench to compare imputations methods for univariate time series](https://journal.r-project.org/archive/2018/RJ-2018-024/index.html). _The R Journal_ (IF 3.984), 10(1), 208-233.

---

### 3. ForecastTB: Test Bench for the Comparison of Forecast Methods
* Provides a test bench for the comparison of forecasting methods in uni-variate time series.
* Forecasting methods are compared using different error metrics.
* Proposed forecasting methods and alternative error metrics can be used.

![w3](https://user-images.githubusercontent.com/10669836/134778685-38cca478-aef2-49d7-ad48-a57693cf92c3.PNG)
#### CRAN
* [https://cran.r-project.org/package=ForecastTB](https://cran.r-project.org/package=ForecastTB)
* [Shiny App](https://psfonline.shinyapps.io/ForeCastTB1/)

<iframe src="https://psfonline.shinyapps.io/ForeCastTB1/" width="100%" height="600px"></iframe>
Please click on three parallel lines on left-top of the Shiny panel for better visualization.
{:.note}

#### Publication/Manual
* **Bokde N.**, Yaseen Z. M. and Andresen G. B. (2020). [ForecastTB - An R Package as a Test-bench for Time Series Forecasting: Application of Wind Speed and Solar Radiation Modeling](https://www.mdpi.com/1996-1073/13/10/2578). _Energies_ (IF 3.004), 13(10), 2578.

---

### 4. CleanTS: Testbench for Univariate Time Series Cleaning
* A reliable and efficient tool for cleaning univariate time series data.
* It implements reliable and efficient procedures for automating the process of cleaning univariate time series data.
* The package provides integration with already developed and deployed tools for missing value imputation and outlier detection.
* It also provides a way of visualizing large time-series data in different resolutions.

![w4](https://user-images.githubusercontent.com/10669836/134778677-f44d6e6c-cf06-4046-8d66-ad2270afa87e.PNG)
#### CRAN
* [https://cran.r-project.org/package=cleanTS](https://cran.r-project.org/package=cleanTS)
* [Shiny App](https://mayur1009.shinyapps.io/cleanTS/)

<iframe src="https://mayur1009.shinyapps.io/cleanTS/" width="100%" height="700px"></iframe>
Please click on three parallel lines on left-top of the Shiny panel for better visualization.
{:.note}

#### Publication/Manual
* **Bokde N.**, Yaseen Z. M. and Andresen G. B. (2022). [cleanTS: Automated (AutoML) Tool to Clean Univariate Time Series at Microscales](https://arxiv.org/abs/2110.11815). _arXiv_.

---

### 5. GuessCompx: Empirically Estimates Algorithm Complexity
* Make an empirical guess on the time and memory complexities of an algorithm or a function.
* Tests multiple, increasing size random samples of your data and tries to fit various complexity functions o(n), o(n2), o(log(n)), etc.
* Based on best fit, it predicts the full computation time on your whole dataset. Results are plotted with 'ggplot2'.
![w5](https://user-images.githubusercontent.com/10669836/134778671-e0ae37a9-0dee-4428-96c6-63b160608069.PNG)
#### CRAN
* [https://cran.r-project.org/package=GuessCompx](https://cran.r-project.org/package=GuessCompx)
#### Publication/Manual
* Agenis-Nevers M., **Bokde N.**, Yaseen Z., and Shende M. (2020). [An empirical estimation for time and memory algorithm complexities: Newly developed R package](https://link.springer.com/article/10.1007/s11042-020-09471-8). _Multimedia Tools and Applications_ (IF 2.757). (https://doi.org/10.1007/s11042-020-09471-8)

---

### 6. Jaya: a Gradient-Free Optimization Algorithm
* Maximization or Minimization of a fitness function using Jaya Algorithm (JA).
* A population based method which repeatedly modifies a population of individual solutions.
* Capable of solving both constrained and unconstrained optimization problems.
* It does not contain any hyperparameters.
* For further details: R.V. Rao (2016) <doi:10.5267/j.ijiec.2015.8.004> .
![w6a](https://user-images.githubusercontent.com/10669836/134778951-a1aab9bf-be55-4edf-924f-b78cab5a4dec.PNG)
![w6b](https://user-images.githubusercontent.com/10669836/134778958-c7482a0e-47b7-47ad-9e21-6c617db893ac.PNG)
#### CRAN
* [https://cran.r-project.org/package=Jaya](https://cran.r-project.org/package=Jaya)
#### Publication/Manual
* **Bokde N.**, and Shende M. (2020). [A guide to Jaya Package](https://cran.rstudio.com/web/packages/Jaya/vignettes/A_guide_to_JA.html). 

---

### 7. WindCurves: Tool to Fit Wind Turbine Power Curves
* Provides a tool to fit and compare the wind turbine power curves with successful curve fitting techniques.
* Facilitates to examine and compare the performance of a user-defined power curve fitting techniques.
* Also, provide features to generate power curve discrete points from a graphical power curves.
* Data on the power curves of the wind turbine from major manufacturers are provided.
![w7](https://user-images.githubusercontent.com/10669836/134779462-31abb810-78fa-4be7-8a6a-1d341f92490b.PNG)
#### CRAN
* [https://cran.r-project.org/package=WindCurves](https://cran.r-project.org/package=WindCurves)
#### Publication/Manual
* **Bokde N.**, Feijoo A., and Villanueva D. (2018). [Wind turbine power curves based on Weibull cumulative distribution function](https://www.mdpi.com/2076-3417/8/10/1757). _Applied Sciences_ (Invited/Feature paper) (IF 2.679), 8(10), 1757.

---

### 8. decomposedPSF: Time Series Prediction with PSF and Decomposition Methods (EMD and EEMD)
* Predict future values with hybrid combinations of Pattern Sequence based Forecasting (PSF), Autoregressive Integrated Moving Average (ARIMA), Empirical Mode Decomposition (EMD) and Ensemble Empirical Mode Decomposition (EEMD) methods based hybrid methods.
#### CRAN
* [https://cran.r-project.org/package=decomposedPSF](https://cran.r-project.org/package=decomposedPSF)
#### Publication/Manual
* **Bokde N.**, Feijoo A., Villanueva D., and Kulat K. (2019). [A review on hybrid empirical mode decomposition models for wind speed and wind power prediction](https://www.mdpi.com/1996-1073/12/2/254). _Energies_ (IF 3.004), 12(2), 254.
* **Bokde N.**, Feijoo A., and Kulat K. (2018). [Analysis of Differencing and Decomposition prepossessing methods for wind speed prediction](https://www.sciencedirect.com/science/article/pii/S1568494618304290?casa_token=i-1txOkUNcMAAAAA:laMUdOcRv7mPGy4YpFGvOsNL4CjW20MELiGunz9v5zmi-Di8OZqZtdq6Elol6BIdBWY5QdY). _Applied Soft Computing_ (IF 6.725), 71(), 926-938.
* **Bokde N.**, Tranberg B., and Andresen G. B. (2021). [Short-term CO2 emissions forecasting based on decomposition approaches and its impact on electricity market scheduling](https://www.sciencedirect.com/science/article/pii/S0306261920314926). _Applied Energy_ (IF 9.746). 281, 116061. (Preprint: https://arxiv.org/pdf/2003.10868).

---

### 9. imputePSF: Impute Missing Data in Time Series Data with PSF Based Method
* Imputes the missing values in time series data with PSF algorithm based approach.
* The details about PSF algorithm are available at: <https://cran.r-project.org/package=PSF>.
#### CRAN
* [https://cran.r-project.org/package=imputePSF](https://cran.r-project.org/package=imputePSF)

---

