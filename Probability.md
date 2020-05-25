# Data Analytics in Action 2019-2020/Term 1


*Question 2:*

> The probability of an “unhealthy supplier” in your supplier pool that produces a certain amount of defective hi-tech component is computed as 0.5%. While obtaining parts from these suppliers, you do your own inspection. Based on your inspection, you either accept or reject the supplier delivery. We know that if the supplier is labeled unhealthy, the probability of rejecting the delivery is 85%. On the other hand, a healthy supplier’s delivery can also be rejected with probability 10%. As the procurement manager of the company, you want to know the probability that the delivery is from an unhealthy supplier given that you reject its delivery?

*Answer 2:*

>Yes, as the procurement manager of the company, it is possible to calculate the probability that the delivery is from an unhealthy supplier given that it is rejected. The first step of this calculation is to examine what information is given to us.
*	The probability of an “unhealthy supplier” that produces a certain amount of defective hi-tech component is computed as 0.5%.
*	If the supplier is labeled unhealthy, the probability of rejecting the delivery is 85%.
*	If the supplier is labeled healthy, the probability of rejecting the delivery is 10%.
>With this information in mind, I have created a table with the probabilities of true rejects, false rejects, true accepts, and false accepts of deliveries based on healthy and unhealthy labels.

**Figure 1**

>In addition to the table, I have constructed a probability tree with the likelihoods of the rejects and accepts given unhealthy and healthy labels. Something to pay attention to is that Event A is the delivery has an unhealthy label and Event B is that the delivery is rejected.

**Figure 2**

>Unfortunately, to calculate the probability that the delivery is from an unhealthy supplier given that the delivery is rejected, P(A|B), cannot be performed using the table or probability tree. This is because P(A|B) has to take into account the true rejections, P(B|A), as well as the false rejections, P(B|¯A). Thus, to calculate P(A|B) has to be done using Bayes’ Theorem:
P(A│B)  =  (P(B|A)  ∙ P(A))/(P(B)) 


>This what each part of the theorem means in correlation to the problem:
* P(B|A), the probability that the delivery is rejected given that it is has an unhealthy label.
* P(A), the probability that the delivery has an unhealthy label.
* P(B), the probability that the delivery is rejected. This is a mutually exclusive event meaning that it has to take into account the delivery being rejected from with a unhealthy label and with a healthy label. Thus the denominator turns into: P(B|A) ∙ P(A) + P(B|¯A) ∙ P(¯A).

>Thus, I have substituted Bayes’ Theorem with the variables in question:

* P(Unhealthy│Reject)=(P(Reject│Unhealthy)∙P(Unhealthy))/(P(Reject│Unhealthy)∙P(Unhealthy)+P(Reject│Healthy)∙P(Healthy))

> Before we put together the final calculation, here are the individual calculations for each probability:

**Figure 3**

> Using the calculations in the table above and substituting them into Bayes’ Theorem, the final probability calculation of P(Unhealthy | Reject) or P(A|B) is the following:

P(Unhealthy│Reject)=  0.00425/(0.00425+0.0995) =  0.00425/0.10375 = 0.04095 ≈ 0.041

> In conclusion, the probability that the delivery is from an unhealthy supplier given that the delivery has been rejected is approximately 4.1%.
