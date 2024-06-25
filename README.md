To start, we study the simpliest cases with with C = 0  
E(1,0) = (1+2+3+4+5+6)/6 = 3.5  

E(2,0) : we roll again only if the first roll is < 3.5, i.e {1,2,3}. We don't roll if we have 4,5 or 6, i.e. an expected value of 5  
E(2,0) = 1/2 * 3.5 + 1/2 * 5. 5 = 4.25.  

So, the generalisation is 
$E(N,0) = P(rollAgain) * E(N-1,0) + P(Don't Roll Again) * E(actualEarn)$  
We roll again if the dice score is the dice score is lower than the expected value. And don't roll if the score is greater that the expected value.  
$E(N,0) = P(dice < E(N-1,0)) * E(N-1,0) + P(dice > E(N-1,0)) * E(ActualEarn)$

For a dice, the expected value is the mean of all the possible results. If we dont roll again, it is because we have a score greater than the previous expected value.  
E(actual earn) =$\frac{1}{6-⌈E(N-1,0)⌉}\sum_{i=⌈E(N-1,0)⌉}^{6} i$  
We can represent E(actual earn) as a mean of all the possible scores  

E(actual earn)= $\frac{⌈E(N-1,0)⌉+6}{2}$

P(dice < E(N-1,0)) represent the number of scores that are less than the Expected values : $\frac{⌊E(N-1,0)⌋}{6}$

P(dice >= E(N-1,0)) represent the number of scores that are greater than the Expected values : $\frac{6-⌊E(N-1,0)⌋}{6}$

Finally,

E(N,0) = $\frac{⌊E(N-1,0)⌋}{6} * ⌈E(N-1,0)⌉ + \frac{6-⌊E(N-1,0)⌋}{6} * \frac{⌈E(N-1,0)⌉+6}{2}$

We can generalise with the cost C. At each new roll, a cost is applied. 

E(N,C) = $\frac{⌊E(N-1,0)⌋}{6} * ⌈E(N-1,0)⌉ + \frac{6-⌊E(N-1,0)⌋}{6} * \frac{⌈E(N-1,0)⌉+6}{2} - C$
