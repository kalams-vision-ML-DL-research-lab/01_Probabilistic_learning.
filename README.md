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

09_continuoues_Uniform_Distribution.

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

P(Third Tree|worng prediction of test) = .86 / 3.0 == .28.7

~ 28.7% Chances that the test was wrongly predicted by the third Decision-tree.


-----------------------------------------------------------------------------------------
# i.e. Parcel from sendeer to Reciver Passes sequentially through Two post offices (P1, P2). chances of any post office lossing an incomig parcel is 0.2, indepenthy of all other parcels. given that a parcel has lost, chances that it lost by the second post office. 

#Chances of lossing a parcel are P(L) = 0.2 
#lossing form second post office will be (Not lossing from 1st office*lossing form 2nd office)

P(L n P2) 0.8*0.2 = 0.16

Total chance of the lossing of the parcel is P(L n P1) + P(L n P2) = 0.16 + 0.2 = 0.36

P(L|P2) = 0.16 / 0.36 == 0.4.
# ~ 40% chances that the parcel is lost by the second post-office. 

-----------------------------------------------------------------------------------------
# Binomial_Distribution~(p,n)

# Independent occurence of the events and outcomes can be maped as success and failure. i.e. detected(not-detected), spam(ham), having deciese(not having deciese), etc.

# Making prediction about (at-least, at-most, exactly) k successs out of n independent-trials of an any evnet.

#Random-variable: A real valued fuction which maps a real number to every out come of the sample space, helpful for doing statical-operatuions(i.e. Expection, Varience) of the outcomes of the event.

i.e. R.V(X) maping as set of values of number of time the success has occured out n independent trials. 

P(X= x) PMF(Probability masses of functions) = c(n,k)*(p)^k*(1-p)^n-k.

# E[X] (expection of Binomial R.V(X)): SUMMATION(P(X = x)*(x) i.e.( Summation of all the (probability)(mass of that outcome)) 

# Varience(X): ( E[x^2] - (E[X])^2 ).

i.e. Air defence system firs one intercepor at each 8 incoming hostile drones. each hit to the droen is independent to each other, with probability of 0.7. what are the "chances" that in an interceptor at-least 6 
enemy-drones were hit. 

sol. Maping random variable X as Number of successful hits.

X ~ Binomial(n = 8, p = 0.7)

P(X is greter than or equals to 6)

P(X >or = 6) = P(X = 6) + P(X = 7) + P(X = 8)

P(X >or = 6) =   0.296 + 0.197 + 0.576 = 0.5517

# ~55.17% Chances that at-least 6 enemy drones were hit in an interceptor. 
-----------------------------------------------------------------------------------------

# Hypergeomatric~(N, m, N-m, n, m-n)

# Outcomes of the sample space are dependent. choosing sample of size k without replacement out of population of size N. 

# PMF  = P(X = x) = c(m, k).c(N-m, k-x) // c(N, n)  where k, k-x are subset of n(selected samlpe)

N = Total Population Size.
m = class_1, N-m = class_2. where m, N-m are subsets of the set N.

# Applied for prediction of kowing out of selected sample (at-least, at-most, exactly) k belongs to a perticular class of size m, from the known population size N. 

E[X] = m*(N//k) or (probability of success).(belonging_class(m))

i.e. In a locality there were 22 houses estsbilished, out of them 9 were of terrorist recidances and rest were of civilean. in an operation surface to surface missiles were targated in that locality, to eliminate terrorist recidances. If  houses were hited, then the chances that at-least 7 were terrorist recidances would be?. 

sol.
Total established houses(N) = 22, Terrorist recidances(m) = 9, Civilian houses(N-m) = 13, 
Total no. of hited houses(n) = 13

Maping R.V(X) as (number of terrorist_hited_houses)

probability of at_least 10 were of terriorist = P(X = 7) + P(X = 8) + P(X = 9)

P(X > or = 7) = 0.124 + 0.023 + 0.044 
=
# ~14.9% chances that at-leat 7 would be of terrorist recidances.
-----------------------------------------------------------------------------------------

# CDF_VS_PDF of the a continuous random variable.
 
#Cumulative distribution function as named cumulative it accumulates the probabilites of values of the Random variable X till a pirticular mass(value). 
# Irrespective of that the R.V(x) is discrete or continuous the CDF of the fuction will alwasy exists.
# Non_Decresing.

# F(a) = P(X <= a)
# 0 <= F(a) <= 1

#Probability dencity function: It exist for continuous disrtibution of the R.V(X).
#AS named probabilites of the R.V(X) are continuously distributes under a dencity-curve.

# Helpful to analysies how likely a data point falls in between a specific (very-small) range of points.
-----------------------------------------------------------------------------------------

# Poisson-Distribution~(lambda).
#Expected value the random variable X of the outcome space act as a parameter for the PMF.

# PMF P(X= x) e^-(lambda).(lambda)^x / x!

# To make prediction about the event having number of trials(N) as very large, and having chances of success very less.
# fallows properties of binomial distribution i.e. Events can be maped as success or failure, Independent occurance of events, etc.

# i.e. The chances that trained Ml-model gives wrong predictions is 0.002. If the sample of 2000 datasets given to Model for testing purpose. chances that the model will predict at most 5 data points worngly will be?
sol.
maping R.V(X) as set no.'s wrongly predicted outcomes.

expected value(lambda)= (total_no. of data_points).(chances of success) = 2000.(0.002) = 10

chances that model will predict at most 5 wrong data points = P(X=< 5).

P(X <= 5) = P(X= 0) + P(X= 1) + P(X= 2) + P(X= 3) + P(X= 4) + P(X = 5)

= 0.0000454 + 0.000499 + 0.0103 + 0.02925 + 0.06708 = 0.0671

# ~6.71% Chances that the model will predict at most 5 data points wrongly. 
 
# i.e. The deployed model detects anomalies with an avrage rate of 8 detection per minute. what will be tha chances that the models detect 3 anomaly within 15 seconds. 
-----------------------------------------------------------------------------------------

# Exponential_Distribution~(lambda)
#parameter lambda is 1 over by avarage(Expected) time.

#Useful to make prediction time of the rare events in future. it maps occurance time of the events, i.e. number of peoples entering into the mall. 
# @Exected delivery time of the parsel, expected reciving of the cab. 
# @Expected anomaly dectaction time of the model.

#PMF = (lambda).e^-(lambda).(t)    where t is the time.
#CDF = 1 - e^-(lambda) 

# i.e. The detection time for one anomaly is expected to 30 seconds by the model. If 6 enemy jets enters the air field, then what are the chances that the model will detect at least 5 withine 60 seconds. 
sol. 
lambda = one over by the avarage time, that is 1/30.

#prob. of success for one detection will be 1 - e^-2.

#this case fallosws binomial's property i.e. (k success out of n trials).

#Chances that it will detect at least 5 jets within 60 seconds. will be detecting exact 5 jets + detecting all 6 jets.

# P(X= 5) = C(6, 5).((1- e^-2))^5.(e^-2) = ~ 0.3924
# P(X= 6) = C(^, 6).((1- e^-2))^6 = ~  0.4179
#  p(x >= 5) = 0.8103

# ~81.07% there Chances that the model detect at lest 5 out 6 jets within 60 seconds.









