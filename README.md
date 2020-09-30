# Econ-HW-2
PP1 (Please see attached Corresponding Graphs for throws 10, 100 and 500)
If the dice were fair, the probability of getting a 6 is E(6)=1/6
 
If the dice were unfair, E(1,2,3,4,5)=5/6

results from throws:
``````
rolls_PP1
1 
1 
`````

Conclusions for PP1

•The dice would be judged unfair if it rolled a 6, therefore the probability is 1/6 or 0.167

•	The dice would be judged fair if it rolled any number besides 6, therefore the probability is 5/6 or 0.833




PP2
Rolling a fair dice a total of 30 times should produce 5 rolls resulting in 6.

•	Given a fair dice, the probability of getting 1 more or less roll would be (4/5 + 1/25) = 0.84

•	Given a fair dice, the probability of getting 2 more or less roll would be (3/5 + 2/25) = 0.68

•	Given a fair dice, the probability of getting 3 more or less roll would be (2/5 + 3/25) = 0.52

•	If the dice is unfair, then the probabilities can vary indefinitely

rolls results from throws

> table(rolls)
rolls

`````
rolls_PP2
1 2 3 4 5 6 
6 6 4 2 5 7
``````

dbinom(1, size=30, prob=.5)
[1] 2.793968e-08
> dbinom(2, size=30, prob=.5)
[1] 4.051253e-07
> dbinom(3, size=30, prob=.5)
[1] 3.78117e-06
``````
summary(rolls_PP2)
   Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    1.0     2.0     3.0     3.5     5.0     6.0 
````    
PP3 
rolls_PP3<-sample(1:6,100,rep=T)

[1] 1 6 3 3 2 2 4 2 4 2 5 5 4 1 2 3 2 6 3 6 5 3 1 3
 [25] 6 5 2 2 2 1 4 4 4 2 5 2 3 4 2 3 2 6 3 6 1 2 4 5
 [49] 2 1 5 6 3 2 2 3 2 3 5 6 4 1 4 5 5 5 6 3 5 1 4 1
 [73] 6 6 2 3 3 1 5 4 1 3 4 3 5 2 1 1 3 5 2 6 6 6 3 4
[97] 3 4 3 2

````
Frequency of each roll 
 1  2  3  4  5  6 
13 22 11 15 15 24
````
> dbinom(1, size=100, prob=.5)
[1] 7.888609e-29
````
> dbinom(2, size=100, prob=.5)
[1] 3.904861e-27
````
> dbinom(3, size=100, prob=.5)
[1] 1.275588e-25
```
> summary(rolls_PP3)
   Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
   1.00    2.00    3.00    3.39    5.00    6.00 
`````

We rolled the dice 100 times and got 24 6's. 

standard deviation 𝜎=[𝑁𝑝(1−𝑝)]^(1/2)=(100*1/6*5/6)^(1/2)=13.89
variance= (13.89)^2= 192.93

•	As per directions given, anything besides a rolling proportion of 1/6 would be an unfair roll. However one must acknowledge that there are multiple variables that play a role in altering this proportion making it so that a dice is technically not unfair simply because the proportions of results fail to match a particular criteria, rather a true dice is fair in the randomness of the results of different roles cause by surfaces, force, and damage among other factors. 
`````
Our Experiment Protocol 
````
rolls_PP4<-sample(1:6,500,rep=T)
print(rolls_PP4)
> print(rolls_PP4)
  [1] 2 6 6 3 6 1 5 3 3 2 6 5 1 3 2 3 2 3 1 3 4 5 5 5
 [25] 4 4 5 1 5 4 2 6 5 1 1 2 5 3 1 3 3 4 3 5 5 4 1 3
 [49] 2 6 5 3 4 1 4 5 4 6 1 2 3 1 5 4 1 6 2 1 3 6 3 6
 [73] 4 4 6 1 5 5 5 4 6 5 5 1 4 3 3 3 5 5 6 5 2 2 3 3
 [97] 1 2 6 6 2 5 1 1 2 2 1 3 3 3 3 3 5 3 6 2 6 2 1 3
[121] 6 2 4 2 5 5 1 6 6 2 3 4 6 3 5 5 3 6 5 1 6 5 1 2
[145] 1 6 3 6 1 6 2 2 1 6 4 5 5 3 5 3 5 6 5 1 6 5 5 2
[169] 2 6 1 6 1 1 1 4 5 6 3 3 5 1 1 3 2 5 2 4 6 6 5 5
[193] 1 1 6 5 1 2 5 2 5 4 4 6 5 3 5 5 2 5 4 3 6 5 4 3
[217] 2 2 4 2 6 2 4 2 6 1 2 6 5 3 5 2 3 6 5 3 6 1 2 2
[241] 4 5 5 2 2 3 4 1 4 3 1 3 5 4 5 1 5 3 2 3 5 4 2 3
[265] 2 2 6 4 4 1 6 5 4 6 1 6 2 6 6 3 1 5 2 3 6 6 4 6
[289] 2 3 5 5 5 4 6 6 2 5 2 5 1 3 6 1 5 2 1 5 1 5 2 6
[313] 6 5 4 2 3 1 3 2 3 1 6 1 6 1 6 1 1 3 2 5 3 5 6 4
[337] 2 6 5 1 1 1 1 6 2 6 1 2 1 6 6 6 5 2 4 6 5 4 6 4
[361] 3 6 1 5 2 4 6 1 3 4 6 6 6 2 5 3 6 4 3 4 2 6 6 6
[385] 3 2 6 4 4 3 5 4 1 1 1 3 4 6 4 1 5 5 6 4 1 5 2 2
[409] 1 5 6 4 4 1 2 5 2 4 2 5 4 3 2 4 3 1 4 1 6 3 1 2
[433] 2 4 4 3 1 1 4 4 3 2 5 1 4 2 6 3 2 5 5 3 2 2 1 1
[457] 4 2 6 1 6 1 5 3 5 5 6 6 3 5 4 2 3 3 3 1 3 2 2 2
[481] 5 2 2 2 4 4 3 1 3 6 5 3 6 4 3 5 3 2 2 5
```
> table(rolls_PP4)
rolls_PP4
 1  2  3  4  5  6 
81 86 83 85 95 70
````
We rolled the dice 30 times and got 70 6's.
````
standard deviation 𝜎=[𝑁𝑝(1−𝑝)]^(1/2)=(500*1/6*5/6)^(1/2)=69.44
variance= (69.44)^2= 4281.91
`````

After Performing a Chi Square Test with five degrees of freedom and a 90 percent confidence interval we can conclude from the 
data that the odds of getting a 6 from a dice thrown 500 times is 83 or a 16.6 percent chance of getting a 6. When we conducted our Chi Test 
we had a p-value of .3285. Our P-value is greater than our a=value , our .1 confidence interval, therefore we fail to reject the Null Hypothesis which confirms our 
expierment protocal that higher volume or a higher number of throws will allow an individual to determine if a dice is loaded or not. 

````

As a group we decided to take the volume approach to this problem, we expect at while the random nature of a dice roll may deviate the resulting rolls in 6 away from the “fair” 1/6 proportion, with a higher volume of rolls we should be able to equal out the resulting proportion to nearly fair. Therefore, we decide to further the rolls to 500 total rolls with an expected 83 rolls resulting in a 6.
````


