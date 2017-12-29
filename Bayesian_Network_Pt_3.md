*this lesson is under construction*

#### upward propagation

Last lesson we look at downward propagation of evidence. This time we will look at upward propagation. With upward propagation we mean 
evidence (e.g. an observation) changing the probabilities of the nodes that are upstream (i.e. have a path towards this node). 
Naturally, this is no different from the downstream propagation case (for 2 nodes) as in the previous lesson. The difference lies in the 
fact that we will have to use bayes rule in this case. Great, so we finally see Bayes' rule come into play. 

Why do we have to use Bayes' rule in this case is because we do not have the CPD for the upstream case. That is, we know P(B|A),
but not P(A|B) (we have specified this in the network at the start - we set as convention we specify the CDP for the downstream case).
If we know P(A|B) we can just use the law of total probability to compute P(A), of course. So, let's use Bayes Rule to compute P(A|B)!
Using the general form: **P(A|B)=P(B|A) * P(A) / P(B)** and from that finding the specifics for this problem:

P(A=1|B0)=P(B=0|A1) * P(A1) / P(B0)

P(A=1|B1)=P(B=1|A1) * P(A1) / P(B1)

P(A=0|B0)=P(B=0|A0) * P(A0) / P(B0)

P(A=0|B1)=P(B=1|A0) * P(A0) / P(B1)


Great, so that is all there is to upward propagation in a simple network like this. What is so interesting about this? Well, let's attach some semantic meaning to our nodes A and B. <(For this purpose, I have created the same network as before, but now with some interpretation to the nodes. Try opening the network {placeholder} and play around with it. You can see that {placeholder} changes when {placeholder} cahnges)> Now, i'm sure that does not sound super exciting, but as we build bigger networks in the next sections you will grow to appreciate it. 

#### recap

What have we learned from the past few lessons? We have seen that we can compute everything we need to know from the CPT (conditional probabilities in one direction) and a given prior and that we can extend this to arbitrarily many states. So far, everthing should be fairly intuitive. The most important thing is that so far, we have not invoked anything that seems specific to a network. (Except for the  choice for the conditional matrix - but that was just a convention). 

We can now do:
- downward propagation 
- upward propagation
- set and change priors

But, what we worked with so far wasn't much of a network - in fact it was just two nodes. You have probably used bayes rule in such a context already - without having to invoke any network structure or directionality. In the next section we will have a look at larger networks, and the complications and uses that brings to the table. 
