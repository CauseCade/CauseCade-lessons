*this lesson is under construction*

#### upward propagation

Last lesson







P(A=1|B0)=P(B=0|A1) * P(A1) / P(B0)

P(A=1|B1)=P(B=1|A1) * P(A1) / P(B1)

P(A=0|B0)=P(B=0|A0) * P(A0) / P(B0)

P(A=0|B1)=P(B=1|A0) * P(A0) / P(B1)


Great, so that is all there is to upward propagation in a simple network like this. What is so interesting about this? Well, let's attach some semantic meaning to our nodes A and B. <(For this purpose, I have created the same network as before, but now with some interpretation to the nodes. Try opening the network {placeholder} and play around with it. You can see that {placeholder} changes when {placeholder} cahnges)> Now, i'm sure that does not sound super exciting, but as we build bigger networks in the next sections you will grow to appreciate it. 

#### recap

What have we learned from the past few lessons? We have seen that we can compute everything we need to know from the linkmatrix (conditional probabilities in one direction) and a given prior and that we can extend this to arbitrarily many states. So far, everthing should be fairly intuitive. The most important thing is that so far, we have not invoked anything that seems specific to a network. (Except for the  choice for the conditional matrix - but that was just a convention). 

We can now do:
- downward propagation 
- upward propagation
- set and change priors

But, what we worked with so far wasn't much of a network - in fact it was just two nodes. In the next section we will have a look at larger networks, and the complications and uses that brings to the table.
