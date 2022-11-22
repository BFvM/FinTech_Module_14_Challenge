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

## Q1: What impact resulted from increasing or decreasing the training window?

Adjustment of the model to 6mth DateOffSet with the same windows produced a Strategy Retrun of over 1.8. The recall score also improved from 96 to 98.

![SVC Model Prediction 6mth DateOffSet](https://user-images.githubusercontent.com/110360757/203215795-93c86331-1885-4a75-b80b-691986b836f7.png)
![Actual vs Strategy return 6mth DateOffSet](https://user-images.githubusercontent.com/110360757/203215810-fa45286a-c494-4fa8-a743-7d20bcb5889f.png)

A further trial to increase the DateOffSet to 12mth keeping the same indow parameters increased recall to 100but lowered the Strategy Return to just over 1.6 sitting on top of the Actual Return graph.

![SVC Model Prediction 12Mth DateOffSet](https://user-images.githubusercontent.com/110360757/203216118-967b2511-dcc4-4663-a8fe-515d58775858.png)
![Actual vs Strategy Returns 12mth DateOffSet](https://user-images.githubusercontent.com/110360757/203216270-deeafb94-b20d-4e11-b3d4-2dbaf0000c1e.png)

Increaseing the training window improved both accuracy and recall. The sweet spot seems to be a DateOffSet of 6 monthsin regard to delivering the best return. Increasing te DateOffSet beyond this appears to decrease the return inline with the actual return. 

## Q2: What impact resulted from increasing or decreasing either or both of the SMA windows?

When the SMA window was increased to 50 short and 100 long keeping the baseline 3mth DateOffSet, recall increased to 100 whilst accuracy remained at 56. Similar to the 12moth DateOffSet the Strategy and Actual returns are the same with a return of just below 1.4

![SVC Model Prediction SMA 50 - 100 ](https://user-images.githubusercontent.com/110360757/203217918-c96ce37a-5c39-4b88-b9c8-bba8bca6f6e4.png)
![Actual vs Strategy Returns SMA 50 - 100 ](https://user-images.githubusercontent.com/110360757/203218052-3818b1c5-f6f6-4f72-9983-d7940454cee7.png)

## Q3. The best Strategy Return result tested in the data was a 6mth DateOffSet with the SMA set to 4 short and 100 long as shown below.

![Actual vs Strategy return 6mth DateOffSet](https://user-images.githubusercontent.com/110360757/203218835-d4ea89be-3a69-4ada-9668-4d322dddecce.png)

## Evaluating the Logistic Regression Classifier

## Q: Did this new model perform better or worse than the provided baseline model? Did this new model perform better or worse than your tuned trading algorithm?

The LogisticRegression classifier was applied to the baseline data and produced the following results:

![Baseline - LR Model Prediction](https://user-images.githubusercontent.com/110360757/203219309-3bb46db6-1869-47e7-bfb9-0006216eb560.png)
![Baseline - LR Model graph](https://user-images.githubusercontent.com/110360757/203219320-d4a88f4d-2f9a-4f7a-8cbe-c50895aa4531.png)

This modelling dropped our accuracy to 52, and whilst the precision remained at 56, the recall dropped through the floor to 66 relative to our baseline of 96 delivering a final return lower then the Actual Return. Overall it performed worse than the 'tuned' model; however, testing a range of SMA windows may have yielded better results.
