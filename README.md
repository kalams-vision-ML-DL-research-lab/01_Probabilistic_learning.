# 01_Probabilistic_learning.

# This repository projects is base on Foundational-Probabilistic-Learning(i.e. Baysian-Model, Uncertinity Prediction, Distirbutions). for Real-World "Defence" and "Societal" Predictions.

# Rescources: Probability and Statistical Infrence(Ningth Edition).

https://github.com/kalams-vision-ML-DL-research-lab/01_Probabilistic_learning..git

# Contentent:
01_Baysian_Models.

02_Binomial Distribution.

03_Hyper_geomatric_Distribution.

04_Cumulative_Distribution_function-VS-Probability_density_function.

05_Poisson_Distribution.

06_Exponential_Distribution.

07_Geomatric_Distribution.

08_Gaussion_Distribution.

09_Continuous_Uniform_Distribution.
-------------------------------------------------------

# Bay's Theoram.

In real world machine-learning prediction use of Bay's theoram is very much wast. i.e. classification, making predctions about uncertainity, etc.

Having disjoint subsets(A1, A2, A3,..An) of sample-space(S) of a event, chances of an any event(H) belongs to a certain subset.

# Total Probability Theoram.
# n == intersection
P(H) = P(H n A1) + P(H n A1)  + P(H n A2) + P(H n A3) + ....P(H n An)

# Bay's Theoram
given the event H has occured, then chances that it belongs to subset (A2)

P(H|A2) = P(H n A2) // P(H n A1) + P(H n A1)  + P(H n A2) + P(H n A3) + ....P(H n An).
-----------------------------------------------------------------------------------------
# To make trustworthy predictions of a Randomly chosen Person from population of 470 pepole is COVID-19 positive, Bootstrap Aggragating(Bagging) Ensembling method with four decision trees were used. every tree has independent probability of giving correct prediction, with (.38, .22, .14, .26) probabilities respectively. Given that the test was wrongly predicted by a tree, Chances that the tree was third one. 

P(worng prediction of test) = .62 + .78 + .86 + .74 = 3.0

P(Third Tree|worng prediction of test) = .86 // 3.0 == .28.7

~ 28.7% Chances that the test was wrongly predicted by the third Decision-tree.


-----------------------------------------------------------------------------------------
# i.e. Parcel from sendeer to Reciver Passes sequentially through Two post offices (P1, P2). chances of any post office lossing an incomig parcel is 0.2, indepenthy of all other parcels. given that a parcel has lost, chances that it lost by the second post office. 

#Chances of lossing a parcel are P(L) = 0.2 
#lossing form second post office will be (Not lossing from 1st office*lossing form 2nd office)

P(L n P2) 0.8*0.2 = 0.16

Total chance of the lossing of the parcel is P(L n P1) + P(L n P2) = 0.16 + 0.2 = 0.36

P(L|P2) = 0.16 // 0.36 == 0.4.
# ~ 40% chances that the parcel is lost by the second post-office. 

-----------------------------------------------------------------------------------------













