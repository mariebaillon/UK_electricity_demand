# **Multiplicative decomposition model to predict the UK long-term electricity demand with monthly and hourly resolution**

## Description

The UK electricity market is changing to adapt to Net Zero targets and respond to disruptions like the Russia-Ukraine war. This requires strategic planning to decide on the construction of new electricity generation plants for a resilient UK electricity grid. Such planning is based on forecasting the UK electricity demand long-term (from 1 year and beyond).

This project aims to develop a long-term predictive model by isolating the different components of the UK electricity demand, optimising predictions for each of these components, and multiplying them to deliver a single long-term prediction. 

This type of approach is extremely flexible and accurate with an error of 3.25% for 3 years in predicting the monthly electricity demand and 8.31% for 3 years in predicting the hourly electricity demand. 

## Features
* Hybrid model combining Fourier series and neural network.
* Use of independent variables like percentage of renewable energy in electricity supply, UK population growth, and average temperature over the UK weighted by population density.
* Proposed model validated with monthly and hourly resolution for the electricity demand data.
* Comparison with a traditional stochastic time series model like SARIMA.

## Pre-requisites
* The code for this project is written and run using Mathematica 14.1.0.0.
* All the supporting data is stored in a folder called 'DataDir'.

## Code organisation

| Name of the notebook  | Comment |
| ------------- |:-------------:|
| 1-Dependent_variable_pre_proc.nb | Pre-processing of the UK electricity demand data from 2009 to 2023 |
| 2-Dependent_variable_EDA.nb | Exploratory data analysis of the UK electricity demand dataset |
| 3-Independent_variables_pre_proc.nb | Data pre-processing for all the independent variables |
| 4-Variables_correlation | Study of correlation between the demand data and the independent variables, and between independent variables |
| 5-Proposed_model_monthly_data.nb | Multiplicative decomposition model applied to monthly electricity demand |
| 6-Proposed_model_hourly_data.nb | Multiplicative decomposition model applied to hourly electricity demand |
| 7-Baseline_model_monthly_and_hourly_data.nb | Traditional SARIMA model applied to monthly and hourly electricity demand |
| 8-Sensitivity_studies_neural_network.nb | All sensitivities studies carried out on the neural network |
| 9-Sensitivity_studies_trend_extraction.nb | Comparison of different methods to extract the trend from the time series |

## License
Creative Commons Public Licenses, see LICENSE.txt.


## Suggestions for further developments
* Improving the neural network by specifically modelling the disruption from major events, in particular the Covid-19 pandemic. An intervention model with a pulse function or step function that estimates the impact of lockdowns on the electricity demand, could be integrated as input to the neural network. 
* Developing a model for the exogenous variables would allow to extend the predictions of the model to 2023 or beyond. 
