# Statistical Machine Learning - Assignment 2
This repository contains the source code for assignment 2 of the COMP90051 Statistical Machine Learning course at the University of Melbourne.

## Multi-armed bandit (MAB) algorithms

For this assignment, the following algorithms were implemented.

1. ε-greedy and UCB MABs (StatML lecture 16)
2. Off-policy evaluation (Li et al., 2010, 2011)
3. LinUCB contextual MAB (Li et al., 2010)
4. TreeBootstrap contextual MAB (Elmachtoub et al., 2017) 
5. Evaluation and hyperparameter tuning for LinUCB
6. KernelUCB contextual MAB (Valko et al., 2013)

Further details can be found in the project specification ***project2.pdf*** or in the Python notebook ***mbachfischer.ipynb***.

## Project overview

Multi-armed bandits (MABs) are a simple but powerful framework for sequential decision making under uncertainty. 
Through the 2000s, Yahoo! Research led the way in applying MABs to problems in online advertising, information retrieval, and media recommendation. One of their many applications was to Yahoo! News, in deciding what news items to recommend to users based on article content, user profile, and the historical engagement of the user with articles. 

Given decision making in this setting is sequential (what do we show next?) and feedback is only available for articles shown, Yahoo! researchers observed a perfect formulation for MABs like those (ε-Greedy and UCB) learned about in class. 

Going further, however, they realised that incorporating some element of user-article state requires contextual bandits: articles are arms; context per round incorporates information about both user and article (arm); and {0, 1}-valued rewards represent clicks. 

Therefore the per round cumulative reward represents click-through-rate, which is exactly what services like Yahoo! News want to maximise to drive user engagement and advertising revenue. 

In this project, you will work individually (not in teams) to implement several MAB algorithms. Some will be directly from class, while others will be more advanced and come out of papers that you will have to read and understand yourself.