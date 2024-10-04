https://arxiv.org/abs/2306.03985

abstract : RL showed robust on many tasks in time series. So, using trained agent with stock datas,  
doing a real world simulation \-\> result was impressive before coivd and even though result decreased a lot,   
it is still positive for after 2021\.

RL uses monte carlo method to build trajectory. And because it is MC method, t+1 time is not affected by time 0 \~ t-1. It somehow show insight

Still, gradient boosting models such as LGBM is used widely. Due to LGBM's structure, it easily overfit but rl shows great robust in time series. Maybe, stochastic policy can prevent model from overfitting. Maybe, entropy regularization is the key to overfitting issue.
