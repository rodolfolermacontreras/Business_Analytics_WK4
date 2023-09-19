# Business_Analytics_WK4
Week 4: Prescriptive Modeling: Ranking Using Predictors: This week,  you will predict returns of loans and use this prediction and the default predictions from last week to implement simple strategies to pick a portfolio of loans to invest in. 

# Week 4 - Picking Loans using Regression of Loan Returns

This notebook carries out the following steps
  1. Reads the saved returns data from the pickle 
  2. Build several classifier and regression models with the data (Save the time-consuming models for loading in later re-runs)
  3. Uses the regressions for returns and the classification models from before for implementimg some simple strategies for picking loans to invest in. A new greedy strategy has been added but you should try others.
  4. Tests these strategies on a portfolio of 100 loans
  5. Performs a sensitivity analysis of the performance of the loan to the number of loans invested in from 100 to 1000
  6. (optional) Re-run the test strategies on different test and train sets from different time periods
      - `2013` & `2014`
  
Things for you to do
- Decide on one of the return columns to focus on and justify why. Note that you should do this BEFORE looking at the results of the regressions for predicting all the return columns to not get biased
- For the return column you picked, examine the various types of regularized regressions to pick the best regularized model, or simply use automated analysis to pick a subset of variables to include in a regular regression. You will need to finalize your best model before moving to the next step
- For the return column you picked, try various strategies for picking the best set of loans to invest in, using the ideas from the case. You should use the best model for the return column you picked here
- Interpret the results of the different strategies
- Vary the number of loans selected and see how it affects the results
- Think of a new rule to pick the best loans using the analyses you have done so far, and add it to the script. e.g. 
    - Rank by return but only accept if P(default) is not too high. 
    - If you want to go further, you can try to implement a two-stage model: First, estimate expected return in two stages: Stage 1 - default or not default, Stage 2 - resulting return given stage 1 state, and combine them using Pr(default) predicted from another classification model from last week
    
Prepare your **presentation**. Your presentation should contain about 5 to 6 slides. Add an extra slide at the end if you tried the BONUS.
1. Begin by stating the objective of the presentation and what your objective is. Which questions do you seek to answer? What are the main points of the presentation?
2. (3) Which method did you use to compute returns? Why? How did the different predictive model perform? Which metric are you using to evaluate the predictions? 
4.  Compare the different strategies to select loans based on the predictions obtained. Present a table containing the predicted return percentages. Which method do you think Alice should use? Which new strategy do you propose to select the loans? Does it perform better than the previous ones?
5. Include your robustness results. How do your strategies scale? Do your results change by changing the number of loans you are able to invest in? what if you have a limited budget? Does this affect the best strategy that you selected on the previous slide?
6.  State your conclusions. What is the main idea you wish to convey with the presentation? Do you think the findings from this script will be useful to solve the overall problem? What are the main takeways from the analysis you performed?

BONUS
- Is there correlation between higher predicted returns and probability of default (computed in module M3). If so, how can you exploit this to improve your models?
- Can you improve your models using the results from module 2? If so, clearly state the improvements in terms of the metric you used to evaluate your models.
- Can you derive new variables from the original ones to improve your models? If so, clearly state the improvements in terms of the metric you used to evaluate your models.
- Use a more sophisticated (although less interpretable) predictive model such as tree boosting or support vector machine to obtain new results. Do these models perform better?
- Are there any exogenous variables (i.e. variables from other data sets, such as economic growth of the country) you might use to improve your models?
