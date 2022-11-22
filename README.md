# FinTech_Module_14_Challenge
Machine_Learning_Trading_Bot

## Challenge Overview
In this challenge we seek to improve an existing algorithmic trading system to increase the 'firm’s' competitive advantage. Using an existing baseline trading algorithm and model we consider a range of variables to seek to improve the returns on the trading algorithm. We also apply a machine learning model to determine if the model can yield better returns.

Steps within the challenge are:
1. Implement an algorithmic trading strategy that uses macine learning to automate trade decisions
2. Adjust input parameters to optimise the algorithm
3. Train a machine learning model and compare it to the baseline model
4. Create an evaluation report

## Technologies
Pandas, Jupyter Lab, PyVizlot, SciKit Learn, Numpy 

## Project analysis and report

Baseline modelling with 3mth DateOffSet and SMA short (4), and long windows (100) delivered the following results

![Baseline - SVC Model Prediction](https://user-images.githubusercontent.com/110360757/203215440-6fd069ae-3498-4c31-abd3-884f02d94740.png)
![Basline - Actual vs Strategy returns](https://user-images.githubusercontent.com/110360757/203215455-c435f4c8-f36b-40d3-9fcb-fb6d28c8b973.png)

Adjustment of the model to 6mth DateOffSet with the same windows produced a Strategy Retrun of over 1.8. The recall score also improved from 96 to 98.

![SVC Model Prediction 6mth DateOffSet](https://user-images.githubusercontent.com/110360757/203215795-93c86331-1885-4a75-b80b-691986b836f7.png)
![Actual vs Strategy return 6mth DateOffSet](https://user-images.githubusercontent.com/110360757/203215810-fa45286a-c494-4fa8-a743-7d20bcb5889f.png)

A further trial to increase the DateOffSet to 12mth keeping the same indow parameters increased recall to 100but lowered the Strategy Return to just over 1.6 inline with the Actual Return.

![SVC Model Prediction 12Mth DateOffSet](https://user-images.githubusercontent.com/110360757/203216118-967b2511-dcc4-4663-a8fe-515d58775858.png)
![SVC Model Prediction 12Mth DateOffSet](https://user-images.githubusercontent.com/110360757/203216126-26a3eb86-49b8-49dc-9965-5eee121a30e2.png)

